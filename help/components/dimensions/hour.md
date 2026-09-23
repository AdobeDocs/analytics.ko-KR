---
title: 시간
description: 지표가 발생한 시간입니다.
feature: Dimensions
exl-id: 323c46dd-87d0-487a-b954-e5ccbc1b919d
TQID: https://experienceleague.adobe.com/Gkigdxnrted-gkPoGCQMx229EvCmVvSt9Rr5QP-IfGU
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
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 78%
---
# 시간

&#39;시간&#39; [차원](overview.md)은(는) 주어진 지표가 발생한 시간을 보고합니다(내림). 첫 번째 차원 항목은 날짜 범위에서 첫 번째 시간이고 마지막 차원 항목은 날짜 범위에서 마지막 시간입니다. 이 차원은 시간에 따른 지표를 볼 수 있으므로 트렌드 보고서에 중요합니다.

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

차원 항목에는 해당 날짜와 함께 보고서의 날짜 범위 내에 지정된 시간이 포함됩니다. 형식은 `HH:HH YYYY-MM-DD`를 사용합니다.

## 일광 절약 시간제

일광 절약 시간제는 봄에는 시계를 1시간 앞당기고 가을에는 1시간 뒤로 설정하는 방식입니다. 보고서 세트의 시간대에서 일광 절약 시간제를 사용하는 경우 Adobe는 그에 따라 해당 시간에 대한 데이터를 조정합니다.

* **일광 절약 시간제가 시작되는 시기**: 3월 보고서 데이터에서 일반적으로 1시간 차이가 나타납니다. 여기가 일광 절약 시간제가 시작되는 곳입니다. 해당 시간이 존재하지 않으므로 이 시간은 데이터 수집에 포함되지 않습니다. 적은 양의 데이터가 여전히 이 시간에 포함될 수 있습니다. Adobe 데이터 수집 서버는 일광 절약 시간 조정을 고려하는데 수 초 (최대 1분)가 소요됩니다.
* **일광 절약 시간제가 끝나는 시기**: 11월 보고서에는 일반적으로 2배 누적 시간이 나타납니다. 이 때가 일광 절약 시간제가 끝나는 곳입니다. 시간이 두 번 발생했으므로 두 시간 모두 보고서에서 집계됩니다.
