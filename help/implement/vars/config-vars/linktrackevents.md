---
title: linkTrackEvents
description: 링크 추적 이미지 요청에 포함할 이벤트를 결정합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkTrackEvents

일부 구현에서는 모든 링크 추적 이미지 요청에 모든 변수를 포함하기를 원하지 않습니다. 및 [`linkTrackVars`](linktrackvars.md) 변수를 사용하여 `linkTrackEvents` [`tl()`](../functions/tl-method.md) 호출에 차원 및 지표를 선택적으로 포함할 수 있습니다.

이 변수는 페이지 보기 호출([`t()`](../functions/t-method.md) 메서드)에 사용되지 않습니다.

## Adobe Experience Platform Launch를 사용한 링크 추적 호출의 이벤트

Launch는 인터페이스에 정의된 이벤트를 자동으로 감지하여 링크 추적 히트에 포함합니다.

> [!IMPORTANT] 사용자 지정 코드 편집기를 사용하여 Launch에서 이벤트를 설정하는 경우 사용자 지정 코드도 `linkTrackEvents` 사용할 때 이벤트를 포함해야 합니다.

## s.linkTrackEvents in AppMeasurement and Launch 사용자 지정 코드 편집기

이 `s.linkTrackEvents` 변수는 링크 추적 이미지 요청(`tl()` 메서드)에 포함할 쉼표로 구분된 이벤트 목록을 포함하는 문자열입니다. 링크 추적 히트에 지표를 포함하려면 다음 세 가지 기준을 충족해야 합니다.

* 변수에서 원하는 이벤트를 [`events`](../page-vars/events/events-overview.md) 설정합니다. (예: `s.events = "event1";`)
* Set the `events` variable in `linkTrackVars`. (예: `s.linkTrackVars = "events";`)
* 변수에서 원하는 이벤트를 `linkTrackEvents` 설정합니다. (예: `s.linkTrackEvents = "event1";`)

```js
s.linkTrackEvents = "event1,event2,event3,purchase";
```

이 변수의 기본값은 빈 문자열입니다. 이 변수가 정의되지 않은 경우 모든 이벤트가 링크 추적 이미지 요청에 포함됩니다. Launch는 인터페이스에 설정된 이벤트를 기반으로 이 변수를 자동으로 채우므로 Launch를 사용하여 구현에서 항상 설정됩니다.

> [!TIP] 이 변수에서 이벤트를 지정할 때 Analytics 개체 식별자(`s.`)를 사용하지 마십시오. 예를 들어, `s.linkTrackEvents = "event1";` 는 올바르지만 `s.linkTrackEvents = "s.event1";` 틀립니다.

## 예

다음 링크 추적 함수에는 Adobe로 전송된 이미지 요청에만 `event1` ( `event2`아님)이 포함됩니다.

```js
s.events = "event1,event2";
s.linkTrackVars = "events";
s.linkTrackEvents = "event1";
s.tl(this,"o","Example Custom Link");
```
