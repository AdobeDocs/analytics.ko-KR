---
title: rfl
description: 문자로 구분된 문자열에서 특정 값을 제거합니다.
feature: Variables
exl-id: d66b757e-b39f-4b6e-9999-6fbde87505af
source-git-commit: 7c7a7d8add9edb1538df12b440bc0a15f09efe5e
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 98%

---

# Adobe 플러그인: rfl (목록에서 제거)

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`rfl` 플러그인을 사용하면 [`events`](../page-vars/events/events-overview.md), [`products`](../page-vars/products.md), [`list`](../page-vars/list.md) 등 구분된 문자열에서 값을 &quot;안전하게&quot; 제거할 수 있습니다. 이 플러그인은 구분 기호에 대한 걱정 없이 구분된 문자열에서 특정 값을 제거하려는 경우 유용합니다. 몇 가지 다른 플러그인은 이 코드를 사용하여 올바로 실행됩니다. 한 번에 두 개 이상의 Analytics 변수에서 특정 함수를 실행할 필요가 없거나 종속 플러그인을 사용하지 않는 경우에는 이 플러그인이 필요하지 않습니다.

플러그인은 다음 논리를 사용합니다.

* 제거할 값이 있으면 플러그인이 제거할 값을 제외한 모든 항목을 변수에 유지합니다.
* 제거할 값이 없는 경우에는 플러그인이 원래 문자열을 그대로 유지합니다.

<!--## Install the plug-in using the Web SDK or the Adobe Analytics extension

Adobe offers an extension that allows you to use most commonly-used plug-ins.

1. Log in to [Adobe Experience Platform Data Collection](https://experience.adobe.com/data-collection) using your AdobeID credentials.
1. Click the desired tag property.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. Install and publish the [!UICONTROL Common Analytics Plugins] extension
1. If you haven't already, create a rule labeled "Initialize Plug-ins" with the following configuration:
    * Condition: None
    * Event: Core – Library Loaded (Page Top)
1. Add an action to the above rule with the following configuration:
    * Extension: Common Analytics Plugins
    * Action Type: Initialize RFP (Remove From List)
1. Save and publish the changes to the rule.-->

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
/* Adobe Consulting Plugin: rfl (removeFromList) v2.1  */
function rfl(lv,vr,d1,d2,df){var b=lv,f=vr,e=d1,h=d2,g=df;if("-v"===b)return{plugin:"rfl",version:"2.1"};a:{if("undefined"!==typeof window.s_c_il){var c=0;for(var a;c<window.s_c_il.length;c++)if(a=window.s_c_il[c],a._c&&"s_c"===a._c){c=a;break a}}c=void 0}"undefined"!==typeof c&&(c.contextData.rfl="2.1");if(!b||!f)return"";c=[];a="";e=e||",";h=h||e;g=g||!1;b=b.split(e);e=b.length;for(var d=0;d<e;d++)-1<b[d].indexOf(":")&&(a=b[d].split(":"),a[1]=a[0]+":"+a[1],b[d]=a[0]),-1<b[d].indexOf("=")&&(a=b[d].split("="),a[1]=a[0]+"="+a[1],b[d]=a[0]),b[d]!==f&&a?c.push(a[1]):b[d]!==f?c.push(b[d]):b[d]===f&&g&&(a?c.push(a[1]):c.push(b[d]),g=!1),a="";return c.join(h)};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`rfl` 함수에서는 다음 인수를 사용합니다.

* **`lv`** (필수, 문자열): 구분된 값 목록을 포함하는 변수 (또는 문자열)
* **`vr`** (필수, 문자열): `lv` 인수에서 제거할 값입니다. Adobe에서는 한 번의 `rfl` 호출 동안 여러 값을 제거하는 것은 권장하지 않습니다.
* **`d1`** (선택 사항, 문자열): `lv` 인수가 사용하는 구분 기호입니다. 기본값은 쉼표(`,`)입니다.
* **`d2`** (선택 사항, 문자열): 반환 문자열에서 사용할 구분 기호입니다. 기본값은 `d1` 인수와 동일한 값으로 설정됩니다.
* **`df`** (선택 사항, 부울): `true`일 경우, 모든 인스턴스가 아닌 `lv` 인수에서 `vr` 인수의 중복 인스턴스만 강제 적용합니다. 설정하지 않으면 기본값이 `false`로 설정됩니다.

이 함수를 호출하면 `lv` 인수가 들어 있지만 `vr` 인수에 지정된 값의 인스턴스 (또는 중복된 인스턴스)는 없는 수정된 문자열이 반환됩니다.

## 호출 예

### 예 #1

...

```js
s.events = "event22,event24,event25";
```

...이고, 다음 코드가 실행되면...

```js
s.events = rfl(s.events,"event24");
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22,event25";
```

### 예 #2

...

```js
s.events = "event22,event24,event25";
```

...이고, 다음 코드가 실행되면...

```js
s.events = rfl(s.events,"event26");
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22,event24,event25";
```

이 예에서 s.events는 &quot;event26&quot;을 포함하지 않았으므로 rfl 호출을 수행해도 s.events에 변화가 생기지 않았습니다.

### 예 #3

...

```js
s.events = "event22,event24,event25";
```

...이고, 다음 코드가 실행되면...

```js
s.events = rfl(s.events);
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "";
```

`rfl` 호출에서 `lv` 인수 또는 `vr` 인수가 비어 있으면 플러그인은 아무 것도 반환하지 않습니다.

### 예 #4

...

```js
s.prop4 = "hello|people|today";
```

...이고, 다음 코드가 실행되면...

```js
s.eVar5 = rfl(s.prop4,"people","|");
```

...s.prop4의 최종 값은 여전히 다음과 같습니다.

```js
s.prop4 = "hello|people|today";
```

...하지만 s.eVar5의 최종 값은 다음과 같습니다.

```js
s.eVar5 = "hello|today";
```

플러그인은 값을 반환한다는 점만 기억하십시오. `lv` 인수를 통해 전달된 변수를 실제로 “재설정”하지는 않습니다.

### 예 #5

...

```js
s.prop4 = "hello|people|today";
```

...이고, 다음 코드가 실행되면...

```js
s.prop4 = rfl(s.prop4,"people");
```

...s.prop4의 최종 값은 여전히 다음과 같습니다.

```js
s.prop4 = "hello|people|today";
```

`lv` 인수 값에 기본값이 아닌 다른 구분 기호 (즉, 쉼표)가 포함되어 있는 경우에 대비하여 `d1` 인수를 반드시 설정하십시오.

### 예 #6

...

```js
s.events = "event22,event23,event25";
```

...이고, 다음 코드가 실행되면...

```js
s.events = rfl(s.events,"EVenT23");
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22,event23,event25";
```

이 예는 실용적이지 않지만 대/소문자를 구분하는 값을 전달해야 함을 보여 줍니다.

### 예 #7

...

```js
s.events = "event22,event23:12345,event25";
```

...이고, 다음 코드가 실행되면...

```js
s.events = rfl(s.events,"event23");
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22,event25";
```

### 예 #8

...

```js
s.events = "event22,event23:12345,event25";
```

...이고, 다음 코드가 실행되면...

```js
s.events = rfl(s.events,"event23:12345");
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22,event23:12345,event25";
```

직렬화 및/또는 숫자/통화 구문을 사용하는 이벤트를 제거해야 하는 경우 `rfl` 호출에서 이벤트 자체 (즉, 직렬화/숫자/통화 값 없이)만 지정해야 합니다.

### 예 #9

...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

...이고, 다음 코드가 실행되면...

```js
s.events = rfl(s.events,"event23");
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22,event24,event25");
```

### 예 #10

...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

...이고, 다음 코드가 실행되면...

```js
s.events = rfl(s.events,"event23", "", "",true);
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22,event23,event24,event25");
```

### 예 #11

...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

...이고, 다음 코드가 실행되면...

```js
s.events = rfl(s.events,"event23", "", "|",true);
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22|event23|event24|event25");
```

### 예 #12

...

```js
s.events = "event22,event23,event24,event25";
```

...이고, 다음 코드가 실행되면...

```js
s.events = rfl(s.events,"event23,event24");
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22,event23,event24,event25";
```

`vr` 인수에서는 여러 값을 설정할 수 없습니다. 위의 예에서 `rfl` 논리는 먼저 `lv` 인수의 값 (즉, s.events)을 분할한 다음 구분된 각 값을 전체 `vr` 인수 값 (예: `"event23,event24"`)과 일치시키려고 합니다.

### 예 #13

...

```js
s.events = "event22,event23,event24,event25";
```

...이고, 다음 코드가 실행되면...

```js
s.events = rfl(s.events,"event23");
s.events = rfl(s.events,"event24");
```

...s.events의 최종 값은 다음과 같습니다.

```js
s.events = "event22,event25");
```

목록에서 제거할 각 값은 자체 `rfl` 호출 내에 포함되어야 합니다.

### 예 #14

...

```js
s.linkTrackVars = "events,eVar1,eVar2,eVar3";
```

...이고, 다음 코드가 실행되면...

```js
s.linkTrackVars = rfl(s.linkTrackVars,"eVar2", ",", ",", false);
```

...s.linkTrackVars의 최종 값은 다음과 같습니다.

```js
s.linkTrackVars = "events,eVar1,eVar3";
```

이 `rfl` 호출의 끝에 있는 마지막 세 개의 인수 (즉, &quot;,&quot;,&quot;,&quot;,false)는 필요하지 않지만, 기본 설정과 일치하므로 있어도 “아무런 해”가 되지 않습니다.

### 예 #15

...

```js
s.events = "event22,event23,event24";
```

...이고, 다음 코드가 실행되면...

```js
rfl(s.events,"event23");
```

...s.events의 최종 값은 여전히 다음과 같습니다.

```js
s.events = "event22,event23,event24";
```

다시 말하지만, 플러그인은 값을 반환한다는 점만 기억하십시오. `lv` 인수를 통해 전달된 변수를 실제로 “재설정”하지는 않습니다.

## 버전 내역

### 2.1 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 2.01 (2019년 9월 17일)

* 기본 구분 기호 값에 대한 작은 버그 수정

### 2.0 (2018년 4월 16일)

* 포인트 릴리스 (다시 컴파일됨, 더 작은 코드 크기).
* `join` 플러그인이 불필요하게 되었습니다.

### 1.0 (2016년 7월 18일)

* 초기 릴리스.
