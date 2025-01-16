---
title: getTimeSinceLastVisit
description: 두 방문 사이의 경과 시간을 측정합니다.
feature: Variables
exl-id: c5cef219-8a8a-4e57-a372-f2e063325a67
role: Admin, Developer
source-git-commit: 2b48ea372a5e0d8589f09d2209373bd4c47be578
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 72%

---

# Adobe 플러그인: getTimeSinceLastVisit

{{plug-in}}

`getTimeSinceLastVisit` 플러그인을 사용하면 방문자가 마지막 방문 후 사이트를 다시 방문하는 시간을 추적할 수 있습니다.

## 웹 SDK 확장을 사용하여 플러그인 설치

Adobe은 Web SDK에서 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해 주는 확장을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 왼쪽의 **[!UICONTROL 태그]**&#x200B;를 클릭한 다음 원하는 태그 속성을 클릭합니다.
1. 왼쪽의 **[!UICONTROL 확장]**&#x200B;을 클릭한 다음 **[!UICONTROL 카탈로그]** 탭을 클릭합니다
1. **[!UICONTROL 일반적인 웹 SDK 플러그인]** 확장을 찾아 설치합니다.
1. 왼쪽의 **[!UICONTROL 데이터 요소]**&#x200B;를 클릭한 다음 원하는 데이터 요소를 클릭합니다.
1. 다음 구성으로 원하는 데이터 요소 이름을 설정합니다.
   * 확장: 일반적인 웹 SDK 플러그인
   * 데이터 요소: `getTimeSinceLastVisit`
1. 변경 사항을 저장하고 데이터 요소에 게시합니다.

## 웹 SDK을 수동으로 구현하는 플러그인 설치

이 플러그인은 아직 웹 SDK의 수동 구현 내에서 사용할 수 없습니다.

## Adobe Analytics 확장을 사용하여 플러그인 설치

Adobe은 Adobe Analytics에서 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해 주는 확장을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그] 버튼을 클릭합니다.
1. [!UICONTROL 일반적인 Analytics 플러그인] 확장 기능을 설치 및 게시합니다.
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨 (페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: getTimeSinceLastVisit 초기화
1. 변경 사항을 저장하고 규칙에 퍼블리싱합니다.

## 사용자 지정 코드 편집기를 사용하여 플러그인 설치

일반 Analytics 플러그인 확장 프로그램을 사용하지 않으려면 사용자 지정 코드 편집기를 사용할 수 있습니다.

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
