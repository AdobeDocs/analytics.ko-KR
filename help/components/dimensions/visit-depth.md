---
title: 방문 깊이
description: 방문의 깊이를 보고하는 방문 기반 차원입니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 57%

---


# 방문 깊이

방문 깊이 차원은 방문자가 전체 방문에서 본 페이지 보기의 수를 보고합니다. Visit depth increases only if the hit is a page view, and the [Page](page.md) dimension is not the same as the last page view&#39;s dimension item. 방문 기반 차원으로서, 이것은 전체 방문에 대해 동일한 값을 포함함을 의미합니다. 이 변수는 방문이 끝난 후 방문의 모든 히트에 대해 설정됩니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## Dimension 항목

Dimension items include the string `"Pages per visit"` followed by a number representing the number of pages in the visit. The dimension item of `"Pages per visit: 1"` represents a single-page visit, while the dimension item `"Pages per visit: 8"` represents a visit with 8 page views (and any number of link tracking calls).

## 히트 깊이와 비교

차원 간의 비교가 필요하면 [히트 깊이](hit-depth.md)를 참조하십시오.