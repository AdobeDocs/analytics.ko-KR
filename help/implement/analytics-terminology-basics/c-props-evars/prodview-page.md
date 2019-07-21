---
description: products 변수는 제품 및 제품 카테고리를 추적하는 데 사용됩니다(구매 수량 및 구매 가격도 추적).
keywords: Analytics 구현; products 변수; 제품 보기; 성공 이벤트
seo-description: products 변수는 제품 및 제품 카테고리를 추적하는 데 사용됩니다(구매 수량 및 구매 가격도 추적).
seo-title: 자세한 제품 보기 페이지
solution: Analytics
title: 자세한 제품 보기 페이지
topic: 개발자 및 구현
uuid: 464 c 9 DAF-B 042-4 FB 8-8 CA 6-E 104 C 0 BCEF 45
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 자세한 제품 보기 페이지

products 변수는 제품 및 제품 카테고리를 추적하는 데 사용됩니다(구매 수량 및 구매 가격도 추적).

A success event should always be set in conjunction with the *`products`* variable.

```js
s.events="prodView"
```

>[!NOTE]
>
>While *`prodView`* is treated in implementation like an event, it does not have the same flexibility in the interface. The *`prodView`*event is an instance of the product and is only available in the *`products`* report. Adobe recommends you use a *`custom`* event in addition to the *`prodView`* event. 이렇게 하면, 다른 전환 보고서에서 다른 지표와 함께 제품 보기 지표를 볼 수 있습니다.

```js
s.products=";diamond earrings (54321)"
```

>[!NOTE]
>
>제품 문자열 구문은 세미콜론으로 시작해야 합니다. 이것은 기존 구문 요구 사항으로서, 이전에는 카테고리 및 제품을 구분하는 데 사용되었습니다. 하지만 제품을 분류하는 방식을 변경하려는 경우 인터페이스 내에 제한이 생기므로 보고 시 유연성을 극대화하려면, 이 부분을 비워 두고 분류를 사용하여 카테고리를 설정하는 것이 가장 좋습니다.

## 장바구니 페이지(scOpen, scAdd, scRemove ) {#section_469B64F4150149DFB6B2C731279C0BC7}

```js
s.events="scOpen,scAdd" 
s.products=";SKU" 
```

## 첫 번째 체크아웃 페이지 {#section_E15607A9AECB44F79631926C853CF64E}

```js
s.events="scCheckout" 
s.products=”;SKU" 
```

## 확인 페이지 {#section_E006943CD5FD42358086581CA44B9660}

```js
s.events="purchase" 
s.products=";SKU" 
```

>[!NOTE]
>
>While using the SKU in the product string may make the *`products`* report less readable, it provides the maximum flexibility later when you want to classify your products. SKU에서, 완료, 제조업체, 카테고리 및 하위 카테고리를 가리키는 카테고리를 만들 수 있습니다.

when the *`products`* 변수가 *`purchase`* 이벤트와 함께 설정되면, 위에 표시된 것처럼 구매 수량과 총 구매 가격이 제품 값에 포함됩니다.
