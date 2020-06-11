---
title: 브라우저 너비 - 버킷
description: 브라우저 창의 너비(픽셀 단위).
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# 브라우저 너비

&#39;Browser width - bucketed&#39; 차원은 100픽셀 그룹으로 분류된 브라우저 창의 너비를 표시합니다. 이 차원은 방문자가 컨텐츠를 보는 범위를 이해하려는 경우 유용합니다. 일반적으로 컨텐츠가 표시되는 범위를 이해하면 컨텐츠를 볼 수 있도록 최적화할 수 있습니다.

이 크기는 화면 너비와 다릅니다. Browser width는 볼 수 있는 브라우저 공간 내의 픽셀 수이며 화면 너비는 전체 모니터 너비(픽셀)입니다. 사용자 시스템에서 이러한 두 변수 간의 차이점을 보려면 브라우저 콘솔(대부분의 브라우저에서 F12)을 열고 다음 코드를 콘솔에 복사하여 붙여 넣습니다.

```javascript
"Browser width: " + window.innerWidth + " pixels\nScreen width: " + screen.width + " pixels";
```

브라우저 너비는 스크롤 막대 또는 테두리가 포함되지 않으므로 항상 화면 너비보다 작거나 같습니다.

## 데이터로 이 차원 채우기

이 차원은 이미지 요청의 [`bw` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 검색합니다. AppMeasurement는 브라우저에서 JavaScript 변수를 사용하여 이 데이터 `window.innerWidth` 를 수집합니다. AppMeasurement 라이브러리(예: Adobe Experience Platform Launch)를 사용하는 경우 이 차원은 기본적으로 작동합니다. AppMeasurement 외부(예: API를 통해) 데이터 수집 메서드를 사용하는 경우 각 방문의 첫 번째 히트에 `bw` 쿼리 문자열 매개 변수를 포함해야 합니다.

Adobe는 방문에 대해 브라우저 너비를 유지합니다. 브라우저 너비를 중간에 조정하면 조정이 기록되지 않습니다.

## 차원 값

차원 값에는 100픽셀 그룹으로 분류된 수집된 모든 브라우저 너비가 포함됩니다. 예를 들어 히트의 브라우저 너비가 있는 경우, `1280`차원 값으로 그룹화됩니다 `1200 to 1299`.
