---
title: 년
description: 지표가 발생한 연도입니다.
feature: Dimensions
exl-id: 872fb659-fb19-40ac-b371-e89c5a5d0274
TQID: https://experienceleague.adobe.com/udpZMXip1fKw7-lKNDS7pkgr432G18uzYIXjDRL6jjQ
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
source-wordcount: '124'
ht-degree: 51%
---
# 년

Year&#39; [차원](overview.md)은(는) 주어진 지표가 발생한 연도를 보고합니다. 첫 번째 차원 항목은 날짜 범위에서 첫 번째 해이고 마지막 차원 항목은 날짜 범위에서 가장 최근 연도입니다.

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

차원 항목은 주어진 연도를 포함하며, 이때 날짜는 괄호 안에 포함됩니다.
