---
title: 요일
description: 날짜 범위와 관계없이 요일
feature: Dimensions
exl-id: 01aa6b5f-49e6-4f86-97c7-8d0ff431e15b
TQID: https://experienceleague.adobe.com/9nudTrYTDMEFXSo81uUuw9KFT3mRPhZer3cX81AwoPM
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
source-wordcount: '167'
ht-degree: 62%
---
# 요일

요일&#39; [차원](overview.md)은 히트가 발생한 요일을 보고합니다. 이 보고서는 주별로 구분된 보고서가 필요하지만 요일을 차원 항목으로 고정하고 싶지 않은 경우 유용합니다. 이 차원은 어떤 날짜 범위에든 작동하므로 특히나 예약된 보고서에서 차원으로서 중요합니다.

## 이 차원을 데이터로 채우기

이 차원은 각 히트의 타임스탬프에서 파생됩니다. 설정할 변수가 없습니다. 모든 구현에서 즉시 작동합니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(히트 타임스탬프에서 파생) |
| **웹 SDK/XDM 필드** | 없음(히트 타임스탬프에서 파생) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 히트 |

## 차원 항목

차원 항목에는 히트가 발생한 요일을 나타내는 `Sunday` - `Saturday`이 포함됩니다. 차원 항목의 순서는 기본적으로 [사용자 지정 달력](/help/admin/tools/manage-rs/edit-settings/general/custom-calendar.md)에서 첫 번째 요일을 따릅니다.
