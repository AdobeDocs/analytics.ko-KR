---
title: formatTime
description: 초 수를 그에 해당하는 분, 시간 등으로 변환합니다.
translation-type: ht
source-git-commit: 56b21b6acb948c478d7b2a29c3e8375a8fe77ce2
workflow-type: ht
source-wordcount: '824'
ht-degree: 100%

---


# Adobe 플러그인: formatTime

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`formatTime` 플러그인을 사용하면 초 수를 전체 형식의 원하는 벤치마크 값으로 반올림하여 표시할 수 있습니다. 초 단위의 시간 값을 캡처하여 전체 형식(예: 분, 일 또는 주)으로 변환하려는 경우 이 플러그인을 사용하는 것이 좋습니다. 초 기반 값을 시간이 반올림된 형식으로 변환하는 것을 원치 않으면 이 플러그인은 불필요합니다.

## Adobe Experience Platform Launch 확장 기능을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해 주는 확장 기능을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그] 버튼을 클릭합니다.
1. [!UICONTROL 일반적인 Analytics 플러그인] 확장 기능을 설치 및 게시합니다.
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨(페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: formatTime 초기화
1. 변경 사항을 저장하고 규칙에 게시합니다.

## Launch 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 [!UICONTROL 구성] 버튼을 클릭합니다.
1. [!UICONTROL 사용자 지정 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 버튼이 표시됩니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: formatTime v2.0 */
function formatTime(ns,tf,bml){var f=ns,d=tf,e=bml;function h(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(arguments&&"-v"===arguments[0])return{plugin:"formatTime",version:"2.0"};var b=function(){if("undefined"!==typeof window.s_c_il)for(var b=0,c;b<window.s_c_il.length;b++)if(c=window.s_c_il[b],c._c&&"s_c"===c._c)return c}();"undefined"!==typeof b&&(b.contextData.formatTime="2.0");if(!("undefined"===typeof f||isNaN(f)||0>Number(f))){b="";if("string"===typeof d&&"d"===d||("string"!==typeof d||!h("h,m,s",d))&&86400<=f){var c=86400;var g="days";b=isNaN(e)?1:c/(e*c)}else"string"===typeof d&&"h"===d||("string"!==typeof d||!h("m,s",d))&&3600<=f?(c=3600,g="hours",b=isNaN(e)?4:c/(e*c)):"string"===typeof d&&"m"===d||("string"!==typeof d||!h("s",d))&&60<=f?(c=60,g="minutes",b=isNaN(e)?2:c/(e*c)):(c=1,g="seconds",b=isNaN(e)?.2:c/e);b=Math.round(f*b/c)/b+" "+g;0===b.indexOf("1 ")&&(b=b.substring(0,b.length-1));return b}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`formatTime` 메서드에서는 다음 인수를 사용합니다.

* **`ns`** (필수, 정수): 변환하거나 서식을 지정할 초 수
* **`tf`** (선택 사항, 문자열): 초를 반환하는 형식 유형. 기본값은 초입니다.
   * 일 단위 시간을 원하는 경우 `"d"`로 설정합니다(기본적으로 가장 가까운 1/4일 벤치마크로 반올림됨).
   * 시간 단위 시간을 원하는 경우 `"h"`로 설정합니다(기본적으로 가장 가까운 1/4시간 벤치마크로 반올림됨).
   * 분 단위 시간을 원하는 경우 `"m"`으로 설정합니다(기본적으로 가장 가까운 1/2분 벤치마크로 반올림됨).
   * 초 단위 시간을 원하는 경우 `"s"`로 설정합니다(기본적으로 가장 가까운 5초 벤치마크로 반올림됨).
* **`bml`** (선택 사항, 숫자): 반올림 벤치마크의 길이입니다. 기본값은 `tf` 인수에 나열된 벤치마크로 지정됩니다.

이 메서드는 `tf` 인수에 지정하는 단위를 사용하여 형식이 지정된 초 수를 반환합니다. `tf` 인수가 설정되지 않으면:

* 1분 미만의 시간은 가장 가까운 5초 벤치마크로 반올림됩니다.
* 1분과 1시간 사이의 모든 시간은 가장 가까운 1/2분 벤치마크로 반올림됩니다.
* 1시간과 1일 사이의 모든 시간은 가장 가까운 1/4시간 벤치마크로 반올림됩니다.
* 하루보다 큰 모든 시간은 가장 가까운 일 벤치마크로 반올림됩니다.

## 예

### 예 #1

다음 코드...

```js
s.eVar1 = s.formatTime(38242);
```

...은(는) s.eVar1을 &quot;10.5시간&quot;과 같게 설정합니다.

38242초로 전달된 이 인수는 10시간 37분 22초와 같습니다. 이 호출에서 tf 인수가 설정되지 않고 전달된 초 수가 1시간에서 하루 사이이므로 플러그인은 가장 가까운 1/4시간 벤치마크로 변환된 초 수를 반환합니다.

### 예 #2

다음 코드...

```js
s.eVar1 = s.formatTime(38250);
```

...은(는) s.eVar1을 &quot;10.75시간&quot;과 같게 설정합니다.
38250초로 전달된 이 인수는 10시간 37분 30초와 같습니다. 이 경우 전달된 초 수를 가장 가까운 1/4시간 벤치마크로 반올림하면 최종 값은 10.75시간으로 설정됩니다.

### 예 #3

다음 코드...

```js
s.eVar1 = s.formatTime(38242, "m");
```

...은(는) s.eVar1을 &quot;637.5분&quot;과 같게 설정합니다.

이 경우, &quot;m&quot; 인수는 플러그인이 초 수를 가장 가까운 1/2분 벤치마크로 변환하도록 합니다.

### 예 #4

다음 코드...

```js
s.eVar1 = s.formatTime(38242, "m", 20);
```

...은(는) s.eVar1을 &quot;640분&quot;과 같게 설정합니다.

tf 인수 값(&quot;m&quot;)은 플러그인이 초 수를 분으로 변환하도록 하지만 bml 인수 값(20)은 플러그인이 분 변환을 가장 가까운 20분 벤치마크로 반올림하도록 합니다.

### 예 #5

다음 코드...

```js
s.eVar1 = s.formatTime(125, "s", 2);
```

...은(는) s.eVar1을 &quot;126초&quot;와 같게 설정하며, 이것은 125초와 가장 가까운 2초 벤치마크입니다.

### 예 #6

다음 코드...

```js
s.eVar1 = s.formatTime(125, "m", 3);
```

...은(는) s.eVar1을 &quot;3분&quot;과 같게 설정하며, 이것은 125초와 가장 가까운 3분 벤치마크입니다.

### 예 #7

다음 코드...

```js
s.eVar1 = s.formatTime(145, "m", .4);
```

...은(는) s.eVar1을 &quot;2.4분&quot;과 같게 설정하며, 이것은 145초와 가장 가까운 2/5분 벤치마크(예: .4 = 2/5)입니다.

## 버전 내역

### 2.0(2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 1.1(2018년 5월 21일)

* 반올림을 더 유연하게 계산할 수 있도록 `bml` 인수를 추가했습니다.

### 1.0(2018년 4월 15일)

* 초기 릴리스.
