---
title: Java 활성화
description: 브라우저에서 Java가 활성화되어 있는지 여부를 결정합니다.
feature: Dimensions
exl-id: 2d4b4ea2-65ba-4d39-a040-f989b5eddc6e
TQID: https://experienceleague.adobe.com/EjiqmqpByH-q9AL-934s5HXAv78JTXpEJZ1Bwk-y5MI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
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
source-wordcount: '249'
ht-degree: 51%
---
# Java 활성화

Java 활성화&#39; [차원](overview.md)은(는) 현재 브라우저에 Java가 활성화되어 있는지 여부를 결정합니다. 사이트에 Java 기반 기능을 도입하고 Java가 이미 활성화된 방문자의 수를 알고 싶은 경우 유용합니다. Java를 비활성화한 사용자를 위해 활성화 방법에 대한 지침이나 대안을 제공할 수 있습니다.

## 이 차원을 데이터로 채우기

Java 활성화 기능은 자동으로 수집되며, 클라이언트측: AppMeasurement은 브라우저에서 Java가 활성화되었는지 여부를 감지하고 &quot;Y&quot; 또는 &quot;N&quot;을 보고합니다. AppMeasurement 또는 Web SDK(태그) 구현에서 즉시 작동하며 설정할 변수가 없습니다. AppMeasurement 또는 웹 SDK 외부의 데이터를 수집하는 경우(API 등을 통해)에는 &quot;Y&quot; 또는 &quot;N&quot;을 보내 이 차원을 사용합니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(자동 수집됨) |
| **웹 SDK/XDM 필드** | 없음(자동 수집됨) |
| **쿼리 매개 변수** | [`v`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<javaEnabled>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 1바이트 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

차원 항목은 &quot;활성화됨&quot;, &quot;비활성화됨&quot; 및 &quot;알 수 없음&quot;을 포함합니다.

* **활성화됨**: 브라우저에 Java가 활성화되어 있습니다. `v` 쿼리 문자열이 값 &quot;Y&quot;를 포함했습니다.
* **비활성화됨**: 브라우저에 Java가 비활성화되어 있거나 Java가 지원되지 않습니다. `v` 쿼리 문자열이 값 &quot;N&quot;를 포함했습니다.
* **알 수 없음**: AppMeasurement에서 Java 지원을 확인할 수 없습니다. 이미지 요청에 `v` 쿼리 문자열이 없습니다.
