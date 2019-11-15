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


# mediaName

이 변수는 비디오나 미디어 항목의 이름을 지정합니다.

<!-- 

mediaName.xml

 -->

[!UICONTROL 데이터 삽입 API] 및 [!UICONTROL 데이터 소스 완전 처리]를 통해서만 사용할 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 64KB | pev3 | 비디오; 다음 비디오 흐름; 이전 비디오 흐름; 본 비디오 세그먼트; 비디오 사용 시간 | 없음 |

**구문 및 가능한 값** {#section_F97A2253BBD24FEBBC225F233A319F5D}

**autoTrack 메서드:**

[!UICONTROL s.Media.autoTrack]을 사용하는 경우에는, *`mediaName`변수를 명시적으로 구현할 필요가 없습니다.* JavaScript용 AppMeasurement 코드에 의해 자동으로 결정됩니다.

**수동 추적 메서드:**

구문:

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName) 
```

```js
s.Media.play(mediaName,mediaOffset)
```

```js
s.Media.stop(mediaName,mediaOffset)
```

```js
s.Media.close(mediaName)
```

가능한 값:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

```js
s.Media.play("de_bofr_1045Making_400k", "0")
```

```js
s.Media.play("de_bofr_1045Making_400k", "414")
```

```js
s.Media.close("de_bofr_1045Making_400k")
```

**예** {#section_4B9584265B1A47289818141B2A88021D}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230") 
```

```js
s.Media.play("de_bofr_1045Making_400k", "0")
```

```js
s.Media.play("de_bofr_1045Making_400k", "414")
```

```js
s.Media.close("de_bofr_1045Making_400k")
```

```js
Resulting pev3 parameter syntax: pev3=[Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers]  
  
```

```js
Possible pev3 Values: 
  pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 
  11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32  
  
```

**함정, 질문 및 팁** {#section_941A445BB52E4063B0F6920E61BB90DE}

* 플레이어를 [!UICONTROL s.Media.autoTrack] = true를 사용하여 추적할 수 없는 경우에만 미디어 추적 메서드를 호출해야 합니다.
* 이 변수는 VARCHAR(100)와는 대조적으로 mySQL TEXT 변수로 저장됩니다.
