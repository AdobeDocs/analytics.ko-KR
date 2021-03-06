---
title: events
description: 사이트에 대한 대부분의 지표를 제어하는 events 변수를 설정합니다.
feature: Variables
exl-id: 6ef99ee5-40c3-4ff2-a75d-c97f2e8ec1f8
source-git-commit: 5e71564e3aade426d84a039a6864d441d165345a
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 84%

---

# events

차원 및 지표는 보고서에 중요한 구성 요소입니다. `events` 변수는 사이트에서 많은 지표의 데이터 수집을 담당합니다. 이벤트는 일반적으로 보고서에서 [지표](/help/components/metrics/overview.md)를 증가시킵니다.

이벤트를 구현하려면 먼저 보고서 세트 설정의 [성공 이벤트](/help/admin/admin/c-success-events/success-event.md) 아래에서 이벤트를 만들고 구성해야 합니다. 링크 추적 히트에서 사용자 지정 이벤트를 사용할 계획이라면, [`linkTrackVars`](../../config-vars/linktrackvars.md)와 [`linkTrackEvents`](../../config-vars/linktrackevents.md)가 올바로 설정되었는지 확인하십시오.

## 웹 SDK를 사용한 이벤트

사용자 지정 이벤트는 다음과 같습니다 [Adobe Analytics용 매핑](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) 다음 XDM 필드에서 다음을 수행합니다.

* 사용자 지정 이벤트 1-100이 `_experience.analytics.event1to100.event1` - `_experience.analytics.event1to100.event100`.
* 사용자 지정 이벤트 101-200이 `_experience.analytics.event101to200.event100` - `_experience.analytics.event101to200.event200`.
* 이 패턴은 100개 이벤트마다 반복됩니다. `_experience.analytics.event901to1000.event901` - `_experience.analytics.event901to1000.event1000`. `eventx.value` 값을 지정하는 데 사용됩니다. `eventx.id` 직렬화에 대한 id를 지정하는 데 사용됩니다.
* 주문은 `commerce.purchases.value`.
* 단위는 모두 합계에 매핑됩니다 `productListItems[].quantity` 필드.
* 매출이 모두 합계에 매핑됩니다 `productListItems[].priceTotal` 필드.
* 제품 보기가 `commerce.productListViews.value`.
* 장바구니가 `commerce.productListOpens.value`.
* 장바구니 추가는에 매핑됩니다 `commerce.productListAdds.value`.
* 장바구니 제거가 `commerce.productListRemovals.value`.
* 장바구니 보기가 `commerce.productListViews.value`.
* 체크아웃은 `commerce.checkouts.value`.

## Adobe Analytics 확장을 사용하는 이벤트

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 이벤트를 설정할 수 있습니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL 이벤트] 섹션을 찾습니다.

다음과 같은 몇 가지 기능을 사용할 수 있습니다.

* 드롭다운을 사용하면 포함할 이벤트를 선택할 수 있습니다.
* 직렬화를 위한 선택적 텍스트 필드. 자세한 내용은 [이벤트 직렬화](event-serialization.md)를 참조하십시오.
* 이벤트 값에 대한 선택적 텍스트 필드. 통화 이벤트를 위한 통화를 포함하거나, 비통화 이벤트를 위한 정수를 포함하여 여러 번 증가시킬 수 있습니다. 예를 들어 드롭다운 아래에서 `event1`을 선택하고 이 필드에 `10`을 포함하면 보고에서 `event1`이 10만큼 증가합니다.
* 다른 이벤트를 추가하는 버튼. 히트에 포함할 수 있는 이벤트 수에는 적절한 제한이 없습니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.events

`s.events` 변수는 히트에 포함할 이벤트에 대한 쉼표로 구분된 목록을 포함하는 문자열입니다. 이 변수에는 바이트 제한이 없으므로 잘리지 않습니다. 유효 값 항목:

* `event1` - `event1000`: 원하는 대로 설정하는 사용자 지정 이벤트입니다. 조직의 [솔루션 디자인 문서](../../../prepare/solution-design.md)에서 각 이벤트를 사용하는 방법을 기록하십시오. 사용 가능한 이벤트 수는 조직의 Analytics 계약에 따라 다릅니다. 비 레거시 계약에 있는 대부분의 조직에는 사용할 수 있는 사용자 지정 이벤트 1,000개가 있습니다. 사용 가능한 사용자 지정 이벤트의 수를 모를 경우에는 조직의 계정 관리자에게 문의하십시오.
* `purchase`: [&#39;주문&#39;](/help/components/metrics/orders.md) 지표를 1씩 증가시키고, `products` 변수에 설정된 값을 사용하여 [&#39;판매량&#39;](/help/components/metrics/units.md) 및 [&#39;수입&#39;](/help/components/metrics/revenue.md)을 계산합니다. 자세한 내용은 [구매 이벤트](event-purchase.md)를 참조하십시오.
* `prodView`: [&#39;제품 보기&#39;](/help/components/metrics/product-views.md) 지표를 증가시킵니다.
* `scOpen`: [&#39;장바구니 수&#39;](/help/components/metrics/carts.md) 지표를 증가시킵니다.
* `scAdd`: [&#39;장바구니 추가&#39;](/help/components/metrics/cart-additions.md) 지표를 증가시킵니다.
* `scRemove`: [&#39;장바구니 제거 수&#39;](/help/components/metrics/cart-removals.md) 지표를 증가시킵니다.
* `scView`: [&#39;장바구니 보기 수&#39;](/help/components/metrics/cart-views.md) 지표를 증가시킵니다.
* `scCheckout`: [&#39;체크아웃&#39;](/help/components/metrics/checkouts.md) 지표를 증가시킵니다.

>[!NOTE]
>
>이 변수는 대/소문자를 구분합니다. 정확한 데이터 수집을 위해 이벤트 값을 대/소문자로 잘못 변경하지 마십시오.

```js
// Set the events variable to a single value
s.events = "event1";

// Set the events variable to multiple values
s.events = "event1,event13,purchase";
```

### 카운터 이벤트를 여러 번 증가시키기

원하는 경우 사용자 지정 이벤트를 두 번 이상 카운트할 수 있습니다. 문자열 내에서 원하는 이벤트에 정수를 지정하십시오. 보고서 세트 설정에서 생성된 이벤트는 기본적으로 카운터 이벤트입니다.

```js
// Count event1 ten times
s.events = "event1=10";

// Count event1 twice and event2 once
s.events = "event1=2,event2";
```

>[!NOTE]
>
>카운터 이벤트는 통화 또는 소수점 값을 지원하지 않습니다. 통화에는 통화 이벤트를 사용하고, 소수점 값에는 숫자 이벤트를 사용하십시오.

### 통화 이벤트 사용

사용자 지정 이벤트를 변경하여 정수 대신 통화를 사용할 수 있습니다. 보고서 세트 통화와 `currencyCode` 변수가 일치하지 않는 경우 통화 이벤트가 보고서 세트의 통화로 자동 변환됩니다. 이 이벤트는 배송비, 할인 또는 환불을 계산하는 데 유용합니다. 이벤트를 해당 제품에만 연결하려는 경우 `products` 변수에서 통화 이벤트를 설정할 수 있습니다.

통화 이벤트를 구현하려면 먼저 보고서 세트 설정의 [성공 이벤트](/help/admin/admin/c-success-events/success-event.md) 아래에서 원하는 이벤트를 &#39;통화&#39;로 설정해야 합니다.

```js
// Send $9.99 USD in event1 using the events variable. Make sure the event type for event1 is Currency in Report suite settings
s.currencyCode = "USD";
s.events = "event1=9.99";

// Send $9.99 USD in event1 using the products variable. Make sure the event type for event1 is Currency in Report suite settings
s.currencyCode = "USD";
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=9.99";
```

>[!NOTE]
>
>`events` 변수와 `products` 변수 모두에서 통화 값을 설정하는 경우 `events`의 통화 값이 사용됩니다. 통화 값을 `events` 및 `products` 변수 모두에서 설정하지 마십시오.

### 숫자 이벤트 사용

사용자 지정 이벤트를 변경하여 정수 대신 소수점 값을 허용할 수 있습니다. 숫자 이벤트는 통화 변환을 사용하지 않는다는 점을 제외하면 통화 이벤트와 유사하게 동작합니다. 이벤트를 해당 제품에만 연결하려는 경우 `products` 변수에서 숫자 이벤트를 설정할 수 있습니다.

숫자 이벤트를 구현하려면 먼저 보고서 세트 설정의 [성공 이벤트](/help/admin/admin/c-success-events/success-event.md) 아래에서 원하는 이벤트를 &#39;숫자&#39;로 설정해야 합니다.

```js
// Send 4.5 in event1 using the events variable. Make sure the event type for event1 is Numeric in Report suite settings
s.events = "event1=4.5";

// Send 4.5 in event1 using the products variable. Make sure the event type for event1 is Numeric in Report suite settings
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=4.5";
```

>[!NOTE]
>
>`events` 변수와 `products` 변수 모두에서 숫자 값을 설정하는 경우 `events`의 숫자 값이 사용됩니다. 숫자 값을 `events` 및 `products` 변수 모두에서 설정하지 마십시오.
