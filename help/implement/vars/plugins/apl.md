---
title: apl(appendToList)
description: 여러 값을 지원하는 변수에 값을 추가합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:apl(appendToList)

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `apl` 플러그인을 사용하면 목록 구분 변수(예: [`events`](../page-vars/events/events-overview.md), [`linkTrackVars`](../config-vars/linktrackvars.md)및 기타)에 새 값을 안전하게 추가할 수 [`list`](../page-vars/list.md)있습니다.

* 추가하려는 값이 변수에 없으면 코드는 문자열 끝에 값을 추가합니다.
* 추가하려는 값이 변수에 이미 있으면 이 플러그인은 값을 변경하지 않습니다. 이 기능을 사용하면 구현에서 중복 값을 방지할 수 있습니다.
* 추가할 변수가 비어 있으면 플러그인은 변수를 새 값으로 설정합니다.

구분된 값의 문자열을 포함하는 기존 변수에 새 값을 추가하려면 이 플러그인을 사용하는 것이 좋습니다. 구분된 값이 포함된 변수에 대해 문자열을 연결하려면 이 플러그인이 필요하지 않습니다.

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
   * 작업 유형:APL 초기화(목록에 추가)
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
/* Adobe Consulting Plugin: apl (appendToList) v3.2 (Requires inList v2.0 or higher) */
s.apl=function(lv,vta,d1,d2,cc){if(!lv||"string"===typeof lv){if("undefined"===typeof this.inList||"string"!==typeof vta||""===vta)return lv;d1=d1||",";d2=d2||d1;1==d2&&(d2=d1,cc||(cc=1));2==d2&&1!=cc&&(d2=d1);vta=vta.split(",");for(var g=vta.length,e=0;e<g;e++)this.inList(lv,vta[e],d1,cc)||(lv=lv?lv+d2+vta[e]:vta[e])}return lv};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `apl` 메서드는 다음 인수를 사용합니다.

* **`lv`** (필수, 문자열):구분 기호로 구분된 항목 목록을 포함하여 새 값을 추가할 변수
* **`vta`** (필수, 문자열):인수 값에 추가할 새 값의 쉼표로 구분된 `lv` 목록입니다.
* **`d1`** (선택 사항, 문자열):인수에 이미 포함되어 있는 개별 값을 구분하는 데 사용되는 구분 기호입니다. `lv`  설정되지 않은 경우 기본적으로 쉼표(`,`)로 설정됩니다.
* **`d2`** (선택 사항, 문자열):출력 구분 기호. 기본값이 설정되지 않은 경우 `d1` 동일한 값으로 설정됩니다.
* **`cc`** (선택 사항, 부울):대/소문자를 구분하는 검사가 사용되는지 여부를 나타내는 플래그. 중복 `true`검사는 대소문자를 구분합니다. 중복 검사가 `false` 설정되어 있거나 설정되지 않은 경우 대/소문자를 구분하지 않습니다. 기본값은 `false`입니다.

이 `apl` 메서드는 `lv` 인수 값과 `vta` 인수에 중복되지 않은 값을 반환합니다.

## 호출 예

### 예 #1

...

```js
s.events = "event22,event24";
```

...다음 코드가 실행됩니다.

```js
s.events = s.apl(s.events, "event23");
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22,event24,event23";
```

### 예 #2

...

```js
s.events = "event22,event23";
```

...다음 코드가 실행됩니다.

```js
s.events = s.apl(s.events, "event23");
```

...s.events의 마지막 값은 여전히 다음과 같습니다.

```js
s.events = "event22,event23";
```

이 예에서 s.events에 이미 &quot;event23&quot;이 포함되어 있으므로 apl 호출은 s.events를 변경하지 않았습니다.

### 예 #3

...

```js
s.events = ""; //blank value
```

...다음 코드가 실행됩니다.

```js
s.events = s.apl(s.events, "event23");
```

...s.events의 최종 값은...입니다.

```js
s.events = "event23";
```

### 예 #4

...

```js
s.prop4 = "hello|people";
```

...다음 코드가 실행됩니다.

```js
s.eVar5 = s.apl(s.prop4, "today", "|");
```

...s.prop4의 최종 값은 여전히..

```js
s.prop4 = "hello|people";
```

...s.eVar5의 최종 값은

```js
s.eVar5 = "hello|people|today";
```

플러그인은 값만 반환한다는 점을 염두에 두십시오.반드시 lv 인수를 통해 전달된 변수를 &quot;재설정&quot;할 필요는 없습니다.

### 예 #5

...

```js
s.prop4 = "hello|people";
```

...다음 코드가 실행됩니다.

```js
s.prop4 = s.apl(s.prop4, "today");
```

...s.prop4의 최종 값은..

```js
s.prop4 = "hello|people,today";
```

lv 인수의 값에 있는 항목과 d1/d2 인수에 있는 것 간에 구분 기호를 일관되게 유지해야 합니다.

### 예 #6

...

```js
s.events = "event22,event23";
```

...다음 코드가 실행됩니다.

```js
s.events = s.apl(s.events,"EVenT23", ",", ",", true);
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22,event23,EVentT23";
```

이 예는 실용적이지 않지만 대/소문자를 구분하는 플래그를 사용할 때 주의할 필요가 있음을 보여 줍니다.

### 예 #7

...

```js
s.events = "event22,event23";
```

...다음 코드가 실행됩니다.

```js
s.events = s.apl(s.events, "event23,event24,event25");
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22,event23,event24,event25");
```

플러그인은 s.events에 이미 있으므로 s.events에 &quot;event23&quot;을 추가하지 않습니다.  그러나 이전에 s.events에 둘 다 포함되지 않았으므로 event24 및 event25를 s.events에 추가합니다.

### 예 #8

...

```js
s.linkTrackVars = "events,eVar1";
```

...다음 코드가 실행됩니다.

```js
s.linkTrackVars = s.apl(s.linkTrackVars, "campaign", ",", ",", false);
```

...s.linkTrackVars의 최종 값은 다음과 같습니다.

```js
s.linkTrackVars = "events,eVar1,campaign";
```

마지막 세 개의 인수(예:&quot;,&quot;, &quot;,&quot;,&quot;, false)는 이 파일 호출 끝에 필요하지 않지만, 기본 인수 값과 일치하므로 설정함으로써 &quot;아무 것도 손상시키지 않습니다&quot;도 아닙니다.

### 예 #9

...

```js
s.events = "event22,event24";
```

...다음 코드가 실행됩니다.

```js
s.apl(s.events, "event23");
```

...s.events의 마지막 값은 여전히 다음과 같습니다.

```js
s.events = "event22,event24";
```

반환 값을 변수에 할당하지 않고 플러그인을 모두 실행해도 실제로 lv 인수를 통해 전달된 변수가 &quot;재설정&quot;되지는 않습니다.

### 예 #10

...

```js
s.list2 = "casesensitivevalue|casesensitiveValue"
```

...다음 코드가 실행됩니다.

```js
s.list2 = s.apl(s.list2, "CasESensiTiveValuE", "|", "-", true);
```

...s.list2의 최종 값은 다음과 같습니다.

```js
s.list2 = "casesensitivevalue-casesensitiveValue-CasESensiTiveValuE"
```

두 구분 기호 인수가 다르므로 전달된 값은 첫 번째 구분 기호 인수(&quot;|&quot;)로 구분되고 두 번째 구분 기호 인수(&quot;-&quot;)로 결합됩니다.

## 버전 내역

### 3.2(2019년 9월 25일)

* 이전 버전의 플러그인을 사용한 `apl` 호출 호환성 문제가 해결되었습니다.
* 크기를 줄이기 위해 콘솔 경고를 제거했습니다.
* Admin Console 도움말에 `inList 2.1`

### 3.1(2018년 4월 22일)

* `d2` 인수가 설정되지 않은 경우 기본적으로 `d1` 인수의 값이 설정됩니다.

### 3.0(2018년 4월 16일)

* 전체 플러그인 분석/다시 작성
* 고급 오류 검사 추가
* 이제 `vta` 인수가 여러 값을 한 번에 수락합니다.
* 반환 값의 형식을 지정하는 `d2` 인수를 추가했습니다.
* 인수를 `cc` 부울로 변경했습니다.

### 2.5(2016년 2월 18일)

* 이제 비교 처리를 위해 `inList` 메서드를 사용합니다

### 2.0(2016년 1월 26일)

* `d` (구분 기호) 인수는 이제 선택 사항입니다(기본값: 쉼표).
* `u` (대/소문자 구분 플래그) 인수는 이제 선택 사항입니다(대소문자를 구분하지 않도록 기본값).
* (대/소문자 구분 플래그) `u` 인수에 관계없이, 목록에 값이 이미 있는 경우 플러그인은 목록에 값을 더 이상 추가하지 않습니다