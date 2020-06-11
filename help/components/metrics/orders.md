---
title: 주문
description: 구매한 횟수.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---


# 주문

&#39;주문 수&#39; 지표는 사이트에서 발생한 총 구매 이벤트 수를 보여줍니다. 이 지표는 eCommerce 사이트에서 전환을 측정하는 데 중요합니다. 이 지표를 모든 차원과 결합하여 어느 차원 값이 주문에 기여했는지 확인할 수 있습니다. 예를 들어, 구매에 기여한 상위 캠페인( [추적 코드](../dimensions/tracking-code.md) 차원 사용) 또는 상위 내부 검색어(eVar 사용) [를](../dimensions/evar.md)볼 수 있습니다.

## 이 지표의 계산 방법

이 지표는 변수에 `purchase` 존재하는 히트 수를 [`events`](/help/implement/vars/page-vars/events/events-overview.md) 계산합니다.
