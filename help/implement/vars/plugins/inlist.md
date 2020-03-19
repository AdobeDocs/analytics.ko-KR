---
title: inList
description: 값이 다른 문자로 구분된 값에 포함되어 있는지 확인합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:inList

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `inList` 플러그인을 사용하면 구분된 문자열 또는 JavaScript 배열 개체 내에 값이 이미 있는지 확인할 수 있습니다. 여러 다른 플러그인은 `inList` 플러그인에 따라 다릅니다. 이 플러그인은 부분 문자열과 일치하지 않는 JavaScript 메서드보다 `indexOf()` 차별화된 이점을 제공합니다. 예를 들어 이 플러그인을 사용하여 체크 인한 경우 `"event2"`이 플러그인은 포함된 `"event25"`문자열과 일치하지 않습니다. 구분 기호로 구분된 문자열 또는 배열의 값을 확인하지 않아도 되거나 자신의 `indexOf()` 논리를 사용하려는 경우에는 이 플러그인이 필요하지 않습니다.

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
   * 작업 유형:InList 초기화
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
/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `inList` 메서드는 다음 인수를 사용합니다.

* **`lv`** (필수, 문자열 또는 배열):검색할 값의 구분된 목록 또는 JavaScript 배열 개체
* **`vtc`** (필수, 문자열):검색할 값
* **`d`** (선택 사항, 문자열):인수에서 개별 값을 구분하는 데 사용되는 구분 `lv` 기호입니다. 설정되지 않은 경우 기본적으로 쉼표(`,`)로 설정됩니다.
* **`cc`** (선택 사항, 부울):로 `true`설정하면 대/소문자를 구분합니다. 로 `false` 설정하거나 생략하면 대/소문자를 구분하지 않는 검사가 수행됩니다. 기본값은 `false`입니다.

이 메서드를 호출하면 일치 항목을 찾은 `true` 경우 일치하는 항목을 찾지 못한 `false` 경우 반환됩니다.

## 호출 예

### 예 #1

...

```js
s.events="event22,event24";
```

...다음 코드가 실행됩니다.

```js
if(s.inList(s.events,"event22"))
```

...조건문이 true입니다.

### 예 #2

...

```js
s.events="event22,event24";
```

...다음 코드가 실행됩니다.

```js
if(s.inList(s.events,"event2"))
```

...inList 호출이 event2와 s.events의 구분된 값 중 하나를 정확히 일치시키지 않았으므로 조건if 문은 false입니다.

### 예 #3

...

```js
s.events="event22,event24";
```

...다음 코드가 실행됩니다.

```js
if(!s.inList(s.events,"event23"))
```

...inList 호출이 event23과 s.events의 구분 기호로 구분된 값 중 하나를 정확히 일치시키지 않았기 때문에 조건if 문이 true가 됩니다(inList 변수 호출 시작 시 &quot;NOT&quot; 연산자 주의).

### 예 #4

...

```js
s.events = "event22,event23";
```

...다음 코드가 실행됩니다.

```js
if(s.inList(s.events,"EVenT23","",1))
```

...조건문은 false입니다.  이 예는 실용적이지 않지만 대/소문자를 구분하는 플래그를 사용할 때 주의할 필요가 있음을 보여 줍니다.

### 예 #5

...

```js
s.linkTrackVars = "events,eVar1";
```

...다음 코드가 실행됩니다.

```js
if(s.inList(s.linkTrackVars,"eVar1","|"))
```

...조건문은 false입니다.  호출로 전달된 d 인수의 값(예:&quot;|&quot;)에서는 s.linkTrackVars의 개별 값이 파이프 문자로 구분된다고 가정하지만 실제로는 값이 쉼표로 구분됩니다.  이 경우 플러그인은 s.linkTrackVars의 전체 값(예:&quot;events,eVar1&quot;) 및 찾을 값(예:&quot;eVar1&quot;).

## 버전 내역

### v2.1(2019년 9월 26일)

* 인수가 부울이 되지 않도록 `cc` 옵션을 추가했습니다. 예를 들어 `1` 는 유효한 케이스 확인 값입니다.

### v2.0(2018년 4월 17일)

* 포인트 릴리스(다시 컴파일되고 더 작은 코드 크기).

### v1.01(2017년 9월 27일)

* 크기를 줄이기 위해 최적화된 코드

### v1.0(2009년)

* 초기 릴리스.


