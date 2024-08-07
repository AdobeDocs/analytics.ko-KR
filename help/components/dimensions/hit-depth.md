---
title: 히트 깊이
description: 방문의 히트 수입니다.
feature: Dimensions
exl-id: 84c27e3f-4228-4455-95bf-0239928337b5
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 94%

---

# 히트 깊이

&#39;히트 깊이&#39; [차원](overview.md)은(는) 주어진 히트가 방문까지 얼마나 진행되었는지 보고합니다. 이 차원은 방문자가 사이트에서 작업을 수행하는 방문까지의 거리를 이해하는 데 중요합니다. 히트 깊이는 페이지 보기 ([`t()`](/help/implement/vars/functions/t-method.md))와 링크 추적 히트 ([`tl()`](/help/implement/vars/functions/tl-method.md))를 포함하여 모든 유형의 히트를 계산합니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## 차원 항목

차원 항목에는 문자열 `"Hit Depth"`가 포함되며 그 뒤에는 방문까지의 히트 수를 나타내는 숫자가 옵니다. `"Hit Depth 1"`이라는 차원 항목은 방문의 첫 번째 히트를 나타내고 차원 항목 `"Hit Depth 8"`은 방문의 8번째 히트를 나타냅니다.

## 방문 깊이와 비교

히트 깊이는 페이지 보기와 링크 추적 히트를 포함하여 모든 유형의 히트를 계산합니다. 방문 깊이는 페이지 보기 히트에 대해서만 증가&#x200B;_하며_ [페이지](page.md) 차원 항목은 이전 페이지의 값과 동일하지 않습니다. 또한 방문 깊이는 방문 기반 차원으로서, 이것은 방문 깊이가 방문의 모든 히트에 대해 동일한 값임을 의미합니다. 다음 표에서는 방문 예와 방문이 히트 깊이 + 방문 깊이를 고려하는 방식에 대해 설명합니다.

| 페이지 시퀀스 | 히트 깊이 | 방문 깊이에 포함됩니까? | 방문 깊이 |
| --- | --- | --- | --- |
| 홈 페이지 | 1 | 예 | 4 |
| 제품 페이지 | 2 | 예 | 4 |
| 홈 페이지 | 3 | 예 | 4 |
| 사용자 지정 링크 클릭 | 4 | 아니요 (사용자 지정 링크) | 4 |
| 사용자 지정 링크 클릭 | 5 | 아니요 (사용자 지정 링크) | 4 |
| 제품 페이지 | 6 | 예 | 4 |
| 사용자 지정 링크 클릭 | 7 | 아니요 (사용자 지정 링크) | 4 |
| 제품 페이지 | 8 | 아니요 (이전 페이지와 동일) | 4 |
