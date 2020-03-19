---
title: getPercentPageViewed
description: 방문자가 본 페이지의 비율을 검색합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:getPercentPageViewed

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

The `getPercentPageViewed` plug-in measures a visitor&#39;s scroll activity to see how much of a page they view before moving on to another page. 페이지 높이가 작거나 스크롤 활동을 측정하지 않으려는 경우에는 이 플러그인이 필요하지 않습니다.

## Launch 사용자 정의 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려면 사용자 정의 코드 편집기를 사용할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. 원하는 속성을 클릭합니다.
1. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 확장 프로그램 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
1. 단추를 표시하는 [!UICONTROL Configure tracking using custom code] 아코디언을 [!UICONTROL Open Editor] 확장합니다.
1. 사용자 정의 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여 넣습니다.
1. Analytics 확장 프로그램에 변경 사항을 저장하고 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣습니다(사용 [`s_gi`](../functions/s-gi.md)). 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getPercentPageViewed v4.0 w/handlePPVevents helper function (Requires p_fo plug-in) */
s.getPercentPageViewed=function(pid,ch){var s=this,a=s.c_r("s_ppv");a=-1<a.indexOf(",")?a.split(","):[];a[0]=s.unescape(a[0]); pid=pid?pid:s.pageName?s.pageName:document.location.href;s.ppvChange="undefined"===typeof ch||!0==ch?!0:!1;if("undefined"=== typeof s.linkType||"o"!==s.linkType)s.ppvID&&s.ppvID===pid||(s.ppvID=pid,s.c_w("s_ppv",""),s.handlePPVevents()), s.p_fo("s_gppvLoad") &&window.addEventListener&&(window.addEventListener("load",s.handlePPVevents,!1),window.addEventListener("click",s.handlePPVevents, !1),window.addEventListener("scroll",s.handlePPVevents,!1)),s._ppvPreviousPage=a[0]?a[0]:"",s._ppvHighestPercentViewed=a[1]?a[1]:"",s._ppvInitialPercentViewed=a[2]?a[2]:"",s._ppvHighestPixelsSeen=a[3]?a[3]:"",s._ppvFoldsSeen=a[4]?a[4]:"",s._ppvFoldsAvailable=a[5]?a[5]:""};

/* Adobe Consulting Plugin: handlePPVevents helper function (for getPercentPageViewed v4.0 Plugin) */
s.handlePPVevents=function(){if("undefined"!==typeof s_c_il){for(var c=0,g=s_c_il.length;c<g;c++)if(s_c_il[c]&& (s_c_il[c].getPercentPageViewed||s_c_il[c].getPreviousPageActivity)){var s=s_c_il[c];break}if(s&&s.ppvID){var f=Math.max (Math.max(document.body.scrollHeight,document.documentElement.scrollHeight),Math.max(document.body.offsetHeight, document.documentElement.offsetHeight),Math.max(document.body.clientHeight,document.documentElement.clientHeight)),h= window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight;c=(window.pageYOffset|| window.document.documentElement.scrollTop||window.document.body.scrollTop)+h;g=Math.min(Math.round(c/f*100),100);var k=Math.floor(c/h);h=Math.floor(f/h);var d="";if(!s.c_r("s_tp")||s.unescape(s.c_r("s_ppv").split(",")[0])!==s.ppvID||s.p_fo(s.ppvID) ||1==s.ppvChange&&s.c_r("s_tp")&&f!=s.c_r("s_tp")){(s.unescape(s.c_r("s_ppv").split(",")[0])!==s.ppvID||s.p_fo(s.ppvID+"1"))&&s.c_w("s_ips",c);if(s.c_r("s_tp")&&s.unescape(s.c_r("s_ppv").split(",")[0])===s.ppvID){s.c_r("s_tp");d=s.c_r("s_ppv");var e=-1< d.indexOf(",")?d.split(","):[];d=e[0]?e[0]:"";e=e[3]?e[3]:"";var l=s.c_r("s_ips");d=d+","+Math.round(e/f*100)+","+Math.round(l/ f*100)+","+e+","+k}s.c_w("s_tp",f)}else d=s.c_r("s_ppv");var b=d&&-1<d.indexOf(",")?d.split(",",6):[];f=0<b.length?b[0]: escape(s.ppvID);e=1<b.length?parseInt(b[1]):g;l=2<b.length?parseInt(b[2]):g;var m=3<b.length?parseInt(b[3]):c,n=4<b.length? parseInt(b[4]):k;b=5<b.length?parseInt(b[5]):h;0<g&&(d=f+","+(g>e?g:e)+","+l+","+(c>m?c:m)+","+(k>n?k:n)+","+(h>b?h:b)); s.c_w("s_ppv",d)}}};

/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v2.0 */
s.p_fo=function(on){var s=this;s.__fo||(s.__fo={});if(s.__fo[on])return!1;s.__fo[on]={};return!0};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `getPercentPageViewed` 메서드는 다음 인수를 사용합니다.

* **`pid`** (선택 사항, 문자열): 플러그인의 측정에서 제공한 백분율과 상호 연관시킬 수 있는 페이지 기반 식별자입니다.  기본값은 `pageName` 변수입니다.
* **`ch`** (선택 사항, 부울): 플러그인이 초기 로드 후 페이지 크기에 대한 변경 사항을 고려하지 않게 하려면 `false` (또는 `0`)로 설정합니다. 생략하면 이 인수의 기본값이 `true`로 설정됩니다. 대부분의 경우 이 인수를 생략하는 것이 좋습니다.

이 메서드를 호출하면 아무 것도 반환되지 않습니다.대신 다음 변수를 설정합니다.

* `s._ppvPreviousPage`:본 이전 페이지의 이름입니다. 현재 페이지에 대한 최종 스크롤 측정은 새 페이지가 로드될 때까지 사용할 수 없습니다.
* `s._ppvHighestPercentViewed`: 방문자가 본 이전 페이지의 가장 높은 비율(높이 기준)입니다. 방문자가 이전 페이지에서 아래로 스크롤한 가장 먼 지점입니다.
* `s._ppvInitialPercentViewed`: 이전 페이지를 처음 로드했을 때 표시된 이전 페이지의 백분율.
* `s._ppvHighestPixelsSeen`: 방문자가 이전 페이지를 스크롤할 때 본 가장 큰 총 픽셀 수.
* `s._ppvFoldsSeen`:방문자가 이전 페이지를 스크롤할 때 도달한 &quot;페이지 접기&quot;의 최대 수입니다. 이 변수에는 &quot;페이지 상단&quot; 접기가 포함됩니다.
* `s._ppvFoldsAvailable`:이전 페이지에서 아래로 스크롤할 수 있는 총 &quot;페이지 접기&quot; 수입니다.

보고서에서 차원 데이터를 보려면 이러한 변수 중 하나 이상을 eVar에 지정합니다.

이 플러그인은 위의 값을 포함하는 퍼스트 파티 쿠키를 `s_ppv` 만듭니다. 브라우저 세션이 끝날 때 만료됩니다.

## 호출 예

### 예 #1

다음 코드...

```js
if(s.pageName) s.getPercentPageViewed();
if(s._ppvPreviousPage)
{
  s.prop1 = s._ppvPreviousPage;
  s.prop2 = "highestPercentViewed=" + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed + " + | foldsSeen=" + s._ppvFoldsSeen + " | foldsAvailable=" + s._ppvFoldsAvailable;
}
```

* s.pageName이 설정되었는지 확인하고, 설정되었으면 코드가 getPercentPageViewed 함수를 실행합니다
* getPercentPageViewed 함수가 실행되면 위의 &quot;반환&quot; 섹션에 설명된 변수를 만듭니다
* &quot;반환&quot; 변수가 성공적으로 설정된 경우:
   * 코드는 s.prop1을 s.ppvPreviousPage 값(즉, s.pageName 또는 이전 페이지의 이전 값)과 동일하게 설정합니다.
   * 또한 코드는 방문자가 도달한 접기 수 및 사용 가능한 접기 수와 함께, s.prop2를 이전 페이지에서 본 가장 높은 비율 및 이전 페이지에서 본 초기 백분율과 같게 설정합니다

**참고**: 전체 페이지가 처음 로드될 때 표시되는 경우 가장 많이 본 비율과 처음 본 비율 모두 100이고 사용 가능한 접기 수와 접기 모두 1입니다.   처음 로드될 때 전체 페이지가 보이지 않지만 방문자가 다음 페이지로 이동하기 전에 페이지 아래로 스크롤되지 않으면 본 가장 높은 비율과 처음 본 비율 차원 모두 동일한 값이 됩니다.

### 예 #2

s.prop5가 전체 페이지 이름이 아닌 롤업된 &quot;페이지 유형&quot;을 캡처하도록 따로 설정되어 있다고 가정합니다.

다음 코드는 s.prop5가 설정되었는지 여부를 결정하고, 설정되면, 값을 &quot;이전 페이지&quot;로 저장하여 본 가장 높은 비율 및 본 초기 퍼센트 차원과 상관 관계를 만듭니다.  이 값은 여전히 s.ppvPreviousPage 변수에 저장되지만 이전 페이지 이름 대신 이전 페이지 유형인 것처럼 처리할 수 있습니다.

```js
if(s.prop5) s.getPercentPageViewed(s.prop5);
if(s._ppvPreviousPage)
{
  s.prop1 = s._ppvPreviousPage;
  s.prop2 = "highestPercentViewed = " + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed;
}
```

## 버전 내역

### v4.0(2019년 10월 7일)

* 추가 `s._ppvFoldsSeen` 및 `s._ppvFoldsAvailable` 솔루션

### v3.01(2018년 8월 13일)

* 페이지에 여러 AppMeasurement 개체가 있는 페이지의 문제를 수정했습니다.

### v3.0(2018년 4월 13일)

* 포인트 릴리스(다시 컴파일되고 더 작은 코드 크기)
* 이제 플러그인은 반환 값 대신 Adobe Analytics 변수에 할당할 변수를 만듭니다
