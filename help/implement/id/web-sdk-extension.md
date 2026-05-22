---
title: 웹 SDK 태그 확장을 사용한 방문자 식별
description: 웹 SDK 태그 확장을 구현할 때 방문자를 올바르게 식별합니다.
exl-id: 65de7fc3-a344-4f04-b523-1f5edf681d2f
TQID: 'https://experienceleague.adobe.com/4PVDioBDa-1VXg9Fpy0wA8-RZZYSXzVijj-b2kdEALQ'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
subfeature_v2:
  - id: b3e5f43e-2e2f-43c0-810a-044a5f91e31a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 0%

---

# 웹 SDK 태그 확장을 사용한 방문자 식별

Adobe Experience Platform 데이터 수집의 웹 SDK 태그 확장 기능을 통해 조직은 태그 관리 인터페이스를 사용하여 웹 SDK을 구현할 수 있습니다. 도메인 간 ID 공유 및 방문자 프로필 마이그레이션과 같은 고급 시나리오는 확장 규칙 및 작업을 통해 쉽게 구성할 수 있습니다. 웹 SDK을 사용하면 미래 지향적 구현을 구현할 수 있으며 Customer Journey Analytics으로 원활하게 업그레이드할 수 있습니다.

ID 데이터는 XDM의 `identityMap`을(를) 사용하여 사용자 지정 ID 및 여러 네임스페이스를 지원하도록 확장할 수 있습니다. Adobe에서는 고급 시나리오에 다른 ID 관리 옵션을 사용하여 Adobe Experience Cloud ID 서비스를 Analytics의 기본 식별자로 사용하는 것이 좋습니다.

방문자 ID 서비스는 기본적으로 태그 확장에 제공되므로 **[!UICONTROL Edge 도메인]**&#x200B;을(를) 원하는 값으로 설정해야 합니다. 이 필드가 올바르게 설정되면 방문자 식별이 추가 구성 없이 작동합니다.

>[!NOTE]
>
>웹 SDK 태그 확장을 사용하는 경우 방문자 ID 서비스 태그 확장을 포함하지 마십시오. 방문자 ID 서비스 태그 확장은 [Adobe Analytics 확장](analytics-extension.md)을 사용하는 경우에만 필요합니다.
