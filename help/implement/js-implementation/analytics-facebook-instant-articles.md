---
description: Facebook 인스턴트 아티클의 Analytics 구현 방법을 참조하십시오.
keywords: Analytics 구현; 임베드; 사용자 지정 변수; 사용자 지정 이벤트; 방문자 추적; 추적; 제한 사항
seo-description: Facebook 인스턴트 아티클의 Analytics 구현 방법을 참조하십시오.
seo-title: Facebook 인스턴트 아티클
solution: Analytics
title: Facebook 인스턴트 아티클
topic: 개발자 및 구현
uuid: 04 b 6366 b -7 c 52-4 DAE-B 2 DD-BB 6 B 78 FD 409 C
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Facebook 인스턴트 아티클

Facebook 인스턴트 아티클의 Analytics 구현 방법을 참조하십시오.

Facebook 인스턴트 아티클은 Facebook에서 빠른 대화형 문서를 만들기 위한 게시자용의 새로운 방법입니다. 인스턴트 아티클은 모바일 웹보다 최고 10배 더 빠르게 컨텐츠를 로드할 수 있습니다.

Facebook 인스턴트 아티클 내에 Adobe Analytics를 포함하여 방문자가 컨텐츠와 상호 작용할 때의 방문자 행동을 추적할 수 있습니다. 게시자 컨텐츠는 게시자의 웹 사이트가 아니라 Facebook 앱 내에 있으므로, 태깅 접근 방식은 표준 Analytics 구현과는 다소 다릅니다.

## 1단계. 분석 HTML 페이지 포함 {#section_0DF847F8BA624CF8A239C10003A39E59}

Facebook Instant Article 컨텐츠를 만들 때 분석 HTML 컨텐츠를 iFrame 내에 포함할 수 있습니다. 예:

```
<iframe class="no-margin" src="https://[your-domain-here]/analytics.html" height="0"></iframe>
```

## 2단계. 분석 HTML 수정 {#section_76707B51D63A47FF833C2D3FFF8412B4}

아래의 샘플 HTML을 사용하여 인스턴트 문서에서 통계를 캡처할 수 있습니다. 이 파일은 일반적으로 회사 웹 서버 중 하나에서 호스트됩니다. 인스턴트 문서가 로드될 때마다, 1단계에서 설명한 대로 iframe에서 파일을 로드하면 Adobe에 분석 데이터를 보내는 작업이 시작됩니다.

```
<html> 
    <head> 
        <title>Facebook Stats</title> 
        <script language="javaScript" type="text/javascript" src="https://[your-domain-here]/js/VisitorAPI.js"></script> 
        <script language="javaScript" type="text/javascript" src="https://[your-domain-here]/js/AppMeasurement.js"></script> 
    </head> 
    <body> 
        <script> 
            //Standard Variable Configuration 
   var v_orgId = "[your-marketing-cloud-org-id]@AdobeOrg"; 
   var s_account = "[your-report-suite-id]"; 
   var s_trackingServer = "[your-tracking-server]"; 
   var s_visitorNamespace = "[your-namespace]"; 
     
   //Instantiation 
   var visitor = Visitor.getInstance(v_orgId); 
   visitor.trackingServer = s_trackingServer; 
     
   var s = s_gi(s_account); 
   s.account = s_account; 
   s.trackingServer = s_trackingServer; 
   s.visitorNamespace = s_visitorNamespace; 
   s.visitor = visitor; 
     
   //Custom Variables 
   s.pageName = s.Util.getQueryParam("pageName"); 
   s.prop10 = "Facebook Instant Article"; 
       
   //Page View Image Request Call 
   s.t(); 
        </script> 
    </body> 
</html> 
```

**특정 구현에 대해 이 샘플 HTML을 수정하려면**

1. 회사 웹 서버 상의 일반적인 디렉토리에서 수정되지 않은 VisitorAPI.js 및 AppMeasurement.js 버전의 최신 사본을 호스트하는 것이 좋습니다.

   이 파일들은 필요할 경우 Analytics의 코드 관리자 내에서도 다운로드할 수 있습니다.

1. Analytics 구현 표준 구성 변수를 포함합니다.

   1. Experience Cloud 조직 ID입니다.
   1. Facebook Instant Article 트래픽을 캡처할 보고서 세트 ID.
   1. 회사의 추적 서버 도메인.
   1. 방문자 네임스페이스 변수. **참고:** 이러한 값들 중 많은 수는 표준 Analytics 구현 내에서 찾을 수 있습니다. 필요할 경우 고객 지원 또는 Adobe 컨설팅에서 적절한 값을 제공하는 데 도움을 줄 수 있습니다.

1. [사용자 지정 변수 및 이벤트 추적을 설정합니다](../../implement/js-implementation/analytics-facebook-instant-articles.md#section_932C41BD21154C25B99389299BDF3E0B).
1. Include the page view image request syntax `( s.t())`.

## 3단계. 사용자 지정 변수 및 이벤트 추적 설정 {#section_932C41BD21154C25B99389299BDF3E0B}

사용자 지정 변수 및 이벤트는 다양한 접근 방식을 통해 분석 HTML 내에서 추적할 수 있습니다. 첫 번째 접근 방식은 표준 Analytics 구현에서 수행할 수도 있는 것과 유사하게 사용자 지정 구성에서 JavaScript 논리를 포함하는 것입니다. 예를 들어, prop의 값을 설정하려면, 일반적인 구현에서 사용하는 것과 동일한 구문을 사용하십시오.

```
s.prop10 = "Facebook Instant Article";
```

iframe `src` 특성에서 쿼리 문자열 매개 변수를 활용하여 변수를 동적으로 iframe에 보낼 수도 있습니다. 예:

```
<iframe class="no-margin" src="https://[your-domain-here]/analytics.html?prop1=dynamic%20article%20title&eVar1=facebook%20page%20name&pageName=your%20page%20name%20here&cmpId=your%20campaignID%20here" height="0"></iframe>
```

이러한 쿼리 문자열 매개 변수는 다음과 같이 그 후에 라이브러리 내에서 `Util.getQueryParam`[!DNL AppMeasurement] 함수를 사용하여 분석 HTML JavaScript의 사용자 지정 변수 섹션에서 설정할 수 있습니다.

```
s.pageName = s.Util.getQueryParam("pageName"); 
s.campaign = s.Util.getQueryParam("cmpId"); 
s.eVar1 = s.Util.getQueryParam("eVar1"); 
s.prop1 = s.Util.getQueryParam("prop1"); 
```

## 방문자 추적 {#section_60F0C77659534949831E85B5FD9AE81E}

분석 HTML 페이지가 웹 서버에 호스트되는 한, Adobe에서는 모든 Facebook 인스턴트 아티클에서 기존의 개인 정보 보호 정책을 지원할 수 있습니다. 이것은 최종 사용자가 기본 사이트에서 추적을 옵트 아웃한 경우 추가적인 단계를 수행하지 않아도 최종 사용자가 모든 Facebook 인스턴트 아티클에서도 추적을 옵트 아웃하게 됨을 의미합니다. 또한 이 유틸리티 페이지를 사용하면 ID 서비스 (방문자 ID) 가 지원되므로 Facebook 인스턴트 아티클에 캡처된 지표 및 변수를 나머지 Experience Cloud와 통합할 수 있습니다. (An example is for targeted advertising using [!DNL Adobe Audience Manager]).

## 추적 제한 사항 {#section_1EE1BB069A3148DB9446371AFE196567}

이 접근 방식에는 주목해야 할 문제가 몇 가지 있습니다. Facebook Instant Article에서 일반적으로 JavaScript를 통해서만 액세스할 수 있는 모든 DOM 값(예: 레퍼러)은 추적을 위해 iframe에서 검색할 수 없습니다. 그렇지만, 브라우저, 장치, 화면 크기 또는 해상도와 같은 표준 기술 보고서는 일반적으로 작동해야 합니다. 게다가, pageURL은 유틸리티 페이지에서 [!DNL document.referrer]를 참조해서도 구할 수 있습니다.

## 다음은 무엇입니까? {#section_A170A10E2A3642A784DF720195DA8B38}

[!DNL Adobe Analytics] Facebook 및 Adobe 발행자와 협력하여 업계 선도적인 분석 기능을 모바일 웹의 출판업체에 제공함으로써 놀라운 사용자 경험을 제공할 수 있게 되었습니다. Adobe에서는 고객들의 더욱 진화하고 있는 분석 요구에 답하기 위한 최상의 장기적 솔루션을 만드는 데 전념하고 있습니다.

Facebook Instant Article 프로젝트는 빠르게 움직이고 있으며, 변경 사항도 항상 발생하므로 이 사이트를 방문하여 업데이트가 있는지 자주 확인하십시오. 통합은 더 개선되고, 향후에는 더 많은 게시자가 Facebook 인스턴트 아티클을 채택할 것이므로 변경 사항들이 있을 것임을 예상하십시오.

질문이나 문제가 있을 경우, 담당 Adobe 컨설턴트나 고객 지원 센터에 문의하십시오.
