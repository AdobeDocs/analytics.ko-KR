---
title: 웹 SDK JavaScript 라이브러리를 사용한 방문자 식별
description: 웹 SDK JavaScript 라이브러리를 구현할 때 방문자를 올바르게 식별합니다.
source-git-commit: 3055a76f797438be71e82ea8f73800dc82ff4805
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# 웹 SDK JavaScript 라이브러리를 사용한 방문자 식별

Adobe Experience Platform Web SDK(`alloy.js`)는 Analytics를 포함한 모든 Adobe Experience Cloud 애플리케이션에 대한 데이터 수집에 대한 통합된 최신 접근 방식을 제공합니다. ID 데이터는 XDM의 `identityMap`을(를) 사용하여 사용자 지정 ID 및 여러 네임스페이스를 지원하도록 확장할 수 있습니다. Adobe에서는 고급 시나리오에 다른 ID 관리 옵션을 사용하여 Adobe Experience Cloud ID 서비스를 Analytics의 기본 식별자로 사용하는 것이 좋습니다.

조직에서 웹 SDK JavaScript 라이브러리를 사용하여 Adobe Analytics으로 데이터를 전송하는 경우 방문자 식별을 위해 최소 구성이 필요합니다. 방문자 ID 서비스는 기본적으로 라이브러리에 대해 만들어지며, **[!UICONTROL 명령에서]** Edge 도메인`configure`을(를) 설정해야 합니다. 이 필드를 원하는 값으로 설정하면 추가 구성 없이 방문자 식별이 작동합니다.
