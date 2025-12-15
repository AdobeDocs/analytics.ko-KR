---
title: Adobe Analytics의 Edge Network 이벤트 유형
description: Adobe Analytics에서 Edge Network에서 받은 이벤트를 해석하는 방법.
feature: Implementation Basics
role: Admin, Developer
exl-id: 31085025-9c38-4375-8dfb-4fded6542ca7
source-git-commit: 0096a53505b3b1bc925c813c2c6c11ee3c7ee0c0
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 20%

---

# Adobe Analytics의 Edge Network 이벤트 유형

Adobe Analytics에서는 AppMeasurement에서 호출하는 함수에 따라 히트를 다르게 처리합니다. 예를 들어 [`s.t`](/help/implement/vars/functions/t-method.md)과(와) [`s.tl`](/help/implement/vars/functions/tl-method.md)은(는) 특정 차원을 포함하거나 생략하고 [페이지 보기 수](/help/components/metrics/page-views.md)를 다르게 증가시킵니다. Adobe Experience Platform에는 [`sendEvent`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/sendevent/overview) 명령만 포함되어 있습니다. [`xdm`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/sendevent/xdm) 또는 [`data`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/sendevent/data) 페이로드 내의 특정 속성은 Adobe Analytics에서 해당 데이터를 해석하는 방법을 결정합니다.

Edge Network에서는 다음 논리를 사용하여 Adobe Analytics [페이지 보기 수](/help/components/metrics/page-views.md) 및 [이벤트 연결](/help/components/metrics/page-events.md)을 결정합니다.

## `xdm` 개체를 사용한 페이지 보기 및 링크 이벤트

| XDM 페이로드에는 다음이 포함됩니다. | Adobe Analytics... |
|---|---|
| `xdm.web.webPageDetails.name` 또는 `xdm.web.webPageDetails.URL` 및 `xdm.web.webInteraction.type` 없음 | 페이로드를 **페이지 조회수**&#x200B;로 간주 |
| `xdm.eventType = web.webpagedetails.pageViews` | 페이로드를 **페이지 조회수**&#x200B;로 간주 |
| `xdm.web.webInteraction.type` (`xdm.web.webPageDetails.name` 또는 `xdm.web.webPageDetails.URL`) | 페이로드를 **링크 이벤트** <br/>고려하며 `xdm.web.webPageDetails.name` 및 `xdm.web.webPageDetails.URL`을(를) `null`(으)로 설정합니다. |
| `xdm.web.webInteraction.type` (`xdm.web.webInteraction.name` 또는 `xdm.web.webInteraction.URL`) | 페이로드를 **링크 이벤트** <br/>(으)로 간주합니다. `xdm.web.webPageDetails.name` 및 `xdm.web.webPageDetails.URL`을(를) `null`(으)로 설정합니다. |
| `xdm.web.webInteraction.type`이(가) 없고 `xdm.web.webPageDetails.name`이(가) 없으며 `xdm.web.webPageDetails.URL`이(가) 없습니다 | 페이로드 중단 및 데이터 무시 |

>[!TIP]
>
>페이로드의 XDM 필드 이름은 대소문자를 구분합니다(예: `webPageDetails.URL`). `xdm.eventType` 필드는 허용되는 고유한 값 집합이 있는 문자열 값이며, 해당 값의 대/소문자가 XDM 필드 이름과 일치하지 않을 수 있습니다. 허용되는 값은 `eventType`XDM ExperienceEvent 클래스[의 ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent#eventType) 필드를 참조하십시오.

+++`xdm` 필드를 사용하는 최소 페이지 보기

```json
{
  "xdm": {
    "web": {
      "webPageDetails": {
        "name": "Example page",
        "URL": "https://example.com/page"
      }
    }
  }
}
```

+++

+++`xdm.eventType`을(를) 사용한 최소 페이지 보기

```json
{
  "xdm": {
    "eventType": "web.webpagedetails.pageViews"
  }
}
```

+++

+++권장 필드를 사용하는 최소 링크 이벤트

```json
{
  "xdm": {
    "web": {
      "webInteraction": {
        "type": "other",
        "name": "Header nav: Pricing",
        "URL": "https://example.com/pricing"
      }
    }
  }
}
```

+++

## `data` 개체를 사용한 페이지 보기 및 링크 이벤트

| 데이터 개체 페이로드에 다음 포함... | Adobe Analytics... |
|---|---|
| `data.__adobe.analytics.pageName` 또는 `data.__adobe.analytics.pageURL` 및 `data.__adobe.analytics.linkType` 없음 | 페이로드를 **페이지 조회수**&#x200B;로 간주 |
| `data.__adobe.analytics.linkType` (`data.__adobe.analytics.linkName` 또는 `data.__adobe.analytics.linkURL`) | 페이로드를 **링크 이벤트** <br/>고려하며 `data.__adobe.analytics.pageName` 및 `data.__adobe.analytics.pageURL`을(를) `null`(으)로 설정합니다. |
| `data.__adobe.analytics.linkType`이(가) 없고 `data.__adobe.analytics.pageName`이(가) 없으며 `data.__adobe.analytics.pageURL`이(가) 없습니다 | 페이로드 중단 및 데이터 무시 |

+++`data` 필드를 사용하는 최소 페이지 보기

```json
{
  "data": {
    "__adobe": {
      "analytics": {
        "pageName": "Example page",
        "pageURL": "https://example.com/page"
      }
    }
  }
}
```

+++

+++`data` 필드를 사용하는 최소 링크 이벤트

```json
{
  "data": {
    "__adobe": {
      "analytics": {
        "linkType": "o",
        "linkName": "Header nav: Pricing",
        "linkURL": "https://example.com/pricing"
      }
    }
  }
}
```

+++

>[!NOTE]
>
>동일한 페이로드에 `xdm` 개체와 `data` 개체를 모두 포함하는 경우 Adobe Analytics에서 각 필드에 대해 두 개체를 모두 확인합니다.

## A4T 및 의사 결정 관련 이벤트

페이지 보기 수와 링크 이벤트를 구분하는 것 외에도 다음 논리는 특정 의사 결정 이벤트가 A4T로 분류되는지 또는 삭제되는지 여부를 결정합니다.

| XDM 페이로드에는 다음이 포함됩니다. | Adobe Analytics... |
|---|---|
| `xdm.eventType = decisioning.propositionDisplay` 및 `xdm._experience.decisioning` | 페이로드를 **A4T** 호출로 간주합니다. |
| `xdm.eventType = decisioning.propositionDisplay` 및 `xdm._experience.decisioning` 없음 | 페이로드 중단 및 데이터 무시 |
| `xdm.eventType = decisioning.propositionInteract` 및 `xdm._experience.decisioning`이고 `xdm.web.webInteraction.type`은(는) 없음 | 페이로드를 **A4T** 호출로 간주합니다. |
| `xdm.eventType = decisioning.propositionInteract`, `xdm._experience.decisioning` 및 `xdm.web.webInteraction.type` 없음 | 는 페이로드를 삭제하고 데이터를 무시합니다. |
| `xdm.eventType = decisioning.propositionFetch` | 페이로드 중단 및 데이터 무시 |

>[!TIP]
>
>다음 `eventType` 값은 더 이상 사용되지 않습니다. 이러한 값은 현재 대응 항목과 동일한 방식으로 논리에 영향을 줍니다.
>
>* 이벤트 유형 `display`은(는) 더 이상 사용되지 않습니다. 대신 `decisioning.propositionDisplay`를 사용하십시오.
>* 이벤트 유형 `click`은(는) 더 이상 사용되지 않습니다. 대신 `decisioning.propositionInteract`를 사용하십시오.
>* 이벤트 유형 `personalization.request`은(는) 더 이상 사용되지 않습니다. 대신 `decisioning.propositionFetch`를 사용하십시오.

+++최소 A4T 디스플레이

```json
{
  "xdm": {
    "eventType": "decisioning.propositionDisplay",
    "_experience": {
      "decisioning": {
        "propositions": [
          {
            "id": "example-proposition-id",
            "scope": "example-scope",
            "scopeDetails": { "decisionProvider": "AJO" }
          }
        ],
        "propositionEventType": { "display": 1 }
      }
    }
  }
}
```

+++

+++최소 A4T 상호 작용

```json
{
  "xdm": {
    "eventType": "decisioning.propositionInteract",
    "_experience": {
      "decisioning": {
        "propositions": [
          {
            "id": "example-proposition-id",
            "scope": "example-scope",
            "scopeDetails": { "decisionProvider": "AJO" }
          }
        ],
        "propositionEventType": { "interact": 1 }
      }
    }
  }
}
```

+++

자세한 내용은 [Adobe Analytics ExperienceEvent 전체 스키마 확장 필드 그룹](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/analytics-full-extension)을 참조하십시오.
