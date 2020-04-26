---
title: AMP를 사용한 구현
description: AMP 페이지에서 Adobe Analytics를 구현합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# AMP를 사용한 구현

[AMP](https://amp.dev)는 빠르고 매끄럽게 로딩되는 웹 페이지를 손쉽게 만들 수 있는 방법을 제공하는 오픈 소스 HTML 프레임워크입니다.

Adobe Analytics는 JavaScript 라이브러리를 사용하여 이미지 요청을 컴파일하고 전송하므로 AMP를 사용하여 페이지에서 Adobe에 데이터를 전송하려면 구현에서 조정이 필요합니다.

## AMP를 사용하여 페이지에서 Adobe Analytics를 구현할 방법 결정

Adobe는 AMP를 사용하여 페이지에서 Adobe Analytics를 구현하는 두 가지 방법을 만들었습니다. 둘 다 `<amp-analytics>` HTML 태그를 사용합니다. 자세한 내용은 ampproject GitHub의 [amp-analytics 태그](https://github.com/ampproject/amphtml/tree/master/extensions/amp-analytics)를 참조하십시오.

* **`"adobeanalytics"`추적 템플릿 사용**: 페이지에서 바로 Analytics 요청 구성
* **`"analytics_nativeConfig"`추적 템플릿 사용**: 일반 사이트에 배포하는 것과 동일한 AppMeasurement 코드가 들어 있는 iframe 사용

다음 표에서는 이 두 방법을 비교합니다.

|  | **&quot;adobeanalytics&quot; 템플릿** | **&quot;adobeanalytics_nativeConfig&quot; 템플릿** |
|---|---|---|
| 기존 보고서 세트의 방문자/방문수 | 높은 인플레이션 | 최소한의 인플레이션 |
| 별도의 보고서 세트 사용 | 권장 | 불필요 |
| 새 방문자와 재방문자 | 지원되지 않음 | 지원됨 |
| 방문자 ID 서비스 | 지원되지 않음 | 지원됨 |
| 비디오 및 링크 추적 | 부분 지원 | 아직 지원되지 않음 |
| 구현의 어려움 | 약간 어려움 | 상대적으로 쉬움 |
| Adobe Experience Cloud 통합 | 지원되지 않음 | 부분 지원 |

조직 내에서 장단점을 따져 사용할 방법을 결정하십시오. 샘플 코드가 필요하면 Adobe의 GitHub 저장소에서 [AMP 예](https://github.com/Adobe-Marketing-Cloud/mobile-services/tree/master/samples/mobile-web)를 참조하십시오.

>[!WARNING] AMP를 사용하여 `"adobeanalytics"` 템플릿과 `"adobeanalytics_nativeConfig"` 템플릿을 동일한 페이지에서 모두 사용하지 마십시오. 그럴 경우 브라우저 콘솔에서 오류가 생성되고 방문자가 두 번 카운트될 수 있습니다.

## 방법 1: &quot;adobeanalytics&quot; 템플릿에서 amp-analytics 태그 사용

`"adobeanalytics"` 추적 템플릿은 `<amp-analytics>` HTML 태그를 사용하여 추적 요청을 바로 구성합니다. 페이지 표시 또는 클릭과 같이 특정 페이지 이벤트에서 실행되는 히트 요청을 지정할 수 있습니다. 선택기를 지정하여 특정 요소 ID나 클래스에 적용되도록 클릭 이벤트를 사용자 지정할 수 있습니다. `type="adobeanalytics"`를 amp-analytics 태그에 추가하여 템플릿을 로드할 수 있습니다.

다음의 코드 예제에는 두 개의 트리거(`pageLoad`, `click`)가 정의되어 있습니다. `pageLoad` 트리거는 문서가 표시될 때 실행되며 `vars` 섹션에 정의되어 있는 대로 `pageName` 변수를 포함합니다. 두 번째 트리거인 `click`은 단추를 클릭하면 실행됩니다. `eVar1`은 값이 `button clicked`인 이 이벤트에 대해 설정됩니다.

```html
<amp-analytics type="adobeanalytics">
  <script type="application/json">
    {
      "requests": {
        "myClick": "${click}&v1=${eVar1}",
      },
      "vars": {
        "host": "example.sc.omtrdc.net",
        "reportSuites": "reportSuiteID",
        "pageName": "Adobe Analytics Using amp-analytics tag"
      },
      "triggers": {
        "pageLoad": {
          "on": "visible",
          "request": "pageView"
        },
        "click": {
          "on": "click",
          "selector": "button",
          "request": "myClick",
          "vars": {
            "eVar1": "button clicked"
          }
        }
      }
    }
  </script>
</amp-analytics>
```

`click` 트리거에서는 특정 DOM 요소를 클릭할 때마다(이 경우, 임의 단추 클릭), `buttonClick` 요청이 실행되어 이 히트를 비 링크 추적 호출로 나타내도록 자동으로 설정되게 하는 선택기를 지정할 수 있습니다.

또한, `amp-analytics`에서는 AMP에서 인식하는 데이터 값을 제공할 수 있도록 많은 수의 변수 대체를 지원합니다. 자세한 내용은 GitHub에서 [amp-analytics에서 지원되는 변수](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md)를 참조하십시오.

>[!NOTE] 이 방법을 사용하여 Adobe에 보내는 이미지 요청에는 많은 기본 보고서(예: 브라우저, 화면 크기 또는 레퍼러)에 대한 데이터가 포함되지 않습니다. 히트에 이 정보를 포함하려면 이 정보가 이미지 요청 쿼리 문자열의 일부로 포함되었는지 확인하십시오. 자세한 내용은 [데이터 수집 쿼리 매개 변수](../validate/query-parameters.md)를 참조하십시오.

Adobe는 내장된 AMP 함수를 사용하여 방문자를 식별하고 쿠키 `adobe_amp_id`를 설정합니다. 이 방문자 ID는 Adobe Analytics에서 설정한 다른 모든 ID(예: `s_vi` 쿠키)에 대해 고유합니다. Adobe Experience Cloud ID 서비스는 이 구현 방법을 사용하여 지원되지 않습니다.

>[!NOTE] AMP는 CDN을 사용하여 컨텐츠를 전달합니다. AMP는 방문자가 컨텐츠를 검색하는 각 CDN에 대해 서로 다른 고유한 방문자를 카운트하도록 구성되어 있어서 고유 방문자 수를 부풀릴 수 있습니다.

AMP가 고유 방문자를 식별하는 방법 때문에 AMP 페이지에는 별도의 보고서 세트를 사용하는 것이 좋습니다.

이 솔루션을 사용하려면 `host` 속성에서 지정하는 추적 서버가 주 사이트의 추적 서버와 일치하여 기존의 개인정보 보호정책 제어 사항이 준수되도록 해야 한다는 것입니다. 아니면, AMP를 사용하여 페이지에 대한 개인정보 보호정책을 만드십시오.

## 방법 2: &quot;adobeanalytics_nativeConfig&quot; 템플릿에서 amp-analytics 태그 사용

`"adobeanalytics_nativeConfig"` 태그는 일반적인 웹 페이지에서 사용하는 것과 동일한 태깅 방식을 사용하게 되므로 구현하기가 더 쉽습니다. `amp-analytics` 태그에 다음 내용을 추가하십시오.

```html
<amp-analytics type="adobeanalytics_nativeConfig">
  <script type="application/json">
    {
      "requests": {
        "base": "https://${host}",
        "iframeMessage": "${base}/stats.html?campaign=${queryParam(campaign)}&pageURL=${ampdocUrl}&ref=${documentReferrer}"
      },
      "vars": {
        "host": "example.sc.omtrdc.net"
      },
      "extraUrlParams": {
      "pageName": "Example AMP page",
      "v1": "eVar1 example value"
      }
    }
 </script>
</amp-analytics>
```

웹 서버에 호스팅된 HTML 페이지도 필요합니다.

```html
<html>
  <head>
    <title>Stats Example</title>
    <script language="JavaScript" type="text/javascript" src="VisitorAPI.js"></script>
    <script language="JavaScript" type="text/javascript" src="AppMeasurement.js"></script>
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
      s.visitorNamespace = s_visitorNamespace;
      s.visitor = visitor;
      s.pageName = s.Util.getQueryParam("pageName");
      s.eVar1 = s.Util.getQueryParam("v1");
      s.campaign = s.Util.getQueryParam("campaign");
      s.pageURL = s.Util.getQueryParam("pageURL");
      s.referrer = s.Util.getQueryParam("ref");
      s.t();
    </script>
  </body>
</html>
```

이 접근 방법에서는 `iframeMessage` 요청 매개 변수에 추가된 쿼리 문자열 매개 변수를 통해 데이터를 유틸리티 웹 페이지에 보냅니다. 이러한 쿼리 문자열 매개 변수의 이름은 `stats.html` 페이지가 이 매개 변수에서 데이터를 수집하도록 구성되어 있는 한 원하는 방식대로 지정할 수 있습니다.

`"adobeanalytics_nativeConfig"` 템플릿에서도 amp-analytics 태그의 `extraUrlParams` 섹션에 나열된 변수를 기반으로 쿼리 문자열 매개 변수를 추가합니다. 위의 예에는 `pageName` 및 `v1` 매개 변수가 포함되어 있습니다.

>[!IMPORTANT] `stats.html` 페이지는 AMP 자체가 호스팅되는 도메인과는 별도의 하위 도메인에서 호스팅되어야 합니다. AMP 프레임워크는 AMP 페이지 자체가 존재하고 있는 것과 동일한 하위 도메인의 iframe을 허용하지 않습니다. 예를 들어 AMP가 `amp.example.com`에서 호스팅된다면, `stats.html` 페이지를 반드시 `ampmetrics.example.com`과 같은 별도의 하위 도메인에서 호스팅하십시오.

이 방법을 사용하면 사용자가 기본 사이트의 추적을 옵트 아웃하는 경우 모든 AMP의 추적 또한 옵트 아웃하게 됩니다. 또한 이 유틸리티 페이지를 사용하는 것은 AMP가 Adobe Experience Cloud ID 서비스를 지원할 수 있음을 의미합니다. 별도의 보고서 세트는 필요하지 않습니다.

링크 추적 및 비디오 추적은 이 방법에서 사용할 수 없습니다. AMP의 `iframeMessage` 태그는 페이지당 한 번만 로드될 수 있으므로 프레임이 로드된 후 다른 이미지 요청을 전송할 수 없습니다. 또한 이 메서드를 실행하려면 더 많은 처리 리소스가 필요하며 이는 스크롤 성능에 영향을 줄 수 있습니다. 모든 리소스는 비동기적으로 로드되므로 이 방법은 페이지 로드 시간에는 영향을 주지 않습니다.

## FAQ

**둘 중 한 방법에 비디오 추적을 사용할 수 있습니까?**

아니요. AMP 표준은 &quot;visible&quot;, &quot;click&quot; 및 &quot;timer&quot;에 대한 트리거만 지원하며 `amp-analytics` 태그가 수신할 수 있는 비디오 추적에 대한 명시적 트리거는 아직 지원하지 않습니다. 또한 `"adobeanalytics_nativeConfig"` 템플릿은 한 번만 로드할 수 있으므로 페이지가 로드된 후 후속 이미지 요청을 수행할 수 없습니다.

**AMP 방문자를 데이터에 있는 다른 방문자와 구별하려면 어떻게 해야 합니까?**

모든 AMP 페이지의 경우 [!UICONTROL JavaScript 버전] 차원은 `AMP vX.X`와 유사한 값을 수집합니다. 사용자 지정 차원을 &#39;AMP&#39;로 설정하여 이러한 방문자를 세그먼트화할 수도 있습니다.

**이 구현 방법은 Facebook 인스턴트 아티클과 어떻게 비교할 수 있습니까?**

Facebook 인스턴트 아티클에서는 `"adobeanalytics_nativeConfig"` 메서드와 유사한 솔루션을 지원합니다. 이 방법의 `stats.html` 페이지는 AMP와 FIA 모두에 대한 분석 요구를 동시에 충족할 수 있습니다. FIA에서의 추적 구현에 대한 자세한 내용은 [Facebook 인스턴트 아티클](fb-instant-articles.md)을 참조하십시오.
