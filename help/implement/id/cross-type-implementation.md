---
title: 다양한 구현 유형 추적
description: 서로 다른 구현 유형을 사용하고 이러한 유형 간에 방문자를 원활하게 추적합니다.
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
feature: Implementation Basics
role: Admin, Developer, Leader
TQID: https://experienceleague.adobe.com/FM6c33rpXxzy1huu8KE0VBkfe4FGIySczmVMrprFEUY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
  - id: df312454-73c4-43f6-a90e-18f5043f074c
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 444
ht-degree: 61%

---

# 다양한 구현 유형 추적

Adobe Analytics 구현의 핵심 아키텍처는 모든 구현 유형에서 일관되게 적용됩니다. 이 프로세스는 변수를 정의하고 Adobe의 데이터 수집 서버에 전송되는 이미지 요청으로 컴파일하는 단계를 포함합니다. 이 개념은 동일한 사이트의 여러 페이지에서 Adobe Experience Platform 데이터 수집의 AppMeasurement, Web SDK 및 각각의 확장 간에 원활하게 전환할 수 있음을 의미합니다.

모든 페이지에서 동일한 구현 유형을 사용하여 사이트 구현에서 일관성을 유지하는 것이 좋습니다. 단, 사이트의 일부에 다른 요구 사항이 있는 경우 이 페이지를 사용하여 방문자가 페이지 간에 일관되게 추적되도록 할 수 있습니다.

두 개 이상의 구현 유형을 사용하는 경우(AppMeasurement 및 하드코딩된 이미지 요청 등) 다음 변수가 올바르게 설정되고 서로 일치하는지 확인하십시오.

>[!NOTE]
>
>모든 구현 유형은 동일한 방문자 식별 유형(기존 Analytics ID 또는 방문자 ID 서비스)을 사용해야 합니다. Adobe에서는 가능한 모든 구현에서 방문자 ID 서비스 를 사용하는 것을 권장합니다.

| 변수 | 웹 SDK 태그 확장 기능 | 웹 SDK(Alloy) | Analytics 확장 기능 | AppMeasurement | 하드코딩된 이미지 요청 |
|---|---|---|---|---|---|
| 보고서 세트 ID | 서비스로 Adobe Analytics 추가([데이터스트림 구성](https://experienceleague.adobe.com/ko/docs/experience-platform/datastreams/configure) 시) | 서비스로 Adobe Analytics 추가([데이터스트림 구성](https://experienceleague.adobe.com/ko/docs/experience-platform/datastreams/configure) 시) | [!UICONTROL 라이브러리 관리] 섹션의 [!UICONTROL 보고서 세트] ([확장 구성](https://experienceleague.adobe.com/kr/docs/experience-platform/tags/extensions/client/analytics/overview) 시) | [`s_gi`](../vars/functions/s-gi.md)의 문자열 인수 | URL `pathname`의 일부(`/b/ss/` 다음) |
| Experience Cloud ID 서비스 | [기본적으로 포함됨](web-sdk-extension.md) | [기본적으로 포함됨](alloy.md) | [Experience Cloud ID 서비스 확장 사용](analytics-extension.md) | 구현 [`VisitorAPI.js`](appmeasurement.md) | 원하는 ID를 얻으려면 [ID 서비스에 대해 별도의 호출을](https://experienceleague.adobe.com/ko/docs/id-service/using/implementation/direct-integration)하고 쿼리 문자열에 `mid`을(를) 포함하십시오. |
| Edge 도메인 | [확장을 구성](https://experienceleague.adobe.com/ko/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration)할 때 [!UICONTROL Edge 도메인] 필드 | `edgeDomain` 속성([Web SDK 구성](https://experienceleague.adobe.com/ko/docs/experience-platform/web-sdk/commands/configure/overview) 시) | [확장을 구성](https://experienceleague.adobe.com/kr/docs/experience-platform/tags/extensions/client/analytics/overview)할 때 [!UICONTROL 일반] 섹션에서 [!UICONTROL SSL 추적 서버] | [`trackingServerSecure`](../vars/config-vars/trackingserversecure.md) 변수 | 이미지 요청 URL의 `hostname` |

이러한 변수가 각 구현 유형에서 일관되지 않으면 Adobe은 이러한 변수를 별도의 방문자로 간주할 수 있습니다. 방문자가 사이트의 구현 유형 간에 원활하게 추적되지 않는 경우 가장 일반적인 이유는 ID 서비스가 잘못 구성된 것입니다. 각 구현 유형이 사이트에서 동일한 Experience Cloud ID(`mid`)를 올바르게 가져오는지 확인하십시오.
