---
title: products
description: 표시되는 제품 또는 장바구니에 표시되는 데이터를 전송합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# products

이 `products` 변수는 제품과 연결된 속성을 추적합니다. 이 변수는 일반적으로 개별 제품 페이지, 장바구니 페이지 및 구매 확인 페이지에서 설정됩니다. 다중 값 변수입니다. 즉, 동일한 히트에서 여러 제품을 보내고 Adobe가 값을 별도의 차원 값으로 구문 분석할 수 있습니다.

> [!NOTE] 이 변수가 [`events`](events/events-overview.md) 변수의 장바구니 이벤트 없이 히트에 설정되면 &#39;제품 보기&#39; 지표가 1씩 증가합니다. 각 히트에서 적절한 장바구니 이벤트를 설정해야 합니다.

## Adobe Experience Platform Launch의 제품

Launch에는 이 변수를 설정하는 전용 필드가 없습니다.그러나 도움이 필요한 타사 익스텐션이 여러 개 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 [!UICONTROL Extensions] [!UICONTROL Catalog] 이동한 다음 을 클릭하여 사용 가능한 모든 익스텐션을 확인합니다.
4. &quot;product&quot;라는 용어를 검색하면 이 변수를 설정하는 데 도움이 되는 여러 가지 익스텐션이 표시됩니다.

이러한 확장 기능 중 하나를 사용하거나 아래의 AppMeasurement 구문에 따라 사용자 지정 코드 편집기를 사용할 수 있습니다.

## s.products in AppMeasurement and Launch custom code editor

이 `s.products` 변수는 제품별로 구분된 여러 필드를 포함하는 문자열입니다. 각 개별 제품은 모든 필드에 최대 100바이트를 포함할 수 있습니다. 문자열에서 각 필드를 세미콜론(`;`)으로 구분합니다.

* **카테고리** (선택 사항):주요 제품 카테고리 조직은 제품을 카테고리로 그룹화하는 방법을 결정합니다.
* **제품 이름** (필수):제품의 이름입니다.
* **수량** (선택 사항):장바구니에 들어 있는 제품은 몇 개입니까? 이 필드는 구매 이벤트가 있는 히트에만 적용됩니다.
* **가격** (선택 사항):제품의 총 가격(소수)입니다. 수량이 두 개 이상인 경우 개별 제품 가격이 아닌 총계로 가격을 설정합니다. 이 값의 통화를 [`currencyCode`](../config-vars/currencycode.md) 변수와 일치하도록 정렬합니다. 이 필드에 통화 기호를 포함하지 마십시오. 이 필드는 구매 이벤트가 있는 히트에만 적용됩니다.
* **이벤트** (선택 사항):제품과 연결된 이벤트입니다. 파이프를 사용하여 여러 이벤트를 구분합니다(`|`). 자세한 내용은 [이벤트를](events/events-overview.md) 참조하십시오.
* **eVar** (선택 사항):제품과 연결된 머천다이징 eVar 파이프로 여러 머천다이징 eVar 구분(`|`). 자세한 내용은 [머천다이징 eVar](../../../components/c-variables/c-merch-variables/var-merchandising.md) 를 참조하십시오.

```js
// Set a single product using all available fields
s.products = "Example category;Example product;1;3.50;event1=4.99|event2=5.99;eVar1=Example merchandising value 1|eVar2=Example merchandising value 2";
```

이 변수는 동일한 히트에서 여러 제품을 지원합니다. 장바구니 및 여러 제품이 포함된 구매 시 유용합니다. 제품당 100바이트 제한이 있지만 `products` 변수의 전체 길이는 64K입니다. 각 제품을 문자열에 쉼표(`,`)로 구분합니다.

```js
// Set multiple products - useful for when a visitor views their shopping cart
s.products = "Example category 1;Example product 1;1;3.50,Example category 2;Example product 2,1,5.99";
```

> [!IMPORTANT] 제품 이름, 카테고리 및 머천다이징 eVar 값에서 모든 세미콜론, 쉼표 및 파이프를 제거하십시오. 제품 이름에 쉼표가 포함되어 있으면 AppMeasurement가 새 제품의 시작으로 구문 분석합니다. 이 부정확한 구문 분석은 제품 문자열의 나머지 부분에서 발생하여 차원 및 보고서에서 잘못된 데이터를 초래합니다.

## 예

이 `products` 변수는 필드를 생략하고 여러 제품을 포함할 때 유연합니다. 이러한 유연성을 통해 구분 기호를 쉽게 찾을 수 있으므로 구현에서 잘못된 데이터를 Adobe로 보낼 수 있습니다.

```js
// Include only product and category. Common on individual product pages
s.products = "Example category;Example product";

// Include only product name if you do not want to use product category
s.products = ";Example product";

// One product has a category, the other does not. Note the comma and adjacent semicolon to omit category
s.products = "Example category;Example product,;Example product";

// A visitor purchases a single product; record quantity and price
s.events = "purchase";
s.products = "Example category;Example product;1;6.99";

// A visitor purchases multiple products with different quantities
s.events = "purchase";
s.products = "Example category;Example product 1;9;26.91,Example category;Example product 2;4;9.96";

// Attribute currency event1 only to product 2 and not product 1
s.events = "event1";
s.products = "Example category 1;Example product 1;1;1.99,Example category 2;Example product 2;1;2.69;event1=1.29";

// Use multiple numeric events in the product string
s.events = "event1,event2";
s.products = "Example category;Example product;1;4.20;event1=2.3|event2=5";

// Use merchandising eVars without any events. Note the adjacent semicolons to skip events
s.products = "Example category;Example product;1;6.69;;eVar1=Merchandising value";

// Use merchandising eVars without category, quantity, price, or events
s.products = ";Example product;;;;eVar1=Merchandising value";

// Multiple products using multiple different events and multiple different merchandising eVars
s.events = "event1,event2,event3,event4,purchase";
s.products = "Example category 1;Example product 1;3;12.60;event1=1.4|event2=9;eVar1=Merchandising value|eVar2=Another merchandising value,Example category 2;Example product 2;1;59.99;event3=6.99|event4=1;eVar3=Merchandising value 3|eVar4=Example value four";
```
