---
title: 이벤트까지 남은 시간
description: 방문의 첫 번째 히트와 지표 사이의 시간입니다.
feature: Dimensions
exl-id: 2586673f-d908-4b69-901a-5fafe635d0d5
TQID: https://experienceleague.adobe.com/vO3S-yZwV7KSLmIzRfwNDrVaB3NzpsIocmHsAaamfj0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
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
source-wordcount: '197'
ht-degree: 53%
---
# 이벤트까지 남은 시간

이벤트까지 남은 시간&#39; [차원](overview.md)은(는) 방문의 첫 번째 히트와 원하는 지표 사이에 경과된 시간을 보고합니다. 이 차원은 양식 제출이나 구매와 같은 성공 이벤트에 도달하는 데 걸리는 시간을 파악하는 데 유용합니다.

## 이 차원을 데이터로 채우기

Adobe은 이 차원 서버측을 방문의 첫 번째 히트와 대상 이벤트 사이의 경과 시간으로부터 계산합니다. 설정할 변수가 없습니다. 기술적으로 즉시 작동하지만 사용자 지정 및 구매 이벤트가 사이트에서 구현될 때 가장 잘 작동합니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(Adobe에서 계산) |
| **웹 SDK/XDM 필드** | 없음(Adobe에서 계산) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

차원 항목에는 `"Less than 1 minute"`부터 `"More than 15 hours"` 범위의 시간 기반 버킷이 포함됩니다. 예를 들어 방문자가 첫 번째 히트에서 구매까지 23분을 소요했다면 `"10 to 30 minutes"` 차원 항목 아래에 속합니다. 이 지표에 대해 버킷을 사용자 지정할 수 없습니다.
