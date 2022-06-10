---
title: apl (appendToList)
description: 여러 값을 지원하는 변수에 값을 추가합니다.
feature: Variables
exl-id: 08ca43f4-f2cc-43fb-a8eb-7c9dd237dfba
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 94%

---

# Adobe 플러그인: apl (appendToList)

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`apl` 플러그인을 사용하면 [`events`](../page-vars/events/events-overview.md), [`linkTrackVars`](../config-vars/linktrackvars.md), [`list`](../page-vars/list.md) 및 기타 변수와 같은 목록 구분 변수에 새 값을 안전하게 추가할 수 있습니다.

* 추가하려는 값이 변수에 없으면 코드는 값을 문자열 끝에 추가합니다.
* 추가하려는 값이 변수에 이미 있으면 이 플러그인은 값을 변경하지 않습니다. 이 기능을 사용하면 구현에서 중복 값을 방지할 수 있습니다.
* 추가하려는 변수가 비어 있으면 플러그인은 이 변수를 새 값으로 설정합니다.

구분된 값으로 이루어진 문자열을 포함하는 기존 변수에 새 값을 추가하려면 이 플러그인을 사용하는 것이 좋습니다. 구분된 값이 포함된 변수용 문자열을 연결하려는 경우에는 이 플러그인이 필요하지 않습니다.

## Web SDK 또는 Adobe Analytics 확장을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해 주는 확장 기능을 제공합니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그] 버튼을 클릭합니다.
1. [!UICONTROL 일반적인 Analytics 플러그인] 확장 기능을 설치 및 게시합니다.
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨 (페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: APL 초기화 (목록에 추가)
1. 변경 사항을 저장하고 규칙에 퍼블리싱합니다.

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
/* Adobe Consulting Plugin: apl (appendToList) v4.0 */
function apl(lv,va,d1,d2,cc){var b=lv,d=va,e=d1,c=d2,g=cc;if("-v"===b)return{plugin:"apl",version:"4.0"};var h=function(){if("undefined"!==typeof window.s_c_il)for(var k=0,b;k<window.s_c_il.length;k++)if(b=window.s_c_il[k],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof h&&(h.contextData.apl="4.0");window.inList=window.inList||function(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1};if(!b||"string"===typeof b){if("string"!==typeof d||""===d)return b;e=e||",";c=c||e;1==c&&(c=e,g||(g=1));2==c&&1!=g&&(c=e);d=d.split(",");h=d.length;for(var f=0;f<h;f++)window.inList(b,d[f],e,g)||(b=b?b+c+d[f]:d[f])}return b};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`apl` 함수에서는 다음 인수를 사용합니다.

* **`lv`** (필수, 문자열): 구분 기호로 구분된 항목 목록을 포함하여 새 값을 추가할 변수입니다.
* **`vta`** (필수, 문자열): `lv` 인수 값에 추가할 새 값들을 쉼표로 구분한 목록입니다.
* **`d1`** (선택 사항, 문자열): `lv` 인수에 이미 포함되어 있는 개별 값을 구분하는 데 사용되는 구분 기호입니다.  설정하지 않으면 기본값이 쉼표 (`,`)로 설정됩니다.
* **`d2`** (선택 사항, 문자열): 출력 구분 기호입니다. 설정하지 않으면 기본값이 `d1`과 동일한 값으로 설정됩니다.
* **`cc`** (선택 사항, 부울): 대/소문자 검사를 사용하는지 여부를 나타내는 플래그입니다. `true`면 중복 검사는 대/소문자를 구분합니다. `false`거나 설정되지 않으면 중복 검사는 대/소문자를 구분하지 않습니다. 기본값은 `false`입니다.

`apl` 함수는 `lv` 인수의 값과 `vta` 인수에 있는 중복되지 않은 값을 반환합니다.

## 예

```js
// Set the events variable to "event22,event24,event23".
s.events = "event22,event24";
s.events = apl(s.events,"event23");

// The events variable remains unchanged because the apl function does not add duplicate values
s.events = "event22,event23";
s.events = apl(s.events,"event23");

// Set the events variable to "event23" if the events variable is blank
s.events = "";
s.events = apl(s.events,"event23");

// Append a value to eVar5. The value of prop4 remains unchanged.
// The value of eVar5 is "hello|people|today".
s.prop4 = "hello|people";
s.eVar5 = apl(s.prop4, "today", "|");

// Sets prop4 to "hello|people,today". Be mindful of correct delimiters!
s.prop4 = "hello|people";
s.prop4 = apl(s.prop4, "today");

// Sets the events variable to "event22,event23,EVentT23". Be mindful of capitalization when using the cc argument!
s.events = "event22,event23";
s.events = apl(s.events,"EVenT23", ",", ",", true);

// Sets the events variable to "event22,event23,event24,event25".
s.events = "event22,event23";
s.events = apl(s.events, "event23,event24,event25");

// Sets linkTrackVars to "events,eVar1,campaign".
// The last three arguments at the end of this apl call are not necessary because they match the default argument values.
s.linkTrackVars = "events,eVar1";
s.linkTrackVars = apl(s.linkTrackVars, "campaign", ",", ",", false);

// This apl call does not do anything because the code does not assign the returned value to a variable.
s.events = "event22,event24";
apl(s.events, "event23");

// Sets the list2 variable to "apple-APPLE-Apple".
// Since the two delimiter arguments are different, the value passed in is delimited by "|", then joined together by "-".
s.list2 = "apple|APPLE";
s.list2 = apl(s.list2, "Apple", "|", "-", true);

// Sets the list3 variable to "value1,value1,value1" (unchanged).
// Only new values are deduplicated. Existing duplicate values remain.
s.list3 = "value1,value1,value1";
s.list3 = apl(s.list3,"value1");
```

## 버전 내역

### 4.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 3.2 (2019년 9월 25일)

* 이 플러그인의 이전 버전을 사용한 `apl` 호출의 호환성 문제를 해결했습니다.
* 콘솔 경고를 제거하여 크기를 줄였습니다.
* `inList 2.1`을 추가했습니다.

### 3.1 (2018년 4월 22일)

* `d2` 인수는 설정되지 않은 경우 기본값이 `d1` 인수의 값으로 설정됩니다.

### 3.0 (2018년 4월 16일)

* 전체 플러그인 분석/다시 작성
* 고급 오류 검사를 추가했습니다.
* `vta` 인수가 이제 여러 값을 한 번에 허용합니다.
* 반환 값의 형식을 지정하는 `d2` 인수를 추가했습니다.
* `cc` 인수를 부울로 변경했습니다.

### 2.5 (2016년 2월 18일)

* 이제 비교 처리를 위해 `inList` 함수를 사용합니다.

### 2.0 (2016년 1월 26일)

* `d` (구분 기호) 인수는 이제 선택 사항입니다(기본값: 쉼표).
* `u` (대/소문자 구분 플래그) 인수는 이제 선택 사항입니다(기본값: 대/소문자를 구분하지 않음).
* `u` (대/소문자 구분 플래그) 인수에 관계없이, 목록에 값이 이미 있으면 플러그인이 값을 목록에 더 이상 추가하지 않습니다.
