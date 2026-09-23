---
title: 확인된 상태
description: 결합에 대한 인식을 결정하는 플래그.
feature: Dimensions
exl-id: 8c6e9003-96f8-460f-a490-203f67be6337
TQID: https://experienceleague.adobe.com/JUBtgXBDboIgX0xbvuflF5q-oEwqHx4vKvJd0Y5XMLY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
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
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 46%
---
# 확인된 상태

&#39;확인된 상태&#39; [차원](overview.md)은(는) [크로스 디바이스 분석](../cda/overview.md)가상 보고서 세트와 관련이 있습니다. 보고서 실행 시 시스템에 의해 히트가 확인(결합)되거나 확인되지 않는 경우 이를 보고합니다. 이 차원은 CDA에서 데이터를 얼마나 잘 결합하는지 또는 &quot;압축&quot;하는지를 이해하는 데 도움이 됩니다.

## 이 차원을 데이터로 채우기

이 차원은 각 히트가 개인에 결합되었는지 여부에 따라 보고서를 실행할 때 [크로스 디바이스 분석](../cda/overview.md)에 의해 계산됩니다. Cross-Device Analytics가 가상 보고서 세트에 대해 구성되어 있으면 즉시 작동합니다. 설정할 변수가 없습니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(교차 장치 분석으로 계산) |
| **웹 SDK/XDM 필드** | 없음(교차 장치 분석으로 계산) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

차원 항목은 `"Identified"` 및 `"Unidentified"`를 포함합니다.

* **`"Identified"`**: 히트는 사용자에게 매핑됩니다.
* **`"Unidentified"`**: 히트는 사용자에게 매핑되지 않고 모든 기여도 방법에도 매핑될 수 없습니다.
