---
title: 고객 충성도
description: 방문자가 이전에 구매한 횟수를 기반으로 한 카테고리입니다.
feature: Dimensions
exl-id: 48ac1fdf-9a32-4bcc-8b23-bf58358a3470
TQID: https://experienceleague.adobe.com/Essa0dflFlsqwtTQ4JdaSEOkX6T-zEYrQGhgXBWhfcI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
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
source-wordcount: '280'
ht-degree: 73%
---
# 고객 충성도

고객 충성도&#39; [차원](overview.md)은(는) 이전 구매 횟수가 0회, 이전 구매 횟수가 1회, 이전 구매 횟수가 2회 또는 이전 구매 횟수가 3회 이상인 사이트 방문자 수를 보고합니다. 이 차원은 사이트가 구매 행동에 영향을 미치는 방식을 파악하는 데 유용합니다. 새 방문자에 대해 유사한 행동을 유도할 수 있도록 세그먼트에서 이 차원을 사용하여 구매를 위해 재방문하는 방문자에 집중할 수도 있습니다.

## 이 차원을 데이터로 채우기

Adobe은 방문자의 구매 내역에서 이 차원을 서버측에서 계산합니다. 설정할 변수가 없습니다. 사이트에 구현되고 있는 [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) 이벤트에 따라 다릅니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(Adobe에서 계산) |
| **웹 SDK/XDM 필드** | 없음(Adobe에서 계산) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

차원 항목에는 다음 항목이 포함됩니다.

* **고객이 아님**: 히트 시 방문자는 이전에 구매한 적이 없습니다.
* **새 고객**: 히트 당시 방문자는 이전에 한 번 구매했습니다.
* **재방문 고객**: 히트 당시 방문자는 이전에 두 번 구매했습니다.
* **단골 고객**: 히트 당시 방문자는 이전에 3회 이상 구매했습니다.

방문자가 구매 (`purchase` 이벤트 트리거) 시, 해당 히트와 모든 후속 히트가 다음 &quot;버킷&quot;으로 이동합니다. 예를 들어 방문자가 사이트에서 제품을 처음 구입하는 경우 이 고객은 &quot;고객이 아님&quot;에서 &quot;새 고객&quot;으로 이동하고 주문은 &quot;새 고객&quot;으로 인한 것이 됩니다. 차원 항목 &quot;고객이 아님&quot;에는 주문을 귀속할 수 없습니다.
