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



# hierN

[!UICONTROL 계층] 변수는 사이트의 계층에서 페이지의 위치를 결정합니다.

<!-- 

hierN.xml

 -->

이 변수는 사이트 구조의 수준이 4 이상인 사이트에 가장 유용합니다. 예를 들어 미디어 사이트의 스포츠 섹션에는 스포츠, 해외 스포츠, 야구 및 Red Sox, 이렇게 4개 수준이 있을 수 있습니다. 누군가 야구 페이지를 방문하면 스포츠, 해외 스포츠 및 야구가 해당 방문을 모두 반영합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 255바이트 | H1-H5 | 계층 | "" |

사용할 수 있는 [!UICONTROL 계층] 변수에는 5가지가 있으며, 이 변수들은 Adobe 고객 지원 센터에서 활성화해야 합니다. 계층 활성화 시, 변수에 대한 구분 기호와 계층의 최대 수준 수를 결정해야 합니다. 예를 들어, 구분 기호가 쉼표인 경우 스포츠 계층은 다음과 같이 표시될 수 있습니다.

```js
s.hier1="Sports,Local Sports,Baseball"
```

섹션 이름 중에 그 안에 구분 기호가 포함되는 섹션이 없도록 하십시오. 예를 들어 섹션 중 하나를 "Coach Griffin, Jim"이라고 한다면, 쉼표 이외의 구분 기호를 선택해야 합니다. 각 계층 섹션은 255바이트로 제한되며, 총 변수 제한도 255바이트입니다. 구분 기호를 선택한 후(계층이 만들어질 때)에는 쉽게 변경되지 않습니다.

기본 계층에 대한 구분 기호 변경에 대해서는 Adobe 고객 지원 센터에 문의하십시오. || 또는 /|\와 같이 여러 문자로 구성된 구분 기호를 사용할 수도 있지만, 계층 섹션에는 잘 사용되지 않습니다.

**구문 및 가능한 값** {#section_0739948A68A2420DAB1CBEA3115A5A66}

각 구분 기호 사이에 공백을 넣지 마십시오. 다음 예제 구문에서, N은 1과 5 사이의 숫자입니다.

```js
s.hierN="Level 1[<delimiter>Level 2[<delimiter>Level 3[...]]]"
```

계층 수준을 구분할 때를 제외하고는 구분 기호를 사용하지 마십시오. 구분 기호는 선택한 문자 또는 문자들일 수 있습니다.

**예** {#section_38E0929F88DD45B6ACDF473DF155971D}

```js
s.hier1="Toys|Boys 6+|Legos|Super Block Tub"
```

```js
s.hier4="Sports/Local Sports/Baseball"
```

**구성 설정** {#section_E823FB3CAD744D2480EBCE2DF9B134CC}

없음

**함정, 질문 및 팁** {#section_104E5BD320764BDEA5FA8D13A70C78E3}

* 계층이 설정되고 나면 구분 기호를 변경할 수 없습니다. 계층의 구분 기호를 변경해야 하는 경우에는 Adobe 고객 지원 센터에 문의하십시오.
* 계층을 설정하고 나면 수준 수를 변경할 수 없습니다.

> [!NOTE] 계층을 변경하면 서비스 요금이 발생할 수 있습니다.

