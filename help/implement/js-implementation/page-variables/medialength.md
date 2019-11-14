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


# mediaLength

 변수는 재생되는 미디어의 전체 길이를 지정합니다.

<!-- 

mediaLength.xml

 -->

<table id="table_B1AE8A9DF9D545C2965CDB2DB6C2969B"> 
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
   <td> 전체 pev3 요청에 대한 최대 크기 없음 - 크기는 브라우저의 URL 길이 제한으로 제한됩니다. </td> 
   <td> pev3 </td> 
   <td> 비디오 사용 시간; <p>본 비디오 세그먼트 </p> </td> 
   <td> 없음 </td> 
  </tr> 
 </tbody> 
</table>

**구문 및 가능한 값** {#section_FEC1B01FDD234ACEB63C0558BEEB5CBC}

**autoTrack 메서드:**

[!UICONTROL s.Media.autoTrack]을 사용하는 경우에는, [!UICONTROL mediaLength] 변수를 명시적으로 구현할 필요가 없습니다. JavaScript용 AppMeasurement 코드에 의해 자동으로 결정됩니다.

**수동 추적 메서드:**

구문:

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName)
```

가능한 값:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

**예** {#section_048B2D31BB584647A5D335AE94E5A599}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

```js
Resulting pev3 parameter syntax: pev3= [Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers]  
  
```

```js
Possible pev3 values: pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32
```

**함정, 질문 및 팁** {#section_1CEDC78FEF4940E9BC02A2AF1EE2FB01}

* 플레이어를 [!UICONTROL s.Media.autoTrack] = true를 사용하여 추적할 수 없는 경우에만 미디어 추적 메서드를 호출해야 합니다.
* [!UICONTROL autoTrack]을 사용하여 추적하는 경우가 아니라면, 반드시 길이를 초 단위로 설정해야 합니다.

