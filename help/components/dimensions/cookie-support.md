---
title: 쿠키 지원
description: 브라우저가 쿠키를 지원하는지 여부를 결정합니다.
feature: Dimensions
exl-id: 07d4fe12-0d60-469d-98b1-e93ce5a0fd21
TQID: https://experienceleague.adobe.com/axOR-Ut8kkRSCTYPescoSCa44g25E8xxp4gg-yQlyYw
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
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
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 38%
---
# 쿠키 지원

&#39;쿠키 지원&#39; [차원](overview.md)은(는) 브라우저가 지정된 히트에 대한 쿠키를 지원하는지 여부를 보고합니다. 쿠키를 지원하는 브라우저를 사용하는 방문자와 쿠키를 의도적으로 비활성화하는 방문자의 비율을 파악하는 것이 유용합니다.

## 이 차원을 데이터로 채우기

쿠키 지원은 자동으로 수집되며 클라이언트측: AppMeasurement은 이름이 `s_cc`인 쿠키를 설정한 다음 존재 여부를 보고합니다. 브라우저가 쿠키를 지원하고 활성화되어 있는 경우 `Y`, 쿠키가 비활성화되어 있는 경우 `N`. AppMeasurement 또는 Web SDK(태그) 구현에서 즉시 작동하며 설정할 변수가 없습니다. AppMeasurement 또는 Web SDK 외부의 데이터를 수집하는 경우(API 등을 통해) 각 히트에서 `Y` 또는 `N`을(를) 보냅니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(자동 수집됨) |
| **웹 SDK/XDM 필드** | 없음(자동 수집됨) |
| **쿼리 매개 변수** | [`k`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<cookiesEnabled>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 1바이트 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

차원 항목은 `Enabled`, `Disabled` 및 `Unknown`을 포함합니다.

* **`Enabled`**: 브라우저가 쿠키를 지원하고 브라우저에 쿠키가 활성화되어 있습니다.
* **`Disabled`**: 브라우저가 쿠키를 지원하지 않거나 방문자가 쿠키를 비활성화했습니다.
* **`Unknown`**: AppMeasurement가 쿠키 지원을 확인할 수 없습니다. 이미지 요청에 `k` 쿼리 문자열이 없습니다.
