---
title: 매출
description: 모든 주문 내에서 구매된 제품의 통화량입니다.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '113'
ht-degree: 100%

---


# 매출

매출 지표는 모든 주문 내에서 구매된 제품의 통화량을 보여줍니다. 이 지표는 eCommerce 사이트에서 전환을 측정하는 데 필수적입니다. 이 지표를 임의의 차원과 결합하여 매출에 기여한 차원 항목을 확인할 수 있습니다. 예를 들어 상위 캠페인([추적 코드](../dimensions/tracking-code.md) 차원 사용)이나 상위 내부 검색어([eVar](../dimensions/evar.md) 사용)를 볼 수 있습니다.

## 이 지표의 계산 방법

[`events`](/help/implement/vars/page-vars/events/event-purchase.md) 변수에 `purchase`가 존재하는 모든 히트에 대해 [`products`](/help/implement/vars/page-vars/products.md) 변수 내의 &#39;가격&#39; 필드를 합합니다.

이 지표는 페이지의 통화가 보고서 세트의 기본 통화와 다른 경우 [currencyCode](/help/implement/vars/config-vars/currencycode.md) 변수에 의존합니다.
