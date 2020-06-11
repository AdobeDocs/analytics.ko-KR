---
title: 제품
description: 제품의 이름입니다.
translation-type: tm+mt
source-git-commit: bddfc52d460e87a70e7cff149f197570f405037a
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---


# 제품

&#39;제품&#39; 차원은 히트에서 제품 이름을 보고합니다. 이 변수는 변수를 사용하고 최상위 판매자나 가장 많이 본 제품 등의 지표를 보려는 구현에 유용합니다. `products` 사이트에 제품이 없을 경우 이 차원은 의도적으로 비어 있을 수 있습니다.

## 데이터로 이 차원 채우기

이 차원은 변수의 문자열 두 번째 부분을 [`products`](/help/implement/vars/page-vars/products.md) 참조합니다. 첫 번째 및 두 번째 세미콜론(`;`) 사이의 문자가 이 차원을 채웁니다.

## 차원 값

이 변수는 구현의 사용자 지정 문자열을 기반으로 하므로 조직에서 차원 값이 무엇인지 결정합니다. 제품에 대해 일관된 명명 규칙을 설정하는 것이 좋습니다. [제품을 다르게 그룹화하거나 보다 친숙한 이름을 제공하려는 경우 분류를](../c-classifications2/c-classifications.md) 사용할 수 있습니다. &#39;제품&#39; 및 &#39;카테고리&#39; 차원을 모두 사용하는 것이 좋습니다.
