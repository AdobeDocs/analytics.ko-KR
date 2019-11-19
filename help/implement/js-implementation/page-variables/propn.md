---
description: 페이지 변수는 pageName, List Props, List Variables 등과 같이, 보고서를 직접 채웁니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: 페이지 변수
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: edf88e40cae8b6886b04257f266666c13a37f88d

---


# propN

속성(`prop`) 변수는 트래픽 모듈 내에서 사용자 지정 보고서를 작성하는 데 사용됩니다.

<!-- 

propN.xml

 -->

props 변수는 경로 지정 보고서용으로 또는 상관 관계 보고서에서 카운터(페이지 보기가 전송되는 횟수 카운트)로 사용할 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 100바이트 | c1 - c75 | 사용자 지정 트래픽 | "" |

**구문 및 가능한 값**

```js
s.propN="value"
```

[!UICONTROL 속성] 변수에는 표준 변수 제한 외에 제한이 없습니다.

**예**

```js
s.prop2="editorial" 
```

```js
s.prop15="toy category"
```

**구성 설정**

 변수의 방문, 방문자 및 `prop`경로 지표 표시에 대해서는 Adobe 고객 지원 센터에 문의하십시오.
