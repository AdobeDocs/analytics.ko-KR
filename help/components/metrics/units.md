---
title: 판매량
description: 모든 주문 내에서 구매된 제품의 총 수입니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 87%

---


# 판매량

판매량 지표는 모든 주문 내에서 구매된 제품의 총 수를 보여줍니다. 이 지표는 eCommerce 사이트에서 전환을 측정하는 데 필수적입니다. 이 지표를 모든 차원과 결합하여 구매한 제품 수에 기여한 차원 항목을 확인할 수 있습니다. 예를 들어 구매된 제품 수에 기여한 상위 캠페인([추적 코드](../dimensions/tracking-code.md) 차원 사용)이나 상위 내부 검색어([eVar](../dimensions/evar.md) 사용)를 볼 수 있습니다.

## 이 지표의 계산 방법

[`events`](/help/implement/vars/page-vars/events/events-overview.md) 변수에 `purchase`가 존재하는 모든 히트에 대해 [`products`](/help/implement/vars/page-vars/products.md) 변수 내의 &#39;수량&#39; 필드를 합합니다.

## 주문과 판매량 비교

[주문](orders.md) 지표는 구매 이벤트의 수만 기록합니다. 판매량 지표는 고객이 두 개 이상의 제품을 구매할 수 있기 때문에 일반적으로 &#39;주문&#39;의 수치보다 높습니다. 이러한 경우 단일 주문이 여러 판매량으로 존재합니다.

주문이 판매량보다 높은 경우에는 구현에 결함이 없는지 확인하는 것이 좋습니다. 구매 시 `products` 변수가 올바로 설정되지 않을 수 있는데, 이렇게 되면 일반적으로 문제가 발생할 수 있습니다.
