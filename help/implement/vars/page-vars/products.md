---
title: products
description: 표시되거나 장바구니에 있는 제품에 대한 데이터를 전송합니다.
feature: Variables
exl-id: f26e7c93-f0f1-470e-a7e5-0e310ec666c7
source-git-commit: f0e69d68dd6a5413a050e00f5dca1c820ecee389
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 74%

---

# products

`products` 변수는 제품과 제품에 연결된 속성을 추적하는데 일반적으로 개별 제품 페이지, 장바구니 페이지 및 구매 확인 페이지에서 설정됩니다. 이 변수는 여러 값을 갖는 변수입니다. 이것은 동일한 히트에서 여러 제품을 보낼 수 있고 Adobe가 값을 별도의 차원 항목으로 구문 분석함을 의미합니다.

>[!NOTE]
>
>히트에서 이 변수가 [`events`](events/events-overview.md) 변수 없이 설정되면 [제품 보기](/help/components/metrics/product-views.md) 지표가 1만큼 증가합니다. `products` 변수가 있는 각 히트에 대해 적합한 이벤트를 설정해야 합니다.

## 웹 SDK를 사용하는 제품

제품은 다음과 같습니다 [Adobe Analytics용 매핑](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) 여러 XDM 필드에서 다음을 수행합니다.

* 카테고리가 `productListItems[].lineItemId`.
* 제품이 `productListItems[].name`.
* 수량이 매핑된 경우 `productListItems[].quantity`.
* 가격이 `productListItems[].priceTotal`.
* 머천다이징 eVar가에 매핑됩니다 `productListItems._experience.analytics.customDimensions.eVars.eVar1` to `productListItems._experience.analytics.customDimensions.eVars.eVar250`, 제품에 연결할 eVar에 따라 다릅니다.
* 머천다이징 이벤트가에 매핑됨 `productListItems[]._experience.analytics.event1to100.event1.value` to `productListItems._experience.analytics.event901to1000.event1000.value`, 제품에 연결할 이벤트에 따라 다릅니다.

>[!NOTE]
>
>`lineItemId` 표준 Analytics 이벤트 스키마의 일부가 아니므로 사용자 지정 필드로 추가해야 합니다. 앞으로는 전용 &#39;카테고리&#39; 필드를 추가할 예정입니다.


## Adobe Analytics 확장을 사용하는 제품

Adobe Experience Platform 데이터 수집에는 이 변수를 설정할 전용 필드가 없습니다. 그러나 도움이 되는 타사 확장은 여러 개 있습니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그]를 클릭하여 사용 가능한 모든 확장을 확인합니다.
4. product라는 용어를 검색하면 이 변수를 설정하는 데 도움이 되는 사용 가능한 몇 가지 확장이 표시됩니다.

이 확장 중 하나를 사용하거나 아래의 AppMeasurement 구문에 따라 사용자 지정 코드 편집기를 사용할 수 있습니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.products

`s.products` 변수는 제품당 여러 개의 구분된 필드를 포함하는 문자열입니다. 각 필드는 문자열에서 세미콜론 (`;`)으로 구분하십시오.

* **카테고리** (선택 사항): 제품 카테고리입니다. 이 필드의 최대 길이는 100바이트입니다.
* **제품 이름** (필수): 제품의 이름입니다. 이 필드의 최대 길이는 100바이트입니다.
* **수량** (선택 사항): 장바구니에 들어 있는 제품의 수. 이 필드는 구매 이벤트가 있는 히트에만 적용됩니다.
* **가격** (선택 사항): 제품의 총 가격 (소수). 수량이 두 개 이상인 경우 개별 제품 가격이 아니라 합계로 가격을 설정합니다. 이 값의 통화를 [`currencyCode`](../config-vars/currencycode.md) 변수와 일치하도록 맞춥니다. 이 필드에 통화 기호를 포함하지는 마십시오. 이 필드는 구매 이벤트가 있는 히트에만 적용됩니다.
* **이벤트** (선택 사항): 제품에 연결된 이벤트. 여러 이벤트는 파이프(`|`)를 사용하여 구분하십시오. 자세한 내용은 [이벤트](events/events-overview.md)를 참조하십시오.
* **eVar** (선택 사항): 제품에 연결된 머천다이징 eVar. 여러 머천다이징 eVar는 파이프(`|`)를 사용하여 구분하십시오. 자세한 내용은 [머천다이징 eVar](evar-merchandising.md)를 참조하십시오.

```js
// Set a single product using all available fields
s.products = "Example category;Example product;1;3.50;event1=4.99|event2=5.99;eVar1=Example merchandising value 1|eVar2=Example merchandising value 2";
```

이 변수는 동일한 히트에서 여러 제품을 지원합니다. 여러 제품이 포함된 장바구니 및 구매 시 유용합니다. 전체 `products` 문자열의 최대 길이는 64K입니다. 문자열에서 각 제품은 쉼표 (`,`)로 구분하십시오.

```js
// Set multiple products - useful for when a visitor views their shopping cart
s.products = "Example category 1;Example product 1;1;3.50,Example category 2;Example product 2;1;5.99";
```

>[!WARNING]
>
>제품 이름, 카테고리 및 머천다이징 eVar 값에서 모든 세미콜론, 쉼표 및 파이프를 제거하십시오. 제품 이름에 쉼표가 포함되어 있으면 AppMeasurement가 해당 쉼표를 새 제품의 시작으로 구문 분석합니다. 이렇게 잘못된 구문 분석이 제품 문자열의 나머지 부분에서 발생하면 차원 및 보고서에서 잘못된 데이터가 생성됩니다.

## 예

`products` 변수는 필드를 생략하고 여러 제품을 포함할 때 유연합니다. 이러한 유연성으로 인해 구분 기호가 쉽게 누락될 수 있고, 이렇게 되면 구현에서 잘못된 데이터를 Adobe에 보내게 됩니다.

```js
// Include only product and category. Common on individual product pages
s.products = "Example category;Example product";

// Include only product name
s.products = ";Example product";

// One product has a category, the other does not. Note the comma and adjacent semicolon to omit category
s.products = "Example category;Example product 1,;Example product 2";

// A visitor purchases a single product; record quantity and price
s.events = "purchase";
s.products = ";Example product;1;6.99";

// A visitor purchases multiple products with different quantities
s.events = "purchase";
s.products = ";Example product 1;9;26.91,Example category;Example product 2;4;9.96";

// Attribute currency event1 only to product 2 and not product 1
s.events = "event1";
s.products = ";Example product 1;1;1.99,Example category 2;Example product 2;1;2.69;event1=1.29";

// Use multiple numeric events in the product string
s.events = "event1,event2";
s.products = ";Example product;1;4.20;event1=2.3|event2=5";

// Use merchandising eVars without any events. Note the adjacent semicolons to skip events
s.products = ";Example product;1;6.69;;eVar1=Merchandising value";

// Use merchandising eVars without category, quantity, price, or events
s.products = ";Example product;;;;eVar1=Merchandising value";

// Multiple products using multiple different events and multiple different merchandising eVars
s.events = "event1,event2,event3,event4,purchase";
s.products = "Example category 1;Example product 1;3;12.60;event1=1.4|event2=9;eVar1=Merchandising value|eVar2=Another merchandising value,Example category 2;Example product 2;1;59.99;event3=6.99|event4=1;eVar3=Merchandising value 3|eVar4=Example value four";
```

`digitalData` [데이터 레이어](../../prepare/data-layer.md)를 사용하는 경우 `digitalData.product` 객체 배열을 반복할 수 있습니다.

```js
for(var i = 0; i < digitalData.product.length; i++) {
    // Add individual product info to the product string
    s.products += digitalData.product[i].category.primaryCategory + ";" + digitalData.product[i].productInfo.productName;
    // If there are more products, add a comma
    if(i != digitalData.product.length - 1) {
        s.products += ",";
    }
}
```
