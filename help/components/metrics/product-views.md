---
title: 제품 보기
description: 제품 페이지에 대한 보기 수입니다.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# 제품 보기

&#39;제품 보기 횟수&#39; 지표는 제품을 본 횟수를 보여줍니다. 이 지표는 가장 많이 본 제품을 보거나 시간에 따른 총 제품 보기 트렌드의 트렌드를 확인하려는 경우에 유용합니다.

## 이 지표의 계산 방법

이 지표는 다음 중 하나 **와** 일치하는 히트 수를 계산합니다.

* 이 값 `prodView` 은 변수에 [`events`](/help/implement/vars/page-vars/events/events-overview.md) 있습니다. or
* 변수가 [`products`](/help/implement/vars/page-vars/products.md) 설정되고 장바구니 이벤트가 변수에 `events` 존재하지 않습니다. 사용자 지정(`event1` -)이 아닌 이벤트 `event1000`는 장바구니 이벤트입니다.