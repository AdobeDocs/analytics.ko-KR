---
title: 마지막 방문 이후의 일 수
description: 현재 히트와 마지막으로 방문한 시간 사이의 일 수입니다.
feature: Dimensions
exl-id: 8063bdc6-516a-4dd0-a4ca-ded739e8d406
TQID: https://experienceleague.adobe.com/VOkdvehFSgp1xBEq49W5FIphzHi8ZCbrsoMnI7rgQMs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 168
ht-degree: 79%

---

# 마지막 방문 이후의 일 수

마지막 방문 이후의 일 수 [차원](overview.md)은(는) 방문자의 현재 히트와 이전 방문(있는 경우) 사이에 경과된 시간의 크기를 측정합니다. 이 차원은 방문자가 사이트를 방문한 후 취하는 동작을 이해하는 데 도움이 됩니다. 해당 예는 다음과 같습니다.

* 사용자가 사이트를 얼마나 자주 다시 방문합니까?
* 반환 빈도와 전환 사이에는 어떤 상관 관계가 있습니까? 반복 구매자가 자주 방문합니까, 아니면 드물게 방문합니까?
* 캠페인을 클릭하여 이동한 사용자가 자주 방문합니까?

처음 방문하는 사람은 이 차원에 포함되지 않습니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## 차원 항목

차원 항목에는 방문자의 마지막 방문과 현재 히트 사이의 일 수가 포함됩니다. 각 일 수는 방문자의 마지막 방문과 현재 히트가 같은 날 발생한 경우 `"Same day"` 발생하는 별도의 차원 항목입니다.
