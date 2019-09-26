---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.linkTrackEvents

The  variable is a comma-separated list of events that are sent with a [!UICONTROL custom], [!UICONTROL exit], or [!UICONTROL download] link.

If an event is not in *`linkTrackEvents`*, it is not sent to [!DNL Analytics], even if it is populated in the [!UICONTROL onClick] event of a link, as shown in the following example:

```js
s.linkTrackVars="events" 
s.events="event1,event2" 
s.t() // both event1 and event2 are recorded 
<a href="help.php" onClick="s=s_gi('rs1');s.tl(this,'o')">event1 is recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.events='event2';s.tl(this,'o')">No events are recorded</a> 
```

[!DNL help.php]에 연결된 첫 번째 링크를 보면 이벤트 변수가 링크를 누르기 전에 설정되었던 값을 유지함을 알 수 있습니다. 이렇게 되면 사용자 지정 링크로 event1을 보낼 수 있습니다. 두 번째 예인 [!DNL test.php]에 연결된 링크에서는 event2가 *`linkTrackEvents`*.

혼동 및 잠재적 문제를 방지하려면 링크 추적에 사용되는 링크의 *`linkTrackVars`* onClick *`linkTrackEvents`* 이벤트를 작성하고  입력하는 것이 좋습니다.

The *`linkTrackEvents`* variable contains the events that should be sent with [!UICONTROL custom], [!UICONTROL download], and [!UICONTROL exit] links. 이 변수는 "events"가 *`linkTrackVars`* 포함된 경우에만 고려됩니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 전환 | "없음" |

## 구문 및 가능한 값

The *`linkTrackEvents`*&#x200B;변수는 쉼표로 구분된 이벤트 목록(공백 없음)입니다.

```js
s.linkTrackEvents="event1[,event2[,event3[...]]]"
```

 *`linkTrackEvents`*. These events are listed in [Events](https://docs.adobe.com/content/help/en/analytics/implementation/analytics-basics/ref-events.html). 이벤트 이름의 앞이나 뒤에 공백이 있으면, 이벤트를 링크 이미지 요청으로 보낼 수 없습니다.

## 예

```js
s.linkTrackEvents="purchase,event1"
```

```js
s.linkTrackEvents="scAdd,scCheckout,purchase,event14"
```

## 구성 설정

없음

## 함정, 질문 및 팁

* JavaScript 파일은 "events" 변수를 *`linkTrackEvents`* 포함하는 *`linkTrackVars`* 경우입니다. "events"는 정의된 *`linkTrackVars`* 경우에만 포함되어야 *`linkTrackEvents`* 합니다.

* 페이지에서 이벤트가 실행되어 *`linkTrackEvents`*. That event is recorded again with any [!UICONTROL exit], [!UICONTROL download], or [!UICONTROL custom] links unless the events variable is reset prior to that event (in the [!UICONTROL onClick] of a link or after the call to the *`t()`* function).

* If *`linkTrackEvents`* contains spaces between event names, the events are not recorded.
