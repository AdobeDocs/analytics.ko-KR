---
title: getVisitNum
description: 방문자의 현재 방문 횟수를 추적합니다.
translation-type: tm+mt
source-git-commit: fb1cdcb53732be46037a79587fc2541e629496e3
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 99%

---


# Adobe 플러그인: getVisitNum

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getVisitNum` 플러그인은 원하는 기간(일 수) 내에 사이트를 방문하는 모든 방문자에 대해 방문 횟수를 반환합니다. Analysis Workspace에서는 비슷한 기능을 제공하는 &#39;방문 횟수&#39; 차원을 제공합니다. 방문 횟수가 증가되는 방식을 더 자유롭게 제어하려면 이 플러그인을 사용하는 것이 좋습니다. Analysis Workspace의 내장 &#39;방문 횟수&#39; 차원이 보고 요구 사항에 적합한 경우 이 플러그인은 필요하지 않습니다.

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
   * 작업 유형: getVisitNum 초기화
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
/* Adobe Consulting Plugin: getVisitNum v4.2 */
function getVisitNum(rp,erp){var a=rp,l=erp;function m(c){return isNaN(c)?!1:(parseFloat(c)|0)===parseFloat(c)}function n(c){var b=new Date,e=isNaN(c)?0:Math.floor(c);b.setHours(23);b.setMinutes(59);b.setSeconds(59);"w"===c&&(e=6-b.getDay());if("m"===c){e=b.getMonth()+1;var a=b.getFullYear();e=(new Date(a?a:1970,e?e:1,0)).getDate()-b.getDate()}b.setDate(b.getDate()+e);"y"===c&&(b.setMonth(11),b.setDate(31));return b}if("-v"===a)return{plugin:"getVisitNum",version:"4.2"};var f=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof f&&(f.contextData.getVisitNum="4.2");window.cookieWrite=window.cookieWrite||function(c,b,e){if("string"===typeof c){var a=window.location.hostname,d=window.location.hostname.split(".").length-1;if(a&&!/^[0-9.]+$/.test(a)){d=2<d?d:2;var h=a.lastIndexOf(".");if(0<=h){for(;0<=h&&1<d;)h=a.lastIndexOf(".",h-1),d--;h=0<h?a.substring(h):a}}g=h;b="undefined"!==typeof b?""+b:"";if(e||""===b)if(""===b&&(e=-60),"number"===typeof e){var f=new Date;f.setTime(f.getTime()+6E4*e)}else f=e;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(e?" expires="+f.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof window.cookieRead)?window.cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};a=a?a:365;l="undefined"!==typeof l?!!l:m(a)?!0:!1;var p=(new Date).getTime();f=n(a);if(window.cookieRead("s_vnc"+a))var d=window.cookieRead("s_vnc"+a).split("&vn="),k=d[1];if(window.cookieRead("s_ivc"))return k?(window.cookieWrite("s_ivc",!0,30),k):"unknown visit number";if("undefined"!==typeof k)return k++,d=l&&m(a)?p+864E5*a:d[0],f.setTime(d),window.cookieWrite("s_vnc"+a,d+"&vn="+k,f),window.cookieWrite("s_ivc",!0,30),k;d=m(a)?p+864E5*a:n(a).getTime();window.cookieWrite("s_vnc"+a,d+"&vn=1",f);window.cookieWrite("s_ivc",!0,30);return"1"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getVisitNum` 메서드에서는 다음 인수를 사용합니다.

* **`rp`** (선택 사항, 정수 또는 문자열): 방문 횟수 카운터가 재설정되기 전 일 수입니다. 설정하지 않으면 기본값이 `365`로 설정됩니다.
   * 이 인수가 `"w"`이면 카운터는 그 주가 끝날 때(이번 주 토요일 오후 11시 59분) 재설정됩니다.
   * 이 인수가 `"m"`이면 카운터는 그 달이 끝날 때(이번 달 마지막 날) 재설정됩니다.
   * 이 인수가 `"y"`이면 카운터는 한 해가 끝날 때(12월 31일) 재설정됩니다.
* **`erp`** (선택 사항, 부울): `rp` 인수가 숫자인 경우 이 인수는 방문 횟수 만료를 연장할지 여부를 결정합니다. `true`로 설정하면 이후 사이트 히트는 방문 횟수 카운터를 재설정합니다. `false`로 설정하면 방문 번호 카운터가 재설정될 때 이후 사이트 히트가 연장되지 않습니다. 기본값은 `true`입니다. `rp` 인수가 문자열이면 이 인수는 유효하지 않습니다.

방문자가 30분 동안 활동이 없다가 사이트를 다시 방문할 때마다 방문 횟수가 증가합니다. 이 메서드를 호출하면 방문자의 현재 방문 횟수를 나타내는 정수가 반환됩니다.

이 플러그인은 `[LENGTH]`가 `rp` 인수에 전달되는 값인 경우 `"s_vnc[LENGTH]"`라는 자사 쿠키를 설정합니다. 예를 들어 `"s_vncw"`, `"s_vncm"` 또는 `"s_vnc365"`라는 쿠키를 설정할 수 있습니다. 이 쿠키의 값은 주가 끝날 때, 달이 끝날 때 또는 365일 동안의 비활동 후와 같은 방문 카운터가 재설정되는 때를 나타내는 Unix 타임스탬프의 조합입니다. 여기에는 현재 방문 횟수도 포함되어 있습니다. 이 플러그인은 `true`로 설정되고 30분 동안 활동이 없으면 만료되는 `"s_ivc"`라는 다른 쿠키를 설정합니다.

## 호출 예

### 예 #1

지난 365일 이내에 사이트를 방문하지 않은 방문자의 경우 다음 코드는 s.prop1을 값 1과 동일하게 설정합니다.

```js
s.prop1=s.getVisitNum();
```

### 예 #2

첫 번째 방문 후 364일 이내에 사이트를 재방문한 방문자의 경우, 다음 코드는 s.prop1을 2로 설정합니다.

```js
s.prop1=s.getVisitNum(365);
```

이 방문자가 두 번째 방문 후 364일 이내에 사이트를 재방문한 경우, 다음 코드는 s.prop1을 3으로 설정합니다.

```js
s.prop1=s.getVisitNum(365);
```

### 예 #3

첫 번째 방문 후 179일 이내에 사이트를 재방문한 방문자의 경우, 다음 코드는 s.prop1을 2로 설정합니다.

```js
s.prop1=s.getVisitNum(180,false);
```

하지만 이 방문자가 두 번째 방문하고 1일 이상의 기간 후 사이트를 재방문한 경우, 다음 코드는 s.prop1을 1으로 설정합니다.

```js
s.prop1=s.getVisitNum(180,false);
```

호출의 두 번째 인수가 false인 경우 방문 횟수를 1로 &quot;재설정&quot;해야 할 시기를 결정하는 루틴은 방문자가 사이트를 처음 방문한 후 &quot;x&quot;일(이 예에서는 365일)로 결정합니다.

두 번째 인수가 true면(또는 설정되지 않으면) 플러그인은 방문자가 활동하지 않은지 &quot;x&quot;일(다시, 이 예에서는 365일)이 된 이후에만 방문 횟수를 1로 재설정합니다.

### 예 #4

이번 주 동안(일요일에 시작) 처음으로 사이트를 방문하는 모든 방문자의 경우 다음 코드는 s.prop1을 1로 설정합니다.

```js
s.prop1=s.getVisitNum("w");
```

### 예 #5

이번 달 동안(각 달의 1일에 시작) 처음으로 사이트를 방문하는 모든 방문자의 경우 다음 코드는 s.prop1을 1로 설정합니다.

```js
s.prop1=s.getVisitNum("m");
```

getVisitNum 플러그인은 소매 기반 달력(예: 4-5-4, 4-4-5 등)을 고려하지 않는다는 점을 기억하십시오.

### 예 #6

이번 연도 동안(1월 1일에 시작) 처음으로 사이트를 방문하는 모든 방문자의 경우 다음 코드는 s.prop1을 1로 설정합니다.

```js
s.prop1=s.getVisitNum("y");
```

### 예 #7

그 주의 방문자 방문 횟수, 그 월의 방문자 방문 횟수 및 그 연도의 방문자 방문 횟수(모두 다른 Analytics 변수 내에서)를 추적하려면 다음과 유사한 코드를 사용해야 합니다.

```js
s.prop1=s.getVisitNum("w");
s.prop2=s.getVisitNum("m");
s.prop3=s.getVisitNum("y");
```

이 경우 플러그인은 기간당 개별 방문 횟수를 계속 추적할 수 있도록 세 개의 서로 다른 쿠키(서로 다른 각 기간에 대해 하나씩)를 만듭니다.

## 버전 기록

### 4.2(2021년 3월 19일)

* 컨텍스트 데이터로 버전 번호를 추가했습니다.

### 4.11(2019년 9월 30일)

* `erp` 인수가 명시적으로 `false`로 설정되던 문제를 수정했습니다.

### 4.1(2018년 5월 21일)

* `endOfDatePeriod` 플러그인을 v1.1로 업데이트했습니다.

### 4.0(2018년 4월 17일)

* 포인트 릴리스(다시 컴파일됨, 더 작은 코드 크기).
* 플러그인이 이제 `rp` 인수를 기반으로 쿠키를 동적으로 생성함에 따라 쿠키 인수를 제거했습니다.

### 3.0(2016년 6월 5일)

* 전체 정비
* 다양한 버전의 `getVisitNum` 플러그인에서 사용할 수 있는 모든 이전 솔루션을 결합했습니다.
