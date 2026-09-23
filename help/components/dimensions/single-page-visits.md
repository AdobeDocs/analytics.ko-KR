---
title: 단일 페이지 방문 (차원)
description: 방문이 단일 페이지로 이루어졌음을 나타내는 플래그입니다.
feature: Dimensions
exl-id: f7b58941-add4-4e7b-8645-a64280fd9dcb
TQID: https://experienceleague.adobe.com/mMxxlVpQi7IsSuxSZGijnvWeoqCa-ybf8otPRDf6AyQ
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
source-wordcount: '187'
ht-degree: 66%
---
# 단일 페이지 방문 횟수

>[!BEGINSHADEBOX]

*이 도움말 페이지에서는 &#39;단일 페이지 방문 횟수&#39;가 [차원](overview.md)(으)로 작동하는 방식을 설명합니다. 자세한 내용은 [단일 페이지 방문 횟수](../metrics/single-page-visits.md) 지표를 참조하십시오.*

>[!ENDSHADEBOX]

단일 페이지 방문 횟수 차원은 하나의 고유한 [페이지](page.md) 차원 항목으로 이루어진 방문 횟수를 보고합니다. [단일 페이지 방문 횟수](../metrics/single-page-visits.md) 지표의 차원 양식입니다.

이 차원은 [세그먼테이션](../segmentation/seg-home.md) 내의 구성 요소로서 가장 일반적으로 사용됩니다. 일반적으로 보고서에서 차원으로 사용되지 않습니다.

## 이 차원을 데이터로 채우기

Adobe은 각 방문에 하나의 고유 페이지가 포함되어 있는지 여부를 평가하여 이 차원 서버측을 계산합니다. 설정할 변수가 없습니다. 모든 구현에 대해 즉시 작동합니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(Adobe에서 계산) |
| **웹 SDK/XDM 필드** | 없음(Adobe에서 계산) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

유일한 차원 항목은 `"Enabled"`입니다. 방문이 단일 페이지로 이루어진 경우 히트가 이 값으로 설정됩니다. 다른 모든 히트는 이 보고서에서 생략됩니다.
