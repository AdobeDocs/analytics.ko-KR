---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics Implementation
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: ca0797a353661a72d4064aa5aa84c3d9b7eb38a5

---


# s.linkTrackEvents

이 변수는 사용자 지정, 종료 또는 다운로드 링크로 전송되며 쉼표로 구분된 이벤트 목록입니다. The `linkTrackEvents` parameter should include each event you want to track with every file download, exit link, and custom link. 이 링크 유형 중 하나가 발생하면, 식별된 각 변수의 현재 값이 추적됩니다. 이 변수는 [`linkTrackVars`](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html)에 "events"가 포함된 경우에만 고려합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 전환 | "없음" |

If an event is not in `linkTrackEvents`, it is not sent to Analytics, even if it is populated in the `onClick` event of a link, as shown in the following example:

```js
s.linkTrackVars="events" 
s.events="event1,event2" 
s.t() // both event1 and event2 are recorded 
<a href="help.php" onClick="s=s_gi('rs1');s.tl(this,'o')">event1 is recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.events='event2';s.tl(this,'o')">No events are recorded</a> 
```

The values of [`linkTrackVars`](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html) and `linkTrackEvents` override the settings in the JS file and ensure only the variables and events specified in the custom link code are set for the specific link. 두 가지 모두에 대한 설정은 모든 파일 다운로드, 종료 링크 및 사용자 지정 링크에 영향을 줍니다. 변수(또는 이벤트)가 현재 페이지에 적용되지만 특정 파일 다운로드, 종료 링크 또는 사용자 지정 링크와 관계없는 경우 각 변수 및 이벤트 인스턴스가 부풀려질 수 있습니다.

적절한 변수가 사용자 지정 링크 코드로 설정되도록 하기 위해 다음과 같이, 사용자 지정 링크 코드 내에서  *`linkTrackVars`* and *`linkTrackEvents`* within the custom link code, as follows:

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

In the above example, the value for `prop1` is set within the custom link code itself. The value of `prop2` comes from the current value of the variable as set on the page.

*참고:(또는`linkTrackVars``linkTrackEvents`)가 null(또는 ""과 같은 빈 문자열)인 경우 현재 페이지에 대해 정의된 모든 Analytics 변수(또는 이벤트)가 추적됩니다. 즉, 값이 있는 모든 변수는 링크 데이터와 함께 전송됩니다. 이 경우 각 변수의 인스턴스가 부풀려질 가능성이 높습니다. 다른 변수와 연결된 인스턴스 또는 페이지 보기가 부풀려지지 않도록 링크 추적에 사용되는 링크의`linkTrackVars`이벤트에서`linkTrackEvents`와`onClick`를 채우는 것이 좋습니다.*

링크 데이터(사용자 지정, 종료 및 다운로드 링크)와 함께 보내야 하는 모든 변수는 `linkTrackVars`. `linkTrackEvents`를 사용하는 경우 `linkTrackVars`에 "events"를 포함해야 합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 임의 | "없음" |

When populating `linkTrackEvents`, do not use the 's.' prefix for variables. 예를 들어 "s.event1"로 채우는 대신 "event1"로 채워야 합니다. 다음 예는 이 매개 변수를 사용하는 방법을 보여 줍니다.

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

첫 번째 링크에서 events 변수는 링크를 클릭하기 전에 설정된 값을 보유합니다. This allows `event1` to be sent with the custom link. In the second example, the link to `event2` is not recorded because it is not listed in `linkTrackEvents`.

혼동 및 잠재적 문제가 발생하지 않게 하기 위해 링크 추적에 사용되는 링크의 [ 이벤트에서 `linkTrackVars`](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html)`linkTrackEvents` 및 `onClick`를 채우는 것이 좋습니다.

## 구문 및 가능한 값

*`linkTrackEvents`* 변수는 쉼표로 구분된 이벤트 목록(공백 없음)입니다.

```
s.linkTrackEvents="event1[,event2[,event3[...]]]"
```

이벤트 이름만 `linkTrackEvents`에서 허용됩니다. 이러한 이벤트는 [이벤트](https://docs.adobe.com/content/help/en/analytics/implementation/analytics-basics/ref-events.html)에 나열되어 있습니다. 이벤트 이름 앞이나 뒤에 공백이 있으면 링크 이미지 요청과 함께 이벤트를 보낼 수 없습니다.

## 예

To track `prop1`, `eVar1`, and `event1` with every file download, exit link, and custom link, use the following settings within the global JS file:

```
s.linkTrackVars="prop1,eVar1,events"
```

```
s.linkTrackEvents="event1"
```

**기타 예**

```
s.linkTrackEvents="purchase,event1"
```

```
s.linkTrackEvents="scAdd,scCheckout,purchase,event14"
```

## 구성 설정

없음

## 함정, 질문 및 팁

* JavaScript 파일은 `linkTrackEvents`에 "events" 변수가 포함된 경우에만 `linkTrackVars`를 사용합니다. "events"는 `linkTrackVars`가 정의된 경우에만 `linkTrackEvents`에 포함해야 합니다.

* 페이지에서 이벤트가 실행되어 `linkTrackEvents`. 이 이벤트는 해당 이벤트 전(링크의 `onClick`에서 또는 `t()` 함수 호출 후)에 events 변수가 다시 설정되지 않는 경우 종료, 다운로드 또는 사용자 지정 링크로 다시 기록되지 않습니다.

* `linkTrackEvents`의 이벤트 이름 사이에 공백이 있을 경우에는 이벤트가 기록되지 않습니다.
