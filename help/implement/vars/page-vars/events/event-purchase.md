---
title: 구매 이벤트
description: 구매 이벤트를 사용하여 '주문 수', '판매량' 및 '매출액' 지표의 데이터를 수집합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# 구매 이벤트

purchase 이벤트는 `events` 변수의 값입니다. 이 값은 사이트가 생성하는 매출에 대한 데이터를 수집하려는 조직에 유용합니다. 이는 [`products`](../products.md) 및 [`purchaseID`](../purchaseid.md) 변수에 크게 의존합니다.

구매 이벤트를 설정하면 다음 지표에 영향을 줍니다.

* &#39;주문 수&#39; 지표는 1씩 증가합니다
* &#39;단위&#39; 지표는 `products` 변수의 제품 수로 증가합니다
* &#39;매출액&#39; 지표는 `products` 변수의 가격 매개 변수 합으로 증가합니다

## Adobe Experience Platform Launch에서 구매 이벤트 설정

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다. [!UICONTROL Rules]
4. 아래에서 [!UICONTROL Actions]기존 [!UICONTROL Adobe Analytics - Set Variables] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 드롭다운을 [!UICONTROL Extension] Adobe Analytics로 설정하고 [!UICONTROL Action Type] 을 [!UICONTROL Set Variables]설정합니다.
6. 섹션을 [!UICONTROL Events] 찾아 이벤트 드롭다운을 로 설정합니다 [!UICONTROL purchase].

Launch에 `products` 전용 필드가 `purchaseID` 없고 같은 기타 종속 변수가 있습니다. 이러한 변수에 대해 AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기에서 구매 이벤트 설정

purchase 이벤트는 events 변수의 일부로 설정되는 문자열입니다.

```js
// Set the purchase event by itself
s.events = "purchase";

// Set the purchase event alongside other events
s.events = "purchase,event1,event2";
```

## 구매 이벤트 중복 제거

구매 이벤트를 실행하면 Adobe는 다음을 확인합니다.

* 히트에 `purchaseID` 변수가 포함되어 있습니까? 그렇지 않은 경우 Adobe는 히트의 정보를 사용하여 &quot;임시 구매 ID&quot;를 만듭니다. 이 임시 구매 ID는 해당 히트의 방문자에게만 적용됩니다. 이전 5개의 임시 구매 ID는 보고서 세트당 각 방문자 ID에 저장됩니다.
* 임시 구매 ID가 저장된 마지막 5개의 임시 구매 ID와 일치합니까? 일치하는 경우 이미지 요청이 중복 구입으로 간주됩니다. 구매 이벤트를 포함한 모든 전환 변수가 보고에 표시되지 않습니다.
* 변수가 정의된 `purchaseID` 경우, 모든 방문자 간에 보고서 세트에서 이미 수집된 값과 일치합니까? 일치하는 경우 이미지 요청이 중복 구입으로 간주됩니다. 구매 이벤트를 포함한 모든 전환 변수가 보고에 표시되지 않습니다.
