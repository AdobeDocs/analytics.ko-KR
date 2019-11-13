---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 82060388a9a2122b66c57725cafa0eb4ce54e147

---


# s.linkTrackVars

 변수는 사용자 지정, 종료 및 다운로드 링크와 함께 전송되는, 쉼표로 구분되는 변수 목록입니다.

The [`linkTrackVars`](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html) parameter should include each variable that you want to track with every file download, exit link, and custom link.

The settings for `linkTrackVars` and `linkTrackEvents` within the JS file affect every file download, exit link, and custom link. 변수(또는 이벤트)가 현재 페이지에 적용되지만 특정 파일 다운로드, 종료 링크 또는 사용자 지정 링크와 관계없는 경우 각 변수 및 이벤트 인스턴스가 부풀려질 수 있습니다.

적절한 변수가 사용자 지정 링크 코드로 설정되도록 하려면 다음과 같이 사용자 지정 링크 코드 `linkTrackVars` 내에서 및 `linkTrackEvents` 설정을 지정하는 것이 좋습니다.

```js
<a href="index.html" onClick=" 
var s=s_gi('rsid'); 
s.linkTrackVars='prop1,prop2,eVar1,eVar2,events'; 
s.linkTrackEvents='event1'; 
s.prop1='Custom Property of Link'; 
s.events='event1'; 
s.tl(this,'o','Link Name'); 
">My Page 
```

위의 예에서 prop1의 값은 사용자 지정 링크 코드 자체 내에 설정됩니다. prop2의 값은 페이지에 설정된 변수의 현재 값에서 가져옵니다.

The values of `linkTrackVars` and `linkTrackEvents` override the settings in the JS file and ensure only the variables and events specified in the custom link code are set for the specific link.

*참고:(또는`linkTrackVars``linkTrackEvents`)가 null(또는 ""과 같은 빈 문자열)인 경우 현재 페이지에 대해 정의된 모든 Analytics 변수(또는 이벤트)가 추적됩니다. 즉, 값이 있는 모든 변수는 링크 데이터와 함께 전송됩니다. 이 경우 각 변수의 인스턴스가 부풀려질 가능성이 높습니다. 다른 변수와 연결된 인스턴스 또는 페이지 보기가 부풀려지지 않도록 링크 추적에 사용되는 링크의`linkTrackVars`onClick`linkTrackEvents`이벤트에서[!UICONTROL 와]를 채우는 것이 좋습니다.*

링크 데이터(사용자 지정, 종료 및 다운로드 링크)와 함께 보내야 하는 모든 변수는 `linkTrackVars`. `linkTrackEvents`를 사용하는 경우 `linkTrackVars`에 "events"를 포함해야 합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 임의 | "없음" |

When populating `linkTrackVars`, do not use the 's.' prefix for variables. 예를 들어 `linkTrackVars`를 "s.prop1"로 채우지 않고 "prop1"로 채워야 합니다. 다음 예제는 `linkTrackVars` 사용 방법을 보여줍니다.

```js
s.linkTrackVars="eVar1,events" 
s.linkTrackEvents="event1" 
s.events="event1" 
s.eVar1="value A" 
s.eVar2="value B" 
s.t() // eVar1, event1 and event2 are recorded 
<a href="https://google.com">event1 and eVar1 are recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.eVar1='value C';s.events='';s.tl(this,'o')">eVar1 is recorded</a> 
```

google.com에 연결된 링크는 종료 링크(Google을 사용하지 않는 경우)이므로, event1과 eVar1이 종료 링크 데이터와 함께 보내져서, eVar1과 연결된 인스턴스와 event1이 실행되는 횟수를 증가시킵니다. [!DNL test.php]에 연결된 링크에서 [!UICONTROL eVar1]은 'value C' 값과 함께 전송됩니다. 이 값은 `tl()` 호출 시 eVar1의 현재 값이기 때문입니다.

## 구문 및 가능한 값

`linkTrackVars` 변수는 개체 이름 접두사가 없고 대소문자를 구분하고 변수 이름을 쉼표로 구분하는 목록입니다. 's.eVar1' 대신 'eVar1'을 사용하십시오.

```
s.linkTrackVars="variable_name[,variable_name[...]]"
```

The `linkTrackVars` variable may contain only variables that are sent to [!DNL Analytics], namely: `events`, `campaign`, `purchaseID`, `products`, `eVar1-75`, `prop1-75`, `hier1-5`, `channel`, `server`, `state`, `zip`, and `pageType`.

## 예

```
s.linkTrackVars="events,prop1,eVar49"
```

```
s.linkTrackVars="products"
```

## 구성 설정

없음

## 함정, 질문 및 팁

* `linkTrackVars`가 비어 있으면 값이 있는 모든 변수가 모든 서버 호출과 함께 추적됩니다.
* `linkTrackVars`에 나열된 모든 변수는 모든 다운로드, 종료 또는 사용자 지정 링크 시 추적되는 값이 있습니다.
* `linkTrackEvents`를 사용하는 경우 `linkTrackVars`에 "events"를 포함해야 합니다.

* 변수에 "s." 또는 "s_objectname." 접두사를 사용하지 마십시오.
