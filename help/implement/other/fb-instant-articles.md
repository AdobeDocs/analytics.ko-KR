---
title: Facebook 인스턴트 아티클로 구현
description: Facebook 인스턴트 아티클 페이지에서 Adobe Analytics를 구현합니다.
translation-type: ht
source-git-commit: 9d2007bead6a4963022f8ea884169802b1c002ff

---


# Facebook 인스턴트 아티클로 구현

Facebook 인스턴트 아티클을 사용하면 게시자가 Facebook에서 빠른 대화형 문서를 만들기 수 있습니다. 인스턴트 아티클은 모바일 웹보다 최고 10배 더 빠르게 컨텐츠를 로드할 수 있습니다.

Facebook 인스턴트 아티클에 Adobe Analytics를 포함하여 방문자 행동을 추적할 수 있습니다. 게시자 컨텐츠는 게시자의 웹 사이트가 아니라 Facebook 앱 내에 있으므로, 태깅 접근 방식은 표준 Analytics 구현과는 다소 다릅니다.

## 워크플로우

Adobe Analytics를 구현하는 주요 워크플로우는 다음과 같습니다.

1. `stats.html` 페이지를 만듭니다. 이 페이지를 코딩하여 URL에서 쿼리 문자열 매개 변수를 가져오고 각 매개 변수를 Analytics 변수에 지정하십시오.
1. 웹 서버에서 `stats.html` 페이지를 호스팅합니다.
1. iframe의 `stats.html` 파일을 참조하여 Facebook 인스턴트 아티클에 Analytics를 구현합니다.
1. iframe `src` 특성에 쿼리 문자열 매개 변수를 포함합니다.

### 1단계: `stats.html` 페이지 만들기

아래의 샘플 HTML을 사용하여 인스턴트 문서에서 통계를 캡처할 수 있습니다. 이 파일은 일반적으로 회사 웹 서버 중 하나에서 호스트됩니다. 인스턴트 아티클이 로드될 때마다 iframe에 파일이 로드되고, 그러면 데이터가 Adobe에 전송되기 시작합니다.

```html
<html>
  <head>
    <title>Facebook Stats</title>
      <script language="javaScript" type="text/javascript" src="VisitorAPI.js"></script>
      <script language="javaScript" type="text/javascript" src="AppMeasurement.js"></script>
  </head>
  <body>
    <script>
      var v_orgId = "INSERT-ORG-ID-HERE";
      var s_account = "examplersid";
      var s_trackingServer = "example.sc.omtrdc.net";
      var visitor = Visitor.getInstance(v_orgId);
      visitor.trackingServer = s_trackingServer;

      var s = s_gi(s_account);
      s.account = s_account;
      s.trackingServer = s_trackingServer;
      s.visitor = visitor;

      s.pageName = s.Util.getQueryParam("pageName");
      s.pageURL = document.referrer; // The referrer to the utility page is the parent frame
      s.campaign = s.Util.getQueryParam("cmpId");
      s.eVar1 = "Facebook Instant Article";
      s.eVar2 = s.Util.getQueryParam("eVar2");

      s.t();
    </script>
  </body>
</html>
```

### 2단계: 웹 서버에서 `stats.html` 페이지 호스팅

최신 버전의 `AppMeasurement.js` 및 `VisitorAPI.js`와 함께 `stats.html` 페이지를 호스팅하는 것이 좋습니다. 조직의 적절한 엔지니어링 팀과 협력하여 이 파일을 올바른 위치에 호스팅하십시오.

### 3단계: 각 Facebook 인스턴트 아티클 페이지에서 `stats.html` 참조

Facebook 인스턴트 아티클 컨텐츠를 만들 때 분석 HTML 컨텐츠를 iframe 내에 포함하십시오. 예:

```html
<iframe class="no-margin" src="https://example.com/stats.html" height="0"></iframe>
```

### 4단계: 사용자 지정 변수 및 이벤트 추적 설정

사용자 지정 변수 및 이벤트는 두 가지 서로 다른 접근 방식을 통해 분석 HTML 내에서 추적할 수 있습니다.

* 변수 값과 이벤트를 `stats.html` 페이지에 직접 포함합니다. 여기에서 정의된 변수는 모든 Facebook 인스턴트 아티클에 대해 일반적으로 동일한 값들에 가장 적합합니다.
* iframe을 참조하는 쿼리 문자열의 일부로 변수 값을 포함합니다. 이 방법을 사용하면 Facebook 인스턴트 아티클에서 Analytics 코드를 호스팅하는 iframe에 변수 값을 전송할 수 있습니다.

다음 예는 쿼리 문자열에 포함된 몇 가지 사용자 지정 변수를 보여줍니다. 그런 다음 `stats.html` 내의 JavaScript가 `s.Util.getQueryParam()`을 사용하여 쿼리 문자열을 확인합니다.

```html
<iframe class="no-margin" src="https://example.com/stats.html?eVar2=Dynamic%20article%20title&pageName=Example%20article%20name&cmpId=exampleID123" height="0"></iframe>
```

> [!NOTE] 레퍼러 차원은 iframe의 특성으로 인해 자동으로 추적되지 않습니다. 추적하려는 경우 이 차원을 쿼리 문자열의 일부로 포함하도록 하십시오.

## Facebook 인스턴트 아티클 및 개인 정보

분석 HTML 페이지가 웹 서버에 호스팅되는 한, Adobe에서는 모든 Facebook 인스턴트 아티클에서 기존의 개인 정보 보호 정책을 지원합니다. 사용자가 기본 사이트의 추적을 옵트 아웃하는 경우 모든 Facebook 인스턴트 아티클의 추적 또한 옵트 아웃됩니다. 또한 유틸리티 페이지가 Facebook 인스턴트 아티클 데이터를 Experience Cloud의 나머지 데이터와 통합할 수 있도록 Adobe Experience Cloud ID 서비스를 지원합니다.
