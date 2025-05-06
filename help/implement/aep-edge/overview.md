---
title: Adobe Experience Platform Edge를 사용하여 Adobe Analytics 구현
description: Adobe Analytics에서 Experience Platform의 XDM 데이터 사용 개요
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 8e701a3da6f04ccf2d7ac3abd10c6df86feb00a7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 73%

---

# Adobe Experience Platform Edge Network를 사용하여 Adobe Analytics 구현

Adobe Experience Platform Edge Network를 사용하면 여러 제품을 대상으로 한 데이터를 중앙 위치에 전송할 수 있습니다. Edge Network는 적절한 정보를 원하는 제품에 전달합니다. 이 개념을 사용하면 특히 여러 데이터 솔루션에 걸쳐 구현 노력을 통합할 수 있습니다.

Adobe는 Edge Network로 데이터를 전송하는 세 가지 주요 방법을 제공합니다.

* **[Adobe Experience Platform Web SDK](web-sdk/overview.md)**: Adobe Experience Platform 데이터 수집 UI에서 Web SDK 확장 기능을 사용하여 데이터를 Edge로 전송합니다.
* **[Adobe Experience Platform Mobile SDK](mobile-sdk/overview.md)**: Adobe Experience Platform 데이터 수집 UI에서 Mobile SDK 확장 기능을 사용하여 데이터를 Edge로 전송합니다.
* **[Adobe Experience Platform Edge Network API](api/overview.md)**: API를 사용하여 데이터를 Edge Network으로 직접 보냅니다.

## Adobe Analytics에서 Edge Network 데이터를 처리하는 방법

Adobe Experience Platform Edge Network로 전송된 데이터는 다음과 같이 두 가지 형식을 따를 수 있습니다.

* XDM 오브젝트: [XDM(경험 데이터 모델)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html) 기반 스키마를 따릅니다. XDM을 통해 이벤트의 일부로 정의된 필드를 유연하게 작업할 수 있습니다. 이벤트가 Adobe Analytics에 도달하면 Adobe Analytics가 처리할 수 있는 형식으로 변환됩니다.
* 데이터 오브젝트: Adobe Analytics에 매핑된 특정 필드를 사용하여 Edge Network에 데이터를 전송합니다. Edge Network는 이러한 필드의 존재를 감지하고 스키마를 준수할 필요 없이 Adobe Analytics에 전달합니다.

Edge Network에서는 다음 논리를 사용하여 Adobe Analytics 페이지 보기 수 및 링크 이벤트를 결정합니다.

| XDM 페이로드에는 다음이 포함됩니다. | Adobe Analytics... |
|---|---|
| `xdm.web.webPageDetails.name` 또는 `xdm.web.webPageDetails.URL` 및 `xdm.web.webInteraction.type` 없음 | 페이로드를 **페이지 조회수**&#x200B;로 간주 |
| `xdm.eventType = web.webPageDetails.pageViews` | 페이로드를 **페이지 조회수**&#x200B;로 간주 |
| `xdm.web.webInteraction.type` (`xdm.web.webInteraction.name` 또는 `xdm.web.webInteraction.url`) | 페이로드를 **링크 이벤트**&#x200B;로 간주 |
| `xdm.web.webInteraction.type` (`xdm.web.webPageDetails.name` 또는 `xdm.web.webPageDetails.url`) | 페이로드를 **링크 이벤트** <br/>고려하며 `xdm.web.webPageDetails.name` 및 `xdm.web.webPageDetails.URL`을(를) `null`(으)로 설정합니다. |
| `xdm.web.webInteraction.type` 아님 및(`xdm.webPageDetails.name`, `xdm.web.webPageDetails.URL` 아님) | 페이로드 중단 및 데이터 무시 |

{style="table-layout:auto"}

페이지 보기 수 및 링크 클릭을 구분하는 것 외에도 다음 논리를 사용하여 특정 이벤트가 A4T로 분류되는지 또는 삭제되는지 여부를 결정할 수 있습니다.

| XDM 페이로드에는 다음이 포함됩니다. | Adobe Analytics... |
| --- | --- |
| `xdm.eventType = display` 또는 <br/>`xdm.eventType = decisioning.propositionDisplay` 또는 <br/>`xdm.eventType = personalization.request` 또는 <br/>`xdm.eventType = decisioning.propositionFetch` 및 `xdm._experience.decisioning` | 페이로드를 **A4T** 호출로 간주합니다. |
| `xdm.eventType = display` 또는 <br/>`xdm.eventType = decisioning.propositionDisplay` 또는 <br/>`xdm.eventType = personalization.request` 또는 <br/>`xdm.eventType = decisioning.propositionFetch` 및 `xdm._experience.decisioning` 없음 | 페이로드 중단 및 데이터 무시 |
| `xdm.eventType = click` 또는 `xdm.eventType = decisioning.propositionInteract`과(와) `xdm._experience.decisioning` 및 `web.webInteraction.type` 없음 | 페이로드를 **A4T** 호출로 간주합니다. |
| `xdm.eventType = click` 또는 `xdm.eventType = decisioning.propositionInteract`이고 `xdm._experience.decisioning`이(가) 없으며 `web.webInteraction.type`이(가) 없습니다. | 는 페이로드를 삭제하고 데이터를 무시합니다. |

{style="table-layout:auto"}

자세한 내용은 [Adobe Analytics ExperienceEvent 전체 스키마 확장 필드 그룹](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/event/analytics-full-extension.html)을 참조하십시오.
