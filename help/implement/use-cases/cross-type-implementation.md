---
title: 다양한 구현 유형 추적
description: 서로 다른 구현 유형을 사용하고 이러한 유형 간에 방문자를 원활하게 추적합니다.
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
source-git-commit: 90914569256cf891cb3cf693843e7cf9ede2f4ce
workflow-type: ht
source-wordcount: '442'
ht-degree: 100%

---

# 다양한 구현 유형 추적

Adobe Analytics 구현의 핵심 아키텍처는 모든 구현 유형에서 일관되게 적용됩니다. 이 프로세스는 변수를 정의하고 Adobe의 데이터 수집 서버에 전송되는 이미지 요청으로 컴파일하는 단계를 포함합니다. 이 개념은 동일한 사이트의 여러 페이지에서 Adobe Experience Platform 데이터 수집의 AppMeasurement, Web SDK 및 각각의 확장 간에 원활하게 전환할 수 있음을 의미합니다.

모든 페이지에서 동일한 구현 유형을 사용하여 사이트 구현에서 일관성을 유지하는 것이 좋습니다. 단, 사이트의 일부에 다른 요구 사항이 있는 경우 이 페이지를 사용하여 방문자가 페이지 간에 일관되게 추적되도록 할 수 있습니다.

두 개 이상의 구현 유형을 사용하는 경우에는(AppMeasurement 및 하드코딩된 이미지 요청 등) 다음 변수가 올바르게 설정되어 있으며 서로 일치하는지 확인하십시오.

| 변수 | AppMeasurement | Analytics 확장 | Web SDK | Web SDK 확장 | 하드코딩된 이미지 요청 |
| --- | --- | --- | --- | --- | --- |
| 보고서 세트 ID | [`s_gi`](../vars/functions/s-gi.md) 내 문자열 인수 | [!UICONTROL 라이브러리 관리] 섹션의 [!UICONTROL 보고서 세트] ([확장 구성](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html?lang=ko-KR) 시) | 서비스로 Adobe Analytics 추가([데이터스트림 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=ko-KR) 시) | 서비스로 Adobe Analytics 추가([데이터스트림 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=ko-KR) 시) | URL `pathname`의 일부(`/b/ss/` 다음) |
| 추적 서버 | [`trackingServer`](../vars/config-vars/trackingserver.md) 및 [`trackingServerSecure`](../vars/config-vars/trackingserversecure.md) 변수 | [!UICONTROL 일반] 섹션의 [!UICONTROL 추적 서버] 및 [!UICONTROL SSL 추적 서버] ([확장 구성](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html?lang=ko-KR) 시) | `edgeDomain` 속성([Web SDK 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR) 시) | [!UICONTROL Edge 도메인] ([확장 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=ko-KR) 시) | 이미지 요청 URL의 `hostname` |
| Experience Cloud ID 서비스 | 구현 [`VisitorAPI.js`](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=ko-KR) | [Adobe Experience Cloud ID 서비스 확장](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html?lang=ko-KR) 사용 | [Adobe Experience Cloud ID 서비스 확장](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html?lang=ko-KR) 사용 | [Adobe Experience Cloud ID 서비스 확장](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html?lang=ko-KR) 사용 | [ID 서비스 서버에 대한 별도의 호출](https://experienceleague.adobe.com/docs/id-service/using/implementation/direct-integration.html?lang=ko-KR)을 만들어 원하는 ID 확보 |

{style="table-layout:auto"}

이러한 변수 중 각 구현 유형에서 일관되지 않은 것이 경우 Adobe는 해당 변수를 별도의 방문자로 간주합니다. 방문자가 사이트의 구현 유형 간에 원활하게 추적되지 않는 경우 가장 일반적인 이유는 ID 서비스가 잘못 구성된 것입니다. 자세한 내용은 ID 서비스 사용 안내서의 [구현 방법](https://experienceleague.adobe.com/docs/id-service/using/implementation/implementation-methods.html?lang=ko-KR)을 참조하십시오.
