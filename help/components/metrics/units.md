---
title: 판매량
description: 모든 주문 내에서 구매된 제품의 총 수입니다.
feature: Metrics
exl-id: c7293445-0760-4237-83ae-812224ca6f4b
TQID: https://experienceleague.adobe.com/0v4pF0Iv0IzU9K4CQiTy1-IIYgMCaO37E6QTmAAEPXc
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f1f1a2d4-0976-4881-b091-c2bb8de7ffacid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 173
ht-degree: 80%

---

# 판매량

&#39;Units&#39; [metric](overview.md)은(는) 모든 주문 내에서 구매된 제품의 총 수를 보여줍니다. 이 지표는 eCommerce 사이트에서 전환을 측정하는 데 필수적입니다. 이 지표를 임의의 차원과 결합하여 구매된 제품 수에 기여한 차원 항목을 확인할 수 있습니다. 예를 들어 구매된 제품 수에 기여한 상위 캠페인 ([추적 코드](../dimensions/tracking-code.md) 차원 사용)이나 상위 내부 검색어 ([eVar](../dimensions/evar.md) 사용)를 볼 수 있습니다.

## 이 지표의 계산 방법

[`events`](/help/implement/vars/page-vars/events/events-overview.md) 변수에 `purchase`가 존재하는 모든 히트에 대해 [`products`](/help/implement/vars/page-vars/products.md) 변수 내의 &#39;수량&#39; 필드를 합합니다.

## 주문과 판매량 비교

[주문](orders.md) 지표는 구매 이벤트의 수만 기록합니다. 판매량 지표는 고객이 두 개 이상의 제품을 구매할 수 있기 때문에 일반적으로 &#39;주문&#39;의 수치보다 높습니다. 이러한 경우 단일 주문이 여러 판매량으로 존재합니다.

주문이 판매량보다 높은 경우에는 구현에 결함이 없는지 확인하는 것이 좋습니다. 구매 시 `products` 변수가 올바로 설정되지 않을 수 있는데, 이렇게 되면 일반적으로 문제가 발생할 수 있습니다.
