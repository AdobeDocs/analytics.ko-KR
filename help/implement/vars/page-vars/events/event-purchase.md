---
title: 구매 이벤트
description: 구매 이벤트를 사용하여 '주문', '판매량' 및 '수입' 지표에 대한 데이터를 수집합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# 구매 이벤트

구매 이벤트는 `events` 변수의 값입니다. 이 값은 사이트가 생성하는 수입에 대한 데이터를 수집하려는 조직에 유용하며 [`products`](../products.md) 및 [`purchaseID`](../purchaseid.md) 변수에 크게 의존합니다.

구매 이벤트를 설정하면 다음 지표에 영향을 줍니다.

* &#39;주문&#39; 지표는 1씩 증가합니다.
* &#39;판매량&#39; 지표는 `products` 변수의 제품 수만큼 증가합니다.
* &#39;수입&#39; 지표는 `products` 변수에 있는 가격 매개 변수의 합만큼 증가합니다.

## Adobe Experience Platform Launch에서 구매 이벤트 설정

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL 이벤트] 섹션을 찾아 이벤트 드롭다운을 [!UICONTROL 구매]로 설정합니다.

Launch에서 `products` 및 `purchaseID`와 같은 기타 종속 변수에는  전용 필드가 없습니다. 이 변수를 사용하려면 AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기에서 구매 이벤트 설정

구매 이벤트는 events 변수의 일부로 설정되는 문자열입니다.

```js
// Set the purchase event by itself
s.events = "purchase";

// Set the purchase event alongside other events
s.events = "purchase,event1,event2";
```

## 구매 이벤트 중복 제거

구매 이벤트를 실행하면 Adobe에서는 다음 사항을 확인합니다.

* 히트에 `purchaseID` 변수가 포함되어 있습니까? 그렇지 않은 경우 Adobe는 히트의 정보를 사용하여 &quot;임시 구매 ID&quot;를 만듭니다. 이 임시 구매 ID는 해당 히트의 방문자에게만 적용됩니다. 이전 5개의 임시 구매 ID는 보고서 세트에 대한 각 방문자 ID용으로 저장됩니다.
* 임시 구매 ID가 마지막 5개의 저장된 임시 구매 ID 중 하나와 일치합니까? 일치하는 경우 이미지 요청이 중복 구입으로 간주됩니다. 구매 이벤트를 포함한 모든 전환 변수가 보고에 표시되지 않습니다.
* `purchaseID` 변수가 정의되어 있다면, 해당 값이 모든 방문자에 대해 보고서 세트에 이미 수집된 값과 일치합니까? 일치하는 경우 이미지 요청이 중복 구입으로 간주됩니다. 구매 이벤트를 포함한 모든 전환 변수가 보고에 표시되지 않습니다.
