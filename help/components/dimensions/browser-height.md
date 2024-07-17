---
title: 브라우저 높이 - 전체기간
description: 브라우저 창의 높이(픽셀 단위)입니다.
feature: Dimensions
exl-id: bdfd2ef5-c200-4d6e-b478-3917fca66227
source-git-commit: 2601b0e5c3fa78237ce693801b8dd8c95b853b81
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 87%

---

# 브라우저 높이

&#39;브라우저 높이 - 전체기간&#39; [차원](overview.md)은(는) 사전 정의된 그룹으로 분류된 브라우저 창의 높이를 보여줍니다. 이 차원은 방문자에 대한 사이트에서 폴드 (fold)가 있는 위치를 알려 할 때 유용합니다. 폴드 위치를 알면 콘텐츠를 보는 데 최적화할 수 있습니다.

이 차원은 화면 높이와 다릅니다. 브라우저 높이는 볼 수 있는 브라우저 공간 내의 픽셀 수이며 화면 높이는 전체 모니터 높이(픽셀 단위)입니다. 컴퓨터에서 이러한 두 변수 간의 차이점을 보려면 브라우저 콘솔 (대부분의 브라우저에서 F12)을 열고 다음 코드를 콘솔에 복사하여 붙여넣습니다.

```javascript
console.log(`Browser height: ${window.innerHeight} pixels\nScreen height: ${screen.height} pixels`);
```

브라우저 높이는 브라우저 탐색 영역이나 테두리가 포함되지 않으므로 항상 화면 높이보다 작거나 같습니다.

## 이 차원을 데이터로 채우기

이 차원은 이미지 요청의 [`bh` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 검색합니다. AppMeasurement는 브라우저에서 JavaScript 변수 `window.innerHeight`를 사용하여 이 데이터를 수집합니다. AppMeasurement 라이브러리를 사용하는 경우(Adobe Experience Platform의 태그 등을 통해) 이 차원은 즉시 작동합니다. AppMeasurement 외부의 데이터 수집 방법을 사용하는 경우 (API 등을 통해)에는 각 방문의 첫 번째 히트에서 `bh` 쿼리 문자열 매개 변수를 포함해야 합니다.

Adobe는 방문에 대해 브라우저 높이를 유지합니다. 브라우저 높이를 중간에 조정하면 조정이 기록되지 않습니다.

## 차원 항목

Dimension 항목에는 사전 정의된 그룹으로 분류된 수집된 모든 브라우저 높이가 포함됩니다. 예를 들어 히트의 브라우저 높이가 `720`이라면 차원 항목 `700 to 799`로 그룹화됩니다.
