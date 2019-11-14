---
description: 페이지 변수는 pageName, List Props, List Variables 등과 같이, 보고서를 직접 채웁니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: 페이지 변수
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 45642bdbe18627caa20b1def6443f1e596a41f52

---


# products

 변수는 제품 및 제품 카테고리를 추적하는 데 사용됩니다(구매 수량 및 구매 가격도 추적). 제품은 일반적으로 장바구니 이벤트나 이벤트와 연결하여 설정됩니다.

<!-- 

products.xml

 -->

>[!IMPORTANT]
>
>2016년 1월에 *`prodView`* 이벤트를 자동으로 설정하는 논리를 업데이트했습니다. 이 논리는 *`product`*&#x200B;이 있지만 *`event`*&#x200B;가 없는 경우 발생합니다. 이 업데이트로 인해 *`prodView`이벤트가 늘어날 수 있습니다.* *`prodViews`*&#x200B;는 다음과 같은 경우에만 늘어납니다.
>
>1. 이벤트 변수에 *`shoppingCart`* 또는 *`cart`* 등의 인식할 수 없으며 올바르지 않은 이벤트만 포함되어 있습니다.
   >
   >
1. *`products`변수가 비어 있지 않습니다.*
>
>
가능한 부작용은 *`prodView`* 이벤트에 의해 트리거된 머천다이징 eVar를 빈 *`product`*&#x200B;과 연결할 수 있지만 *`product list`*&#x200B;에 잘못된 제품(예: 나열된 제품이 없는 세미콜론)만 있는 경우에만 가능하다는 것입니다. 

*`products`* 변수는 사용자가 사이트에서 제품과 어떻게 상호 작용하는지를 추적합니다. 예를 들어 products 변수는 몇 번이나 제품을 보았는지, 장바구니에 추가했는지, 체크아웃했는지 및 구입했는지를 추적할 수 있습니다. 또한 사이트에 있는 머천다이징 카테고리의 상대적 효과를 추적할 수도 있습니다. 다음은 products 변수를 사용하는 일반적인 시나리오입니다.

The *`products`* 변수는 항상 성공 이벤트와 함께 설정해야 합니다.

<table id="table_D5A11AFDDD364D0993D387906343DDF3"> 
 <thead> 
  <tr> 
   <th class="entry"> 최대 크기 </th> 
   <th class="entry"> 디버거 매개 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>문자열 "<span class="wintitle"> 제품 </span>"의 최대 크기는 64k입니다. </p> </td> 
   <td> products </td> 
   <td> 제품 <p>카테고리(선택 사항) </p> <p>매출(선택 사항) </p> <p>판매량(선택 사항) </p> <p>사용자 지정 이벤트(선택 사항) </p> <p>eVar(선택 사항) </p> </td> 
   <td> " " </td> 
  </tr> 
 </tbody> 
</table>

**구문** {#section_ABA3682985E540E6AA67A510176CCFFC}

```js
"Category;Product;Quantity;Price;eventN=X[|eventN2=X2];eVarN=merch_category[|eVarN2=merch_category2]"
```

| 필드 | 정의 |
|---|---|
| 카테고리 | 연결된 제품 카테고리가 들어 있습니다. 버전 15에서는, 버전 14에 있는 제한을 수정하는 제품을 여러 카테고리와 연결할 수 있습니다. 이전에 제품 카테고리를 기록하지 않은 경우, 버전 15에 있는 보고서 세트에 대해 이 필드를 채우는 것이 좋습니다. |
| 제품 | (필수) 제품을 추적하는 데 사용되는 식별자. 이 식별자는 [!UICONTROL 제품] 보고서를 채우는 데 사용됩니다. 반드시 체크아웃 프로세스를 통해 동일한 식별자를 사용하십시오. |
| 수량 | 구매된 개수. 이 필드를 기록하려면 [!UICONTROL 구매] 이벤트가 설정되어 있어야 합니다. |
| 가격 | 개별 가격이 아니라, 구매한 총 수량의 복합 비용(판매량 x 개별 단위 가격)을 나타냅니다. 이 필드를 기록하려면 [!UICONTROL 구매] 이벤트가 설정되어 있어야 합니다. |
| 이벤트 | 지정된 제품과 연결된 통화 이벤트. [제품별 통화 이벤트](/help/implement/js-implementation/c-variables/page-variables.md#section_F814DF053C0D463A97DA039E6323720C) 및 [주문 범위 통화 이벤트](/help/implement/js-implementation/c-variables/page-variables.md#section_D06F76A8A1F8498EB1BD6D8C8B9D5BE0)를 참조하십시오. |
| eVar | 특정 제품과 연결된 머천다이징 eVar 값. [머천다이징 변수](/help/components/c-variables/c-merch-variables/var-merchandising.md)를 참조하십시오. |

The values included in the *`products`*&#x200B;변수에 포함된 값은 기록하고 있는 이벤트 유형을 기반으로 합니다. 카테고리/제품 구분 기호(;)는 카테고리 생략 시 자리 표시자로 필요합니다. 이 페이지의 예에서 보듯이, 다른 구분 기호는 포함하고 있는 매개 변수를 구분하는 데 필요할 경우에만 필요합니다.

**비구매 이벤트 관련 products 설정** {#section_D5E689D4AAE941EC851CA9B98328A4DE}

*`products`* 변수는 성공 이벤트와 함께 설정해야 합니다.

**구매 이벤트 관련 products 설정** {#section_618AAC96E7B541A7AABAA028E5F4E5C3}

*`purchase`* 이벤트는 주문 프로세스의 최종 확인("감사합니다!") 페이지에서 설정해야 합니다. 제품 이름, 카테고리, 수량 및 가격은 모두 *`products`* 변수를 채우는 방법을 설명합니다. *`purchaseID`* 변수는 필수가 아니지만, 중복 주문을 방지하기 위해 사용해야 합니다.

**제품별 통화 이벤트** {#section_F814DF053C0D463A97DA039E6323720C}

통화 이벤트가 이벤트 변수 대신 *`products`* 변수에서 값을 받는 경우 해당 값에만 적용됩니다. 제품별 할인, 제품 배송 및 유사한 값을 추적하는 데 유용합니다. 예를 들어, 이벤트 1을 제품 배송을 추적하도록 구성한 경우, 배송비가 "4.50"인 제품이 다음과 유사하게 나타납니다.

```js
s.events="event1" 
s.products="Footwear;Running Shoes;1;99.99;event1=4.50"
```

이 예에서, 4.50이라는 값은 "Running Shoes" 제품과 바로 연결되어 있습니다. 제품 보고서에 event1을 추가하면, "Running Shoes" 라인 항목에 대해 "4.50"가 나열된 것을 보게 됩니다. 가격과 유사하게, 이 값은 나열된 수량에 대한 합계를 반영해야 합니다. 배송비가 각각 4.50인 항목이 2개가 있을 경우, event1은 "9.00"이어야 합니다.

**주문 범위 통화 이벤트** {#section_D06F76A8A1F8498EB1BD6D8C8B9D5BE0}

통화 이벤트가 *`products`* 변수 대신 이벤트 목록에서 값을 받으면 *`products`* 변수의 모든 제품에 적용됩니다. 이는 제품 가격을 수정하거나 제품 목록에서 별도로 추적할 필요 없이 주문 전체에 대한 할인, 배송 및 유사한 값을 추적하는 데 유용합니다.

예를 들어, event10이 주문 전체에 대한 할인을 포함하도록 구성한 경우 10% 할인된 구매는 다음과 같이 표시될 수 있습니다.

```js
s.events="purchase,event10=9.95" 
s.products="Footwear;Running Shoes;1;69.95,Running Essentials;Running Socks;10;29.50" 
s.purchaseID="1234567890"
```

통화 이벤트 보고서에서 보고서 총계는 각 제품에 대한 이벤트 값의 합이 아닌 중복 제거된 이벤트 총계(보고 기간 동안의 총 할인 금액)를 나타냅니다. 예를 들어, "Running Shoes"와 "Running Socks"에 모두 "9.95"가 나열되고, 합계는 "9.95"가 됩니다.

> [!NOTE] 동일한 숫자/통화 이벤트에 대한 값이 *`products`* 변수와 *`events`* 변수에 지정된 경우 *`events`*&#x200B;의 값이 사용됩니다.

**함정, 질문 및 팁** {#section_D38FD0B79C0347B9AB4CF1632183DA2E}

* *`products`]변수는 항상*&#x200B;성공[!UICONTROL  이벤트와 함께 설정해야 합니다. [!UICONTROL 성공] 이벤트를 지정하지 않은 경우 기본 이벤트는 [!UICONTROL prodView]입니다.

* 제품을 채우려면 먼저 제품 및 카테고리 이름에서 모든 쉼표와 세미콜론을 제거하십시오.
* 모든 HTML 문자(등록 기호, 상표 등)를 제거하십시오.
* 가격에서 통화 기호($)를 제거하십시오.

**예** {#section_FCC6EF43D3534ECB9A95CDB05820F564}

<table id="table_6F1334E73CE048A5AC0CC28B561C1B2D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <code> s.products="Category;ABC123" </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.products="Category2;ABC123,;ABC456" </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.products="Category3;ABC123;1;10" </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.products="Category;ABC123;1;10,;ABC456;2;19.98" </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1" </code> <p> <code> s.products="Category;ABC123;;;event1=1.99" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99,;ABC123;2;19.98;event1=1.99" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping|evar2=3 Stars" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping, ;ABC456;2;19.98;event1=1.99|event2=100;evar1=Ground Shipping" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2,event3" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping,;ABC456;2;19.98;event1=1.99|event2=100;evar1=Ground Shipping,;;;;event3=2.9;evar3=20% off" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2,event3=9.95" </code> <p> <code> s.products="Category;ABC123;,;ABC456;2;19.98;event1=1.99|event2=100;evar1=Ground Shipping,;;;;event3=2.9;evar3=2