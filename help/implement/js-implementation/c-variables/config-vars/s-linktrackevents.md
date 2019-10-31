---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# s.linkTrackEvents

이 변수는 [!UICONTROL 사용자 지정], [!UICONTROL 종료] 또는 [!UICONTROL 다운로드] 링크로 전송되며 쉼표로 구분된 이벤트 목록입니다.

이벤트가 *`linkTrackEvents`*&#x200B;에 없는 경우 다음 예에 표시된 대로 링크의 [!UICONTROL onClick] 이벤트에서 채워지더라도 [!DNL Analytics]로 보내지지 않습니다.

```js
s.linkTrackVars="events" 
s.events="event1,event2" 
s.t() // both event1 and event2 are recorded 
<a href="help.php" onClick="s=s_gi('rs1');s.tl(this,'o')">event1 is recorded</a> 
<a href="test.php" onClick="s=s_gi('rs1');s.events='event2';s.tl(this,'o')">No events are recorded</a> 
```

[!DNL help.php]에 연결된 첫 번째 링크를 보면 이벤트 변수가 링크를 누르기 전에 설정되었던 값을 유지함을 알 수 있습니다. 이렇게 되면 사용자 지정 링크로 event1을 보낼 수 있습니다. 두 번째 예인 [!DNL test.php]에 연결된 링크에서는 event2가 *`linkTrackEvents`*.

혼동 및 잠재적 문제가 발생하지 않게 하기 위해 링크 추적에 사용되는 링크의 [!UICONTROL onClick] 이벤트에서 *`linkTrackVars`* 및 *`linkTrackEvents`*&#x200B;를 채우는 것이 좋습니다.

*`linkTrackEvents`* 변수에는 [!UICONTROL 사용자 지정], [!UICONTROL 다운로드] 및 [!UICONTROL 종료] 링크로 전송해야 하는 이벤트가 들어 있습니다. 이 변수는 *`linkTrackVars`*&#x200B;에 "events"가 포함된 경우에만 고려합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | 전환 | "없음" |

## 구문 및 가능한 값

*`linkTrackEvents`* 변수는 쉼표로 구분된 이벤트 목록(공백 없음)입니다.

```js
s.linkTrackEvents="event1[,event2[,event3[...]]]"
```

이벤트 이름만 *`linkTrackEvents`*&#x200B;에서 허용됩니다. 이러한 이벤트는 [이벤트](https://docs.adobe.com/content/help/en/analytics/implementation/analytics-basics/ref-events.html)에 나열되어 있습니다. 이벤트 이름의 앞이나 뒤에 공백이 있으면, 이벤트를 링크 이미지 요청으로 보낼 수 없습니다.

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

* JavaScript 파일은 *`linkTrackVars`*&#x200B;에 "events" 변수가 포함된 경우에만 *`linkTrackEvents`*&#x200B;를 사용합니다. "events"는 *`linkTrackEvents`*&#x200B;가 정의된 경우에만 *`linkTrackVars`*&#x200B;에 포함해야 합니다.

* 페이지에서 이벤트가 실행되어 *`linkTrackEvents`*. 이 이벤트는 해당 이벤트 전(링크의 [!UICONTROL onClick]에서 또는 *`t()`* 함수 호출 후)에 events 변수가 다시 설정되지 않는 경우 [!UICONTROL 종료], [!UICONTROL 다운로드] 또는 [!UICONTROL 사용자 지정] 링크로 다시 기록되지 않습니다.

* *`linkTrackEvents`*&#x200B;의 이벤트 이름 사이에 공백이 있을 경우에는 이벤트가 기록되지 않습니다.
