---
title: linkTrackEvents
description: 링크 추적 이미지 요청에 포함할 이벤트를 결정합니다.
feature: Variables
exl-id: 53c9e122-425c-4ec3-8a32-96e4d112f348
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 67%

---

# linkTrackEvents

일부 구현에서는 모든 링크 추적 이미지 요청에 모든 변수를 포함할 필요가 없습니다. [`tl()`](../functions/tl-method.md) 호출에 차원 및 지표를 선택적으로 포함하려면 [`linkTrackVars`](linktrackvars.md) 및 `linkTrackEvents` 변수를 사용하십시오.

이 변수는 페이지 보기 호출 ([`t()`](../functions/t-method.md) 메서드)에 사용되지 않습니다.

## 웹 SDK를 사용하여 XDM 이벤트에 포함할 Analytics 이벤트를 결정합니다

웹 SDK는 링크 추적 호출에 대한 특정 필드를 제외하지 않습니다. 그러나 를 사용할 수 있습니다 `onBeforeEventSend` Adobe으로 데이터를 보내기 전에 원하는 필드를 지우거나 설정하려면 콜백하십시오. 자세한 내용은 [이벤트 전역 수정](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) 를 참조하십시오.

## Adobe Analytics 확장을 사용한 링크 추적 호출의 이벤트

사용자 지정 코드가 없는 경우 Adobe Experience Platform은 정의된 이벤트를 링크 추적 히트에 자동으로 포함시킵니다.

>[!IMPORTANT]
>
>Analytics 확장의 사용자 지정 코드 편집기에서 이벤트를 설정하는 경우 이벤트를 `linkTrackEvents` 사용자 지정 코드도 사용합니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.linkTrackEvents

`s.linkTrackEvents` 변수는 링크 추적 이미지 요청 (`tl()` 메서드)에 포함할 쉼표로 구분된 이벤트 목록이 포함된 문자열입니다. 링크 추적 히트에 지표를 포함하려면 다음 세 가지 기준을 충족해야 합니다.

* [`events`](../page-vars/events/events-overview.md) 변수에서 원하는 이벤트를 설정합니다. (예: `s.events = "event1";`)
* `linkTrackVars`에서 `events` 변수를 설정합니다. (예: `s.linkTrackVars = "events";`)
* `linkTrackEvents` 변수에서 원하는 이벤트를 설정합니다. (예: `s.linkTrackEvents = "event1";`)

```js
s.linkTrackEvents = "event1,event2,event3,purchase";
```

이 변수의 기본값은 빈 문자열입니다. 이 변수가 정의되지 않으면 모든 이벤트가 링크 추적 이미지 요청에 포함됩니다. 참고로, 데이터 수집은 인터페이스에 설정된 이벤트에 근거해 이 변수를 자동으로 입력하므로 Adobe Experience Platform의 태그를 사용하는 구현에 대해 항상 설정됩니다.

>[!TIP]
>
>이 변수에서 이벤트를 지정할 때 Analytics 개체 식별자 (`s.`)를 사용하지 마십시오. 예를 들어 `s.linkTrackEvents = "event1";`은 올바르지만 `s.linkTrackEvents = "s.event1";`은 틀립니다.

## 예

다음 링크 추적 함수에는 Adobe에 전송된 이미지 요청에서 `event1`만 (`event2`는 아님) 포함됩니다.

```js
s.events = "event1,event2";
s.linkTrackVars = "events";
s.linkTrackEvents = "event1";
s.tl(this,"o","Example Custom Link");
```
