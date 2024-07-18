---
title: 모니터 해상도
description: 방문자 모니터의 해상도(픽셀 단위)입니다.
feature: Dimensions
exl-id: 6bae65eb-4546-4d07-877d-6e257fbe6cfa
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 93%

---

# 모니터 해상도

&#39;모니터 해상도&#39; [차원](overview.md)은(는) 활성 디스플레이의 높이와 너비를 픽셀 단위로 표시합니다. 이 차원은 방문자에 대한 사이트에서 폴드 (fold)가 있는 위치나 방문자가 브라우저 창을 만들 수 있는 너비를 알려 할 때 유용합니다. 폴드 위치를 알면 콘텐츠를 보는 데 최적화할 수 있습니다.

이 차원은 브라우저 높이 및 너비와 다릅니다. 브라우저 높이/너비는 볼 수 있는 브라우저 공간 내의 픽셀 수인데 반해 모니터 해상도는 전체 모니터의 픽셀 수입니다. 컴퓨터에서 이러한 두 변수 간의 차이점을 보려면 브라우저 콘솔 (대부분의 브라우저에서 F12)을 열고 다음 코드를 콘솔에 복사하여 붙여넣습니다.

```js
"Monitor resolution: " + screen.width + "x" + screen.height + "\nBrowser resolution: " + window.innerWidth + "x" + window.innerHeight;
```

브라우저 차원은 브라우저 탐색 막대나 테두리를 포함하지 않으므로 항상 모니터 해상도보다 작습니다.

## 이 차원을 데이터로 채우기

이 차원은 이미지 요청의 [`s` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 검색합니다. AppMeasurement는 브라우저에서 JavaScript 변수 `screen.width` 및 `screen.height`를 사용하여 이 데이터를 수집합니다. AppMeasurement 라이브러리를 사용하는 경우(Adobe Experience Platform의 태그 등을 통해) 이 차원은 즉시 작동합니다. AppMeasurement 외부의 데이터 수집 방법을 사용하는 경우 (API 등을 통해)에는 이미지 요청에 `s` 쿼리 문자열 매개 변수를 포함해야 합니다.

## 차원 항목

차원 항목에는 수집된 모든 모니터 해상도가 포함됩니다. 값의 예로는 `1920 x 1080`, `1366 x 768` 및 `1280 x 720`이 있습니다.
