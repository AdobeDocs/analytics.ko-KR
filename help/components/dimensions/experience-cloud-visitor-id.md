---
title: Experience Cloud 방문자 ID
description: 방문자의 ECID(Experience Cloud ID), Data Warehouse에서 사용할 수 있습니다.
feature: Dimensions
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 21%

---

# Experience Cloud 방문자 ID

Experience Cloud 방문자 ID [차원](overview.md)은(는) 각 방문자에 대한 ECID를 제공합니다. 이 숫자는 연결된 두 개의 64비트 숫자로 구성된 128비트 숫자로 19자리로 채워집니다.

>[!IMPORTANT]
>
>이 차원은 Data Warehouse에서만 사용할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원에는 방문자 ID 서비스(VisitorAPI) 또는 Experience Platform ID 서비스를 사용하는 구현이 필요합니다. 데이터 피드의 `mcvisid` 열에 해당합니다. 자세한 내용은 [데이터 열 참조](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md)를 참조하십시오.

## 차원 항목

Dimension 항목에는 각 방문자의 Experience Cloud ID가 포함됩니다.
