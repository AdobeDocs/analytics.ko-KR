---
title: 매출
description: 모든 주문 내에서 구매된 제품의 통화량입니다.
feature: Metrics
exl-id: a70e4d93-704b-46ac-9cec-31ea20d3dcb5
TQID: https://experienceleague.adobe.com/GJsQWf7h-TihzyNUN6e3VGzOUNyxYD1esuvXet5LM1c
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 74%

---

# 매출

&#39;매출&#39; [지표](overview.md)은(는) 모든 주문 내에서 구매된 제품의 통화량을 보여줍니다. 이 지표는 eCommerce 사이트에서 전환을 측정하는 데 필수적입니다. 이 지표를 임의의 차원과 결합하여 매출에 기여한 차원 항목을 확인할 수 있습니다. 예를 들어 상위 캠페인 ([추적 코드](../dimensions/tracking-code.md) 차원 사용)이나 상위 내부 검색어 ([eVar](../dimensions/evar.md) 사용)를 볼 수 있습니다.

## 이 지표의 계산 방법

[`events`](/help/implement/vars/page-vars/events/event-purchase.md) 변수에 `purchase`가 존재하는 모든 히트에 대해 [`products`](/help/implement/vars/page-vars/products.md) 변수 내의 &#39;가격&#39; 필드를 합합니다.

이 지표는 페이지의 통화가 보고서 세트의 기본 통화와 다른 경우 [currencyCode](/help/implement/vars/config-vars/currencycode.md) 변수에 의존합니다.
