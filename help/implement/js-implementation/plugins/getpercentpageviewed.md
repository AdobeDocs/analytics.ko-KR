---
description: 방문자의 스크롤 활동을 측정하여 다른 페이지로 이동하기 전에 표시되는 페이지 양을 확인합니다. 이 플러그인을 사용하면 사용자가 평균적으로 보는 컨텐츠의 양을 결정하고 사용자의 행동을 기반으로 페이지 길이 및 레이아웃을 최적화할 수 있습니다.
keywords: Analytics 구현
seo-description: 방문자의 스크롤 활동을 측정하여 다른 페이지로 이동하기 전에 표시되는 페이지 양을 확인합니다. 이 플러그인을 사용하면 사용자가 평균적으로 보는 컨텐츠의 양을 결정하고 사용자의 행동을 기반으로 페이지 길이 및 레이아웃을 최적화할 수 있습니다.
seo-title: getPercentPageViewed
solution: Analytics
subtopic: 플러그인
title: getPercentPageViewed
topic: 개발자 및 구현
uuid: 1751dcdb-699f-4bd1-8bcb-5e62fa24896a
translation-type: ht
source-git-commit: f9912a0da5930be965e4d249f3d2c1891cfd6ed6

---


# getPercentPageViewed

getPercentPageViewed 플러그인은 방문자가 다른 페이지로 이동하기 전에 본 페이지 수를 확인하기 위해 방문자의 스크롤 활동을 측정합니다.

>[!NOTE]
>웹 페이지가 길지 않아 방문자가 얼마나 아래로 스크롤했는지 측정할 필요가 없는 경우 getPercentPageViewed 플러그인을 사용하지 않아도 됩니다. 또한 종료 페이지에서만 스크롤 활동을 측정하려는 경우 이 플러그인을 사용할 수 없습니다.

## 전제 조건

getPercentPageViewed 플러그인을 실행하려면 AppMeasurement 및 handlePPVevents 도우미 플러그인이 있어야 합니다.

## 구현

이 플러그인을 구현하려면 코드를 복사하여 [!DNL AppMeasurement] 파일의 **[!UICONTROL Plugins]** 섹션 내 아무 곳에나 붙여넣습니다.

>[!NOTE]
>AppMeasurement 파일에 굵게 표시된 코드의 주석/버전 번호를 추가하면 Adobe 컨설팅에서 잠재적 구현 문제를 해결하는 데 도움이 됩니다.

필요에 따라 doPlugins 함수 내에서 `getPercentPageViewed` 함수를 실행할 수 있습니다(아래 예제 호출 참조).

## 전달할 인수

| 인수 | 정의 |
|---|---|
| pid(선택 사항, 문자열) | 플러그인 측정에서 제공한 백분율과 상관 관계가 있는 페이지 식별자입니다. 기본값은 Analytics의 pageName 변수이거나, pageName 변수가 설정되지 않은 경우 URL입니다. |
| ch(선택 사항, 부울) | 이 인수에 대한 권장/기본값은 "true"입니다. 이 플러그인이 SPA 코드, 동적 HTML 등으로 인해 페이지의 초기 로드 후 페이지 크기에 대한 변경 사항을 고려하지 않도록 하려면 이를 "false"로 설정합니다. |

## 반환

getPercentPageViewed 플러그인은 아무 것도 반환하지 않습니다. 대신 AppMeasurement 개체 내에 다음 변수를 설정합니다.

* `s._ppvPreviousPage`: 새 페이지가 로드될 때까지 최종 측정값을 사용할 수 없으므로 본 이전 페이지의 이름입니다.
* `s._ppvHighestPercentViewed`: 방문자가 본 이전 페이지의 가장 높은 비율(높이 기준)입니다. 즉, 방문자가 이전 페이지에서 가장 멀리 스크롤한 지점입니다.
* `s._ppvInitialPercentViewed`: 이전 페이지를 처음 로드했을 때 표시된 이전 페이지의 백분율입니다.
* `s._ppvHighestPixelSeen`: 방문자가 이전 페이지를 스크롤할 때 본 가장 큰 총 픽셀 수.

## 쿠키

getPercentPageViewed 플러그인은 페이지에서 페이지로 전달되는 `s_ppv`라고 하는 쿠키를 만듭니다. 쿠키의 콘텐츠는 위에 설명된 네 가지 변수에 삽입된 값을 포함하며, 세션이 끝날 때 만료됩니다.

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

위의 코드 샘플:
* s.pageName이 설정되었는지 확인하고, 설정되었으면 코드가 getPercentPageViewed 함수를 실행합니다.
* `getPercentPageViewed` 함수가 실행되면 위의 "반환" 섹션에 설명된 변수가 만들어집니다.
* 반환 변수가 성공적으로 설정된 경우:

   * 이 코드는 s.prop1을 `s._ppvPreviousPag` 값(예: `s.pageName`의 이전 값 또는 이전 페이지)과 동일하게 설정합니다.
   * 또한 이 코드는 s.prop2를 이전 페이지에서 가장 많이 본 비율과 이전 페이지에서 처음 본 비율과 같게 설정합니다.

>[!NOTE]
>전체 페이지가 처음 로드될 때 표시되면 가장 많이 본 비율과 처음 본 비율이 모두 100이 됩니다. 그러나 처음 로드될 때 전체 페이지가 표시되지 않지만 방문자가 페이지를 아래로 스크롤하지 않고 다음 페이지로 이동한 경우 가장 많이 본 비율과 처음 본 비율 차원이 모두 같은 값이 됩니다.

**샘플 호출 2**

s.prop5가 전체 페이지 이름이 아닌 롤업된 "페이지 유형"을 캡처하도록 따로 설정되어 있다고 가정합니다.

다음 코드는 s.prop5가 설정되었는지 여부를 확인하고, 설정되어 있으면 값을 "이전 페이지"로 저장하여 가장 많이 본 비율 및 처음 본 비율 차원과의 상관 관계를 만듭니다. 이 값은 여전히 `s._ppvPreviousPage` 변수에 저장되지만 이전 페이지 이름 대신 이전 페이지 유형인 것처럼 처리할 수 있습니다.

```
if(s._ppvPreviousPage)
{
s.prop1 = s._ppvPreviousPage;
s.prop2 = "highestPercentViewed = " + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed;
}  
```

## S 개체 바꾸기

기본 AppMeasurement 라이브러리 개체를 "s" 이외의 이름으로 인스턴스화할 때 다음에 있는 플러그인 코드의 다음 부분을 변경합니다.

`s.getPercentPageViewed=function(pid,ch)`

아래와 같이 변경하는 것을 의미합니다.

`[objectname].getPercentPageViewed=function(pid,ch)`

## 배포할 코드

PLUGINS SECTION: `s_code.js` 파일에서 PLUGINS SECTION이라는 레이블이 지정된 영역에 다음 코드를 추가합니다. 플러그인 코드의 이 부분은 어떤 방식으로도 변경하지 마십시오.

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
body.clientHeight,document.documentElement.clientHeight));c=(window.pageYOffset||window.document.documentElement.scrollTop||window.document.body.scrollTop)+(window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight);d=Math.min(Math.round
(c/f*100),100);var e="";!a.c_r("s_tp")||a.unescape(a.c_r("s_ppv").split(",")[0])!==a.ppvID||1==a.ppvChange&&
a.c_r("s_tp")&&f!= a.c_r("s_tp")?(a.c_w("s_tp",f),a.c_w("s_ppv","")):e=a.c_r("s_ppv");var b=e&&-1<e.indexOf(",")?e.split(",",4):[];f=0<b.length?b[0]:escape(a.ppvID);var g=1<b.length?parseInt(b[1]):d,h=2<b.length?parseInt(b[2]):d;b=3<b.length?parseInt(b[3]):c;0<d&&(e=f+","+(d>g?d:g)+","+h+","+(c>b?c:b));a.c_w("s_ppv",e)}}}; 

/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v2.0 (Requires AppMeasurement) */ 
s.p_fo=function(on){var s=this;s.__fo||(s.__fo={});if(s.__fo[on])return!1;s.__fo[on]={};return!0}; 
/******************************************** END CODE TO DEPLOY ********************************************/
```
