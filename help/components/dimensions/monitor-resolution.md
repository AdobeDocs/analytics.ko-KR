---
title: 모니터 해상도
description: 방문자 모니터의 해상도(픽셀 단위)
translation-type: tm+mt
source-git-commit: ad206649488a1a2dead717cdfe53f4c630ba3f3b
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 1%

---


# 모니터 해상도

&#39;모니터 해상도&#39; 차원은 활성 디스플레이의 높이와 너비를 픽셀 단위로 보여줍니다. 이 차원은 사이트에서 방문자에게 &quot;접힘&quot;이 있는 위치 또는 방문자가 브라우저 창을 만드는 방법을 이해하려는 경우 유용합니다. 접힌 부분을 이해하면 컨텐츠를 볼 수 있도록 최적화할 수 있습니다.

이 크기는 브라우저 높이 및 너비와 다릅니다. 브라우저 높이/너비는 볼 수 있는 브라우저 공간 내의 픽셀 수이며 모니터 해상도는 전체 모니터의 픽셀 수입니다. 사용자 시스템에서 이러한 두 변수 간의 차이점을 보려면 브라우저 콘솔(대부분의 브라우저에서 F12)을 열고 다음 코드를 콘솔에 복사하여 붙여 넣습니다.

```js
"Monitor resolution: " + screen.width + "x" + screen.height + "\nBrowser resolution: " + window.innerWidth + "x" + window.innerHeight;
```

브라우저 크기는 브라우저 탐색이나 테두리를 포함하지 않으므로 브라우저 크기는 항상 모니터 해상도보다 작습니다.

## 데이터로 이 차원 채우기

이 차원은 이미지 요청의 [`s` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 검색합니다. AppMeasurement는 JavaScript 변수 `screen.width` 및 브라우저에서 이 데이터 `screen.height` 를 수집합니다. AppMeasurement 라이브러리(예: Adobe Experience Platform Launch)를 사용하는 경우 이 차원은 기본적으로 작동합니다. API를 통해 AppMeasurement 외부에 데이터 수집 메서드를 사용하는 경우 이미지 요청에 `s` 쿼리 문자열 매개 변수를 포함해야 합니다.

## 차원 값

차원 값에는 수집된 모든 모니터 해상도가 포함됩니다. 예제 값에는 `1920 x 1080`, `1366 x 768`및 `1280 x 720`.
