---
title: 이벤트까지 남은 시간
description: 방문의 첫 번째 히트와 지표 사이의 시간입니다.
feature: Dimensions
exl-id: 2586673f-d908-4b69-901a-5fafe635d0d5
TQID: https://experienceleague.adobe.com/vO3S-yZwV7KSLmIzRfwNDrVaB3NzpsIocmHsAaamfj0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 84%

---

# 이벤트까지 남은 시간

이벤트까지 남은 시간&#39; [차원](overview.md)은(는) 방문의 첫 번째 히트와 원하는 지표 사이에 경과된 시간을 보고합니다. 이 차원은 양식 제출이나 구매와 같은 성공 이벤트에 도달하는 데 걸리는 시간을 파악하는 데 유용합니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 기술적으로 즉시 작동하지만 사용자 지정 및 구매 이벤트에 가장 잘 작동합니다. 사이트에서는 사용자 지정 이벤트를 구현하는 것이 좋습니다. 사용자 지정 이벤트를 구현하는 경우 이 차원에 대해 추가적인 구현은 필요하지 않습니다.

## 차원 항목

차원 항목에는 `"Less than 1 minute"`부터 `"More than 15 hours"` 범위의 시간 기반 버킷이 포함됩니다. 예를 들어 방문자가 첫 번째 히트에서 구매까지 23분을 소요했다면 `"10 to 30 minutes"` 차원 항목 아래에 속합니다. 이 지표에 대해 버킷을 사용자 지정할 수 없습니다.
