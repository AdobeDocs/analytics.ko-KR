---
title: Activity Map 페이지
description: 링크를 클릭할 때의 페이지 이름입니다.
feature: Dimensions
role: User, Admin
exl-id: 8dc5d5a1-ee44-4c98-80fa-13dd1cf4edf2
TQID: https://experienceleague.adobe.com/WJ0uk-LqIABwehzzy79c2o1cd3EvI-AKUJ--vmLnKRE
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 9%
---
# Activity Map 페이지

&#39;Activity Map 페이지&#39; [차원](overview.md)은(는) 링크를 클릭할 때 방문자가 있었던 페이지를 표시합니다. 이 차원을 사용하여 가장 많이 클릭되는 링크가 포함된 페이지를 결정할 수 있습니다. 이 차원은 Activity Map 오버레이에서 표시할 링크를 판별하는 데에도 사용됩니다.

## 이 차원을 데이터로 채우기

이 차원은 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md) `c.a.activitymap.page`에서 데이터를 검색합니다. 구현에서 [Activity Map](/help/analyze/activity-map/overview.md)을 사용하는 경우, 이 컨텍스트 데이터 변수는 링크를 클릭할 때 자동으로 데이터를 수집합니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음([Activity Map](/help/analyze/activity-map/overview.md) 모듈에서 수집됨) |
| **웹 SDK/XDM 필드** | 없음([Activity Map](/help/analyze/activity-map/overview.md) 모듈에서 수집됨) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 255바이트 |
| **지속성** | 해당 없음 |

클릭한 특정 링크에 대해 이 컨텍스트 데이터 변수는 [Page](page.md) 차원의 값을 수집합니다. 페이지 차원에 값이 없으면 대신 [페이지 URL](page-url.md) 차원이 사용됩니다(페이지 차원이 사용하는 대체 항목과 유사). Activity Map 데이터는 일반적으로 링크를 클릭한 후 다음 히트에서 전송됩니다. 이 차원을 사용하면 데이터를 전송할 때 페이지 값 대신 링크를 클릭했을 때의 페이지 값을 결정할 수 있습니다.

## 차원 항목

Dimension 항목에는 [페이지](page.md) 차원에 있는 모든 값이 포함됩니다.
