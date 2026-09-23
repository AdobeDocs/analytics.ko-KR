---
title: 모니터 해상도
description: 방문자 모니터의 해상도(픽셀 단위)입니다.
feature: Dimensions
exl-id: 6bae65eb-4546-4d07-877d-6e257fbe6cfa
TQID: https://experienceleague.adobe.com/d3AuMT0seRbZpuKVGPeWo98Bkhc8tcJIP6gt4y-rq38
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
source-wordcount: '289'
ht-degree: 51%
---
# 모니터 해상도

&#39;모니터 해상도&#39; [차원](overview.md)은(는) 활성 디스플레이의 높이와 너비를 픽셀 단위로 표시합니다. 이 차원은 방문자에 대한 사이트에서 폴드 (fold)가 있는 위치나 방문자가 브라우저 창을 만들 수 있는 너비를 알려 할 때 유용합니다. 폴드 위치를 알면 콘텐츠를 보는 데 최적화할 수 있습니다.

이 차원은 브라우저 [높이](browser-height.md) 및 [너비](browser-width.md)와 다릅니다. 브라우저 높이/너비는 볼 수 있는 브라우저 공간 내의 픽셀 수인데 반해 모니터 해상도는 전체 모니터의 픽셀 수입니다. 컴퓨터에서 이러한 두 변수 간의 차이점을 보려면 브라우저 콘솔 (대부분의 브라우저에서 F12)을 열고 다음 코드를 콘솔에 복사하여 붙여넣습니다.

```js
"Monitor resolution: " + screen.width + "x" + screen.height + "; Browser resolution: " + window.innerWidth + "x" + window.innerHeight;
```

브라우저 차원은 브라우저 탐색 막대나 테두리를 포함하지 않으므로 항상 모니터 해상도보다 작습니다.

## 이 차원을 데이터로 채우기

모니터 해상도는 브라우저의 `screen.width` 및 `screen.height` 속성에서 클라이언트측에서 자동으로 수집됩니다. AppMeasurement 또는 Web SDK(태그) 구현에서 즉시 작동하며 설정할 변수가 없습니다. AppMeasurement 또는 Web SDK 외부의 데이터를 수집하는 경우(API 등을 통해) 이미지 요청에 값을 전송합니다. 이 데이터가 없거나 데이터 수집 라이브러리에서 모니터 해상도를 수집할 수 없는 경우 해당 데이터가 [!UICONTROL `Not Specified`] 아래에 나열됩니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(자동 수집됨) |
| **웹 SDK/XDM 필드** | 없음(자동 수집됨) |
| **쿼리 매개 변수** | [`s`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<resolution>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 20바이트 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

차원 항목에는 수집된 모든 모니터 해상도가 포함됩니다. 값의 예로는 `1920 x 1080`, `1366 x 768` 및 `1280 x 720`이 있습니다.
