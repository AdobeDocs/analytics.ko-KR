---
title: getTimeSinceLastVisit
description: 두 방문 사이의 경과 시간을 측정합니다.
feature: Variables
exl-id: c5cef219-8a8a-4e57-a372-f2e063325a67
source-git-commit: 7c7a7d8add9edb1538df12b440bc0a15f09efe5e
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 97%

---

# Adobe 플러그인: getTimeSinceLastVisit

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getTimeSinceLastVisit` 플러그인을 사용하면 방문자가 마지막 방문 후 사이트를 다시 방문하는 시간을 추적할 수 있습니다.

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
    * Action Type: Initialize getTimeSinceLastVisit
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
/* Adobe Consulting Plugin: getTimeSinceLastVisit v2.0 */
function getTimeSinceLastVisit(){if(arguments&&"-v"===arguments[0])return{plugin:"getTimeSinceLastVisit",version:"2.0"};var h=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof h&&(h.contextData.getTimeSinceLastVisit="2.0");window.formatTime=window.formatTime||function(c,b,d){function f(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(!("undefined"===typeof c||isNaN(c)||0>Number(c))){var e="";"string"===typeof b&&"d"===b||("string"!==typeof b||!f("h,m,s",b))&&86400<=c?(b=86400,e="days",d=isNaN(d)?1:b/(d*b)):"string"===typeof b&&"h"===b||("string"!==typeof b||!f("m,s",b))&&3600<=c?(b=3600,e="hours",d=isNaN(d)?4:b/(d*b)):"string"===typeof b&&"m"===b||("string"!==typeof b||!f("s",b))&&60<=c?(b=60,e="minutes",d=isNaN(d)?2:b/(d*b)):(b=1,e="seconds",d=isNaN(d)?.2:b/d);e=Math.round(c*d/b)/d+" "+e;0===e.indexOf("1 ")&&(e=e.substring(0,e.length-1));return e}};window.cookieWrite=window.cookieWrite||function(c,b,d){if("string"===typeof c){var f=window.location.hostname,e=window.location.hostname.split(".").length-1;if(f&&!/^[0-9.]+$/.test(f)){e=2<e?e:2;var k=f.lastIndexOf(".");if(0<=k){for(;0<=k&&1<e;)k=f.lastIndexOf(".",k-1),e--;k=0<k?f.substring(k):f}}g=k;b="undefined"!==typeof b?""+b:"";if(d||""===b)if(""===b&&(d=-60),"number"===typeof d){var h=new Date;h.setTime(h.getTime()+6E4*d)}else h=d;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(d?" expires="+h.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,d=b.indexOf(" "+c+"="),f=0>d?d:b.indexOf(";",d);return(c=0>d?"":decodeURIComponent(b.substring(d+2+c.length,0>f?b.length:f)))?c:""};h=new Date;var m=h.getTime(),n=cookieRead("s_tslv")||0,l=Math.round((m-n)/1E3);h.setTime(m+63072E6);cookieWrite("s_tslv",m,h);return n?1800<l||cookieRead("s_inv")?(cookieRead("s_inv")&&(l=cookieRead("s_inv")),cookieWrite("s_inv",l,30),"0"!==l?formatTime(l):"New Visitor"):"":(cookieWrite("s_inv","0",30),"New Visitor")};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getTimeSinceLastVisit` 함수는 인수를 사용하지 않습니다. 이 메서드는 방문자가 마지막으로 사이트를 방문한 이후 경과된 시간을 반환합니다(다음 형식으로 변환됨).

* 마지막 방문 이후 30분에서 1시간 사이의 시간이 가장 가까운 0.5분 벤치마크로 설정됩니다. 예: `"30.5 minutes"`, `"53 minutes"`
* 1시간과 1일 사이의 시간은 가장 가까운 1/4시간 벤치마크로 반올림됩니다. 예: `"2.25 hours"`, `"7.5 hours"`
* 하루보다 큰 시간은 가장 가까운 일 벤치마크로 반올림됩니다. 예: `"1 day"`, `"3 days"`, `"9 days"`, `"372 days"`
* 방문자가 전에 방문한 적이 없거나 경과 시간이 2년을 넘는 경우 이 값은 `"New Visitor"`로 설정됩니다.

>[!NOTE]
>
>이 플러그인은 방문의 첫 번째 히트에 대한 값만 반환합니다.

이 플러그인은 현재 시간의 Unix 타임스탬프로 설정된 `"s_tslv"`라는 자사 쿠키를 만듭니다. 이 쿠키는 2년 동안 활동이 없으면 만료됩니다.

## 예

```js
// Given a visitor's first visit to the site
// Sets prop1 to "New Visitor"
s.prop1 = getTimeSinceLastVisit();

// 35 minutes later, the same visitor returns
// Sets prop1 to "35 minutes"
s.prop1 = getTimeSinceLastVisit();

// 4 days later, the same visitor returns
// Sets prop1 to "4 days"
s.prop1 = getTimeSinceLastVisit();
```

## 버전 내역

### 2.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 1.0 (2018년 4월 16일)

* 포인트 릴리스 (다시 컴파일된 코드 및 더 작은 크기).
* `getDaysSinceLastVisit` 플러그인에서 파생된 코드 (이제 더 이상 사용되지 않으며 이름이 변경됨).
* 이제 반환 값에 `formatTime` 및 `inList` 플러그인을 사용합니다.
