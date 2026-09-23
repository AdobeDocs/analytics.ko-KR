---
title: 마지막 구매 이후 일 수
description: 현재 히트와 마지막 구매 사이의 일 수입니다.
feature: Dimensions
exl-id: 6f0d9d79-cf40-4de3-9d9f-9b1bc57f97b6
TQID: https://experienceleague.adobe.com/q86bc1bMRctUBe7dFEJaALsq0GjALFQQtKU9cRpRkoU
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
source-wordcount: '207'
ht-degree: 64%
---
# 마지막 구매 이후 일 수

마지막 구매 이후 일 수 [차원](overview.md)은(는) 방문자의 현재 히트와 해당 시점의 가장 최근 구매 사이에 경과된 시간을 측정합니다. 이 차원은 방문자가 사용자의 사이트에서 구매를 한 후 취하는 동작을 이해하는 데 도움이 됩니다.

구매한 적이 없는 방문자는 이 차원에 포함되지 않습니다. 또한 방문자의 첫 구매 전에 실행된 히트도 포함되지 않습니다. 방문자의 첫 구매 후 히트만 포함됩니다.

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

차원 항목에는 방문자의 가장 최근 구매와 현재 히트 사이의 일 수가 포함됩니다. 각 일 수는 별도의 차원 항목이며, 방문자의 가장 최근 구매와 현재 히트가 같은 날 발생한 경우에는 &quot;같은 날&quot;이 됩니다.
