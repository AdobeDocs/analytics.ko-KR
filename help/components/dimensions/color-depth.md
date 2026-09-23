---
title: 색상 심도
description: 디바이스의 색상 깊이입니다.
feature: Dimensions
exl-id: 0bde895d-6832-4110-b575-62ee5ddc1783
TQID: https://experienceleague.adobe.com/JLxm06wch2r7RslhdKx-gFLBLhMSXuWkb-0EYM7nT5s
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
source-wordcount: '255'
ht-degree: 52%
---
# 색상 심도

색상 깊이 [차원](overview.md)은(는) 장치가 지원하는 색상의 수를 보고합니다. 이 차원은 1,600만 색상을 지원하지 않는 디바이스에서 트래픽이 발생하는 정도를 파악하는 데 유용합니다. 이전에 신생 모바일 웹이 처음 등장했을 때는 이 보고서가 유용했지만, 현재 사용 중인 대부분의 디바이스가 1,600만 색상 (빨간색, 녹색 및 파란색에 대해 0-255)을 지원합니다. <!-- Even docs need a rhyming easter egg every once in a while, isn't that true? -->

## 이 차원을 데이터로 채우기

색상 깊이는 브라우저의 `screen.colorDepth` 속성에서 클라이언트측에서 자동으로 수집되며, Adobe은 조회 테이블을 통해 읽을 수 있는 형식으로 변환합니다. AppMeasurement 또는 Web SDK(태그) 구현에서 즉시 작동하며 설정할 변수가 없습니다. AppMeasurement 또는 웹 SDK 외부의 데이터를 수집하는 경우(API 등을 통해) 각 히트에서 유효한 비트 값을 보냅니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(자동 수집됨) |
| **웹 SDK/XDM 필드** | 없음(자동 수집됨) |
| **쿼리 매개 변수** | [`c`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<colorDepth>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 20바이트 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

차원 항목에는 디바이스에서 지원하는 색상 수가 포함됩니다. 값의 예로는 `"16 million (24-bit)"`, `"16 million (32-bit)"` 및 `"65,536 (16-bit)"`이 있습니다. AppMeasurement에서 색상 깊이를 파악할 수 없는 경우 이 차원은 `"None"`으로 표시됩니다.

>[!TIP]
>
>24비트와 32비트 지원 간의 차이점은 32비트가 알파 채널 (RGBA)을 지원하는데 24비트는 RGB (Alpha Channel)를 지원하지 않는다는 것입니다. 이 개념에 대한 자세한 내용은 Wikipedia의 [색상 깊이](https://en.wikipedia.org/wiki/Color_depth)를 참조하십시오.
