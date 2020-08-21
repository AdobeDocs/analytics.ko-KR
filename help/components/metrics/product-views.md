---
title: 제품 보기
description: 제품 페이지를 본 횟수입니다.
translation-type: ht
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: ht
source-wordcount: '94'
ht-degree: 100%

---


# 제품 보기

제품 보기 지표는 제품을 본 횟수를 보여줍니다. 이 지표는 가장 많이 본 제품을 보거나 시간에 따른 총 제품 보기 횟수의 트렌드를 알려는 경우에 유용합니다.

## 이 지표의 계산 방법

이 지표는 다음 중 **하나**&#x200B;와 일치하는 히트의 수를 계산합니다.

* 값 `prodView`가 [`events`](/help/implement/vars/page-vars/events/events-overview.md) 변수에 존재합니다. 또는
* [`products`](/help/implement/vars/page-vars/products.md) 변수가 설정되어 있고 장바구니 이벤트가 `events` 변수에 존재하지 않습니다. 사용자 지정(`event1` - `event1000`)이 아닌 모든 이벤트는 장바구니 이벤트입니다.