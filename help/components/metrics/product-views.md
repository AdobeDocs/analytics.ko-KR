---
title: 제품 보기
description: 제품 페이지를 본 횟수입니다.
feature: Metrics
exl-id: 6217391d-8b42-4fdf-b05e-b9b117598ad2
source-git-commit: eb13c3e828bc6d4c547f4529ee7a15182bbbf046
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 88%

---

# 제품 보기

제품 보기 지표는 제품을 본 횟수를 보여줍니다. 이 지표는 가장 많이 본 제품을 보거나 시간에 따른 총 제품 보기 횟수의 트렌드를 알려는 경우에 유용합니다.

## 이 지표의 계산 방법

이 지표는 다음 중 **하나**&#x200B;와 일치하는 히트의 수를 계산합니다.

* 값 `prodView`가 [`events`](/help/implement/vars/page-vars/events/events-overview.md) 변수에 존재합니다. 또는
* 다음 [`products`](/help/implement/vars/page-vars/products.md) 변수가 설정되어 있고 `events` 변수가 비어 있습니다.
