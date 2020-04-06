---
title: linkTrackEvents
description: 링크 추적 이미지 요청에 포함할 이벤트를 결정합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkTrackEvents

일부 구현에서는 모든 링크 추적 이미지 요청에 모든 변수를 포함할 필요가 없습니다. [`tl()`](../functions/tl-method.md) 호출에 차원 및 지표를 선택적으로 포함하려면 [`linkTrackVars`](linktrackvars.md) 및 `linkTrackEvents` 변수를 사용하십시오.

This variable is not used for page view calls ([`t()`](../functions/t-method.md) method).

## Adobe Experience Platform Launch를 사용한 링크 추적 호출의 이벤트

Launch는 인터페이스에 정의된 이벤트를 자동으로 감지하여 링크 추적 히트에 포함합니다.

>[!IMPORTANT] 사용자 지정 코드 편집기를 사용하여 Launch에서 이벤트를 설정하는 경우 사용자 지정 코드도 사용하여 `linkTrackEvents`에서 이벤트를 포함해야 합니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.linkTrackEvents

The `s.linkTrackEvents` variable is a string containing a comma-delimited list of events that you want to include in link tracking image requests (`tl()` method). 링크 추적 히트에 지표를 포함하려면 다음 세 가지 기준을 충족해야 합니다.

* [`events`](../page-vars/events/events-overview.md) 변수에서 원하는 이벤트를 설정합니다. (예: `s.events = "event1";`)
* `linkTrackVars`에서 `events` 변수를 설정합니다. (예: `s.linkTrackVars = "events";`)
* `linkTrackEvents` 변수에서 원하는 이벤트를 설정합니다. (예: `s.linkTrackEvents = "event1";`)

```js
s.linkTrackEvents = "event1,event2,event3,purchase";
```

이 변수의 기본값은 빈 문자열입니다. 이 변수가 정의되지 않으면 모든 이벤트가 링크 추적 이미지 요청에 포함됩니다. Launch는 인터페이스에 설정된 이벤트를 기반으로 이 변수를 자동으로 채우므로 Launch를 사용하여 구현에서 항상 설정됩니다.

>[!TIP] 이 변수에서 이벤트를 지정할 때 Analytics 개체 식별자(`s.`)를 사용하지 마십시오. 예를 들어, `s.linkTrackEvents = "event1";`은 올바르지만 `s.linkTrackEvents = "s.event1";`은 틀립니다.

## 예

다음 링크 추적 함수에는 Adobe에 전송된 이미지 요청에서 `event1`만(`event2`는 아님) 포함됩니다.

```js
s.events = "event1,event2";
s.linkTrackVars = "events";
s.linkTrackEvents = "event1";
s.tl(this,"o","Example Custom Link");
```
