---
description: Adobe Analytics에서 가속 모바일 페이지(AMP) 프로젝트를 구현하십시오.
keywords: Analytics 구현; amp; amp-analytics; Adobeanalytics 템플릿; Adobeanalytics_ nativeconfig 템플릿; 클릭 추적; 방문자 부풀림; ID 서비스
seo-description: Adobe Analytics에서 가속 모바일 페이지(AMP) 프로젝트를 구현하십시오.
seo-title: 가속 모바일 페이지
solution: Analytics
title: 가속 모바일 페이지
topic: 개발자 및 구현
uuid: C 86 E 4 A 80-7191-4 EE 7-AB 20-787730026 C 4 B
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# 가속 모바일 페이지

Adobe Analytics에서 가속 모바일 페이지(AMP) 프로젝트를 구현하십시오.

AMP는 빠르게 렌더링되는 정적 컨텐츠의 웹 페이지를 작성할 수 있는 [개방형 소스 프로젝트](https://www.ampproject.org/)입니다. 이 기능은 모바일에 최적화된 컨텐츠를 한 번 만든 후 모든 위치에서 즉시 로드하려는 게시자에게 이상적입니다. 다음 주제가 포함됩니다.

* [작동 방법](../../implement/js-implementation/accelerated-mobile-pages.md#section_21C2836D63104794BCEBEECB6593AFBF)
* ["adobeanalytics" 템플릿에서 amp-analytics 태그 사용](../../implement/js-implementation/accelerated-mobile-pages.md#section_2E4EBF4EF623440D95DE98E78C47244E)
* ["adobeanalytics_nativeConfig" 템플릿에서 amp-analytics 태그 사용](../../implement/js-implementation/accelerated-mobile-pages.md#section_3556B68304A4492991F439885727E9FF)
* [요약](../../implement/js-implementation/accelerated-mobile-pages.md#section_4D8ED26084F249738A5C2BC66B933A07)
* [FAQ](../../implement/js-implementation/accelerated-mobile-pages.md#section_5F57AA2DE0C5452FB65241058A924C73)

**추가 설명서 및 예제**

* 외부, 개방형 소스 AMP 프로젝트 [설명서](https://www.ampproject.org/docs/get_started/about-amp.html)
* 설정 [예제](https://github.com/Adobe-Marketing-Cloud/mobile-services/tree/master/samples/mobile-web/amphtml)

## 작동 방법 {#section_21C2836D63104794BCEBEECB6593AFBF}

AMP에서는 참여하는 기술 파트너 및 게시자의 다양한 CDN(content delivery network)의 웹에서 캐시된 HTML 페이지에 특별히 태그를 지정했습니다. 이렇게 함으로써, 가장 짧은 지연이 있는 가장 가까운 소스에서 AMP 컨텐츠가 제공됩니다. 이 경우 게시자의 컨텐츠를 로드하는 위치를 100% 확신할 수 없고 타사 쿠키는 방문자 식별에 문제를 일으키기 때문에 분석에 어려움이 생깁니다.

또한, 페이지 용량을 크게 줄이고 페이지 로드 속도를 높이기 위해 AMP에서는 JavaScript와 쿠키의 사용을 제한합니다. 이러한 방식은 처리량을 줄이기 때문에 모바일 장치에 유익하지만 고유 방문자 수를 정확하게 측정하고 사용자 획득 및 유지를 이해하는 데에는 어려움을 초래합니다.

이러한 문제를 해결하기 위해, Adobe에서는 게시자가 `amp-analytics` 태그를 사용하여 비즈니스 요구에 가장 적합하게 선택할 수 있는 두 가지 옵션에 대해 AMP 파트너 및 게시자와 협업했습니다. The first approach uses the `"adobeanalytics"` tracking template to construct the Analytics request directly from within the AMP. The second approach uses the `"analytics_nativeConfig"` tracking template, which uses an iframe containing the AppMeasurement code you deploy on your normal site. 다음 표에서는 각 접근 방법의 장단점을 알 수 있습니다.

|  | **"adobeanalytics" 템플릿** | ** "adobeanalytics_nativeConfig" 템플릿** |
|---|---|---|
| 방문자/방문수(기존 보고서 세트에서) | 높은 인플레이션 | 최소한의 인플레이션 |
| 별도의 보고서 세트 사용 | 권장 | 불필요 |
| 새 방문자와 재방문자 | 지원되지 않음 | 지원됨 |
| 방문자 ID 서비스 | 지원되지 않음 | 지원됨 |
| 비디오 및 링크 추적 | 부분 지원 | 아직 지원되지 않음 |
| 구현의 어려움 | 약간 어려움 | 상대적으로 쉬움 |
| [!DNL Experience Cloud] 통합 | 지원되지 않음 | 경고가 지원됨 |

## "adobeanalytics" 템플릿에서 amp-analytics 태그 사용 {#section_2E4EBF4EF623440D95DE98E78C47244E}

`"adobeanalytics"`추적 템플릿은 `amp-analytics` 태그를 활용하여 추적 요청을 직접 구성합니다. Using the `"adobeanalytics"` template in the `amp-analytics` tag, you can specify hit requests that fire on specific page events, like the page becoming visible or on a click (and in the future, video views and more). 선택기를 지정하여 특정 요소 ID나 클래스에 적용되도록 클릭 이벤트를 사용자 지정할 수 있습니다. Adobe has made this easy to set up using the `"adobeanalytics"` template specifically designed for [!DNL Adobe Analytics]. You can load the template by adding `type="adobeanalytics"` to the amp-analytics tag.

In the following code example, there are two triggers defined: `pageLoad` and `click`. The `pageLoad` trigger will fire when the document becomes visible and will include the `pageName` variable as defined in the `vars section`. The second trigger `click` will fire when a button is clicked. `eVar 1` 값으로 이 이벤트에 대해 설정됩니다 `button clicked`.

```
  <amp-analytics type="adobeanalytics"> 
  <script type="application/json"> 
  { 
        "requests": { 
      "myClick": "${click}&v1=${eVar1}", 
  }, 
  "vars": { 
      "host": "metrics.example.com", 
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

`click` 트리거에서 선택기를 지정하여 특정 DOM 요소를 클릭할 때마다 (이 경우 모든 단추) `buttonClick` 요청이 실행되고 이 히트를 스테이지 이외의 이벤트 (예: `trackLink` 호출) 로 표시하도록 자동으로 설정됩니다.

또한, `amp-analytics`에서는 AMP에서 인식하는 데이터 값을 제공할 수 있도록 많은 수의 변수 대체를 지원합니다. [amp-analytics 변수 설명서](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md)를 방문하면 이 모든 사항과 더 자세한 내용을 알 수 있습니다.

임의의 기술 또는 DOM 변수(예: 브라우저, 화면 크기, 장치, 레퍼러 등)를 통합하려는 경우 이 변수는 자동으로 생성되지 않으므로 명시적으로 요청에 추가해야 합니다. 추적에 사용되는 각각의 사용 가능한 쿼리 문자열 매개 변수에 대한 설명서는 [여기](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=query_parameters)에 있습니다.

amp-analytics로 만들어진 히트를 검사하면 각 요청에서 Adobe가 `vid` 쿼리 매개 변수를 포함한 것을 볼 수 있습니다. Adobe에서는 기본 제공 AMP 함수를 기반으로 `vid`를 설정하여 `adobe_amp_id`라는 이름의 사용자 지정 Analytics 쿠키 ID를 설정했습니다. 이 ID는 다른 곳(예: [!DNL Adobe Analytics])에서 `s_vi cookie`로 설정되는 다른 ID와는 별개의 ID로서, 히트를 전송받는 보고서 세트에서 새로운 방문자 수를 생성합니다.

다음과 같이 몇 가지 알아야 할 사항이 있습니다. 위에 설명한 것처럼 amp-analytics 태그를 사용할 때, 방문자는 일반적인 추적과는 관련이 없으며, AMP는 컨텐츠 제공 네트워크(CDN)에서 로드될 수 있으므로 방문자가 이 AMP를 보는 각 CDN에 대해 고유 방문자가 생깁니다(이 때문에 앞에서 방문자 인플레이션이 언급되었습니다). For this reason, Adobe recommends that if you use the `"adobeanalytics"` template for `amp-analytics`, you put your data into a separate report suite specific to AMP. [!DNL Experience Cloud] 또한 ID 서비스 (이전, *`visitor ID service`*) 는 이 방법으로 지원되지 않으므로 비즈니스에 [!DNL Experience Cloud] 추가 통합이 필요하거나 향후 제공될 경우에는 옵션이 아닐 것입니다.

Finally, and perhaps most importantly, this `amp-analytics` solution requires that the tracking server you specify in the `vars` section matches the tracking server on your main site, so that your existing privacy policy controls are respected. 그렇지 않으면, AMP 전용으로 별도의 개인정보 보호정책을 만들어야 합니다.

## "adobeanalytics_nativeConfig" 템플릿에서 amp-analytics 태그 사용 {#section_3556B68304A4492991F439885727E9FF}

`"adobeanalytics_nativeConfig"` 태그는 일반적인 웹 페이지에서 사용하는 동일한 태깅 방법론을 사용하므로 구현하기가 쉽습니다. 이를 수행하려면 다음을 `amp-analytics` 태그에 추가하십시오.

```
<amp-analytics type="adobeanalytics_nativeConfig"> 
 <script type="application/json"> 
 { 
  "requests": { 
   "base": "https://${host}", 
   "iframeMessage": "${base}/stats.html?campaign=${queryParam(campaign)}&pageURL=${ampdocUrl}&ref=${documentReferrer}" 
  }, 
  "vars": { 
   "host": "statshost.publishersite.com" 
  }, 
  "extraUrlParams": { 
   "pageName": "Adobe Analytics Using amp-analytics tag", 
   "v1": "eVar1 test value" 
  } 
 } 
 </script> 
</amp-analytics>  
```

이 접근 방법에서는 `iframeMessage` 요청 매개 변수에 추가된 특별 쿼리 문자열 매개 변수를 통해 데이터를 유틸리티 웹 페이지에 보냅니다. 이 경우 `ampdocUrl AMP` 변수와 `documentReferrer`가 쿼리 문자열 매개 변수 `pageURL`에 추가된 것을 확인하고 위의 `iframeMessage` 요청을 각각 참조하십시오. 이러한 추가 쿼리 문자열 매개 변수의 이름은 [!DNL stats.html] 페이지(아래 표시)가 이 매개 변수에서 적절한 데이터를 수집하도록 구성되어 있는 한 원하는 방식대로 지정할 수 있습니다.

The `"adobeanalytics_nativeConfig"` template also adds query string parameters based on the variables listed in the `extraUrlParams` section of the amp-analytics tag. 이 경우 `pageName` 페이지가 사용하게 되는 `v1` 및 [!DNL stats.html] 매개 변수가 지정된 것을 볼 수 있습니다.

Be aware that you can only use a single `amp-analytics` template at a time and can not use the `"adobeanalytics"` template as well as the `"adobeanalytics_nativeConfig"` template on the same AMP. 동일한 AMP에서 사용하려고 할 경우, 브라우저 콘솔에 오류가 표시될 수 있으며 방문자 수가 잘못 부풀려집니다.

```
<html> 
<head> 
<title>Stats Test</title> 
<script language="JavaScript" type="text/javascript" src="VisitorAPI.js"></script> 
<script language="JavaScript" type="text/javascript" src="AppMeasurement.js"></script> 
<html> 
<head> 
<title>Stats Test</title> 
<script language="JavaScript" type="text/javascript" src="VisitorAPI.js"></script> 
<script language="JavaScript" type="text/javascript" src="AppMeasurement.js"></script> 
</head> 
<body> 
<script> 
var v_orgId = "1234567@PublisherOrg"; 
var s_account = "reportSuite"; 
var s_trackingServer = "metrics.publisher.com"; 
var s_visitorNamespace = "publisherNamespace"; 
var visitor = Visitor.getInstance(v_orgId); 
visitor.trackingServer = s_trackingServer; 
var s = s_gi(s_account); 
s.account = s_account; 
s.trackingServer = s_trackingServer; 
s.visitorNamespace = s_visitorNamespace; 
s.visitor = visitor; 
s.pagename = s.Util.getQueryParam("pageName"); 
s.eVar1=s.Util.getQueryParam("v1"); 
s.campaign=s.Util.getQueryParam("campaign"); 
s.pageURL=s.Util.getQueryParam("pageURL"); 
s.referrer=s.Util.getQueryParam(“ref”); 
s.t(); 
</script> 
</body> 
</html> 
```

위에 표시된 대로, 기존의 [!DNL VisitorAPI.js]와 [!DNL AppMeasurement.js](예제에서 설명됨) 또는 기존의 구현에서 사용하는 것은 무엇이든 사용하거나 링크로 연결한 다음, 올바른 구성 매개 변수를 추가할 수 있습니다. 올바른 값을 올바른 변수에 입력하기 위해서는, 제공된 `s.Util.getQueryParam` 함수를 사용하여 `iframeMessage` URL에서 전달한 값을 선택하고 일반적인 페이지에서 하듯이 적절한 변수를 설정할 수 있습니다. If you use tag management software like Adobe's [ [!DNL Dynamic Tag Manager] ](https://www.adobe.com/solutions/digital-marketing/dynamic-tag-management.html), the query string parameters should be straightforward to capture. 이 경우 `s.pageName`은 쿼리 문자열 매개 변수 `pageName`으로 전달한 값으로 설정되어 있습니다. 여기에서 페이지 이름은 *`Adobe Analytics Example 2`*.

>[!IMPORTANT]
>
>Due to restrictions on iframes in the AMP framework, your [!DNL stats.html] page must be hosted on a separate subdomain from the domain the AMP itself is hosted on. AMP 프레임워크는 AMP 페이지 자체가 존재하고 있는 것과 동일한 하위 도메인의 iframe을 허용하지 않습니다. 예를 들어 AMP가 [!DNL amp.example.com]에서 호스트된다면, [!DNL stats.html] 페이지를 반드시 [!DNL ampmetrics.example.com] 등과 같은 별도의 하위 도메인에서 호스트하십시오.

유틸리티 페이지는 원래 사이트에서 호스트되므로 모든 AMP에서 기존의 개인정보 보호정책을 지원하기 위해 추가 작업을 할 필요가 없습니다. 이는 최종 사용자가 기본 사이트의 추적을 옵트 아웃하는 경우 추가적인 단계를 수행하지 않아도 모든 AMP의 추적 또한 옵트 아웃하게 됨을 의미합니다. 이 유틸리티 페이지를 사용한다는 것은 AMP에서 캡처한 측정을 나머지 [!DNL Experience Cloud]와 통합할 수 있도록(예를 들어 [!DNL Experience Cloud]를 사용하여 타깃팅된 광고를 위해) AMP가 Adobe의 [!DNL Adobe Audience Manager] ID 서비스를 지원할 수 있음을 의미합니다.

To reiterate, if your organization is not yet using the [!DNL Experience Cloud] ID service (or has tag management software like Adobe's [!DNL Dynamic Tag Manager]), you can tag the [!DNL stats.html] page however you want. 기존 구현을 참조 점으로 사용하십시오. 표준 구현과 유일하게 다른 점은 설정하려는 각 변수에 대해 amp-analytics `iframeMessage` URL에서(또는 [!DNL document.URL] 페이지 내에서는 [!DNL stats.html]) 적용할 수 있는 데이터 포인트를 얻게 된다는 것입니다. 또한, AMP 레퍼러나 AMP 페이지 URL과 같은 [AMP용 변수](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md)를 사용하려면(위에서 설명한 것처럼) 위의 예제와 같이 해당 변수를 iframeMessage 개체에 포함하십시오.

이 솔루션이 유연한 만큼 경고 또한 존재합니다. `amp-analytics``iframeMessage` 의 내재된 제한 사항 때문에 이 개체는 한 번에 한 페이지 로드에서만 로드할 수 있습니다. This means you will not be able to do link tracking or video tracking with the `"adobeanalytics_nativeConfig"` template. Moreover, some DOM values that are typically captured automatically by our [!DNL AppMeasurement] code, such as `referrer` (which impacts the Search Engine Keyword reports, Referrer, and Referrer Type reports, or may include a marketing campaign tracking code) will have to be passed manually to the `iframeMessage` using whatever AMP variables [are available](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md). 이 때문에 AMP 데이터를 기존의 보고서 세트에 넣는 경우 값 AMP로 사용자 지정 변수를 설정하여, 앞서 언급한 보고서들을 볼 때 AMP 트래픽을 제외할 수 있게 하는 것이 좋습니다. 그렇지만, 브라우저, 장치, 화면 크기 또는 해상도와 같은 표준 기술 보고서는 자동으로 작동해야 합니다.

마지막으로, iframe은 별도의 페이지로 로드되고 해당 페이지에서 JavaScript를 완전히 실행하므로 AMP는 AMP 표준에서 의도한 만큼 가볍지는 않습니다. 명확히 말하자면 이것은 페이지 로드 시간에 영향을 주지는 않지만(iframe은 페이지 로드가 완료된 후 로드됨) CPU와 네트워크는 다른 경우보다 약간 더 로드할 것이므로, 원활한 스크롤에 영향을 줄 수도 있습니다. 실제로 큰 영향이 관찰되지 않았지만 Adobe에서는 Google과 함께 이러한 접근 방법이 사용자 환경에 미치는 영향을 최소화하고자 노력하고 있습니다.

## 요약 {#section_4D8ED26084F249738A5C2BC66B933A07}

If you need click tracking and don't mind visitors being counted as entirely new visitors separate from your site, use the `"adobeanalytics"` tracking template, with our recommendation that you put the data into a *`separate report suite`*. [!DNL Experience Cloud] ID 서비스가 필요한 경우 방문자가 방문하거나 인플레이션이 부풀려지는 것을 원하지 않으며, 페이지 로드 시 Analytics만 실행하면 됩니다. `"adobeanalytics_nativeConfig"` 이 솔루션을 사용하는 것이 좋습니다.

Adobe Analytics에서는 Google 및 게시자와 파트너 관계를 맺어 업계 선두의 분석 기능을 매우 빠른 사용자 환경에서 모바일 웹의 게시자에게 제공하게 되어 기쁘게 생각합니다. 현재 이 두 가지 솔루션에서 수익이 발생하고 있음에도 불구하고 Adobe에서는 고객들의 더욱 진화하고 있는 분석 요구에 답하기 위한 최상의 장기적 솔루션을 만드는 데 전념하고 있습니다.

AMP 프로젝트는 빠르게 움직이고 있으며 빈번하게 변경되므로 [ 여기](https://github.com/Adobe-Marketing-Cloud/mobile-services/tree/master/samples/mobile-web/amphtml)를 자주 확인하여 예제의 업데이트를 살펴보십시오. 여기에서 설명한 내용은 시작하기에는 충분하지만 통합은 더 개선되고 시간이 지남에 따라 더 많은 게시자가 AMP를 채택할 것이므로 변경 사항이 발생할 것입니다.

질문이나 문제가 있을 경우, 담당 Adobe 컨설턴트나 고객 지원 센터에 문의하십시오.

## FAQ {#section_5F57AA2DE0C5452FB65241058A924C73}

<table id="table_9A2ED5E482E8423CB54F99613C04BEA0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 질문 </th> 
   <th colname="col2" class="entry"> 답변 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 비디오 추적을 <code>"adobeanalytics"</code> 또는 <code>"adobeanalytics_nativeConfig"</code> 템플릿에 사용할 수 있습니까? </p> </td> 
   <td colname="col2"> <p> 안타깝지만 아직 사용할 수 없습니다. AMP 표준에서는 "표시", "클릭" 및 "타이머"용 트리거만 지원하고, amp-analytics 태그로 수신할 수 있는 비디오 추적을 위한 명시적 트리거는 아직 지원하지 않습니다. 또한, <code>"adobeanalytics_nativeConfig"</code> 태그는 한 번만 로드할 수 있으므로 AMP가 로드된 후 발생하는 비디오 보기와는 호환되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>비교에서 <code>"adobeanalytics_nativeConfig"</code> 템플릿에 대한 방문자 인플레이션이 더 낮다고 설명되어 있는데 어떤 의미입니까? <code>"adobeanalytics"</code> 또는 <code>“adobeanalytics_nativeConfig”</code> 솔루션에서 방문자 인플레이션을 유발하는 것은 무엇입니까? </p> </td> 
   <td colname="col2"> <p><code>"adobeanalytics"</code> 템플릿은 Adobe Analytics에서 방문자 ID 쿠키를 설정하도록 허용하지 않습니다. 이는 사용자의 AMP 페이지에 대한 모든 방문 및 방문자가 자신의 보고서 세트에서 독립적인 새로운 방문과 방문자로 처리됨을 의미합니다. </p> <p>그러나 <code>"adobeanalytics_nativeConfig"</code> 템플릿을 사용하면 Safari 브라우저를 사용하는 새 방문자를 제외하고, 거의 모든 경우에 Adobe Analytics 방문자 ID 쿠키를 설정할 수 있습니다. 즉, 이전에 게시자의 사이트를 방문하지 않은 Safari의 방문자가 Adobe Analytics 보고 시 부풀려집니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AMP용으로 별도의 보고서 세트를 사용해야 합니까? </p> </td> 
   <td colname="col2"> <p>방문자/방문 인플레이션 문제 때문에 adobeanalytics 템플릿을 사용하는 경우 AMP에 대한 별도의 보고서 세트를 사용하는 것이 좋습니다. 하지만, 필요한 경우 해당 트래픽을 결합된 보고서 세트에서 분리할 수 있도록 JavaScript 버전도 amp-analytics 태그에서 "AMP vX.X"로 설정할 예정입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="keyword">Experience Cloud</span> ID 서비스란 무엇입니까? 이 서비스가 필요한 이유는 무엇입니까?  </p> </td> 
   <td colname="col2"> <p><a href="https://marketing.adobe.com/resources/help/en_US/mcvid/" format="https" scope="external"> ID 서비스 </a> (이전 <span class="term"> 방문자 ID 서비스 </span>) 는 <span class="keyword"> Experience Cloud </span> 코어 서비스를 활성화하고 다른 Adobe <span class="keyword"> Experience Cloud </span> 솔루션 간의 통합을 허용합니다. <span class="keyword">Adobe Audience Manager</span>나 <span class="keyword">Adobe Target</span>과의 통합 사항이 있을 경우 이 서비스를 사용할 수 있습니다. 이 서비스는 예정된 많은 <span class="keyword">Adobe Analytics</span> 기능의 기반이기도 합니다. ID 서비스 지원이 필요하거나 향후에 필요한 경우 <code>iframeMessage</code> 솔루션을 사용하는 것이 좋습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><code>"adobeanalytics_nativeConfig"</code> 템플릿의 경우 어디에서 유틸리티 페이지를 호스트해야 합니까? </p> </td> 
   <td colname="col2"> <p>AMP 표준에서는 AMP의 자체 도메인과 하위 도메인에서 iframe이 로드되는 것을 허용하지 않습니다. 따라서, 특히 회사에 AMP 캐싱에 대해 계획하는 자체 CDN이 있는 경우, 사용자의 주 사이트와는 별개인 하위 도메인에서 유틸리티 페이지를 호스트하는 것이 좋습니다. 호환성을 최대화하려면, 실제 AMP 컨텐츠가 배치될 위치와 분리된 <span class="filepath">ampmetrics.publisher.com</span>과 같은 하위 도메인을 선택하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이 솔루션은 <span class="keyword">Facebook 인스턴트 아티클</span>와 유사하지 않습니까 ? Facebook 인스턴트 아티클로 <span class="keyword">Adobe Analytics</span>를 어떻게 설정합니까? </p> </td> 
   <td colname="col2"> <p> Facebook 인스턴트 아티클에서는 위에서 개략적으로 설명한 대로 nativeConfig 솔루션과 유사한 솔루션을 지원합니다. 사실 위에서 만든 stats.html 페이지는 AMP와 FIA 모두에 대한 분석 요구를 동시에 충족할 수 있습니다. FIA에서의 추적 구현에 대한 자세한 내용은 <a href="../../implement/js-implementation/analytics-facebook-instant-articles.md#concept_AC9AD1431CD14F919E329A161A80AA08" format="dita" scope="local"> Facebook 인스턴트 아티클 </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

