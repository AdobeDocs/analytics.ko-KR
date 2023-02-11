---
title: 다양한 구현 유형 추적
description: 서로 다른 구현 유형을 사용하고 이러한 유형 간에 방문자를 원활하게 추적합니다.
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
source-git-commit: 90914569256cf891cb3cf693843e7cf9ede2f4ce
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 14%

---

# 다양한 구현 유형 추적

Adobe Analytics 구현의 핵심 아키텍처는 모든 구현 유형에서 일관됩니다. 이 프로세스에서는 변수를 정의하고 Adobe의 데이터 수집 서버로 전송되는 이미지 요청으로 컴파일합니다. 즉, 동일한 사이트의 여러 페이지에서 Adobe Experience Platform 데이터 수집에서 AppMeasurement, 웹 SDK 및 해당 확장 간을 원활하게 전환할 수 있습니다.

Adobe은 모든 페이지에서 동일한 구현 유형을 사용하여 사이트의 구현 간에 일관성을 유지하는 것을 권장합니다. 그러나 사이트의 일부에 다른 요구 사항이 있는 경우 이 페이지를 사용하여 방문자가 페이지 간에 일관되게 추적되도록 할 수 있습니다.

두 개 이상의 구현 유형(예: AppMeasurement 및 하드코딩된 이미지 요청)을 사용하는 경우 다음 변수가 올바르게 설정되고 서로 일치하는지 확인하십시오.

| 변수 | AppMeasurement | Analytics 확장 | Web SDK | Web SDK 확장 | 하드 코딩된 이미지 요청 |
| --- | --- | --- | --- | --- | --- |
| 보고서 세트 ID | 내의 문자열 인수 [`s_gi`](../vars/functions/s-gi.md) | [!UICONTROL 보고서 세트] 아래에 [!UICONTROL 라이브러리 관리] 섹션 [확장 구성](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html) | 다음의 경우 Adobe Analytics을 서비스로 추가 [데이터 스트림 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html) | 다음의 경우 Adobe Analytics을 서비스로 추가 [데이터 스트림 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html) | URL의 일부 `pathname` (후) `/b/ss/`) |
| 추적 서버 | 다음 [`trackingServer`](../vars/config-vars/trackingserver.md) 및 [`trackingServerSecure`](../vars/config-vars/trackingserversecure.md) 변수 | [!UICONTROL 추적 서버] 및 [!UICONTROL SSL 추적 서버] 아래에 [!UICONTROL 일반] 섹션 [확장 구성](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html) | 다음 `edgeDomain` property when [웹 SDK 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR) | 다음 [!UICONTROL Edge 도메인] when [확장 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html) | 다음 `hostname` 이미지 요청 URL의 |
| Experience Cloud ID 서비스 | 구현 [`VisitorAPI.js`](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html) | 를 사용하십시오 [Adobe Experience Cloud ID 서비스 확장](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html) | 를 사용하십시오 [Adobe Experience Cloud ID 서비스 확장](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html) | 를 사용하십시오 [Adobe Experience Cloud ID 서비스 확장](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html) | 만들기 [id 서비스 서버에 대한 별도의 호출](https://experienceleague.adobe.com/docs/id-service/using/implementation/direct-integration.html) 원하는 ID를 얻으려면 |

{style=&quot;table-layout:auto&quot;}

이러한 변수 중 하나가 각 구현 유형에서 일관되지 않으면 Adobe은 이를 별도의 방문자로 간주합니다. 방문자가 사이트의 구현 유형 간에 원활하게 추적되지 않는 경우 가장 일반적인 이유는 ID 서비스가 잘못 구성되어 있기 때문입니다. 자세한 내용은 [구현 방법](https://experienceleague.adobe.com/docs/id-service/using/implementation/implementation-methods.html) 자세한 내용은 ID 서비스 사용 안내서에서 를 참조하십시오.
