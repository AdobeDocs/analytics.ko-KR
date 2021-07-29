---
title: getPercentPageViewed
description: 방문자가 본 페이지의 비율을 검색합니다.
exl-id: 7a842cf0-f8cb-45a9-910e-5793849bcfb8
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 95%

---

# Adobe 플러그인: getPercentPageViewed

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getPercentPageViewed` 플러그인은 방문자의 스크롤 활동을 측정하여 다른 페이지로 이동하기 전에 표시되는 페이지 양을 확인합니다. 페이지 높이가 작거나 스크롤 활동을 측정하지 않으려는 경우에는 이 플러그인이 필요하지 않습니다.

## Adobe Experience Platform에서 태그를 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해 주는 확장 기능을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [데이터 수집 UI](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그] 버튼을 클릭합니다.
1. [!UICONTROL 일반적인 Analytics 플러그인] 확장 기능을 설치 및 게시합니다.
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨 (페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: getPercentPageViewed 초기화
1. 변경 사항을 저장하고 규칙에 게시합니다.

##  사용자 지정 코드 편집기를 사용하여 플러그인 설치

1. AdobeID 자격 증명을 사용하여 [데이터 수집 UI](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 [!UICONTROL 구성] 버튼을 클릭합니다.
1. [!UICONTROL 사용자 지정 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 버튼이 표시됩니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화 ([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getPercentPageViewed v5.0.1 */
function getPercentPageViewed(pid,ch){var n=pid,r=ch;function p(){if(window.ppvID){var a=Math.max(Math.max(document.body.scrollHeight,document.documentElement.scrollHeight),Math.max(document.body.offsetHeight,document.documentElement.offsetHeight),Math.max(document.body.clientHeight,document.documentElement.clientHeight)),b=window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight,d=(window.pageYOffset||window.document.documentElement.scrollTop||window.document.body.scrollTop)+b,f=Math.min(Math.round(d/a*100),100),l=Math.floor(d/b);b=Math.floor(a/b);var c="";if(!window.cookieRead("s_tp")||decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])!==window.ppvID||window.p_fo(window.ppvID)||1==window.ppvChange&&window.cookieRead("s_tp")&&a!=window.cookieRead("s_tp")){(decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])!==window.ppvID||window.p_fo(window.ppvID+"1"))&&window.cookieWrite("s_ips",d);if(window.cookieRead("s_tp")&&decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])===window.ppvID){window.cookieRead("s_tp");c=window.cookieRead("s_ppv");var h=-1<c.indexOf(",")?c.split(","):[];c=h[0]?h[0]:"";h=h[3]?h[3]:"";var q=window.cookieRead("s_ips");c=c+","+Math.round(h/a*100)+","+Math.round(q/a*100)+","+h+","+l}window.cookieWrite("s_tp",a)}else c=window.cookieRead("s_ppv");var k=c&&-1<c.indexOf(",")?c.split(",",6):[];a=0<k.length?k[0]:encodeURIComponent(window.ppvID);h=1<k.length?parseInt(k[1]):f;q=2<k.length?parseInt(k[2]):f;var t=3<k.length?parseInt(k[3]):d,u=4<k.length?parseInt(k[4]):l;k=5<k.length?parseInt(k[5]):b;0<f&&(c=a+","+(f>h?f:h)+","+q+","+(d>t?d:t)+","+(l>u?l:u)+","+(b>k?b:k));window.cookieWrite("s_ppv",c)}}if("-v"===n)return{plugin:"getPercentPageViewed",version:"5.0.1"};var m=function(){if("undefined"!==typeof window.s_c_il)for(var a=0,b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof m&&(m.contextData.getPercentPageViewed="5.0.1");window.pageName="undefined"!==typeof m&&m.pageName||"";window.cookieWrite=window.cookieWrite||function(a,b,d){if("string"===typeof a){var f=window.location.hostname,l=window.location.hostname.split(".").length-1;if(f&&!/^[0-9.]+$/.test(f)){l=2<l?l:2;var c=f.lastIndexOf(".");if(0<=c){for(;0<=c&&1<l;)c=f.lastIndexOf(".",c-1),l--;c=0<c?f.substring(c):f}}g=c;b="undefined"!==typeof b?""+b:"";if(d||""===b)if(""===b&&(d=-60),"number"===typeof d){var h=new Date;h.setTime(h.getTime()+6E4*d)}else h=d;return a&&(document.cookie=encodeURIComponent(a)+"="+encodeURIComponent(b)+"; path=/;"+(d?" expires="+h.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof window.cookieRead)?window.cookieRead(a)===b:!1}};window.cookieRead=window.cookieRead||function(a){if("string"===typeof a)a=encodeURIComponent(a);else return"";var b=" "+document.cookie,d=b.indexOf(" "+a+"="),f=0>d?d:b.indexOf(";",d);return(a=0>d?"":decodeURIComponent(b.substring(d+2+a.length,0>f?b.length:f)))?a:""};window.p_fo=window.p_fo||function(a){window.__fo||(window.__fo={});if(window.__fo[a])return!1;window.__fo[a]={};return!0};var e=window.cookieRead("s_ppv");e=-1<e.indexOf(",")?e.split(","):[];n=n?n:window.pageName?window.pageName:document.location.href;e[0]=decodeURIComponent(e[0]);window.ppvChange="undefined"===typeof r||1==r?!0:!1;"undefined"!==typeof m&&m.linkType&&"o"===m.linkType||(window.ppvID&&window.ppvID===n||(window.ppvID=n,window.cookieWrite("s_ppv",""),p()),window.p_fo("s_gppvLoad")&&window.addEventListener&&(window.addEventListener("load",p,!1),window.addEventListener("click",p,!1),window.addEventListener("scroll",p,!1)),this._ppvPreviousPage=e[0]?e[0]:"",this._ppvHighestPercentViewed=e[1]?e[1]:"",this._ppvInitialPercentViewed=e[2]?e[2]:"",this._ppvHighestPixelsSeen=e[3]?e[3]:"",this._ppvFoldsSeen=e[4]?e[4]:"",this._ppvFoldsAvailable=e[5]?e[5]:"")};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getPercentPageViewed` 메서드에서는 다음 인수를 사용합니다.

* **`pid`** (선택 사항, 문자열): 플러그인의 측정으로 제공된 백분율과 상호 연관시킬 수 있는 페이지 기반 식별자입니다.  기본값은 `pageName` 변수입니다.
* **`ch`**  (선택 사항, 부울): 플러그인이 초기 로드 후 페이지 크기에 대한 변경 사항을 고려하지 않게 하려면 이 인수를 `false` (또는 `0`)로 설정하십시오. 생략하면 이 인수의 기본값이 `true`로 설정됩니다. 대부분의 경우에는 이 인수를 생략하는 것이 좋습니다.

이 메서드를 호출하면 아무 것도 반환되지 않습니다. 대신 다음 변수를 설정합니다.

* `s._ppvPreviousPage`: 본 이전 페이지의 이름입니다. 현재 페이지에 대한 최종 스크롤 측정은 새 페이지가 로드될 때까지 사용할 수 없습니다.
* `s._ppvHighestPercentViewed`: 방문자가 본 이전 페이지의 가장 높은 비율 (높이 기준)입니다. 방문자가 이전 페이지에서 아래로 가장 멀리 스크롤한 지점입니다.
* `s._ppvInitialPercentViewed`: 이전 페이지를 처음 로드했을 때 표시된 이전 페이지의 백분율.
* `s._ppvHighestPixelsSeen`: 방문자가 이전 페이지를 스크롤할 때 본 가장 큰 총 픽셀 수.
* `s._ppvFoldsSeen`: 방문자가 이전 페이지를 스크롤할 때 도달한 가장 큰 &quot;페이지 접기&quot; 수입니다. 이 변수에는 &quot;페이지 상단&quot; 접기가 포함됩니다.
* `s._ppvFoldsAvailable`: 이전 페이지에서 아래로 스크롤할 수 있는 총 &quot;페이지 접기&quot; 수입니다.

보고서에서 차원 데이터를 보려면 이러한 변수 중 하나 이상을 eVar에 지정하십시오.

이 플러그인은 위의 값을 포함하는 `s_ppv`라는 자사 쿠키를 만들며, 브라우저 세션이 끝날 때 만료됩니다.

## 호출 예

### 예 #1

다음 코드...

```js
if(s.pageName) s.getPercentPageViewed();
if(s._ppvPreviousPage)
{
  s.prop1 = s._ppvPreviousPage;
  s.prop2 = "highestPercentViewed=" + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed + " | foldsSeen=" + s._ppvFoldsSeen + " | foldsAvailable=" + s._ppvFoldsAvailable;
}
```

* s.pageName이 설정되었는지 확인하고, 설정되었으면 코드가 getPercentPageViewed 함수를 실행합니다
* getPercentPageViewed 함수가 실행되면 위의 &quot;반환&quot; 섹션에 설명된 변수가 만들어집니다.
* 반환 변수가 성공적으로 설정된 경우:
   * 이 코드는 s.prop1을 s._ppvPreviousPage의 값 (즉, s.pageName의 이전 값 또는 이전 페이지)과 동일하게 설정합니다.
   * 또한 이 코드는 방문자가 도달한 접기 수 및 사용 가능했던 접기 수와 함께 s.prop2를 이전 페이지에서 가장 많이 본 비율과 이전 페이지에서 처음 본 비율과 동일하게 설정합니다.

**참고**: 전체 페이지가 처음 로드될 때 표시되면 가장 많이 본 비율과 처음 본 비율이 모두 100이 되고 본 접기와 사용 가능한 접기는 모두 1이 됩니다.   페이지가 처음 로드될 때 전체 페이지가 표시되지는 않지만 방문자가 페이지를 아래로 스크롤하는 것을 끝내지 않고 다음 페이지로 이동하면 가장 많이 본 비율과 처음 본 비율 차원이 모두 같은 값이 됩니다.

### 예 #2

s.prop5가 전체 페이지 이름이 아닌 롤업된 &quot;페이지 유형&quot;을 캡처하도록 따로 설정되어 있다고 가정합니다.

다음 코드는 s.prop5가 설정되었는지 여부를 확인하고, 설정되어 있으면 값을 &quot;이전 페이지&quot;로 저장하여 가장 많이 본 비율 및 처음 본 비율 차원과의 상관 관계를 만듭니다.  이 값은 여전히 s._ppvPreviousPage 변수에 저장되지만 이전 페이지 이름 대신 이전 페이지 유형인 것처럼 처리할 수 있습니다.

```js
if(s.prop5) s.getPercentPageViewed(s.prop5);
if(s._ppvPreviousPage)
{
  s.prop1 = s._ppvPreviousPage;
  s.prop2 = "highestPercentViewed = " + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed;
}
```

## 버전 내역

### 5.0.1 (2021년 6월 22일)

* 일부 특수 문자로 인해 플러그인이 중단되는 문제가 해결되었습니다.

### 5.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### v4.0 (2019년 10월 7일)

* `s._ppvFoldsSeen` 및 `s._ppvFoldsAvailable` 솔루션을 추가했습니다.

### v3.01 (2018년 8월 13일)

* 페이지에 여러 AppMeasurement 개체가 있는 페이지의 문제가 해결되었습니다.

### v3.0 (2018년 4월 13일)

* 포인트 릴리스 (다시 컴파일됨, 더 작은 코드 크기)
* 이제 플러그인이 반환 값 대신 Adobe Analytics 변수에 지정할 변수를 만듭니다.
