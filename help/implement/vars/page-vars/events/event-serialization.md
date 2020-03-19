---
title: 이벤트 정리
description: 사이트의 지표 중복 제거에 도움이 됩니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# 이벤트 ID 정리

이벤트 일련화는 중복 이벤트 중복 이벤트가 Analytics 보고에 들어가지 않도록 하는 방법을 구현하는 프로세스입니다. 방문자가 페이지를 새로 고침으로 부풀려지는 지표를 원하지 않는 경우 이벤트 중복 제거가 중요합니다.

> [!NOTE] 데이터 소스는 이벤트 직렬화 또는 중복제거를 지원하지 않습니다.

## 이벤트 정리 설정

먼저 보고서 세트 설정에서 이벤트의 [!UICONTROL Unique Event Recording] 설정을 [!UICONTROL Use Event ID] 설정해야 합니다. See [Success Events](/help/admin/admin/c-success-events/success-event.md) in the Admin user guide.

이벤트 ID를 사용하는 경우 다음 수준에서 중복 제거가 발생합니다.

* 각 변수는 자체 테이블을 사용하여 중복 제거를 수행합니다. 예를 들어, `event1:ABC` 및 `event2:ABC` 둘 다 보고에서 계산됩니다.
* 중복 제거는 모든 방문자에 대해 전체적으로 이루어집니다. 방문자 A가 전송한 `event1:ABC` 다음 방문자 B도 전송하는 `event1:ABC`경우 Adobe는 방문자 B의 두 번째 인스턴스를 무시합니다.
* 중복 제거는 만료되지 않습니다. 방문자가 2년 `event1:ABC` 후 다시 보낸 후 `event1:ABC` 다시 전송하는 경우 Adobe는 두 번째 인스턴스를 무시합니다.

> [!TIP] 이벤트를 중복 제거하려면 [`purchase`](event-purchase.md) [`purchaseID`](../purchaseid.md) 변수를 대신 사용하십시오.

## Adobe Experience Platform Launch에서 이벤트 ID 사용

Analytics 확장 기능(전역 변수)을 구성하는 동안 또는 규칙의 작업으로 이벤트 ID 필드를 설정할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다. [!UICONTROL Rules]
4. 아래에서 [!UICONTROL Actions]기존 [!UICONTROL Adobe Analytics - Set Variables] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 드롭다운을 [!UICONTROL Extension] Adobe Analytics로 설정하고 [!UICONTROL Action Type] 을 [!UICONTROL Set Variables]설정합니다.
6. 각 이벤트에 [!UICONTROL Events] [!UICONTROL Event ID] 필드가 포함된 섹션을 찾습니다.

유효한 값은 최대 20바이트 길이의 영숫자 문자입니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기에서 이벤트 ID 사용

이벤트 정리는 `s.events` 변수의 일부입니다. 문자열의 콜론을 사용하여 각 이벤트에 ID를 할당합니다.

```js
// Assign custom ID serialization to a single value
s.events = "event1:ABC123";

// Assign custom ID serialization to multiple values
s.events = "event1:ABC123,event2:ABC123";
```

이벤트 일련화가 활성화되었지만 일련화 ID가 포함되지 않은 경우 이벤트가 항상 카운트됩니다.
