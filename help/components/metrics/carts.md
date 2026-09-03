---
title: 장바구니
description: 방문자가 장바구니에 첫 번째 제품을 추가한 히트의 수입니다.
feature: Metrics
exl-id: 890bbaba-0140-4995-bbd2-c69aedc801e5
TQID: https://experienceleague.adobe.com/a-qT5Ly8-4mSBGbGTAzbwLIMRFZtqotMPvGFgOrM41Y
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
source-wordcount: 162
ht-degree: 45%

---

# 장바구니

장바구니 수 [지표](overview.md)은(는) 방문자가 장바구니에 첫 번째 제품을 추가한 히트의 수를 보여줍니다.

## 이 지표의 계산 방법

이 지표는 [`events`](/help/implement/vars/page-vars/events/events-overview.md) 변수에 `scOpen`이 존재하는 히트 수를 계산합니다.

## 장바구니 수, 장바구니 보기 수 및 장바구니 추가 수 간의 차이

장바구니 수, 장바구니 보기 및 장바구니 추가는 구현이 필요한 이벤트이므로, 조직에서 이러한 지표 간의 정확한 차이를 결정합니다. 하지만 Adobe은 다음 논리를 위해 이러한 지표를 설계했습니다.

* 장바구니 수는 방문자가 장바구니에 첫 제품을 추가할 때 구매당 한 번만 트리거됩니다.
* 장바구니 보기 수는 방문자가 장바구니를 볼 때마다 트리거됩니다.
* 장바구니 추가는 장바구니에 추가한 모든 제품에 대해 트리거됩니다.

고객이 장바구니에 첫 번째 제품을 추가할 때 의도한 동작은 &#39;장바구니&#39;와 &#39;장바구니 추가&#39;가 모두 트리거되는 것입니다. 이러한 지침은 구체적이지 않으므로 이때에도 조직에서 정확한 구현 논리를 결정합니다.
