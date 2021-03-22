---
title: getPageLoadTime
description: 페이지를 로드하는 데 걸리는 시간을 추적합니다.
translation-type: tm+mt
source-git-commit: b3c5fa41194d74725f48e12a546d8ce1c08b9b7d
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 98%

---


# Adobe 플러그인: getPageLoadTime

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getPageLoadTime` 플러그인은 JavaScript 성능 개체를 사용하여 페이지를 완전히 로드하는 데 걸리는 시간을 측정할 수 있도록 해줍니다. 페이지를 로드하는 데 걸리는 시간을 측정하려면 이 플러그인을 사용하는 것이 좋습니다.

## Adobe Experience Platform Launch 확장을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해주는 확장을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그] 단추를 클릭합니다.
1. [!UICONTROL 일반적인 Analytics 플러그인] 확장을 설치 및 게시합니다.
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨(페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: getPageLoadTime 초기화
1. 변경 사항을 저장하고 규칙에 게시합니다.

## Launch 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
1. [!UICONTROL 사용자 지정 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 단추가 표시됩니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여 넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여 넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getPageLoadTime v2.0 with performanceWriteFull, performanceWritePart, performanceCheck, and performanceRead helper functions (Requires AppMeasurement and the p_fo plugin) */
function getPageLoadTime(){function f(){function a(a,b){if(0<=a&&0<=b)return 6E4>a-b&&0<=a-b?parseFloat((a-b)/1E3).toFixed(2):60}var b=performance.timing;0<b.loadEventEnd&&(clearInterval(window.pi),""===window.cookieRead("s_plt")&&(window.cookieWrite("s_plt",a(b.loadEventEnd,b.navigationStart)),window.cookieWrite("s_pltp",window.pageName)));window.ptc=b.loadEventEnd}if(arguments&&"-v"===arguments[0])return{plugin:"getPageLoadTime",version:"2.0"};var c=function(){if("undefined"!==typeof window.s_c_il)for(var a=0,b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof c&&(c.contextData.getPageLoadTime="2.0");window.pageName="undefined"!==typeof c&&c.pageName||"";window.cookieWrite=window.cookieWrite||function(a,b,e){if("string"===typeof a){var c=window.location.hostname,h=window.location.hostname.split(".").length-1;if(c&&!/^[0-9.]+$/.test(c)){h=2<h?h:2;var d=c.lastIndexOf(".");if(0<=d){for(;0<=d&&1<h;)d=c.lastIndexOf(".",d-1),h--;d=0<d?c.substring(d):c}}g=d;b="undefined"!==typeof b?""+b:"";if(e||""===b)if(""===b&&(e=-60),"number"===typeof e){var k=new Date;k.setTime(k.getTime()+6E4*e)}else k=e;return a&&(document.cookie=encodeURIComponent(a)+"="+encodeURIComponent(b)+"; path=/;"+(e?" expires="+k.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(a)===b:!1}};window.cookieRead=window.cookieRead||function(a){if("string"===typeof a)a=encodeURIComponent(a);else return"";var b=" "+document.cookie,c=b.indexOf(" "+a+"="),f=0>c?c:b.indexOf(";",c);return(a=0>c?"":decodeURIComponent(b.substring(c+2+a.length,0>f?b.length:f)))?a:""};window.p_fo=window.p_fo||function(a){window.__fo||(window.__fo={});if(window.__fo[a])return!1;window.__fo[a]={};return!0};"undefined"!==typeof performance&&p_fo("performance")&&((c=performance,c.clearResourceTimings(),""!==window.cookieRead("s_plt")&&(0<c.timing.loadEventEnd&&clearInterval(window.pi),window._pltLoadTime=window.cookieRead("s_plt"),window._pltPreviousPage=window.cookieRead("s_pltp"),window.cookieWrite("s_plt",""),window.cookieWrite("s_pltp","")),0===c.timing.loadEventEnd)?window.pi=setInterval(function(){f()},250):0<c.timing.loadEventEnd&&(window.ptc?window.ptc===c.timing.loadEventEnd&&1===c.getEntries().length&&(window.pwp=setInterval(function(){var a=performance;0<a.getEntries().length&&(window.ppfe===a.getEntries().length?clearInterval(window.pwp):window.ppfe=a.getEntries().length);""===window.cookieRead("s_plt")&&(window.cookieWrite("s_plt",((a.getEntries()[a.getEntries().length-1].responseEnd-a.getEntries()[0].startTime)/1E3).toFixed(2)),window.cookieWrite("s_pltp",window.pageName))},500)):f()))};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getPageLoadTime` 메서드는 인수를 사용하지 않습니다. 이 메서드를 호출하면 아무 것도 반환되지 않고 대신 다음 변수를 설정합니다.

* `s._pltPreviousPage`: 로드 시간을 이전 페이지에 상호 연관시킬 수 있도록 이전 페이지를 설정합니다.
* `s._pltLoadTime`: 이전 페이지가 로드되는 데 걸린 시간(초)을 설정합니다.

getPageLoadTime 플러그인은 다음과 같이 두 개의 자사 쿠키를 만듭니다.

* `s_plt`: 이전 페이지가 로드되는 데 걸린 시간(초)입니다. 브라우저 세션이 끝날 때 만료됩니다.
* `s_pltp`: 이전 Adobe Analytics 이미지 요청에 기록된 `s.pageName` 변수의 값입니다. 브라우저 세션이 끝날 때 만료됩니다.

## 호출 예

### 예 #1

다음 코드를 실행하면...

```js
if(s.pageName) s.getPageLoadTime();
if(s._pltPreviousPage)
{
  s.prop10 = s._pltLoadTime;
  s.prop11 = s._pltPreviousPage
  s.eVar10 = prop11;
  s.events = "event100=" + s._pltLoadTime;
}
```

...다음 작업이 수행됩니다.

* s.pageName이 설정되어 있으면 getPageLoadTime 플러그인 실행
* s.prop10을 이전 페이지의 로드 시간과 동일하게 설정
* s.prop11 및 s.eVar10을 이전 페이지의 이름과 동일하게 설정(s.pageName에 기록된 대로).
* 사용자 지정 숫자 이벤트인 event100을 이전 페이지의 로드 시간과 동일하게 설정   이 경우 사용자 지정 이벤트의 사용은 이전 페이지의 모든 페이지 로드(모든 방문자/방문으로 인한 페이지 로드)에 대한 총 시간을 구할 수 있도록 해주며, 따라서 계산된 지표를 사용하여 각 페이지의 평균 페이지 로드 시간을 구할 수 있습니다.

## 버전 기록

### 2.0(2021년 3월 19일)

* 컨텍스트 데이터로 버전 번호를 추가했습니다.

### 1.0(2018년 5월 22일)

* 초기 릴리스.
