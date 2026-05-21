---
title: 카테고리
description: 히트의 제품 카테고리입니다.
feature: Dimensions
exl-id: 3517b417-1a44-4d3e-ac16-93fdc5f36404
TQID: https://experienceleague.adobe.com/3G1qDbtVnRj8At-FU1fNaI8KLboMQvo8NKktinrTbs8
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 93%

---

# 카테고리

&#39;범주&#39; [차원](overview.md)은(는) 히트의 제품 범주를 보고합니다. 이 차원은 `products` 변수를 사용하고 최상위 판매자나 가장 많이 본 항목과 같은 제품 카테고리 관련 지표를 보려는 구현에 유용합니다. 사이트에 제품이 없을 경우 의도적으로 이 차원을 비워 둘 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 [`products`](/help/implement/vars/page-vars/products.md) 변수에 있는 문자열의 첫 부분을 참조합니다. 첫 번째 세미콜론 (`;`) 앞의 모든 내용이 이 차원을 채웁니다.

## 차원 항목

이 변수는 구현의 사용자 지정 문자열에 기반하므로 조직에서 차원 항목을 결정합니다. 제품과 카테고리 차원을 모두 사용하여 개별 제품을 의미 있는 카테고리로 그룹화하는 것이 좋습니다.

>[!TIP]
>
>이전 버전의 Adobe Analytics에서는 처리 아키텍처로 인해 &#39;카테고리&#39; 차원에 일부 제한 사항이 적용되었습니다. 이러한 제한 사항은 이후에 제거되어 이제는 모든 지표와 분류를 사용할 수 있습니다.
