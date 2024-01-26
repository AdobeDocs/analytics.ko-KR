---
title: Adobe Experience Platform Edge를 사용하여 Adobe Analytics 구현
description: Adobe Analytics에서 Experience Platform의 XDM 데이터 사용 개요
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 37%

---

# Adobe Experience Platform Edge를 사용하여 Adobe Analytics 구현

Adobe Experience Platform Edge를 사용하면 여러 제품을 대상으로 한 데이터를 중앙 위치에 전송할 수 있습니다. Experience Edge는 적절한 정보를 원하는 제품에 전달합니다. 이 개념을 사용하면 특히 여러 데이터 솔루션에 걸쳐 구현 노력을 통합할 수 있습니다.

Adobe는 Experience Edge로 데이터를 전송하는 세 가지 주요 방법을 제공합니다.

* **[Adobe Experience Platform Web SDK](web-sdk/overview.md)**: Adobe Experience Platform 데이터 수집 UI에서 Web SDK 확장을 사용하여 데이터를 Edge로 전송합니다.
* **[Adobe Experience Platform Mobile SDK](mobile-sdk/overview.md)**: Adobe Experience Platform 데이터 수집 UI에서 Mobile SDK 확장을 사용하여 데이터를 Edge로 전송합니다.
* **[Adobe Experience Platform Edge Network Server API](server-api/overview.md)**: API를 사용하여 데이터를 Edge로 직접 전송합니다.



## Adobe Analytics에서 Experience Edge 데이터를 처리하는 방법

Experience Edge로 전송되는 데이터는 다음을 기반으로 하는 스키마를 준수해야 합니다. [XDM(경험 데이터 모델)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR). XDM을 사용하면 이벤트의 일부로 정의된 필드를 유연하게 사용할 수 있습니다. 이벤트가 Adobe Analytics에 도달하면 이러한 이벤트는 Adobe Analytics에서 처리할 수 있는 보다 구조화된 데이터(페이지 보기 또는 링크 이벤트)로 변환됩니다.

XDM은 페이지 보기 수 또는 링크 이벤트를 정의하는 방법을 자체적으로 규정하지 않으며, Adobe Analytics에 해당 페이로드를 처리하는 방법을 지시하지도 않습니다. 예를 들어 과 같이 페이지 보기 또는 링크 이벤트와 관련된 것으로 보이는 특정 XDM 필드 `eventType`, `web.webPageDetails.pageViews`, 또는 `web.webInteraction.linkEvents` 는 완전히 구현에 영향을 주지 않으며 Adobe Analytics과 관련이 없습니다.

페이지 보기 수 및 링크 이벤트를 제대로 처리하기 위해, 다음 논리가 Adobe Experience Edge 네트워크로 전송된 데이터에 적용되어 Adobe Analytics으로 전달됩니다.

| XDM 페이로드에 다음 포함... | Adobe Analytics... |
|---|---|
| `web.webPageDetails.name` 또는 `web.webPageDetails.URL` 및 아니요 `web.webInteraction.type` | 페이로드 a 고려 **페이지 보기** |
| `web.webInteraction.type` 및 (`web.webInteraction.name` 또는 `web.webInteraction.url`) | 페이로드 a 고려 **링크 이벤트** |
| `web.webInteraction.type` 및 (`web.webPageDetails.name` 또는 `web.webPageDetails.url`) | 페이로드 a 고려 **링크 이벤트** <br/>`web.webPageDetails.name` 및 `web.webPageDetails.URL` 이(가) (으)로 설정됩니다. `null` |
| 아니요 `web.webInteraction.type` 및(아니요) `webPageDetails.name` 및 아니요 `web.webPageDetails.URL`) | 페이로드를 삭제하고 데이터를 무시합니다. |

{style="table-layout:auto"}

