---
description: 페이지 변수는 pageName, List Props, List Variables 등과 같이, 보고서를 직접 채웁니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: 페이지 변수
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 45642bdbe18627caa20b1def6443f1e596a41f52

---


# Media.trackEvents

 변수는 미디어 히트와 함께 전송해야 하는 이벤트를 식별합니다.

<!-- 

media_trackEvents.xml

 -->

이 변수는 JavaScript와 [!UICONTROL ActionSource]에서만 사용할 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | s.Media.trackEvents="None" |

**구문 및 가능한 값** {#section_66A978EF56914BEAAE73359A268A1B4A}

event1이나 purchase와 같은 이벤트 이름

**예** {#section_140A55D80EA24011954F9383CF312237}

```js
s.Media.trackEvents="event1,purchase"
```

**함정, 질문 및 팁** {#section_030B11C64EE84D46A85CA550DB732D28}

이 변수가 채워질 때마다 반드시 [!UICONTROL trackVars]를 events로 채우십시오.
