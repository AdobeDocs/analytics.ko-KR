---
title: getVisitNum
description: 방문자의 현재 방문 횟수를 추적합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe 플러그인: getVisitNum

>[!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getVisitNum` 플러그인은 원하는 기간(일 수) 내에 사이트를 방문하는 모든 방문자에 대해 방문 횟수를 반환합니다. Analysis Workspace에서는 비슷한 기능을 제공하는 &#39;방문 횟수&#39; 차원을 제공합니다. 방문 횟수가 증가되는 방식을 더 자유롭게 제어하려면 이 플러그인을 사용하는 것이 좋습니다. Analysis Workspace의 내장 &#39;방문 횟수&#39; 차원이 보고 요구 사항에 적합한 경우 이 플러그인은 필요하지 않습니다.

## Adobe Experience Platform Launch 확장을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해주는 확장을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. 확장 [!UICONTROL Common Analytics Plugins] 프로그램 설치 및 게시
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
1. Go to the [!UICONTROL Extensions] tab, then click the [!UICONTROL Configure] button under the Adobe Analytics extension.
1. 단추를 표시하는 [!UICONTROL Configure tracking using custom code] 아코디언을 [!UICONTROL Open Editor] 확장합니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여 넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여 넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getVisitNum v4.11 (Requires endOfDatePeriod plug-in) */
s.getVisitNum=function(rp,erp){var s=this,c=function(rp){return isNaN(rp)?!1:(parseFloat(rp)|0)===parseFloat(rp)};rp=rp?rp:365;erp= "undefined"!==typeof erp?!!erp:c(rp)?!0:!1;var e=(new Date).getTime(),b=endOfDatePeriod(rp);if(s.c_r("s_vnc"+rp))var g=s.c_r("s_vnc"+rp).split("&vn="),d=g[1];if(s.c_r("s_ivc"))return d?(b.setTime(e+18E5),s.c_w("s_ivc",!0,b),d):"unknown visit number";if("undefined"!==typeof d)return d++,c=erp&&c(rp)?e+864E5*rp:g[0],b.setTime(c),s.c_w("s_vnc"+rp,c+"&vn="+d,b),b.setTime(e+ 18E5),s.c_w("s_ivc",!0,b),d;c=c(rp)?e+864E5*rp:endOfDatePeriod(rp).getTime();s.c_w("s_vnc"+rp,c+"&vn=1",b);b.setTime(e+18E5); s.c_w("s_ivc",!0,b);return"1"};

/* Adobe Consulting Plugin: endOfDatePeriod v1.1 */
var endOfDatePeriod=function(dp){var a=new Date,b=isNaN(dp)?0:Math.floor(dp);a.setHours(23);a.setMinutes(59);a.setSeconds(59); "w"===dp&&(b=6-a.getDay());if("m"===dp){b=a.getMonth()+1;var d=a.getFullYear();b=(new Date(d?d:1970,b?b:1,0)).getDate()-a.getDate()}a.setDate(a.getDate()+b);"y"===dp&&(a.setMonth(11),a.setDate(31));return a};
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
