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


# mediaSession

이 변수는 사용되는 비디오나 미디어 자산의 세그먼트를 지정합니다.

<!-- 

mediaSession.xml

 -->

<table id="table_8681473270FE44DFBBCCC0FBA6737104"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 255바이트 </td> 
   <td> pev3 </td> 
   <td> 비디오 사용 시간 <p>본 비디오 세그먼트 </p> </td> 
   <td> 없음 </td> 
  </tr> 
 </tbody> 
</table>

**구문 및 가능한 값** {#section_9A63266633C4427CB4A6549E4D887B85}

**autoTrack 메서드:**

If using [!UICONTROL s.Media.autoTrack], the *`mediaName`* does not need to be implemented explicitly. JavaScript용 AppMeasurement 코드에 의해 자동으로 결정됩니다.

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

**예** {#section_3446EC37E017407FA3F43C9BDAEA0B85}

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
Resulting pev3 parameter syntax: pev3=[Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers]
```

```js
Possible pev3 Values: pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32 
```

**함정, 질문 및 팁** {#section_1BCEB037AB724B6EBE87420BD3604B88}

플레이어를 [!UICONTROL s.Media.autoTrack] = true를 사용하여 추적할 수 없는 경우에만 미디어 추적 메서드를 호출해야 합니다.
