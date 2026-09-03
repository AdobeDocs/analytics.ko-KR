---
title: 제품
description: 제품의 이름입니다.
feature: Dimensions
exl-id: 2649c200-4b0a-49a9-8592-9b9af72b91cf
TQID: https://experienceleague.adobe.com/SMFFeSTkQyQoSWNFc8qHJRxYkJQmiJoKd0v4rS6xRKc
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 142
ht-degree: 91%

---

# 제품

&#39;Product&#39; [차원](overview.md)은(는) 히트에서 제품 이름을 보고합니다. 이 차원은 `products` 변수를 사용하고 최상위 판매자나 가장 많이 본 항목과 같은 제품 관련 지표를 보려는 구현에 유용합니다. 사이트에 제품이 없을 경우 의도적으로 이 차원을 비워 둘 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 [`products`](/help/implement/vars/page-vars/products.md) 변수에 있는 문자열의 두 번째 부분을 참조합니다. 첫 번째 및 두 번째 세미콜론 (`;`) 사이의 문자가 이 차원을 채웁니다.

## 차원 항목

이 변수는 구현의 사용자 지정 문자열에 기반하므로 조직에서 차원 항목을 결정합니다. 제품에 대해 일관된 명명 규칙을 설정하는 것이 좋습니다. 제품을 다르게 그룹화하거나 보다 친숙한 이름을 제공하려는 경우 [분류](../classifications/classifications-overview.md)를 사용할 수 있습니다. Adobe에서는 &#39;제품&#39;과 &#39;분류&#39; 차원을 모두 사용할 것을 권장합니다.
