---
description: products 변수는 제품 및 제품 카테고리를 추적하는 데 사용됩니다(구매 수량 및 구매 가격도 추적).
keywords: Analytics 구현;products 변수;제품 보기;성공 이벤트
seo-description: products 변수는 제품 및 제품 카테고리를 추적하는 데 사용됩니다(구매 수량 및 구매 가격도 추적).
seo-title: 자세한 제품 보기 페이지
solution: Analytics
title: 자세한 제품 보기 페이지
topic: 개발자 및 구현
uuid: 464c9daf-b042-4fb8-8ca6-e104c0bcef45
translation-type: tm+mt
source-git-commit: 656fb909447ed079fa42a909a9c197296c9e2723

---


# 자세한 제품 보기 페이지

products 변수는 제품 및 제품 카테고리를 추적하는 데 사용됩니다(구매 수량 및 구매 가격도 추적).

성공 이벤트는 항상 *`products`* 변수와 함께 설정해야 합니다.

```js
s.events="prodView"
```

>[!NOTE]
>
>*`prodView`*&#x200B;는 구현에서 이벤트처럼 처리되지만, 인터페이스에서 동일하게 유연하지는 않습니다. 이벤트 *`prodView`*는 제품의 인스턴스이며, *`products`* 보고서에서만 사용할 수 있습니다. *`prodView`* 이벤트 이외에도 *`custom`* 이벤트를 사용하는 것이 좋습니다. 이렇게 하면, 다른 전환 보고서에서 다른 지표와 함께 제품 보기 지표를 볼 수 있습니다.

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
s.products=";SKU" 
```

## 확인 페이지 {#section_E006943CD5FD42358086581CA44B9660}

```js
s.events="purchase" 
s.products=";SKU" 
```

>[!NOTE]
>
>제품 문자열에서 SKU를 사용하면 *`products`* 보고서의 가독성이 떨어지지만 이후에 제품을 분류할 때 최대한의 유연성을 제공합니다. SKU에서, 완료, 제조업체, 카테고리 및 하위 카테고리를 가리키는 카테고리를 만들 수 있습니다.

When the *`products`* 변수가 *`purchase`* 이벤트와 함께 설정되면, 구매 수량과 총 구매 가격이 위와 같이 제품 값에 포함됩니다.
