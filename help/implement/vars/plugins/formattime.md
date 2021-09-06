---
title: formatTime
description: 초 수를 그에 해당하는 분, 시간 등으로 변환합니다.
exl-id: 4b98e7fe-f05b-4346-b284-697268adc1a2
source-git-commit: ab078c5da7e0e38ab9f0f941b407cad0b42dd4d1
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 96%

---

# Adobe 플러그인: formatTime

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`formatTime` 플러그인을 사용하면 초 수를 전체 형식의 원하는 벤치마크 값으로 반올림하여 표시할 수 있습니다. 초 단위의 시간 값을 캡처하여 전체 형식 (예: 분, 일 또는 주)으로 변환하려는 경우 이 플러그인을 사용하는 것이 좋습니다. 초 기반 값을 시간이 반올림된 형식으로 변환하는 것을 원치 않으면 이 플러그인은 불필요합니다.

## Adobe Experience Platform의 태그를 사용하여 플러그인 설치

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
   * 작업 유형: formatTime 초기화
1. 변경 사항을 저장하고 규칙에 퍼블리싱합니다.

## 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

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
/* Adobe Consulting Plugin: formatTime v2.0 */
function formatTime(ns,tf,bml){var f=ns,d=tf,e=bml;function h(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(arguments&&"-v"===arguments[0])return{plugin:"formatTime",version:"2.0"};var b=function(){if("undefined"!==typeof window.s_c_il)for(var b=0,c;b<window.s_c_il.length;b++)if(c=window.s_c_il[b],c._c&&"s_c"===c._c)return c}();"undefined"!==typeof b&&(b.contextData.formatTime="2.0");if(!("undefined"===typeof f||isNaN(f)||0>Number(f))){b="";if("string"===typeof d&&"d"===d||("string"!==typeof d||!h("h,m,s",d))&&86400<=f){var c=86400;var g="days";b=isNaN(e)?1:c/(e*c)}else"string"===typeof d&&"h"===d||("string"!==typeof d||!h("m,s",d))&&3600<=f?(c=3600,g="hours",b=isNaN(e)?4:c/(e*c)):"string"===typeof d&&"m"===d||("string"!==typeof d||!h("s",d))&&60<=f?(c=60,g="minutes",b=isNaN(e)?2:c/(e*c)):(c=1,g="seconds",b=isNaN(e)?.2:c/e);b=Math.round(f*b/c)/b+" "+g;0===b.indexOf("1 ")&&(b=b.substring(0,b.length-1));return b}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`formatTime` 함수는 다음 인수를 사용합니다.

* **`ns`** (필수, 정수): 변환하거나 서식을 지정할 초 수
* **`tf`** (선택 사항, 문자열): 초를 반환하는 형식 유형. 기본값은 초입니다.
   * 일 단위 시간을 원하는 경우 `"d"`로 설정합니다(기본적으로 가장 가까운 1/4일 벤치마크로 반올림됨).
   * 시간 단위 시간을 원하는 경우 `"h"`로 설정합니다(기본적으로 가장 가까운 1/4시간 벤치마크로 반올림됨).
   * 분 단위 시간을 원하는 경우 `"m"`으로 설정합니다(기본적으로 가장 가까운 1/2분 벤치마크로 반올림됨).
   * 초 단위 시간을 원하는 경우 `"s"`로 설정합니다(기본적으로 가장 가까운 5초 벤치마크로 반올림됨).
* **`bml`** (선택 사항, 숫자): 반올림 벤치마크의 길이입니다. 기본값은 `tf` 인수에 나열된 벤치마크로 지정됩니다.

이 함수는 `tf` 인수에 지정하는 단위를 사용하여 형식이 지정된 초 수를 반환합니다. `tf` 인수가 설정되지 않으면:

* 1분 미만의 시간은 가장 가까운 5초 벤치마크로 반올림됩니다.
* 1분과 1시간 사이의 모든 시간은 가장 가까운 1/2분 벤치마크로 반올림됩니다.
* 1시간과 1일 사이의 모든 시간은 가장 가까운 1/4시간 벤치마크로 반올림됩니다.
* 하루보다 큰 모든 시간은 가장 가까운 일 벤치마크로 반올림됩니다.

## 예

```js
// Sets eVar1 to "10.5 hours".
// 38242 seconds equals 10 hours, 37 minutes, and 22 seconds. Since the tf argument is not set, the value returned is the number of seconds converted to the nearest quarter-hour benchmark.
s.eVar1 = formatTime(38242);

// Sets eVar4 to "10.75 hours".
// 38250 seconds equals 10 hours, 37 minutes, and 30 seconds. This value rounds up to the nearest quarter hour.
s.eVar4 = formatTime(38250);

// Sets eVar9 to "637.5 minutes".
s.eVar9 = formatTime(38242, "m");

// Sets eVar14 to "640 minutes".
// The tf argument forces the returned value to minutes, while the bml argument forces the value to the nearest 20-minute increment.
s.eVar14 = formatTime(38242, "m", 20);

// Sets eVar2 to "126 seconds", the closest 2-second benchmark to 125 seconds.
s.eVar2 = formatTime(125, "s", 2);

// Sets eVar7 to "3 minutes", the closest 3-minute benchmark to 125 seconds.
s.eVar7 = formatTime(125, "m", 3);

// Sets eVar55 to "2.4 minutes, the closest 2/5-minute benchmark to 145 seconds.
s.eVar55 = formatTime(145, "m", .4);
```

## 버전 내역

### 2.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 1.1 (2018년 5월 21일)

* 반올림을 더 유연하게 계산할 수 있도록 `bml` 인수를 추가했습니다.

### 1.0 (2018년 4월 15일)

* 초기 릴리스.
