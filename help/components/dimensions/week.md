---
title: 주
description: 지표가 발생한 주입니다.
feature: Dimensions
exl-id: 944ec843-998c-473f-b8e6-16cf126745b4
TQID: https://experienceleague.adobe.com/Vvr0Svg2khSzWbtWR5hLfveyctOEM-62WU6oxIsvzXs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 92%

---

# 주

&#39;주&#39; [차원](overview.md)은(는) 주어진 지표가 발생한 주를 보고합니다. 첫 번째 차원 항목은 날짜 범위에서 첫 번째 주이고 마지막 차원 항목은 날짜 범위에서 마지막 주입니다. 이 차원은 시간에 따른 지표를 볼 수 있으므로 트렌드 보고서에 필수적입니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## 차원 항목

Analysis Workspace의 차원 항목에는 첫 번째 요일의 날짜 (연도, 월, 일)가 포함됩니다.

Data Warehouse의 차원 항목에는 요청 날짜 범위에 따라 번호가 매겨진 주가 포함됩니다. 예를 들어 첫 번째 주 전체는 `"Week 1"`입니다. 요청에 부분적인 주가 포함된 경우 데이터는 `"Week 0"` 차원 항목으로 그룹화됩니다.
