---
title: 종료 차원
description: 종료 차원 및 그 사용을 나열합니다.
keywords: 종료 페이지, 종료 사이트 섹션, 종료 서버, 종료 사용자 정의 인사이트
feature: Dimensions
exl-id: b2b1ee88-e5c3-44b5-8159-85ec53d20258
TQID: https://experienceleague.adobe.com/YRjvhW8OzBlip9ok0-1D4rYSljkccpIAlDkqCQv7nyo
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
source-wordcount: '234'
ht-degree: 74%
---
# 종료 차원

>[!BEGINSHADEBOX]

*이 도움말 페이지에서는 종료가 [차원](overview.md)(으)로 작동하는 방식을 설명합니다. 종료가 지표로 작동하는 방식에 대한 자세한 내용은 [종료](../metrics/exits.md) 지표를 참조하십시오.*

>[!ENDSHADEBOX]

종료 차원은 마지막 차원 항목을 기록하고 이 값을 해당 방문의 모든 히트에 소급하여 적용합니다. 종료 차원은 보고서 세트 설정의 [트래픽 변수](/help/admin/tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md) 아래에서 경로 지정이 활성화된 모든 변수에 사용할 수 있습니다.

## 데이터로 종료 차원 채우기

주어진 종료 차원은 연결된 트래픽 변수를 기반으로 합니다. Adobe은 방문 중에 해당 변수에 대해 표시된 마지막 값에서 각 종료 차원을 파생합니다. 설정할 전용 변수는 없습니다. 종료가 아닌 변수에 데이터가 있는 경우 해당 종료 차원에도 데이터가 포함됩니다. 트래픽 변수에 데이터가 포함된 경우 종료 차원에 대한 구현 변경은 필요하지 않습니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(방문자의 마지막 히트에서 파생됨) |
| **웹 SDK/XDM 필드** | 없음(방문자의 마지막 히트에서 파생됨) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 방문 |

## 차원 항목

종료 변수는 일반적으로 구현의 사용자 지정 문자열에 기반하므로 조직에서 차원 항목을 결정합니다. 주어진 종료 차원에 있는 값은 연결된 비종료 차원의 차원 항목과 일치합니다. 예를 들어 &#39;종료 페이지&#39; 차원의 차원 항목은 &#39;페이지&#39; 차원의 차원 항목과 유사합니다.
