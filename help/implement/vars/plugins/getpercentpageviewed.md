---
title: getPercentPageViewed
description: 방문자가 본 페이지의 비율을 검색합니다.
feature: Variables
exl-id: 7a842cf0-f8cb-45a9-910e-5793849bcfb8
source-git-commit: 2575db561c244a9b52f98355137e73f05b3b7ee4
workflow-type: ht
source-wordcount: '644'
ht-degree: 100%

---

# Adobe 플러그인: getPercentPageViewed

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getPercentPageViewed` 플러그인은 방문자의 스크롤 활동을 측정하여 다른 페이지로 이동하기 전에 표시되는 페이지 양을 확인합니다. 페이지 높이가 작거나 스크롤 활동을 측정하지 않으려는 경우에는 이 플러그인이 필요하지 않습니다.

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
    * Action Type: Initialize getPercentPageViewed
1. Save and publish the changes to the rule.-->

## 사용자 정의 코드 편집기를 사용하여 플러그인 설치

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
1. [!UICONTROL 사용자 정의 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 버튼이 표시됩니다.
1. 사용자 정의 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 오브젝트가 인스턴스화 ([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣으십시오. 구현에서 코드의 댓글 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getPercentPageViewed v5.1 */
function getPercentPageViewed(pid,ch){var e=pid,i=ch;if("-v"===e)return{plugin:"getPercentPageViewed",version:"5.1"};var t=function(){if(void 0!==window.s_c_il){for(var e,i=0;i<window.s_c_il.length;i++)if((e=window.s_c_il[i])._c&&"s_c"===e._c)return e}}();function o(){if(window.ppvID){var e=Math.max(Math.max(document.body.scrollHeight,document.documentElement.scrollHeight),Math.max(document.body.offsetHeight,document.documentElement.offsetHeight),Math.max(document.body.clientHeight,document.documentElement.clientHeight)),i=window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight,t=(window.pageYOffset||window.document.documentElement.scrollTop||window.document.body.scrollTop)+i,o=Math.min(Math.round(t/e*100),100),n=Math.floor(e/i),p=Math.floor(t/i),s="";if(!window.cookieRead("s_tp")||decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])!==window.ppvID||window.p_fo(window.ppvID)||!0==window.ppvChange&&window.cookieRead("s_tp")&&e!=window.cookieRead("s_tp")){if((decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])!==window.ppvID||window.p_fo(window.ppvID+"1"))&&window.cookieWrite("s_ips",t),window.cookieRead("s_tp")&&decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])===window.ppvID){window.cookieRead("s_tp");var a=window.cookieRead("s_ppv"),c=a.indexOf(",")>-1?a.split(","):[],d=c[0]?c[0]:"",r=window.cookieRead("s_ips"),l=c[3]?c[3]:"";s=d+","+Math.round(r/e*100)+","+Math.round(l/e*100)+","+o+","+l+","+n+","+p}window.cookieWrite("s_tp",e)}else s=window.cookieRead("s_ppv");var v=s&&s.indexOf(",")>-1?s.split(",",7):[],f=v.length>0?v[0]:encodeURIComponent(window.ppvID),$=v.length>1?parseInt(v[1]):o,h=v.length>2?parseInt(v[2]):o,u=v.length>4?parseInt(v[4]):t,k=v.length>5?parseInt(v[5]):n,m=v.length>6?parseInt(v[6]):p;o>0&&(s=f+","+$+","+(o>h?o:h)+","+o+","+(t>u?t:u)+","+(n>k?n:k)+","+(p>m?p:m)),window.cookieWrite("s_ppv",s)}}void 0!==t&&(t.contextData.getPercentPageViewed="5.1"),window.pageName=void 0!==t&&t.pageName||"",window.cookieWrite=window.cookieWrite||function(e,i,t){if("string"==typeof e){if(g=function(){var e=window.location.hostname,i=window.location.hostname.split(".").length-1;if(e&&!/^[0-9.]+$/.test(e)){i=2<i?i:2;var t=e.lastIndexOf(".");if(0<=t){for(;0<=t&&1<i;)t=e.lastIndexOf(".",t-1),i--;t=0<t?e.substring(t):e}}return t}(),i=void 0!==i?""+i:"",t||""===i){if(""===i&&(t=-60),"number"==typeof t){var o=new Date;o.setTime(o.getTime()+6e4*t)}else o=t}return!!e&&(document.cookie=encodeURIComponent(e)+"="+encodeURIComponent(i)+"; path=/;"+(t?" expires="+o.toUTCString()+";":"")+(g?" domain="+g+";":""),void 0!==window.cookieRead)&&window.cookieRead(e)===i}},window.cookieRead=window.cookieRead||function(e){if("string"!=typeof e)return"";e=encodeURIComponent(e);var i=" "+document.cookie,t=i.indexOf(" "+e+"="),o=0>t?t:i.indexOf(";",t);return(e=0>t?"":decodeURIComponent(i.substring(t+2+e.length,0>o?i.length:o)))?e:""},window.p_fo=window.p_fo||function(e){return window.__fo||(window.__fo={}),!window.__fo[e]&&(window.__fo[e]={},!0)};var n=window.cookieRead("s_ppv"),p=n.indexOf(",")>-1?n.split(","):[];p[0]=p.length>0?decodeURIComponent(p[0]):"",e=e||(window.pageName?window.pageName:document.location.href),void 0===i||!0==i?window.ppvChange=!0:window.ppvChange=!1,void 0!==t&&t.linkType&&"o"===t.linkType||(window.ppvID&&window.ppvID===e||(window.ppvID=e,window.cookieWrite("s_ppv",""),o()),window.p_fo("s_gppvLoad2")&&window.addEventListener&&(window.addEventListener("load",o,!1),window.addEventListener("click",o,!1),window.addEventListener("scroll",o,!1)),this._ppvPreviousPage=p[0]?p[0]:"",this._ppvInitialPercentViewed=p[1]?p[1]:"",this._ppvHighestPercentViewed=p[2]?p[2]:"",this._ppvFinalPercentViewed=p[3]?p[3]:"",this._ppvHighestPixelsSeen=p[4]?p[4]:"",this._ppvFoldsAvailable=p[5]?p[5]:"",this._ppvFoldsSeen=p[6]?p[6]:"")}
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getPercentPageViewed` 함수에서는 다음 인수를 사용합니다.

* **`pid`**(선택, 문자열): 현재 페이지와 동일한 변수 또는 값입니다. 기본값은 Analytics AppMeasurement `pageName` 변수이거나, AppMeasurement pageName 변수가 설정되지 않은 경우 현재 URL입니다.
* **`ch`** (선택 사항, 부울): 플러그인이 초기 로드 후 페이지 크기에 대한 변경 사항을 고려하지 않게 하려면 이 인수를 `false` (또는 `0`)로 설정하십시오. 생략하면 이 인수의 기본값이 `true`로 설정됩니다. 대부분의 경우에는 이 인수를 생략하는 것이 좋습니다.

이 함수를 호출하면 아무 것도 반환되지 않습니다. 대신 다음 변수를 설정합니다.

* `window._ppvPreviousPage`: 본 이전 페이지의 이름입니다. 현재 페이지에 대한 최종 스크롤 측정은 새 페이지가 로드될 때까지 사용할 수 없습니다.
* `window._ppvInitialPercentViewed`: 이전 페이지가 처음 로드되었을 때 표시된 이전 페이지의 백분율입니다. 전체 페이지가 처음 로드될 때 표시되면 이 값은 `100`입니다.
* `window._ppvHighestPercentViewed`: 방문자가 본 이전 페이지의 가장 높은 비율(높이 기준)입니다. 방문자가 이전 페이지에서 아래로 가장 멀리 스크롤한 지점입니다. 전체 페이지가 처음 로드될 때 표시되면 이 값은 `100`입니다.
* `window._ppvFinalPercentViewed`: 방문자가 현재 페이지로 이동한 시점에 표시되었던 이전 페이지의 비율입니다. 이 값은 초기 조회 비율보다 크거나 같으며 최고 페이지 조회 비율보다 작거나 같습니다.
* `window._ppvHighestPixelsSeen`: 방문자가 이전 페이지를 스크롤할 때 본 가장 큰 총 픽셀 수.
* `window._ppvFoldsAvailable`: 이전 페이지에서 아래로 스크롤할 수 있는 총 “페이지 접기” 수입니다. 전체 페이지가 처음 로드될 때 표시되면 이 값은 `1`입니다.
* 
   * `window._ppvFoldsSeen`: 방문자가 이전 페이지를 스크롤할 때 도달한 가장 큰 “페이지 접기” 수입니다. 이 변수에는 “페이지 상단” 접기가 포함됩니다. 전체 페이지가 처음 로드될 때 표시되면 이 값은 `1`입니다.

보고서에서 차원 데이터를 보려면 이러한 변수 중 하나 이상을 eVar에 지정하십시오.

이 플러그인은 위의 값을 포함하는 `s_ppv`라는 자사 쿠키를 만들며, 브라우저 세션이 끝날 때 만료됩니다.

## 예

```js
// 1. Runs the getPercentPageViewed function if the page variable is set
// 2. Sets prop1 to the previous value of the page variable
// 3. Sets prop2 to the intial percent, the highest percent, and the final percent viewed; the number of folds available on the page, and the number of folds viewed ( of the previous page)
if(s.pageName) getPercentPageViewed();
if(_ppvPreviousPage)
{
  s.prop1 = _ppvPreviousPage;
  s.prop2 = "initialPercent=" + _ppvInitialPercent + " | highestPercent=" + _ppvHighestPercentViewed + " | finalPercent=" + _ppvFinalPercentViewed + " | foldsAvailable=" + _ppvFoldsAvailable + " | foldsSeen=" + _ppvFoldsSeen;
}

// Given prop5 operates as a page type variable:
// 1. Runs the getPercentPageViewed function if prop5 has a value
// 2. Sets prop1 to the previous value of the page type
// 3. Sets prop2 to the initial percent viewed and the highest percent viewed.
if(s.prop5) getPercentPageViewed(s.prop5);
if(_ppvPreviousPage)
{
  s.prop1 = _ppvPreviousPage;
  s.prop2 = "initialPercent=" + _ppvInitialPercent + " | highestPercent=" + _ppvHighestPercentViewed;
}
```

## 버전 내역

### 5.1(2022년 12월 8일)

* `_finalPercentViewed` 솔루션이 추가되었습니다.

### 5.0.1 (2021년 6월 22일)

* 일부 특수 문자로 인해 플러그인이 중단되는 문제가 해결되었습니다.

### 5.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### v4.0 (2019년 10월 7일)

* `s._ppvFoldsSeen` 및 `s._ppvFoldsAvailable` 솔루션을 추가했습니다.

### v3.01 (2018년 8월 13일)

* 페이지에 여러 AppMeasurement 오브젝트가 있는 페이지의 문제가 해결되었습니다.

### v3.0 (2018년 4월 13일)

* 포인트 릴리스 (다시 컴파일됨, 더 작은 코드 크기)
* 이제 플러그인이 반환 값 대신 Adobe Analytics 변수에 지정할 변수를 만듭니다.
