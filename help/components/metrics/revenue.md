---
title: '수입 '
description: 모든 주문 내에서 구매한 제품의 금액
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---


# 수입 

&#39;매출&#39; 지표는 모든 주문 내에서 구매한 제품의 금액을 보여줍니다. 이 지표는 eCommerce 사이트에서 전환을 측정하는 데 중요합니다. 이 지표를 모든 차원과 결합하여 매출에 기여한 차원 값을 확인할 수 있습니다. 예를 들어 상위 캠페인( [추적 코드](../dimensions/tracking-code.md) 차원 사용) 또는 상위 내부 검색어(eVar 사용)를 [볼 수](../dimensions/evar.md)있습니다.

## 이 지표의 계산 방법

변수에 `purchase` 존재하는 모든 히트에 [`events`](/help/implement/vars/page-vars/events/event-purchase.md) 대해 변수 내의 &#39;가격&#39; 필드를 [`products`](/help/implement/vars/page-vars/products.md) 합계합니다.

이 지표는 페이지의 통화가 보고서 세트의 기본 통화와 다른 경우 [currencyCode](/help/implement/vars/config-vars/currencycode.md) 변수에 의존합니다.
