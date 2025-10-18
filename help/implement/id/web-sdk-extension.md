---
title: 웹 SDK 태그 확장을 사용한 방문자 식별
description: 웹 SDK 태그 확장을 구현할 때 방문자를 올바르게 식별합니다.
source-git-commit: 3055a76f797438be71e82ea8f73800dc82ff4805
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# 웹 SDK 태그 확장을 사용한 방문자 식별

Adobe Experience Platform 데이터 수집의 웹 SDK 태그 확장 기능을 통해 조직은 태그 관리 인터페이스를 사용하여 웹 SDK을 구현할 수 있습니다. 도메인 간 ID 공유 및 방문자 프로필 마이그레이션과 같은 고급 시나리오는 확장 규칙 및 작업을 통해 쉽게 구성할 수 있습니다. 웹 SDK을 사용하면 향후 구현을 검증할 수 있으며 Customer Journey Analytics으로의 원활한 업그레이드를 지원합니다.

방문자 ID 서비스는 기본적으로 태그 확장에 제공되므로 **[!UICONTROL Edge 도메인]**&#x200B;을(를) 원하는 값으로 설정해야 합니다. 이 필드가 올바르게 설정되면 방문자 식별이 추가 구성 없이 작동합니다.

>[!NOTE]
>
>웹 SDK 태그 확장을 사용하는 경우 방문자 ID 서비스 태그 확장을 포함하지 마십시오. 방문자 ID 서비스 태그 확장은 [Adobe Analytics 확장](analytics-extension.md)을 사용하는 경우에만 필요합니다.
