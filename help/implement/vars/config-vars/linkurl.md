---
title: linkURL
description: 링크 추적 호출에서 AppMeasurement가 사용하는 자동으로 생성된 링크 URL을 무시합니다.
feature: Appmeasurement Implementation
exl-id: 15d6e423-d9fc-4f84-ad39-0bd91399cde4
role: Admin, Developer
source-git-commit: 24101efe2b860734c9d176ba8be8f17e26429442
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 34%

---

# linkURL

링크 추적 호출이 Adobe으로 전송될 때마다 AppMeasurement은 클릭한 URL을 감지합니다. 이 URL은 다운로드 링크 및 종료 링크와 같은 링크 유형을 결정하는 데 도움이 됩니다. 감지된 URL을 무시하려면 `linkURL` 변수를 사용하십시오.

Analysis Workspace에는 이 변수에 대해 보고하는 차원이 없습니다. `page_event_var1`데이터 피드[에서 ](/help/export/analytics-data-feed/data-feed-overview.md) 열을 채웁니다. Adobe 클릭한 링크의 URL을 추적하려면 [Prop](../page-vars/prop.md)과 같은 사용자 지정 변수를 사용하는 것이 좋습니다. [Activity Map](/help/analyze/activity-map/overview.md)을 사용하면 클릭한 링크에 대한 데이터 수집을 간소화할 수 있습니다.

## 웹 SDK을 사용하여 URL 연결

링크 URL은 다음 변수에 매핑됩니다.

* [XDM 개체](/help/implement/aep-edge/xdm-var-mapping.md): `web.webInteraction.URL`
* [데이터 개체](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.linkURL` 또는 `data.__adobe.analytics.pev1`

## Adobe Analytics 확장을 사용한 링크 URL

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.linkURL

`s.linkURL` 변수는 클릭한 링크의 전체 URL을 포함하는 문자열입니다. 이 변수는 보고에서 사용할 수 있는 차원을 채우지 않습니다.

```js
s.linkURL = "https://example.com";
```

[tl ()](../functions/tl-method.md) 메서드의 세 번째 인수가 설정되어 있지 않으면, 대신 `linkURL` 변수를 사용합니다.
