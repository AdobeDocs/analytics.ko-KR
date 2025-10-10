---
title: trackingServer
description: HTTP를 통해 Adobe으로 데이터를 전송하는 데 사용되는 도메인입니다.
feature: Appmeasurement Implementation
exl-id: bcc23286-4dd5-45ac-ac6f-7b60e95cb798
role: Admin, Developer
source-git-commit: 35675c2e65456a175d1516dd421b80d2af809286
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 13%

---

# trackingServer

>[!IMPORTANT]
>
>이 변수는 더 이상 사용되지 않습니다. HTTPS가 보급되면 대신 [`trackingServerSecure`](trackingserversecure.md)을(를) 사용하십시오.

`trackingServer` 변수는 AppMeasurement이 HTTP를 통해 Adobe에 데이터를 보내는 데 사용하는 도메인을 결정합니다. 이 변수가 올바르게 정의되지 않으면 구현에서 데이터 손실이 발생할 수 있습니다.

[Adobe Experience Cloud Identity 서비스](https://experienceleague.adobe.com/en/docs/id-service/using/home) 이전에 이 변수는 타사 쿠키가 설정된 위치도 확인했습니다. Adobe은 가능한 모든 구현에서 ID 서비스를 사용하는 것이 좋습니다.

AppMeasurement은 `trackingServer`이(가) 설정되지 않은 경우 [`trackingServerSecure`](trackingserversecure.md)을(를) 대체 항목으로 사용합니다. 많은 이전 구현에서는 보안 페이지에서 `trackingServerSecure`을(를) 대체 항목으로 사용하여 `trackingServer`을(를) 설정하지 않습니다. HTTPS가 보급됨에 따라 Adobe에서는 가능한 경우 `trackingServerSecure`을(를) 사용하는 것이 좋습니다.
