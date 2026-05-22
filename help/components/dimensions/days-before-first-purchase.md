---
title: 첫 구매까지 소요된 일 수
description: 방문자의 첫 방문과 첫 번째 구매 사이의 일 수입니다.
feature: Dimensions
exl-id: 651f9d55-49b9-402a-b7c7-ba4fba62c695
TQID: https://experienceleague.adobe.com/fA8CgahXKwJfiynK-I8yuD-byaIyFPkaii3FzkrrPoI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 83%

---

# 첫 구매까지 소요된 일 수

첫 구매까지 소요된 일 수 [차원](overview.md)은(는) 방문자가 사이트에 처음 도달하고 구매하기까지 경과되는 일 수를 보고합니다. 예를 들어 방문자가 처음 방문한 다음 하루 후에 구매한다면 그 이후의 모든 방문 또는 이벤트는 &quot;1일&quot; 차원 항목에 속합니다.

방문자는 처음 구매한 후 방문자의 남은 쿠키 수명 동안 동일한 차원 항목에 속합니다.

## 이 차원을 데이터로 채우기

Adobe에서는 구현의 [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) 이벤트를 기반으로 이 차원을 자동으로 채웁니다. 사이트에서 `purchase` 이벤트를 구현하는 경우 이 차원이 항상 작동합니다.

## 차원 항목

차원 항목에는 사이트에 대한 방문자의 첫 방문과 첫 번째 구매 사이의 일 수가 포함됩니다. 각 일 수는 방문자의 첫 번째 방문과 첫 번째 구매가 같은 날에 발생한 경우 &quot;같은 날&quot;이 발생하는 별도의 차원 항목입니다.
