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


# Media.trackVars

 변수는 미디어 히트와 함께 전송해야 하는 변수를 식별합니다.

<!-- 

media_trackVars.xml

 -->

이 변수는 JavaScript와 [!UICONTROL ActionSource]에서만 사용할 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | s.Media.trackVars="None" |

**구문 및 가능한 값** {#section_7374684A7EB34AE685E8C40A66CFD289}

[!UICONTROL propN], *`eVarN`*, *`events`*, *`channel`* 등과 같은 변수 이름.

**예** {#section_48653222ABA14AB0A3C4471659971FAA}

```js
s.Media.trackVars="prop2,events,eVar3"
```

**함정, 질문 및 팁** {#section_615AE1B696124B00B78F651B03813EAB}

* [!UICONTROL trackVars]에 eVar3이 지정되어 있어도, 미디어 히트와 함께 전송됩니다.

## 모바일 {#concept_0CEE045F57B444138C0EAA015FC7EA70}

 변수는 쿠키와 구독자 ID가 방문을 식별하는 데 사용되는 순서를 제어합니다.

<!-- 

mobile.xml

 -->

[모바일 네트워크 프로토콜](/help/implement/js-implementation/c-additional-libraries/network-protocols.md)을 참조하십시오.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | 이미지 URL의 경로에 있는 /5/ 또는 /1/ | N/A | 없음 |

**구문 및 가능한 값** {#section_7F1C58090C454882BA9D3D66C9263A76}

```js
s.mobile="any_string" //subscriber id used first, produces /5/ in path of image url 
s.mobile=""  // if set to an empty string or not set at all, cookies used first, produces /1/ in path of image url 
```

**함정, 질문 및 팁** {#section_06CD5CB4EF1E4B9FBE3B9D1F18AAFA30}

JavaScript 쿠키 구현에서 *`s.mobile`* 변수를 사용할 때 방문자 트래픽의 발생 가능한 스파이크를 완화하려면 상호 방문자 ID를 사용합니다.
