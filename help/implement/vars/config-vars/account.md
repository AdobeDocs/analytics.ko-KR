---
title: account
description: (중단됨) 데이터가 전송되는 보고서 세트를 결정합니다.
feature: Appmeasurement Implementation
exl-id: 075d20be-6109-4024-84c4-1d048678d2bd
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/ICQkj-Eo29jve35GewuZUKOPIr01g-WjhbyztrAO0jI'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 38%

---

# account

>[!IMPORTANT]
>
>이 변수는 사용이 중단되었습니다. 구현에서 보고서 세트 대상을 수정해야 하는 경우 [`s.sa()`](../functions/sa-method.md) 함수를 사용하십시오.

이전 버전의 Adobe Analytics에서 `account` 변수는 보낸 데이터를 받을 보고서 세트를 결정했습니다. 데이터를 Adobe Analytics에 전송하려면 보고서 세트 ID가 필요합니다.

* 웹 SDK을 사용하는 경우 보고서 세트는 웹 SDK에서 데이터를 보내는 데이터 스트림 내의 Adobe Analytics 서비스 설정에 있습니다.
* Adobe Analytics 확장을 사용하는 경우 보고서 세트는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 라이브러리 관리] 아코디언 아래에 있습니다.
* [`s_gi()`](../functions/s-gi.md) 함수를 사용하여 Analytics 추적 개체를 인스턴스화하는 경우 보고서 세트 ID가 함수에서 필수 인수로 이미 존재합니다.
