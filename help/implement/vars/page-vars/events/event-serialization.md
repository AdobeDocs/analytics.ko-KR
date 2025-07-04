---
title: 이벤트 직렬화
description: 사이트의 지표 중복 제거에 도움이 됩니다.
feature: Appmeasurement Implementation
exl-id: 54de0fd7-9056-44af-bd59-b8eb55fc816e
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 83%

---

# 이벤트 ID 직렬화

이벤트 직렬화는 중복 이벤트 중복 이벤트가 Analytics 보고에 들어가지 않도록 하는 방법을 구현하는 프로세스입니다. 페이지를 새로 고치는 방문자에 의해 지표가 부풀려지는 것을 원하지 않는 경우 이벤트 중복 제거가 중요합니다.

>[!NOTE]
>
>데이터 소스는 이벤트 직렬화 또는 중복제거를 지원하지 않습니다.

## 이벤트 직렬화 설정

먼저 이벤트의 [!UICONTROL 고유 이벤트 기록]을 보고서 세트 설정에서 [!UICONTROL 이벤트 ID 사용]으로 설정해야 합니다. 관리자 사용 안내서의 [성공 이벤트](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md)를 참조하십시오.

이벤트 ID를 사용할 때 중복 제거는 다음 수준에서 수행됩니다.

* 각 변수는 중복 제거에 자체 테이블을 사용합니다. 예를 들어 `event1:ABC` 및 `event2:ABC`는 둘 다 보고에서 계산됩니다.
* 중복 제거는 모든 방문자에 대해 전체적으로 수행됩니다. 방문자 A가 `event1:ABC`를 전송한 후 방문자 B도 `event1:ABC`를 전송하는 경우 Adobe에서는 방문자 B의 두 번째 인스턴스를 무시합니다.
* 중복 제거는 만료되지 않습니다. 방문자가 `event1:ABC`를 전송하고 2년 후 다시 와서 `event1:ABC`를 전송하는 경우 Adobe에서는 두 번째 인스턴스를 무시합니다.

>[!TIP]
>
>[`purchase`](event-purchase.md) 이벤트를 중복 제거하려면 [`purchaseID`](../purchaseid.md) 변수를 대신 사용하십시오.

## Web SDK를 사용하여 이벤트 ID 사용

[**XDM 개체**](/help/implement/aep-edge/xdm-var-mapping.md)&#x200B;를 사용하는 경우 이벤트 직렬화는 원하는 이벤트의 XDM 필드 `id`을(를) 사용합니다. 전체 XDM 경로는 직렬화하려는 이벤트에 따라 다릅니다.

예를 들어 장바구니 추가 지표를 serialize하려면 `xdm.commerce.productListAdds.id`을(를) 원하는 serialization 값으로 설정합니다. 사용자 지정 이벤트 20을 serialize하려면 `xdm._experience.analytics.event1to100.event20`을(를) 원하는 serialization 값으로 설정하십시오.

[**데이터 개체**](/help/implement/aep-edge/data-var-mapping.md)&#x200B;를 사용하는 경우 이벤트 직렬화는 AppMeasurement 문자열 구문 다음에 나오는 `data.__adobe.analytics.events`을(를) 사용합니다.

## Adobe Analytics 확장을 사용한 이벤트 ID 사용

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에 포함된 작업으로서 이벤트 ID 필드를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운 목록을 Adobe Analytics으로 설정하고 [!UICONTROL 작업 유형]을(를) [!UICONTROL 변수 설정]&#x200B;(으)로 설정합니다.
6. 각 이벤트에 [!UICONTROL 이벤트 ID] 필드가 포함된 [!UICONTROL 이벤트] 섹션을 찾습니다.

유효한 값은 최대 20바이트 길이의 영숫자 문자입니다. 20바이트보다 긴 값을 입력하면 시스템이 처음 20바이트로 잘라냅니다.

## AppMeasurement 및 Analytics 확장 사용자 정의 코드 편집기에서 이벤트 ID 사용

이벤트 직렬화는 `s.events` 변수의 일부입니다. 문자열에서 콜론을 사용하여 각 이벤트에 ID를 할당합니다.

```js
// Assign custom ID serialization to a single value
s.events = "event1:ABC123";

// Assign custom ID serialization to multiple values
s.events = "event1:ABC123,event2:ABC123";
```

이벤트에 직렬화가 활성화되었지만 직렬화 ID가 포함되어 있지 않은 경우 이 이벤트는 항상 계산됩니다.
