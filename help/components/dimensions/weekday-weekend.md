---
title: 평일/주말
description: 히트가 평일과 주말 중 언제 발생했는지를 확인합니다.
feature: Dimensions
exl-id: c3111cdc-a5f9-4244-a725-b1bb1e72fcff
TQID: https://experienceleague.adobe.com/9TJv-49ub1zHsgEGtBeoJVoHhsBktlOr7QhmgLdLRSo
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
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
source-wordcount: '155'
ht-degree: 49%
---
# 평일/주말

평일/주말&#39; [차원](overview.md)은(는) 히트가 평일(월요일 - 금요일)과 주말(토요일 - 일요일) 중 언제 발생했는지 insight을 제공합니다. 히트 시간은 [보고서 세트의 시간대](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)를 기반으로 합니다.

## 이 차원을 데이터로 채우기

이 차원은 각 히트의 타임스탬프에서 파생되며 설정할 변수가 없습니다. 유일한 종속성은 각 히트에 대한 요일을 결정하는 보고서 세트의 시간대입니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(히트 타임스탬프에서 파생) |
| **웹 SDK/XDM 필드** | 없음(히트 타임스탬프에서 파생) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 히트 |

## 차원 항목

이 차원은 항상 `"Weekday"`과 `"Weekend"`, 이렇게 두 개의 차원 항목을 포함합니다. 차원 항목 `"Weekday"`은 월요일부터 금요일까지 모든 히트에 적용되고, 차원 항목 `"Weekend"`은 토요일과 일요일의 모든 히트에 적용됩니다.
