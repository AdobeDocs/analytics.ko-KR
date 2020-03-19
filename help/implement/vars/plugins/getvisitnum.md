---
title: getVisitNum
description: 방문자의 현재 방문 번호를 추적합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:getVisitNum

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

플러그인은 원하는 일 수 내에 사이트를 방문하는 모든 방문자의 방문 번호를 반환합니다. `getVisitNum` 분석 작업 공간에서는 비슷한 기능을 제공하는 &#39;방문 번호&#39; 차원을 제공합니다. 방문 번호가 증가되는 방식을 더 잘 제어하려면 이 플러그인을 사용하는 것이 좋습니다. 분석 작업 공간에 내장된 &#39;방문 번호&#39; 차원으로 보고 요구 사항에 적합한 경우 이 플러그인은 불필요합니다.

## Adobe Experience Platform Launch 익스텐션을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있는 확장 기능을 제공합니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. 원하는 속성을 클릭합니다.
1. 탭으로 이동한 다음 [!UICONTROL Extensions] [!UICONTROL Catalog] 단추를 클릭합니다.
1. 확장 [!UICONTROL Common Analytics Plugins] 프로그램 설치 및 게시
1. 아직 설정하지 않은 경우, &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 다음 구성으로 만듭니다.
   * 조건:없음
   * 이벤트:코어 - 라이브러리가 로드됨(페이지 상단)
1. 다음 구성으로 위 규칙에 작업을 추가합니다.
   * 확장:공통 Analytics 플러그인
   * 작업 유형:getVisitNum 초기화
1. 변경 내용을 저장하고 규칙에 게시합니다.

## Launch 사용자 정의 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려면 사용자 정의 코드 편집기를 사용할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. 원하는 속성을 클릭합니다.
1. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 확장 프로그램 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
1. 단추를 표시하는 [!UICONTROL Configure tracking using custom code] 아코디언을 [!UICONTROL Open Editor] 확장합니다.
1. 사용자 정의 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여 넣습니다.
1. Analytics 확장 프로그램에 변경 사항을 저장하고 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣습니다(사용 [`s_gi`](../functions/s-gi.md)). 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getVisitNum v4.11 (Requires endOfDatePeriod plug-in) */
s.getVisitNum=function(rp,erp){var s=this,c=function(rp){return isNaN(rp)?!1:(parseFloat(rp)|0)===parseFloat(rp)};rp=rp?rp:365;erp= "undefined"!==typeof erp?!!erp:c(rp)?!0:!1;var e=(new Date).getTime(),b=endOfDatePeriod(rp);if(s.c_r("s_vnc"+rp))var g=s.c_r("s_vnc"+rp).split("&vn="),d=g[1];if(s.c_r("s_ivc"))return d?(b.setTime(e+18E5),s.c_w("s_ivc",!0,b),d):"unknown visit number";if("undefined"!==typeof d)return d++,c=erp&&c(rp)?e+864E5*rp:g[0],b.setTime(c),s.c_w("s_vnc"+rp,c+"&vn="+d,b),b.setTime(e+ 18E5),s.c_w("s_ivc",!0,b),d;c=c(rp)?e+864E5*rp:endOfDatePeriod(rp).getTime();s.c_w("s_vnc"+rp,c+"&vn=1",b);b.setTime(e+18E5); s.c_w("s_ivc",!0,b);return"1"};

/* Adobe Consulting Plugin: endOfDatePeriod v1.1 */
var endOfDatePeriod=function(dp){var a=new Date,b=isNaN(dp)?0:Math.floor(dp);a.setHours(23);a.setMinutes(59);a.setSeconds(59); "w"===dp&&(b=6-a.getDay());if("m"===dp){b=a.getMonth()+1;var d=a.getFullYear();b=(new Date(d?d:1970,b?b:1,0)).getDate()-a.getDate()}a.setDate(a.getDate()+b);"y"===dp&&(a.setMonth(11),a.setDate(31));return a};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `getVisitNum` 메서드는 다음 인수를 사용합니다.

* **`rp`** (선택 사항, 정수 또는 문자열):방문 번호 카운터가 재설정되기 전 일 수입니다.  설정되지 않은 경우 기본값이 로 `365` 설정됩니다.
   * 이 인수가 `"w"`끝나면 카운터가 주 말에 재설정됩니다(이번 주 토요일 오후 11시 59분).
   * 이 인수가 `"m"`이면 카운터는 월말(이번 달의 마지막 날)에 재설정됩니다.
   * 이 인수가 `"y"`이면 카운터는 연도 종료(12월 31일)에 재설정됩니다.
* **`erp`** (선택 사항, 부울):인수가 숫자인 `rp` 경우 이 인수는 방문 번호 만료를 연장할지 여부를 결정합니다. 로 설정된 `true`경우 이후 사이트 히트는 방문 번호 카운터를 재설정합니다. 로 설정된 `false`경우, 방문 번호 카운터가 재설정되면 사이트의 후속 히트가 확장되지 않습니다. 기본값은 `true`입니다. 인수가 문자열이면 이 인수가 유효하지 않습니다. `rp`

방문자가 30분 동안 활동이 없는 후 사이트를 다시 방문할 때마다 방문 번호가 증가합니다. 이 메서드를 호출하면 방문자의 현재 방문 번호를 나타내는 정수가 반환됩니다.

이 플러그인은 `"s_vnc[LENGTH]"` 인수로 전달되는 `[LENGTH]` 값이 `rp` 여기서 호출되는 퍼스트 파티 쿠키를 설정합니다. 예: `"s_vncw"`, `"s_vncm"`또는 `"s_vnc365"`. 쿠키의 값은 주 종료, 월말 또는 365일 비활동 후 등 방문 카운터가 재설정되는 시기를 나타내는 Unix 타임스탬프의 조합입니다. 여기에는 현재 방문 번호도 포함되어 있습니다. 이 플러그인은 활동이 없는 30분 후에 만료되도록 `"s_ivc"` 설정되고 `true` 만료되는 다른 쿠키를 설정합니다.

## 호출 예

### 예 #1

지난 365일 이내에 사이트를 방문하지 않은 방문자의 경우 다음 코드는 s.prop1의 값과 동일하게 설정됩니다.

```js
s.prop1=s.getVisitNum();
```

### 예 #2

첫 번째 방문 후 364일 이내에 사이트로 돌아온 방문자의 경우, 다음 코드는 s.prop1을 2로 설정합니다.

```js
s.prop1=s.getVisitNum(365);
```

이 방문자가 두 번째 방문 후 364일 이내에 사이트를 다시 방문하는 경우 다음 코드는 s.prop1을 3으로 설정합니다.

```js
s.prop1=s.getVisitNum(365);
```

### 예 #3

첫 번째 방문 후 179일 이내에 사이트를 다시 방문하는 방문자의 경우 다음 코드는 s.prop1을 2로 설정합니다.

```js
s.prop1=s.getVisitNum(180,false);
```

그러나 이 방문자가 두 번째 방문 후 1일 이상 사이트를 다시 방문하는 경우 다음 코드는 s.prop1을 1로 설정합니다.

```js
s.prop1=s.getVisitNum(180,false);
```

호출의 두 번째 인수가 false와 같은 경우 방문자가 사이트를 처음 방문한 후 방문 번호를 &quot;재설정&quot;할 시기를 결정하는 루틴은 방문자의 &quot;x&quot; 일 수(이 예: 365일)를 지정합니다.

두 번째 인수가 true와 동일하거나 전혀 설정되지 않은 경우 플러그인은 방문자 비활동 상태가 365일인 &quot;x&quot; 일 수 이후에만 방문 번호를 1로 재설정합니다.

### 예 #4

현재 주 동안(일요일에 시작) 처음으로 사이트를 방문하는 모든 방문자의 경우 다음 코드는 s.prop1을 1로 설정합니다.

```js
s.prop1=s.getVisitNum("w");
```

### 예 #5

현재 월 중 처음으로 사이트를 방문하는 모든 방문자(매월 첫째 날)에 대해 다음 코드는 s.prop1을 1로 설정합니다.

```js
s.prop1=s.getVisitNum("m");
```

getVisitNum 플러그인은 소매 기반 달력(예: 4-5-4, 4-4-5 등)을 고려하지 않습니다.

### 예 #6

1월 1일부터 현재 연도 동안 처음으로 사이트를 방문하는 모든 방문자의 경우 다음 코드는 s.prop1을 1로 설정합니다.

```js
s.prop1=s.getVisitNum("y");
```

### 예 #7

다른 Analytics 변수 내에서 해당 주의 방문자 방문 번호, 해당 월의 방문자 방문 번호 및 해당 연도의 방문자 방문 번호를 추적하려면 다음과 유사한 코드를 사용해야 합니다.

```js
s.prop1=s.getVisitNum("w");
s.prop2=s.getVisitNum("m");
s.prop3=s.getVisitNum("y");
```

이 경우 플러그인은 기간당 개별 방문 횟수를 추적할 수 있도록 세 개의 서로 다른 쿠키(각 기간에 대해 하나씩)를 만듭니다.

## 버전 내역

### 4.11(2019년 9월 30일)

* 인수가 명시적으로 설정된 문제를 `erp` `false`수정했습니다.

### 4.1(2018년 5월 21일)

* v1.1로 `endOfDatePeriod` 플러그인을 업데이트했습니다.

### 4.0(2018년 4월 17일)

* 포인트 릴리스(다시 컴파일되고 더 작은 코드 크기).
* 플러그인으로 제거된 쿠키 인수는 이제 `rp` 인수에 따라 쿠키를 동적으로 생성합니다.)

### 3.0(2016년 6월 5일)

* 전체 검토
* 다양한 버전의 플러그인에서 사용할 수 있는 모든 이전 솔루션을 `getVisitNum` 결합했습니다.
