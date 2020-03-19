---
title: events
description: 사이트의 대부분의 지표를 제어하는 events 변수를 설정합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# events

차원 및 지표는 보고서에 중요한 구성 요소입니다. 이 `events` 변수는 사이트에서 여러 지표의 데이터 수집을 담당합니다.

## Adobe Experience Platform Launch의 이벤트

Analytics 확장 기능(전역 변수)을 구성하는 동안 또는 규칙에서 이벤트를 설정할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다. [!UICONTROL Rules]
4. 아래에서 [!UICONTROL Actions]기존 [!UICONTROL Adobe Analytics - Set Variables] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 드롭다운을 [!UICONTROL Extension] Adobe Analytics로 설정하고 [!UICONTROL Action Type] 을 [!UICONTROL Set Variables]설정합니다.
6. 섹션을 [!UICONTROL Events] 찾습니다.

다음과 같은 몇 가지 기능을 사용할 수 있습니다.

* 드롭다운을 사용하여 포함할 이벤트를 선택할 수 있습니다
* 직렬화를 위한 선택적 텍스트 필드입니다. See [event serialization](event-serialization.md) for more information.
* 이벤트 값에 대한 선택적 텍스트 필드입니다. 통화 이벤트에 대한 통화를 포함하거나, 비통화 이벤트에 대한 정수를 포함하여 여러 번 늘릴 수 있습니다. 예를 들어, 드롭다운 `event1` 아래에서 이 필드를 `10` 포함하면 `event1` 보고에서 10개가 증가합니다.
* 다른 이벤트를 추가하는 단추입니다. 히트에 포함할 수 있는 이벤트 수에는 적절한 제한이 없습니다.

## s.events in AppMeasurement and Launch custom code editor

이 `s.events` 변수는 히트에 포함할 쉼표로 구분된 이벤트 목록을 포함하는 문자열입니다. 이 변수에는 바이트 제한이 없으므로 잘리지 않습니다. 유효 값 항목:

* `event1` - `event1000`:원하는 대로 사용자 지정 이벤트를 설정합니다. 조직의 [솔루션 디자인 문서에서](../../../prepare/solution-design.md)각 이벤트를 사용하는 방법을 기록합니다. 사용 가능한 이벤트 수는 조직의 Analytics 계약에 따라 다릅니다. 비기존 계약에 대한 대부분의 조직에는 1,000개의 사용자 지정 이벤트를 사용할 수 있습니다. 사용 가능한 사용자 지정 이벤트 수를 잘 모를 경우 조직의 계정 관리자에게 문의하십시오.
* `purchase`:&#39;주문 수&#39; 지표를 1씩 증가시키고, 변수에 설정된 값을 가져와 &#39;판매량&#39; 및 &#39;매출액&#39;을 계산합니다. `products` 자세한 내용은 [구매 이벤트를](event-purchase.md) 참조하십시오.
* `prodView`:&#39;제품 보기&#39; 지표를 증가시킵니다.
* `scOpen`:&#39;장바구니&#39; 지표를 증가시킵니다.
* `scAdd`:&#39;장바구니 추가&#39; 지표를 증가시킵니다.
* `scRemove`:&#39;장바구니 제거&#39; 지표를 증가시킵니다.
* `scView`:&#39;장바구니 보기&#39; 지표를 증가시킵니다.
* `scCheckout`:&#39;체크아웃&#39; 지표를 증가시킵니다.

> [!NOTE] 이 변수는 대소문자를 구분합니다. 정확한 데이터 수집을 위해 이벤트 값을 잘못 대문자로 변경하지 마십시오.

```js
// Set the events variable to a single value
s.events = "event1";

// Set the events variable to multiple values
s.events = "event1,event13,purchase";
```

### 카운터 이벤트를 여러 번 증가

원하는 경우 사용자 지정 이벤트를 두 번 이상 카운트할 수 있습니다. 문자열 내에서 원하는 이벤트에 정수를 지정합니다. 보고서 세트 설정에서 생성된 이벤트는 기본적으로 카운터 이벤트입니다.

```js
// Count event1 ten times
s.events = "event1=10";

// Count event1 twice and event2 once
s.events = "event1=2,event2";
```

> [!NOTE] 카운터 이벤트는 통화 또는 소수점 값을 지원하지 않습니다. 통화 이벤트에 통화 이벤트를 사용하거나 소수 값에 숫자 이벤트를 사용합니다.

### 통화 이벤트 사용

사용자 지정 이벤트를 변경하여 정수 대신 통화를 사용할 수 있습니다. 보고서 세트 통화 및 `currencyCode` 변수가 일치하지 않는 경우 통화 이벤트가 보고서 세트의 통화로 자동 변환됩니다. 배송비, 할인 또는 환불을 계산하는 데 유용합니다. 이벤트를 해당 제품에만 연결하려면 `products` 변수에서 통화 이벤트를 설정할 수 있습니다.

```js
// Send $9.99 USD in event1 using the events variable. Make sure the event type for event1 is Currency in report suite settings
s.currencyCode = "USD";
s.events = "event1=9.99";

// Send $9.99 USD in event1 using the products variable. Make sure the event type for event1 is Currency in report suite settings
s.currencyCode = "USD";
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=9.99";
```

> [!NOTE] 변수와 변수 모두에서 통화 값을 설정하는 `events` 경우 `products` 에서 통화 값이 `events` 사용됩니다. 통화 값을 `events` 및 `products` 변수 모두에서 설정하지 마십시오.

### 숫자 이벤트 사용

사용자 지정 이벤트를 변경하여 정수 대신 십진수 값을 허용할 수 있습니다. 숫자 이벤트는 통화 변환을 사용하지 않는다는 점을 제외하고 통화 이벤트와 유사하게 동작합니다. 이벤트를 해당 제품에만 연결하려면 `products` 변수에서 숫자 이벤트를 설정할 수 있습니다.

```js
// Send 4.5 in event1 using the events variable. Make sure the event type for event1 is Numeric in report suite settings
s.events = "event1=4.5";

// Send 4.5 in event1 using the products variable. Make sure the event type for event1 is Numeric in report suite settings
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=4.5";
```

> [!NOTE] 변수와 `events` 변수 모두에서 숫자 값을 설정하면 의 숫자 값이 `products` `events` 사용됩니다. 변수와 변수 모두에서 숫자 값을 설정하지 `events` 마십시오 `products` .
