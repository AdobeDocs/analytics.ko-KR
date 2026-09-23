---
title: 브라우저 너비 - 전체기간
description: 브라우저 창의 폭(픽셀 단위)입니다.
feature: Dimensions
exl-id: f0cb28b6-260b-4c3d-bbf8-17fae7ef22a0
TQID: https://experienceleague.adobe.com/f9AknIwL-9ZMJ8tnGMxpUNmlkQiFmbjI3gtlP3KZtSQ
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
source-wordcount: '318'
ht-degree: 45%
---
# 브라우저 폭

&#39;브라우저 너비 - 전체기간&#39; [차원](overview.md)은(는) 사전 정의된 그룹으로 분류된 브라우저 창의 너비를 표시합니다. 이 차원은 방문자가 콘텐츠를 얼마나 넓게 보는지 이해하려 할 때 유용합니다. 일반적으로 콘텐츠가 표시되는 너비를 이해하면 해당 콘텐츠를 최적화할 수 있습니다.

이 차원은 화면 너비와 다릅니다. 브라우저 너비는 볼 수 있는 브라우저 공간 내의 픽셀 수이며 화면 너비는 전체 모니터 너비(픽셀 단위)입니다. 컴퓨터에서 이러한 두 변수 간의 차이점을 보려면 브라우저 콘솔(대부분의 브라우저에서 F12)을 열고 다음 코드를 콘솔에 복사하여 붙여넣습니다.

```javascript
console.log(`Browser width: ${window.innerWidth} pixels\nScreen width: ${screen.width} pixels`);
```

브라우저 너비는 스크롤 막대나 테두리가 포함되지 않으므로 항상 화면 너비보다 작거나 같습니다.

>[!NOTE]
>
>Data Warehouse은 값을 사전 정의된 버킷으로 그룹화하는 대신 정확한 픽셀 너비를 보고하는 &#39;[!UICONTROL 브라우저 너비 - 세부기간]&#39; 차원도 제공합니다.

## 이 차원을 데이터로 채우기

브라우저 너비는 브라우저의 `window.innerWidth` 속성에서 클라이언트측에서 자동으로 수집됩니다. AppMeasurement 또는 Web SDK(태그) 구현에서 즉시 작동하며 설정할 변수가 없습니다. AppMeasurement 또는 웹 SDK 외부의 데이터를 수집하는 경우(API 등을 통해)에는 각 방문의 첫 번째 히트에서 값을 보냅니다. 브라우저 너비를 중간에 조정하면 조정이 기록되지 않습니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(자동 수집됨) |
| **웹 SDK/XDM 필드** | 없음(자동 수집됨) |
| **쿼리 매개 변수** | [`bw`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<browserWidth>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **값 범위** | 0-65,535 |
| **지속성** | 방문 |

## 차원 항목

Dimension 항목에는 사전 정의된 그룹으로 분류된 수집된 모든 브라우저 너비가 포함됩니다. 예를 들어 히트의 브라우저 너비가 `1280`이라면 차원 항목 `1200 to 1299`로 그룹화됩니다.
