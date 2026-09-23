---
title: IP 주소
description: 각 히트가 전송된 IP 주소(Data Warehouse에서 사용 가능).
feature: Dimensions
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
source-wordcount: '153'
ht-degree: 16%
---
# IP 주소

&#39;IP 주소&#39; [차원](overview.md)은(는) 각 히트가 전송된 IP 주소를 나열합니다.

>[!IMPORTANT]
>
>이 차원은 Data Warehouse에서만 사용할 수 있습니다.

## 이 차원을 데이터로 채우기

AppMeasurement은 각 이미지 요청의 HTTP 헤더에서 IP 주소를 자동으로 수집합니다. 데이터 피드의 `ip` 열에 해당합니다. 자세한 내용은 [데이터 열 참조](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md)를 참조하십시오.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(HTTP 요청에서) |
| **웹 SDK/XDM 필드** | 없음(HTTP 요청에서) |
| **쿼리 매개 변수** | 없음(HTTP 요청에서) |
| **XML 태그** | [`<ipAddress>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 해당 없음 |
| **지속성** | 해당 없음 |

보고서 세트의 [일반 계정 설정](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)에서 [!UICONTROL IP 난독화]을(를) 사용하도록 설정하면 Data Warehouse을 포함하여 Analytics의 모든 위치에서 IP 주소가 난독화되거나 제거됩니다.

## 차원 항목

Dimension 항목에는 히트가 전송된 IP 주소가 포함됩니다.
