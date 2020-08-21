---
title: 히트 깊이
description: 방문의 히트 수입니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 75%

---


# 히트 깊이

히트 깊이 차원은 주어진 히트가 방문으로 이어질 때까지의 깊이를 보고합니다. 이 차원은 방문자가 사이트에서 작업을 수행하는 방문까지의 거리를 이해하는 데 중요합니다. 히트 깊이는 페이지 보기([`t()`](/help/implement/vars/functions/t-method.md))와 링크 추적 히트([`tl()`](/help/implement/vars/functions/tl-method.md))를 포함하여 모든 유형의 히트를 계산합니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## Dimension 항목

Dimension items include the string `"Hit Depth"` followed by a number representing the number of hits into the visit. The dimension item of `"Hit Depth 1"` represents the first hit of the visit, while the dimension item `"Hit Depth 8"` represents the 8th hit of the visit.

## 방문 깊이와 비교

히트 깊이는 페이지 보기와 링크 추적 히트를 포함하여 모든 유형의 히트를 계산합니다. Visit depth only increments for page view hits, _and_ the [Page](page.md) dimension item is not the same as the value on the previous page. 또한 방문 깊이는 방문 기반 차원으로서, 이것은 방문 깊이가 방문의 모든 히트에 대해 동일한 값임을 의미합니다. 다음 표에서는 방문 예와 방문이 히트 깊이 + 방문 깊이를 고려하는 방식에 대해 설명합니다.

| 페이지 시퀀스 | 히트 깊이 | 방문 깊이에 포함됩니까? | 방문 깊이 |
| --- | --- | --- | --- |
| 홈 페이지 | 1 | 예 | 4 |
| 제품 페이지 | 2 | 예 | 4 |
| 홈 페이지 | 3 | 예 | 4 |
| 사용자 지정 링크 클릭 | 4 | 아니요(사용자 지정 링크) | 4 |
| 사용자 지정 링크 클릭 | 5 | 아니요(사용자 지정 링크) | 4 |
| 제품 페이지 | 6 | 예 | 4 |
| 사용자 지정 링크 클릭 | 7 | 아니요(사용자 지정 링크) | 4 |
| 제품 페이지 | 8 | 아니요(이전 페이지와 동일) | 4 |
