---
title: 제품
description: 제품의 이름입니다.
translation-type: ht
source-git-commit: cd2225ec00190af6b616f313b419935c4f8dfafd
workflow-type: ht
source-wordcount: '142'
ht-degree: 100%

---


# 제품

제품 차원은 히트에 있는 제품 이름을 보고합니다. 이 차원은 `products` 변수를 사용하고 최상위 판매자나 가장 많이 본 항목과 같은 제품 관련 지표를 보려는 구현에 유용합니다. 사이트에 제품이 없을 경우 의도적으로 이 차원을 비워 둘 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 [`products`](/help/implement/vars/page-vars/products.md) 변수에 있는 문자열의 두 번째 부분을 참조합니다. 첫 번째 및 두 번째 세미콜론(`;`) 사이의 문자가 이 차원을 채웁니다.

## 차원 항목

이 변수는 구현의 사용자 지정 문자열에 기반하므로 조직에서 차원 항목을 결정합니다. 제품에 대해 일관된 명명 규칙을 설정하는 것이 좋습니다. 제품을 다르게 그룹화하거나 보다 친숙한 이름을 제공하려는 경우 [분류](../classifications/c-classifications.md)를 사용할 수 있습니다. Adobe에서는 &#39;제품&#39;과 &#39;분류&#39; 차원을 모두 사용할 것을 권장합니다.
