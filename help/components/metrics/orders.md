---
title: 주문
description: 구매한 횟수입니다.
feature: Metrics
exl-id: b05abb6d-983f-43fe-80ad-a0ddf90de466
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 84%

---

# 주문

&#39;주문&#39; [지표](overview.md)은(는) 사이트에서 수행된 총 구매 이벤트 수를 보여줍니다. 이 지표는 eCommerce 사이트에서 전환을 측정하는 데 필수적입니다. 이 지표를 임의의 차원과 결합하여 주문에 기여한 차원 항목을 확인할 수 있습니다. 예를 들어 구매에 기여한 상위 캠페인 ([추적 코드](../dimensions/tracking-code.md) 차원 사용)이나 상위 내부 검색어 ([eVar](../dimensions/evar.md) 사용)를 볼 수 있습니다.

## 이 지표의 계산 방법

이 지표는 [`events`](/help/implement/vars/page-vars/events/events-overview.md) 변수에 `purchase`이 존재하는 히트 수를 계산합니다.
