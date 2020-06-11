---
title: 판매량
description: 모든 주문 내에서 구매한 총 제품 수.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# 판매량

&#39;판매량&#39; 지표는 모든 주문 내에서 구매한 총 제품 수를 보여줍니다. 이 지표는 eCommerce 사이트에서 전환을 측정하는 데 중요합니다. 이 지표를 모든 차원과 결합하여 구매한 제품 수에 기여한 차원 값을 확인할 수 있습니다. 예를 들어, 구매한 제품에 기여한 상위 캠페인( [추적 코드](../dimensions/tracking-code.md) 차원 사용) 또는 상위 내부 검색어( [eVar](../dimensions/evar.md)사용)를 볼 수 있습니다.

## 이 지표의 계산 방법

변수에 `purchase` 존재하는 모든 히트에 [`events`](/help/implement/vars/page-vars/events/events-overview.md) 대해 변수 내의 &#39;수량&#39; 필드를 [`products`](/help/implement/vars/page-vars/products.md) 합계합니다.

## 주문 및 판매량 비교

주문 [지표는](orders.md) 구매 이벤트 수만 기록합니다. 고객이 두 개 이상의 제품을 구매할 수 있기 때문에 &#39;판매량&#39; 지표는 일반적으로 &#39;주문 수&#39;보다 높습니다. 이러한 경우 단일 주문이 여러 단위로 존재합니다.

주문량이 판매량보다 높은 경우 구현의 무결성을 확인하는 것이 좋습니다. 일반적으로 원치 않는 행동인 구매 시 `products` 변수가 올바르게 설정되지 않을 수 있습니다.
