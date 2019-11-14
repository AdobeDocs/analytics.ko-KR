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


# mediaPlayer

이 변수는 비디오나 미디어 항목을 사용하는 데 사용되는 플레이어를 지정합니다.

<!-- 

mediaPlayer.xml

 -->

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 100바이트 | pev3 | 비디오 플레이어 | 없음 |

**구문 및 가능한 값** {#section_EAA55A3A45B5405F903E3BE6ACAB143F}

**autoTrack 메서드:**

```js
s.Media.playerName = "My Custom Player Name"  //configure player name in global JavaScript or ActionSource
```

**수동 추적 메서드:**

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName)
```

가능한 값:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

**예** {#section_64967E1333D542CCB6CF62F0A1E0EF88}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

```js
Resulting pev3 parameter syntax: pev3=[Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers] 
```

```js
Possible pev3 Values: pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32
```

**함정, 질문 및 팁** {#section_0020E031338F4A4880B9AC5B9A85BEF5}

플레이어를 s.Media.autoTrack = true를 사용하여 추적할 수 없는 경우에만 미디어 추적 메서드를 호출해야 합니다.

