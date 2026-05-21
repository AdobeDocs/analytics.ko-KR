---
title: cookieDomain
description: (중단됨) 쿠키를 설정할 도메인을 결정하는 데 도움이 됩니다.
feature: Appmeasurement Implementation
exl-id: 7e8c26b8-d1a7-49f7-9c12-45fb1633c9d7
role: Admin, Developer
TQID: https://experienceleague.adobe.com/z6occeGLpxezOj7go2DrwG-j-fc9yBuGyHSmZJK9RfQ
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 77%

---

# cookieDomain

>[!IMPORTANT]
>이 변수는 사용이 중단되었습니다. 대신 [`trackingServer`](trackingserver.md)를 사용하십시오.

`cookieDomain` 변수는 AppMeasurement가 쿠키를 설정하는 도메인을 결정합니다. 이 변수를 사용하면 [`cookieDomainPeriods`](cookiedomainperiods.md) 변수를 사용하는 대신 쿠키 도메인을 명시적으로 설정할 수 있습니다.

이 변수는 다음 조건을 **모두** 충족할 때만 사용해야 합니다.

* 구현에서 자사 쿠키를 사용하는 경우. 이 변수는 `sc.adobedc.net`을 포함하는 [`trackingServer`](trackingserver.md) 값을 사용하는 구현에는 필요하지 않습니다.
* 도메인 접미사에 마침표가 있는 경우. 예를 들어 `example.co.uk`가 `cookieDomain` 변수를 사용하여 쿠키 도메인이 `co.uk`가 아니고 `example.co.uk`라고 명시할 수 있습니다.

적은 수의 구현만 `cookieDomain` 변수를 사용할 수 있으며, 그러한 때에도 [`cookieDomainPeriods`](cookiedomainperiods.md)같은 대체 변수를 대신 사용할 수 있습니다.

## 웹 SDK을 사용하는 쿠키 도메인

웹 SDK은 이 변수 없이 올바른 쿠키 스토리지 도메인을 결정할 수 있습니다.

## Adobe Analytics 확장을 사용한 쿠키 도메인

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.cookieDomain

`cookieDomain` 변수는 문자열이며, 쿠키를 저장할 도메인으로 설정됩니다.

```js
s.cookieDomain = "stats.example.com";
```
