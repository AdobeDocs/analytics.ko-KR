---
title: trackingServer
description: HTTP를 통해 Adobe으로 데이터를 전송하는 데 사용되는 도메인입니다.
feature: Appmeasurement Implementation
exl-id: bcc23286-4dd5-45ac-ac6f-7b60e95cb798
role: Admin, Developer
TQID: https://experienceleague.adobe.com/6H8uZ4J-mT8NcC4OiiTgtBnP8eAgaMMzxzUHkS-9kGs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 19%

---

# trackingServer

>[!IMPORTANT]
>
>이 변수는 더 이상 사용되지 않습니다. HTTPS가 보급되면 대신 [`trackingServerSecure`](trackingserversecure.md)을(를) 사용하십시오.

`trackingServer` 변수는 AppMeasurement이 HTTP를 통해 Adobe에 데이터를 보내는 데 사용하는 도메인을 결정합니다. 이 변수가 올바르게 정의되지 않으면 구현에서 데이터 손실이 발생할 수 있습니다.

[Adobe Experience Cloud Identity 서비스](https://experienceleague.adobe.com/kr/docs/id-service/using/home) 이전에 이 변수는 타사 쿠키가 설정된 위치도 확인했습니다. Adobe은 가능한 모든 구현에서 ID 서비스를 사용하는 것이 좋습니다.

AppMeasurement은 [`trackingServerSecure`](trackingserversecure.md)이(가) 설정되지 않은 경우 `trackingServer`을(를) 대체 항목으로 사용합니다. 많은 이전 구현에서는 보안 페이지에서 `trackingServer`을(를) 대체 항목으로 사용하여 `trackingServerSecure`을(를) 설정하지 않습니다. HTTPS가 보급됨에 따라 Adobe에서는 가능한 경우 `trackingServerSecure`을(를) 사용하는 것이 좋습니다.
