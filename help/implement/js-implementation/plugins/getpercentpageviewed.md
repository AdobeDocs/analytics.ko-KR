---
description: 방문자의 스크롤 활동을 측정하여 다른 페이지로 이동하기 전에 표시되는 페이지 양을 확인합니다. 이 플러그인을 사용하면 사용자가 평균적으로 보는 컨텐츠의 양을 결정하고 사용자의 행동을 기반으로 페이지 길이 및 레이아웃을 최적화할 수 있습니다.
keywords: Analytics 구현
seo-description: 방문자의 스크롤 활동을 측정하여 다른 페이지로 이동하기 전에 표시되는 페이지 양을 확인합니다. 이 플러그인을 사용하면 사용자가 평균적으로 보는 컨텐츠의 양을 결정하고 사용자의 행동을 기반으로 페이지 길이 및 레이아웃을 최적화할 수 있습니다.
seo-title: getPercentPageViewed
solution: Analytics
subtopic: 플러그인
title: getPercentPageViewed
topic: 개발자 및 구현
uuid: 1751 DCDB -699 F -4 BD 1-8 BCB -5 E 62 FA 24896 A
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getPercentPageViewed

Getpercentpageviewed 플러그인은 방문자의 스크롤 활동을 측정하여 다른 페이지로 이동하기 전에 방문자가 본 페이지의 양을 확인합니다.

>[!NOTE]
>웹 페이지가 높이가 작고 방문자가 아래로 스크롤되는 정도를 측정하지 않아도 Getpercentpageviewed 플러그인을 사용할 필요가 없습니다. 또한 종료 페이지에서만 스크롤 활동을 측정하려는 경우 이 플러그인을 사용할 수 없습니다.

## 전제 조건

Getpercentpageviewed 플러그인을 실행하려면 appmeasurement 및 handleppvevents Helper 플러그인이 있어야 합니다.

## 구현

To implement this plugin, copy and paste the code to anywhere within the **[!UICONTROL Plugins]** section of the [!DNL AppMeasurement] file.

>[!NOTE]
>코드의 굵은체 주석/버전 번호를 Appmeasurement 파일에 추가하면 Adobe Consulting에서 잠재적 구현 문제를 해결할 수 있습니다.

You can run the `getPercentPageViewed` function as needed within the doPlugins function (see example calls below.)

## 전달할 인수

| 인수 | 정의 |
|---|---|
| pid (선택 사항, 문자열) | 플러그인 측정에 의해 제공된 백분율과 상관 관계가 있는 페이지 식별자. Pagename 변수가 설정되지 않은 경우 기본적으로 Analytics pagename 변수나 URL 이 사용됩니다. |
| ch (선택 사항, 부울) | " true "는 이 인수에 권장되는/기본값입니다. SPA 코드, 동적 HTML 등으로 인해 이 플러그인이 초기 로드 후 페이지의 크기에 대한 변경 사항을 고려하지 않게 하려면 이 값을 "false" 로 설정하십시오. |

## 반환

Getpercentpageviewed 플러그인은 아무 것도 반환하지 않습니다. 대신 AppMeasurement 개체 내에 다음 변수를 설정합니다.

* `s._ppvPreviousPage`: 본 이전 페이지의 이름 (새 페이지가 로드될 때까지 최종 측정을 사용할 수 없기 때문에)
* `s._ppvHighestPercentViewed`: 방문자가 본 이전 페이지의 최고 퍼센트 (높이 수준). 즉, 방문자가 이전 페이지에서 아래로 스크롤한 가장 멀리 떨어진 점입니다.
* `s._ppvInitialPercentViewed`: 이전 페이지가 처음 로드되었을 때 표시되는 이전 페이지의 백분율입니다.
* `s._ppvHighestPixelSeen`: 방문자가 이전 페이지를 스크롤할 때 본 가장 큰 총 픽셀 수.

## 쿠키

The getPercentPageViewed plugin creates a cookie, called `s_ppv`, that is passed from page to page. 쿠키의 콘텐트에는 위에 설명된 네 가지 변수에 삽입된 값이 포함되며 세션이 끝날 때 만료됩니다.

## 호출 예

**샘플 호출 1**

```
if(s.pageName) s.getPercentPageViewed();
if(s._ppvPreviousPage)
{
s.prop1 = s._ppvPreviousPage;
s.prop2 = "highestPercentViewed=" + s._ppvHighestPercentViewed + "initialPercentViewed="s._ppvInitialPercentViewed;
}  
```

위의 코드 샘플은 다음과 같습니다.
* s. pagename 이 설정되어 있는지 확인하고 if so, the code will run the getpercentpageviewed functions.
* `getPercentPageViewed` 함수가 실행되면 위의 "반환" 섹션에 설명된 변수가 만들어집니다.
* " 반환 "변수가 성공적으로 설정된 경우:

   * The code sets s.prop1 equal to the value of `s._ppvPreviousPag`e (i.e. the previous value of `s.pageName`, or the previous page.)
   * 또한 코드는 s. prop 2를 이전 페이지의 가장 높은 백분율과 이전 페이지의 본 초기 비율과 같게 설정합니다.

>[!NOTE]
>전체 페이지가 처음 로드될 때 표시되는 경우 가장 높은 백분율과 본 초기 비율은 모두 100와 같습니다. 하지만 전체 페이지가 처음 로드될 때 표시되지 않지만 방문자가 다음 페이지로 이동하기 전에 페이지를 아래로 스크롤하지 않으면 가장 높은 백분율과 처음에 본 백분율이 모두 동일한 값과 같아집니다.

**샘플 호출 2**

s. prop 5가 전체 페이지 이름이 아닌 롤업된 "페이지 유형" 를 캡처하도록 aside로 설정되었다고 가정합니다.

다음 코드는 s. prop 5가 설정되어 있는지 여부를 결정하고, 그럴 경우, 가장 높은 백분율과 조회한 초기 백분율과 상관 관계를 유지하기 위해 값을 "이전 페이지" 로 저장합니다. The value is still stored in the `s._ppvPreviousPage` variable but can be treated as if it were the previous page type instead of the previous page name.

```
if(s._ppvPreviousPage)
{
s.prop1 = s._ppvPreviousPage;
s.prop2 = "highestPercentViewed = " + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed;
}  
```

## s 개체 바꾸기

" s "이외의 이름으로 기본 appmeasurement 라이브러리 개체를 인스턴스화할 때는 다음 플러그인 코드의 다음 부분을 변경하십시오.

`s.getPercentPageViewed=function(pid,ch)`

to this:

`[objectname].getPercentPageViewed=function(pid,ch)`

## 배포할 코드

플러그인 섹션: `s_code.js` 파일에서 PLUGINS SECTION이라는 레이블이 지정된 영역에 다음 코드를 추가합니다. 플러그인 코드의 이 부분은 어떤 방식으로도 변경하지 마십시오.

```
/******************************************* BEGIN CODE TO DEPLOY *******************************************/ 
/* Adobe Consulting Plugin: getPercentPageViewed v3.01 w/handlePPVevents helper function (Requires AppMeasurement and p_fo plugin) */
s.getPercentPageViewed=function(pid,ch){var s=this,a=s.c_r("s_ppv");a=-1<a.indexOf(",")?a.split(","):[];a[0]=s.unescape(a[0]); 
pid=pid?pid:s.pageName?s.pageName:document.location.href;s.ppvChange=ch?ch:!0;if("undefined"===typeof s.linkType||"o"!==
s.linkType)s.ppvID&&s.ppvID===pid||(s.ppvID=pid,s.c_w("s_ppv",""),s.handlePPVevents()),s.p_fo("s_gppvLoad")&&window
.addEventListener&&(window.addEventListener("load",s.handlePPVevents,!1),window.addEventListener("click",s.handlePPVevents, !1),window.addEventListener("scroll",s.handlePPVevents,!1),window.addEventListener("resize",s.handlePPVevents,!1)),s._ppvPreviousPage
=a[0]?a[0]:"",s._ppvHighestPercentViewed=a[1]?a[1]:"",s._ppvInitialPercentViewed=a[2]?a[2]:"",s._ppvHighestPixelsSeen=a[3]?a[3]:""}; 

/* Adobe Consulting Plugin: handlePPVevents helper function (for getPercentPageViewed v3.01 Plugin) */ 
s.handlePPVevents=function(){if("undefined"!==typeof s_c_il){for(var c=0,d=s_c_il.length;c<d;c++)if(s_c_il[c]&&s_c_il[c].getPercentPageViewed){var a=s_c_il[c];break}if(a&&a.ppvID){var f=Math.max(Math.max(document.body.scrollHeight,document.documentElement.scrollHeight),Math.max(document.body.offsetHeight,document.documentElement.offsetHeight),Math.max(document.
body.clientHeight,document.documentElement.clientHeight));c=(window.pageYOffset||window.document.documentElement.scrollTop|
|window.document.body.scrollTop)+(window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight);d=Math.min(Math.round
(c/f*100),100);var e="";!a.c_r("s_tp")||a.unescape(a.c_r("s_ppv").split(",")[0])!==a.ppvID||1==a.ppvChange&&
a.c_r("s_tp")&&f!= a.c_r("s_tp")?(a.c_w("s_tp",f),a.c_w("s_ppv","")):e=a.c_r("s_ppv");var b=e&&-1<e.indexOf(",")?e.split(",",4):[];f=0<b.length?b[0]:escape(a.ppvID);var g=1<b.length?parseInt(b[1]):d,h=2<b.length?parseInt(b[2]):d;b=3<b.length?parseInt(b[3]):c;0<d&&(e=f+","+(d>g?d:g)+","+h+","+(c>b?c:b));a.c_w("s_ppv",e)}}}; 

/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v2.0 (Requires AppMeasurement) */ 
s.p_fo=function(on){var s=this;s.__fo||(s.__fo={});if(s.__fo[on])return!1;s.__fo[on]={};return!0}; 
/******************************************** END CODE TO DEPLOY ********************************************/
```
