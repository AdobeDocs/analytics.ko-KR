---
title: Adobe Experience Platform Edge를 사용하여 Adobe Analytics 구현
description: Adobe Analytics에서 Experience Platform의 XDM 데이터 사용 개요
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 9d9212313f54e4b44c5341754942ac0e0c78b84c
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 95%

---

# Adobe Experience Platform Edge를 사용하여 Adobe Analytics 구현

Adobe Experience Platform Edge를 사용하면 여러 제품을 대상으로 한 데이터를 중앙 위치에 전송할 수 있습니다. Experience Edge는 적절한 정보를 원하는 제품에 전달합니다. 이 개념을 사용하면 특히 여러 데이터 솔루션에 걸쳐 구현 노력을 통합할 수 있습니다.

Adobe는 Experience Edge로 데이터를 전송하는 세 가지 주요 방법을 제공합니다.

* **[Adobe Experience Platform Web SDK](web-sdk/overview.md)**: Adobe Experience Platform 데이터 수집 UI에서 Web SDK 확장 기능을 사용하여 데이터를 Edge로 전송합니다.
* **[Adobe Experience Platform Mobile SDK](mobile-sdk/overview.md)**: Adobe Experience Platform 데이터 수집 UI에서 Mobile SDK 확장 기능을 사용하여 데이터를 Edge로 전송합니다.
* **[Adobe Experience Platform Edge Network Server API](server-api/overview.md)**: API를 사용하여 데이터를 Edge로 직접 전송합니다.



## Adobe Analytics에서 Experience Edge 데이터를 처리하는 방법

Experience Edge로 전송된 데이터는 [XDM(경험 데이터 모델)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=en) 기반 스키마를 준수해야 합니다. XDM을 통해 이벤트의 일부로 정의된 필드를 유연하게 작업할 수 있습니다. 이벤트가 Adobe Analytics에 연결되면 이러한 이벤트는 Adobe Analytics에서 처리할 수 있는 보다 구조화된 데이터(페이지 조회수 또는 링크 이벤트)로 변환됩니다.

XDM은 페이지 조회수 또는 링크 이벤트를 정의하는 방법을 자체 규정하지 않으며 Adobe Analytics에 페이로드를 처리 방법을 지시하지도 않습니다. 예를 들어 `eventType`, `web.webPageDetails.pageViews` 또는 `web.webInteraction.linkEvents` 등 페이지 조회수 또는 링크 이벤트와 관련 연관성이 있는 특정 기본 제공 XDM 필드는 완전히 구현에 구애받지 않으면 Adobe Analytics와 관련 연관성이 없습니다.

페이지 조회수와 링크 이벤트를 제대로 처리하려면 Adobe Experience Edge Network로 전송되고 Adobe Analytics로 전달되는 데이터에 다음 논리를 적용합니다.

| XDM 페이로드에는 다음이 포함됩니다. | Adobe Analytics... |
|---|---|
| `web.webPageDetails.name` 또는 `web.webPageDetails.URL` 및 `web.webInteraction.type` 없음 | 페이로드를 **페이지 조회수**&#x200B;로 간주 |
| `web.webInteraction.type` (`web.webInteraction.name` 또는 `web.webInteraction.url`) | 페이로드를 **링크 이벤트**&#x200B;로 간주 |
| `web.webInteraction.type` (`web.webPageDetails.name` 또는 `web.webPageDetails.url`) | 페이로드를 **링크 이벤트**&#x200B;로 간주하고 <br/>`web.webPageDetails.name` `web.webPageDetails.URL`을 `null`로 설정 |
| `web.webInteraction.type` 아님 및(`webPageDetails.name`, `web.webPageDetails.URL` 아님) | 페이로드 중단 및 데이터 무시 |

{style="table-layout:auto"}

다음을 참조하십시오. [Adobe Analytics ExperienceEvent 전체 확장 스키마 필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/event/analytics-full-extension.html?lang=en) 추가 정보.
