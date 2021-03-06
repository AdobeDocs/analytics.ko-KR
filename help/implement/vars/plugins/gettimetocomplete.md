---
title: getTimeToComplete
description: 작업을 완료하는 데 걸린 시간을 측정합니다.
feature: Variables
exl-id: 90a93480-3812-49d4-96f0-8eaf5a70ce3c
source-git-commit: 7c7a7d8add9edb1538df12b440bc0a15f09efe5e
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 97%

---

# Adobe 플러그인: getTimeToComplete

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getTimeToComplete` 플러그인은 사용자가 사이트에서 프로세스를 완료하는 데 걸리는 시간을 추적합니다. 시계는 `start` 작업이 호출될 때 시작되고 `stop` 작업이 호출될 때 종료됩니다. 사이트에서 완료하는 데 시간이 걸리는 워크플로가 있고 방문자가 완료하는 데 걸리는 시간을 알고 싶은 경우 이 플러그인을 사용하는 것이 좋습니다. 세부 기간이 단 1초로만 줄어들기 때문에 사이트의 워크플로가 소요되는 시간이 짧은 경우 (3초 미만) 이 플러그인을 사용할 필요가 없습니다.

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
    * Action Type: Initialize getTimeToComplete
1. Save and publish the changes to the rule.-->

## 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
1. [!UICONTROL 사용자 지정 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 버튼이 표시됩니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화 ([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getTimeToComplete v4.0 */
function getTimeToComplete(sos,cn,exp,tp){var f=sos,m=cn,l=exp,e=tp;if("-v"===f)return{plugin:"getTimeToComplete",version:"4.0"};var k=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof k&&(k.contextData.getTimeToComplete="4.0");window.formatTime=window.formatTime||function(c,b,d){function e(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(!("undefined"===typeof c||isNaN(c)||0>Number(c))){var h="";"string"===typeof b&&"d"===b||("string"!==typeof b||!e("h,m,s",b))&&86400<=c?(b=86400,h="days",d=isNaN(d)?1:b/(d*b)):"string"===typeof b&&"h"===b||("string"!==typeof b||!e("m,s",b))&&3600<=c?(b=3600,h="hours",d=isNaN(d)?4:b/(d*b)):"string"===typeof b&&"m"===b||("string"!==typeof b||!e("s",b))&&60<=c?(b=60,h="minutes",d=isNaN(d)?2:b/(d*b)):(b=1,h="seconds",d=isNaN(d)?.2:b/d);h=Math.round(c*d/b)/d+" "+h;0===h.indexOf("1 ")&&(h=h.substring(0,h.length-1));return h}};window.cookieWrite=window.cookieWrite||function(c,b,d){if("string"===typeof c){var e=window.location.hostname,h=window.location.hostname.split(".").length-1;if(e&&!/^[0-9.]+$/.test(e)){h=2<h?h:2;var f=e.lastIndexOf(".");if(0<=f){for(;0<=f&&1<h;)f=e.lastIndexOf(".",f-1),h--;f=0<f?e.substring(f):e}}g=f;b="undefined"!==typeof b?""+b:"";if(d||""===b)if(""===b&&(d=-60),"number"===typeof d){var k=new Date;k.setTime(k.getTime()+6E4*d)}else k=d;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(d?" expires="+k.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,d=b.indexOf(" "+c+"="),e=0>d?d:b.indexOf(";",d);return(c=0>d?"":decodeURIComponent(b.substring(d+2+c.length,0>e?b.length:e)))?c:""};f=f?f.toLowerCase():"start";if("stop"===f||"start"===f){m=m?m:"s_gttc";e?e="d"===e?864E5:"h"===e?36E5:"s"===e?1E3:6E4:(l=30,e=6E4);l=isNaN(l)?30:l;l*=e;k=cookieRead(m);e=new Date;if("stop"===f&&k)return l=Math.round((e.getTime()-k)/1E3),cookieWrite(m,"",0),formatTime(l);"start"!==f||k?k&&Number(k)<e.getTime()+18E5&&cookieWrite(m,k,30):(f=String(e.getTime()),e.setTime(e.getTime()+l),cookieWrite(m,f,e))}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getTimeToComplete` 함수에서는 다음 인수를 사용합니다.

* **`sos`** (선택 사항, 문자열): 타이머를 시작하려면 `"start"`으로 설정합니다. 타이머를 중지하려면 `"stop"`으로 설정합니다. 기본값은 `"start"`입니다.
* **`cn`** (선택 사항, 문자열): 시작 시간을 저장할 쿠키의 이름입니다. 기본값은 `"s_gttc"`입니다.
* **`exp`** (선택 사항, 정수): 쿠키 (및 타이머)가 만료되는 일 수입니다. 기본값은 `0`이고, 이 값은 브라우저 세션의 종료를 나타냅니다.

이 함수를 호출하면 `"start"` 작업과 `"stop"` 작업 사이에 걸린 일, 시간, 분 및/또는 초가 포함된 문자열이 반환됩니다.

## 예

```js
// Start the timer when the visitor starts the checkout
if(s.events.indexOf("scCheckout") > -1) getTimeToComplete("start");

// Stop the timer when the visitor makes the purchase and set prop1 to the time difference between stop and start
// Sets prop1 to the amount of time it took to complete the purchase process
if(s.events.indexOf("purchase") > -1) s.prop1 = getTimeToComplete("stop");

// Simultaneously track the time it takes to complete a purchase and to fill out a registration form
// Stores each timer in their own respective cookies so they run independently
if(inList(s.events, "scCheckout")) getTimeToComplete("start", "gttcpurchase");
if(inList(s.events, "purchase")) s.prop1 = getTimeToComplete("start", "gttcpurchase");
if(inList(s.events, "event1")) getTimeToComplete("start", "gttcregister", 7);
if(inList(s.events, "event2")) s.prop2 = getTimeToComplete("stop", "gttcregister", 7);
```

## 버전 내역

### 4.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 3.1 (2019년 9월 30일)

* 첫 번째 인수에 &quot;start&quot; 또는 &quot;stop&quot;이라는 값을 필요로 하는 논리를 추가했습니다.  전달된 다른 모든 값은 플러그인의 실행을 중지합니다.
* `inList 2.0` 플러그인을 `inList 2.1`로 업데이트했습니다.

### 3.0 (2018년 8월 23일)

* `formatTime v1.0` 플러그인을 `formatTime v1.1`로 업데이트했습니다.

### 3.0 (2018년 4월 17일)

* 포인트 릴리스 (다시 컴파일됨, 더 작은 코드 크기).
* 사소한 버그가 수정되었습니다.

### 2.0 (2016년 6월 21일)

* `p_fo` 플러그인에 대한 종속성을 제거했습니다.
* H-코드 및 AppMeasurement와의 호환성을 추가했습니다.
* 콘솔 로깅을 추가했습니다.
