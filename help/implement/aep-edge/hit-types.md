---
title: Adobe Analytics의 Edge Network 이벤트 유형
description: Adobe Analytics에서 Edge Network에서 받은 이벤트를 해석하는 방법.
feature: Implementation Basics
role: Admin, Developer
exl-id: 31085025-9c38-4375-8dfb-4fded6542ca7
source-git-commit: 6e500007e10086c0ff8108856a3563d7702f1130
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 25%

---

# Adobe Analytics의 Edge Network 이벤트 유형

Adobe Analytics에서는 AppMeasurement에서 호출하는 함수에 따라 히트를 다르게 처리합니다. 예를 들어 [`s.t`](/help/implement/vars/functions/t-method.md)과(와) [`s.tl`](/help/implement/vars/functions/tl-method.md)은(는) 특정 차원을 포함하거나 생략하고 페이지 보기를 다르게 증가시킵니다. Adobe Experience Platform에는 `sendEvent` 명령만 포함되어 있습니다. `xdm` 페이로드 내의 특정 속성은 Adobe Analytics에서 데이터를 해석하는 방법을 결정합니다.

Edge Network에서는 다음 논리를 사용하여 Adobe Analytics 페이지 보기 수 및 링크 이벤트를 결정합니다.

| XDM 페이로드에는 다음이 포함됩니다. | Adobe Analytics... |
|---|---|
| `xdm.web.webPageDetails.name` 또는 `xdm.web.webPageDetails.URL` 및 `xdm.web.webInteraction.type` 없음 | 페이로드를 **페이지 조회수**&#x200B;로 간주 |
| `xdm.eventType = web.webPageDetails.pageViews` | 페이로드를 **페이지 조회수**&#x200B;로 간주 |
| `xdm.web.webInteraction.type` (`xdm.web.webPageDetails.name` 또는 `xdm.web.webPageDetails.url`) | 페이로드를 **링크 이벤트** <br/>고려하며 `xdm.web.webPageDetails.name` 및 `xdm.web.webPageDetails.URL`을(를) `null`(으)로 설정합니다. |
| `xdm.web.webInteraction.type`이(가) 없고 `xdm.webPageDetails.name`이(가) 없으며 `xdm.web.webPageDetails.URL`이(가) 없습니다 | 페이로드 중단 및 데이터 무시 |

| 데이터 개체 페이로드에 다음 포함... | Adobe Analytics... |
|---|---|
| `data.__adobe.analytics.pageName` 또는 `data.__adobe.analytics.pageURL` 및 `data.__adobe.analytics.linkType` 없음 | 페이로드를 **페이지 조회수**&#x200B;로 간주 |
| `data.__adobe.analytics.linkType` (`data.__adobe.analytics.linkName` 또는 `data.__adobe.analytics.linkURL`) | 페이로드를 **링크 이벤트** <br/>고려하며 `data.__adobe.analytics.pageName` 및 `data.__adobe.analytics.pageURL`을(를) `null`(으)로 설정합니다. |
| `data.__adobe.analytics.linkType`이(가) 없고 `data.__adobe.analytics.pageName`이(가) 없으며 `data.__adobe.analytics.pageURL`이(가) 없습니다 | 페이로드 중단 및 데이터 무시 |

>[!NOTE]
>
>동일한 페이로드에 `xdm` 개체와 `data` 개체를 모두 포함하는 경우 Adobe Analytics에서 각 필드에 대해 두 개체를 모두 확인합니다.

페이지 보기 수 및 링크 클릭을 구분하는 것 외에도 다음 논리를 사용하여 특정 이벤트가 A4T로 분류되는지 또는 삭제되는지 여부를 결정할 수 있습니다.

| XDM 페이로드에는 다음이 포함됩니다. | Adobe Analytics... |
|---|---|
| `xdm.eventType = display` 또는 <br/>`xdm.eventType = decisioning.propositionDisplay` 또는 <br/>`xdm.eventType = personalization.request` 또는 <br/>`xdm.eventType = decisioning.propositionFetch` 및 `xdm._experience.decisioning` | 페이로드를 **A4T** 호출로 간주합니다. |
| `xdm.eventType = display` 또는 <br/>`xdm.eventType = decisioning.propositionDisplay` 또는 <br/>`xdm.eventType = personalization.request` 또는 <br/>`xdm.eventType = decisioning.propositionFetch` 및 `xdm._experience.decisioning` 없음 | 페이로드 중단 및 데이터 무시 |
| `xdm.eventType = click` 또는 `xdm.eventType = decisioning.propositionInteract`과(와) `xdm._experience.decisioning` 및 `web.webInteraction.type` 없음 | 페이로드를 **A4T** 호출로 간주합니다. |
| `xdm.eventType = click` 또는 `xdm.eventType = decisioning.propositionInteract`이고 `xdm._experience.decisioning`이(가) 없으며 `web.webInteraction.type`이(가) 없습니다. | 는 페이로드를 삭제하고 데이터를 무시합니다. |

자세한 내용은 [Adobe Analytics ExperienceEvent 전체 스키마 확장 필드 그룹](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/field-groups/event/analytics-full-extension)을 참조하십시오.
