---
title: 모든 검색 페이지 등급
description: 방문자가 사이트에 도달하기 위해 클릭한 검색 엔진의 페이지를 결정합니다.
feature: Dimensions
exl-id: 58ce54c3-cc45-4e84-a14d-5fec0b70f50f
TQID: https://experienceleague.adobe.com/U7WgtQDXInyD1gXeBntncC9Fao1Rdc9W4AHFgx07T4A
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
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 62%
---
# 모든 검색 페이지 등급

&#39;모든 검색 페이지 등급&#39; [차원](overview.md)은(는) 방문자가 사이트에 도달하기 위해 클릭한 검색 결과 페이지에 대한 insight을 제공합니다. 예를 들어, 사이트가 검색 엔진의 검색 결과 중 두 번째 페이지에 나타나는 경우 이 변수의 차원 항목은 &quot;검색 페이지 2&quot;입니다.

## 이 차원을 데이터로 채우기

Adobe은 각 히트의 검색 엔진 [레퍼러](referrer.md)에서 이 차원을 파생하여 방문자가 클릭스루한 검색 결과 페이지를 결정합니다. 설정할 변수가 없습니다. 이 차원이 작동하려면 보고서 세트에 [내부 URL 필터](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md)가 올바로 설정되어 있어야 합니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(검색 엔진 레퍼러에서 파생) |
| **웹 SDK/XDM 필드** | 없음(검색 엔진 레퍼러에서 파생) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

방문자가 검색 엔진에서 사이트까지 클릭하여 도달하는 경우 이 차원의 값은 &quot;검색 페이지&quot; 다음에 클릭한 페이지 번호가 옵니다. 히트가 검색 엔진에서 시작되지 않으면 이 차원의 값은 &quot;Unspecified&quot;입니다.
