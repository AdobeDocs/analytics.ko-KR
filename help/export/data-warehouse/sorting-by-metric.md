---
description: 지표로 정렬하는 방법을 통해 Data Warehouse 보고서를 쉽게 해석하고 다른 Analytics 분류 보고 보기와 비교하는 방법에 대해 알아봅니다.
title: 지표로 정렬
feature: Data Warehouse
exl-id: 6bd82951-c3b4-4ba2-8e4d-b7c9b351911b
TQID: 'https://experienceleague.adobe.com/YPqL6i9RWACubLdf2ywm8xuPyeQkZ30L6rO6FAbhpJI'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: f47edbe0-f963-46ff-a667-71011396f5f3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 17%

---

# 지표로 정렬

내림차순 지표 값으로 정렬된 Data Warehouse의 등급 분류 보고서를 제공합니다.

지표로 정렬하면 Data Warehouse 보고서를 더 쉽게 해석하고, 이러한 보고서를 다른 Analytics 분류 보고 보기와 더 쉽게 비교할 수 있습니다.

다음은 &quot;지표 정렬&quot; 옵션을 활성화하면 Data Warehouse 보고서의 행 순서가 변경되는 방법을 보여줍니다.

날짜 세부기간, 보고 차원 또는 지표가 구성되는 방법 및 &quot;최대 행&quot;의 설정 여부를 기반으로 Data Warehouse 보고서를 &quot;지표 정렬&quot;로 구성할 수 있는 네 가지 방법이 있습니다.

* **레이아웃 1**: 행 항목이 사전 순서로 정렬됩니다(기본값). 최대 행 이 설정되면 보고서에서 처음 N개의 행만 제공됩니다.
* **레이아웃 2**: Data Warehouse에서는 보고서에 있는 모든 행에 대해 지표 정렬을 적용합니다. 첫 번째 지표 값의 타이는 두 번째 지표와 세 번째 지표 등으로 끊어집니다. 모든 지표가 연결되면 분류 라인 항목의 표준 사전 순서가 적용됩니다.
* **레이아웃 3**: 레이아웃 2로, 보고서에 상위 N개 행(즉, &quot;최대 행&quot;에 설정된 숫자)만 출력됩니다.
* **레이아웃 4**: 레이아웃 2로, 각 날짜 세부 기간의 라인 항목을 함께 그룹화하고 해당 시간 범위 내에서 정렬하는 것을 제외합니다.

이 테이블의 &quot;보고서 레이아웃&quot; 열을 참조하여 &quot;지표 정렬&quot;이 다른 Data Warehouse 보고 옵션과 상호 작용하는 방법을 결정하십시오.

| 지표로 정렬할까요? | 지표가 있습니까? | 분류가 있습니까? | 날짜 세부기간? | 최대 행이 설정되었습니까? | 보고서 레이아웃 |
|---|---|---|---|---|---|
| 아니요 | 예 또는 아니요 | 예 또는 아니요 | 예 또는 아니요 | 예 또는 아니요 | 1 |
| 예 | 아니요 | 예 또는 아니요 | 예 또는 아니요 | 예 또는 아니요 | 1 |
| 예 | 예 | 아니요 | 아니요 | 해당 사항 없음 | 1 |
| 예 | 예 | 아니요 | 예 또는 아니요 | 아니요 | 1 |
| 예 | 예 | 예 | 아니요 | 아니요 | 2 |
| 예 | 예 | 아니요 | 예 | 예 | 3 |
| 예 | 예 | 예 | 예 또는 아니요 | 예 | 3 |
| 예 | 예 | 예 | 예 | 아니요 | 4 |
