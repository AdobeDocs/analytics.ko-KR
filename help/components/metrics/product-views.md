---
title: 제품 보기
description: 제품 페이지를 본 횟수입니다.
feature: Metrics
exl-id: 6217391d-8b42-4fdf-b05e-b9b117598ad2
TQID: https://experienceleague.adobe.com/bspBkiEAfkwBQwWV3-KoDKDRNGLogCKkSXvY2Cpyv-M
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f1f1a2d4-0976-4881-b091-c2bb8de7ffacid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 72%

---

# 제품 보기

&#39;제품 보기&#39; [지표](overview.md)은(는) 제품을 본 횟수를 보여줍니다. 이 지표는 가장 많이 본 제품을 보거나 시간에 따른 총 제품 보기 횟수의 트렌드를 알려는 경우에 유용합니다.

## 이 지표의 계산 방법

이 지표는 다음 중 **하나**&#x200B;와 일치하는 히트의 수를 계산합니다.

* 값 `prodView`가 [`events`](/help/implement/vars/page-vars/events/events-overview.md) 변수에 존재합니다. 또는
* [`products`](/help/implement/vars/page-vars/products.md) 변수가 설정되어 있고 `events` 변수가 비어 있습니다.
