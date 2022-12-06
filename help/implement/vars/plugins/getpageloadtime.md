---
title: getPageLoadTime
description: 페이지를 로드하는 데 걸리는 시간을 추적합니다.
feature: Variables
exl-id: 9bf0e26b-f1af-48a6-900a-712f7e588d37
source-git-commit: a00511d62960dc077620b2882f4e7f816267f939
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 64%

---

# Adobe 플러그인: getPageLoadTime

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getPageLoadTime` 플러그인은 JavaScript 성능 개체를 사용하여 페이지를 완전히 로드하는 데 걸리는 시간을 측정할 수 있도록 해 줍니다. 페이지를 로드하는 데 걸리는 시간을 측정하려면 이 플러그인을 사용하는 것이 좋습니다.

>참고/경고: 이 플러그인을 이전 버전에서 업그레이드하는 경우 이 함수를 호출하는 코드도 변경해야 합니다.  프로덕션 환경에 배포하기 전에 구현을 확인하고 철저하게 테스트하십시오

<!--## Install the plug-in using the Web SDK or the Adobe Analytics extension

Adobe offers an extension that allows you to use most commonly-used plug-ins.

1. Log in to [Adobe Experience Platform Data Collection](https://experience.adobe.com/data-collection) using your AdobeID credentials.
1. Click the desired tag property.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. Install and publish the [!UICONTROL Common Analytics Plugins] extension
1. If you haven't already, create a rule labeled "Initialize Plug-ins" with the following configuration:
    * Condition: None
    * Event: Core – Library Loaded (Page Top)
1. Add an action to the above rule with the following configuration:
    * Extension: Common Analytics Plugins
    * Action Type: Initialize getPageLoadTime
1. Save and publish the changes to the rule.-->

## 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
1. [!UICONTROL 사용자 지정 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 버튼이 표시됩니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화 ([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getPageLoadTime v3.0 */
!function(){let e=globalThis.window||this;e.getPageLoadTime=function(t){let i=function(){if(e.s_c_il){for(let t in e.s_c_il)if("s_c"===e.s_c_il[t]._c)return e.s_c_il[t]}}();function n(){var i=performance.timing;i.loadEventEnd>0&&(clearInterval(e.pi),""===e.cookieRead("s_plt")&&e.cookieWrite("s_plt",function e(t,i){if(t>=0&&i>=0)return t-i<6e4&&t-i>=0?parseFloat((t-i)/1e3).toFixed(2):60}(i.loadEventEnd,i.navigationStart)+","+t)),e.ptc=i.loadEventEnd}if(i&&(i.contextData.getPageLoadTime="3.1"),t=t||i&&i.pageName||document.location.href,e.cookieWrite=e.cookieWrite||function(t,i,n){if("string"==typeof t){if(g=function(){var t=e.location.hostname,i=e.location.hostname.split(".").length-1;if(t&&!/^[0-9.]+$/.test(t)){i=2<i?i:2;var n=t.lastIndexOf(".");if(0<=n){for(;0<=n&&1<i;)n=t.lastIndexOf(".",n-1),i--;n=0<n?t.substring(n):t}}return n}(),i=void 0!==i?""+i:"",n||""===i){if(""===i&&(n=-60),"number"==typeof n){var o=new Date;o.setTime(o.getTime()+6e4*n)}else o=n}return!!t&&(document.cookie=encodeURIComponent(t)+"="+encodeURIComponent(i)+"; path=/;"+(n?" expires="+o.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!=typeof cookieRead)&&cookieRead(t)===i}},e.cookieRead=e.cookieRead||function(e){if("string"!=typeof e)return"";e=encodeURIComponent(e);var t=" "+document.cookie,i=t.indexOf(" "+e+"="),n=0>i?i:t.indexOf(";",i);return(e=0>i?"":decodeURIComponent(t.substring(i+2+e.length,0>n?t.length:n)))?e:""},e.p_fo=e.p_fo||function(t){return e.__fo||(e.__fo={}),!e.__fo[t]&&(e.__fo[t]={},!0)},performance&&e.p_fo("performance")){var o=performance;o.clearResourceTimings(),""!==e.cookieRead("s_plt")&&(o.timing.loadEventEnd>0&&clearInterval(e.pi),this._pltLoadTime=e.cookieRead("s_plt").split(",")[0],this._pltPreviousPage=e.cookieRead("s_plt").split(",")[1],e.cookieWrite("s_plt","")),0===o.timing.loadEventEnd?e.pi=setInterval(function(){n()},250):o.timing.loadEventEnd>0&&(e.ptc?e.ptc===o.timing.loadEventEnd&&1===o.getEntries().length&&(e.pwp=setInterval(function(){var i;(i=performance).getEntries().length>0&&(e.ppfe===i.getEntries().length?clearInterval(e.pwp):e.ppfe=i.getEntries().length),""===e.cookieRead("s_plt")&&e.cookieWrite("s_plt",((i.getEntries()[i.getEntries().length-1].responseEnd-i.getEntries()[0].startTime)/1e3).toFixed(2)+","+t)},500)):n())}},e.getPageLoadTime.getVersion=function(){return{plugin:"getPageLoadTime",version:"3.0"}}}();
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getPercentPageViewed` 함수에서는 다음 인수를 사용합니다.

* **`pv`** (선택 사항, 문자열): 페이지 로드 시간을 와 상호 연관시킬 차원입니다.  이 값은 페이지 자체를 식별하는 값과 같아야 합니다. 설정하지 않으면 이 인수의 기본값이 Adobe AppMeasurement pageName 변수(즉, s.pageName)이거나 s.pageName이 설정되지 않은 경우 URL로 설정됩니다.

이 함수를 호출하면 아무 것도 반환되지 않습니다. 대신 다음 변수를 설정합니다.

* `window._pltPreviousPage`: 이전 페이지의 값(즉, pv 인수에 전달된 변수)입니다
* `window._pltLoadTime`: 이전 페이지가 로드되는 데 걸린 시간 (초)을 설정합니다.

getPageLoadTime 플러그인은 다음과 같은 하나의 자사 쿠키를 만듭니다.

* `s_plt`: 이전 페이지가 로드되는 데 걸린 시간(초)입니다.  또한 pv 인수에 전달된 값의 값도 포함합니다.  브라우저 세션이 끝날 때 만료됩니다.

## 예

```js
// 1. Run the getPageLoadTime function if the pageName variable is set
// 2. Set prop10 to the load time of the previous page
// 3. Set eVar10 to the name of the previous page
// 4. Set event100 to the load time (in seconds) of the previous page. A numeric event is required to capture this value.
// You can then use event100 in calculated metrics to obtain the average page load time per page.
if(s.pageName) getPageLoadTime();
if(window._pltPreviousPage)
{
  s.prop10 = window._pltLoadTime;
  s.eVar10 = window._pltPreviousPage
  s.events = "event100=" + window._pltLoadTime;
}
```

## 버전 내역

### 3.0(2022년 12월 6일)

* 플러그인을 솔루션 불가지론자로 만들기 위해 완전히 다시 작성합니다.  예를 들어, 이제 AEP 웹 SDK와 호환됩니다
* 를 생성합니다. `_pltPreviousPage` 및 `_pltLoadTime` AppMeasurement 개체가 아닌 창 개체의 변수
* s_pltp 쿠키가 필요하지 않습니다. 이제 모든 항목이 s_plt 쿠키에만 저장됩니다
* 문제 해결에 도움이 되도록 getVersion 함수를 포함합니다

### 2.0.1(2021년 3월 26일)

* 플러그인이 개체 값을 제대로 설정하지 못하는 문제가 수정되었습니다.

### 2.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 1.0 (2018년 5월 22일)

* 초기 릴리스.
