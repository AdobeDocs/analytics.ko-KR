---
title: 브라우저 너비 - 전체기간
description: 브라우저 창의 폭(픽셀 단위)입니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 88%

---


# 브라우저 너비

브라우저 너비 - 전체기간 차원은 100픽셀 그룹으로 분류된 브라우저 창의 너비를 보여줍니다. 이 차원은 방문자가 컨텐츠를 보는 너비를 이해하려 할 때 유용합니다. 일반적으로 컨텐츠가 보이는 너비를 이해하면 컨텐츠를 보는 데 최적화할 수 있습니다.

이 차원은 화면 너비와 다릅니다. 브라우저 너비는 볼 수 있는 브라우저 공간 내의 픽셀 수이며 화면 너비는 전체 모니터 너비(픽셀 단위)입니다. 컴퓨터에서 이러한 두 변수 간의 차이점을 보려면 브라우저 콘솔(대부분의 브라우저에서 F12)을 열고 다음 코드를 콘솔에 복사하여 붙여 넣습니다.

```javascript
"Browser width: " + window.innerWidth + " pixels\nScreen width: " + screen.width + " pixels";
```

브라우저 너비는 스크롤 막대나 테두리가 포함되지 않으므로 항상 화면 너비보다 작거나 같습니다.

## 이 차원을 데이터로 채우기

이 차원은 이미지 요청의 [`bw` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 검색합니다. AppMeasurement는 브라우저에서 JavaScript 변수 `window.innerWidth`를 사용하여 이 데이터를 수집합니다. AppMeasurement 라이브러리를 사용하는 경우(Adobe Experience Platform Launch 등을 통해) 이 차원은 즉시 작동합니다. AppMeasurement 외부의 데이터 수집 방법을 사용하는 경우(API 등을 통해)에는 각 방문의 첫 번째 히트에서 `bw` 쿼리 문자열 매개 변수를 포함해야 합니다.

Adobe는 방문에 대해 브라우저 너비를 유지합니다. 브라우저 너비를 중간에 조정하면 조정이 기록되지 않습니다.

## Dimension 항목

Dimension 항목에는 100픽셀 그룹으로 분류된 수집된 모든 브라우저 너비가 포함됩니다. For example, if the browser width of a hit is `1280`, then it is grouped in the dimension item `1200 to 1299`.
