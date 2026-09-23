---
title: 방문자 ID
description: Data Warehouse에서 사용할 수 있는 방문자의 고유 식별자입니다.
feature: Dimensions
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
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 18%
---
# 방문자 ID

방문자 ID [차원](overview.md)은(는) 각 방문자에 대한 고유 식별자를 제공합니다.

>[!IMPORTANT]
>
>이 차원은 Data Warehouse에서만 사용할 수 있습니다.

## 이 차원을 데이터로 채우기

Adobe은 각 방문자에 대한 방문자 ID를 자동으로 생성합니다. 이 값은 데이터 피드에서 `visid_high` 및 `visid_low` 열의 연결된 값과 동일합니다. 자동으로 생성된 값을 `visitorID` 변수로 재정의할 수 있습니다. 자세한 내용은 [데이터 열 참조](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md)를 참조하십시오.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | [`visitorID`](/help/implement/vars/config-vars/visitorid.md) |
| **웹 SDK/XDM 필드** | 없음 |
| **쿼리 매개 변수** | [`vid`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<visitorId>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 255바이트 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

Dimension 항목에는 각 방문자에 대한 고유 식별자가 포함됩니다.
