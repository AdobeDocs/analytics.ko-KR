---
title: getTimeParting
description: 특정 동작이 발생하는 시간을 측정합니다.
feature: Variables
exl-id: 3fab36c8-a006-405a-9ef1-2547c2b36b0d
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: ht
source-wordcount: '718'
ht-degree: 100%

---

# Adobe 플러그인: getTimeParting

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getTimeParting` 플러그인을 사용하면 사이트에서 측정 가능한 활동이 발생하는 시간을 세부적으로 캡처할 수 있습니다. 이 플러그인은 주어진 날짜 범위에서 반복 가능한 시간 분할로 지표를 분류하려 할 때 유용합니다. 예를 들어 모든 일요일과 모든 목요일 등 두 가지 서로 다른 요일 간의 전환율을 비교할 수 있습니다. 또한 아침이나 저녁과 같은 하루 동안의 시간 부분을 비교할 수도 있습니다.

Analysis Workspace는 형식이 이 플러그인과 약간 다르게 지정된 유사한 기본 차원을 제공합니다. 자세한 내용은 분석 사용 안내서의 [시간 분할 차원](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md)을 참조하십시오. 일부 조직에서는 Analysis Workspace의 기본 제공 차원으로 충분하다는 것을 판단합니다.

>[!IMPORTANT]
>
>이 플러그인의 버전 4.0 이상은 이전 버전과 상당히 다릅니다. 따라서 이 플러그인을 &quot;처음부터&quot;로 새로 구현하는 것이 좋습니다. 버전 4.0 이전의 플러그인을 참조하는 코드는 이 플러그인의 현재 버전과 호환되지 않습니다.

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
   * 작업 유형: getTimeParting 초기화
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
/* Adobe Consulting Plugin: getTimeParting v6.3 (No Prerequisites Needed) */
function getTimeParting(t){var c=t;if("-v"===t)return{plugin:"getTimeParting",version:"6.3"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c){a=b;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.getTimeParting="6.3");c=document.documentMode?void 0:c||"Etc/GMT";a=(new Date).toLocaleDateString("en-US",{timeZone:c,minute:"numeric",hour:"numeric",weekday:"long",day:"numeric",year:"numeric",month:"long"});a=/([a-zA-Z]+).*?([a-zA-Z]+).*?([0-9]+).*?([0-9]+)(.*?)([0-9])(.*)/.exec(a);return"year="+a[4]+" | month="+a[2]+" | date="+a[3]+" | day="+a[1]+" | time="+(a[6]+a[7])};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getTimeParting` 함수에서는 다음 인수를 사용합니다.

**`t`** (선택 사항이지만 권장됨, 문자열): 방문자의 현지 시간을 변환하여 구할 시간대의 이름입니다.  기본값은 UTC/GMT 시간으로 설정됩니다. 유효한 값에 대한 전체 목록이 필요하면 위키백과의 [TZ 데이터베이스 시간대 목록](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones)을 참조하십시오.

일반적인 유효 값은 다음과 같습니다.

* `"America/New_York"` - 동부 표준시
* `"America/Chicago"` - 중부 표준시
* `"America/Denver"` - 산지 표준시
* `"America/Los_Angeles"` - 태평양 표준시

이 함수를 호출하면 파이프 (`|`)로 구분된 다음 내용을 포함하는 문자열이 반환됩니다.

* 올해
* 이번 달
* 현재 날짜 중 일
* 요일
* 현재 시간 (오전/오후)

## 예

```js
// Use the following code if the visitor resides in Paris, France
s.eVar8 = getTimeParting("Europe/Paris");

// Use the following code if the visitor resides in San Jose, California
s.eVar17 = getTimeParting("America/Los_Angeles");

// Use the following code if the visitor resides in Ghana.
// Note that Ghana is in GMT time, the default time zone that the plug-in uses with no argument
s.eVar22 = getTimeParting();

// Internet Explorer only returns the visitor's local time. Use this conditional statement to accommodate IE visitors
if(!document.documentMode) s.eVar39 = getTimeParting("America/New_York");
else s.eVarX = "Internet Explorer Visitors";

// Given a visitor from Denver Colorado visits a site on August 31, 2020 at 9:15 AM
// Returns the string value "year=2020 | month=August | date=31 | day=Friday | time=6:15 PM"
s.eVar10 = getTimeParting("Europe/Athens");

// Returns the string value "year=2020 | month=August | date=31 | day=Friday | time=6:15 AM"
s.eVar11 = getTimeParting("America/Nome");

// Returns the string value "year=2020 | month=August | date=31 | day=Friday | time=8:45 PM"
s.eVar12 = getTimeParting("Asia/Calcutta");

// Returns the string value "year=2020 | month=September | date=1 | day=Saturday | time=1:15 AM"
s.eVar13 = getTimeParting("Australia/Sydney");
```

## 버전 내역

### 6.3 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 6.2 (2019년 11월 5일)

* 작은 버그 수정
* 전체 코드 크기를 줄였습니다.

### 6.1 (2018년 11월 26일)

* Internet Explorer 브라우저에 대한 수정. 시간을 반환할 수 있지만 방문자의 현지 시간만 사용됩니다.

### 6.0 (2018년 8월 14일)

* 국제 표준에 맞게 전체 재작성. 이제 일광 절약 시간과 모든 시간대를 적절하게 변환합니다.

### 5.0 (2018년 4월 17일)

* 포인트 릴리스 (다시 컴파일됨, 더 작은 코드 크기)
* 일광 절약 시간제 시작/종료 날짜가 이제 자동으로 검색되므로 `tpDST` 매개 변수를 사용할 필요가 없어졌습니다.

>[!CAUTION]
>
>이 플러그인의 이전 버전은 미래의 모든 연도를 수용하지 못했습니다. 이 플러그인의 이전 버전을 사용하는 경우 JavaScript 오류 및 데이터 손실을 방지하려면 최신 버전으로 업그레이드하는 것이 좋습니다. 이 플러그인을 업그레이드할 수 없는 경우 플러그인 코드의 `s._tpdst` 변수에 미래의 해당 연도가 포함되어 있는지 확인하십시오.

### 4.0 (2016년 8월 22일)

* 완전히 새로운 솔루션을 제공하며 이제 연도, 월 및 날짜 정보를 포함합니다.
