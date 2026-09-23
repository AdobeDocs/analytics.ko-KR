---
title: 재방문 빈도
description: 현재 방문과 이전 방문 사이의 시간 간격을 버킷으로 나눈 값입니다.
feature: Dimensions
exl-id: 8ec31e17-a57d-416f-b471-c2c37a98d134
TQID: https://experienceleague.adobe.com/k0H7kOCgrBRY3cZckPXaJ9UgLBPTYWHxKT8gzeMQjcI
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
source-wordcount: '282'
ht-degree: 76%
---
# 재방문 빈도

&#39;재방문 주기&#39; [차원](overview.md)은(는) 재방문자의 방문 사이에 경과된 시간을 보여줍니다. 방문자가 사이트를 재방문할 때 Adobe는 이전 방문이 얼마나 오래 전에 있었는지 확인하고 해당 히트를 적절한 차원 항목으로 버킷합니다. 해당 기간에 방문자에 대한 웹 사이트의 호소력과 적절성을 측정하는 데 도움이 되는 귀중한 차원입니다. 사이트 콘텐츠와 판촉 행사가 방문자에게 미치는 영향을 식별하는 데에도 도움이 될 수 있습니다.

>[!TIP]
>
>처음 방문하는 방문자는 이 차원에 포함되지 않습니다.

## 이 차원을 데이터로 채우기

Adobe은 현재 방문과 방문자의 이전 방문을 비교하여 이 차원 서버측을 계산합니다. 설정할 변수가 없습니다. 모든 구현에 대해 즉시 작동합니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(Adobe에서 계산) |
| **웹 SDK/XDM 필드** | 없음(Adobe에서 계산) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 방문 |

## 차원 항목

차원 항목에는 이전 방문 이후 경과 시간에 따른 시간 기반 버킷이 포함됩니다.

* 1일 미만
* 1~3 일
* 3~7 일
* 7~14 일
* 14일~1개월
* 1개월 이상

## 차원 항목은 프로젝트의 날짜 범위를 벗어나는 버킷 아래에 나타납니다.

프로젝트의 날짜 범위를 설정할 때 날짜 범위를 벗어나는 방문에 차원 항목이 귀속되는 것을 확인하는 것은 일반적입니다. 예를 들어, 방문자가 7월에 사이트에 왔다가 9월 중 같은 날에 두 번 오는 경우, 9월의 재방문 빈도 차원은 &#39;1개월 이상&#39; 아래에 하나의 방문을 표시하고 &#39;1일 미만&#39; 아래에 하나의 방문을 표시합니다.
