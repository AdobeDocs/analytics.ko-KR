---
title: collectHighEntropyUserAgentHints
description: 'collectHighEntropyUserAgentHints 변수를 사용하여 Adobe가 Chromium 브라우저(예: Google Chrome 및 Microsoft Edge)에서 높은 엔트로피 힌트를 요청할지 여부를 결정합니다.'
exl-id: 97cfa0f9-b35d-4c73-822f-adf30d0b7efc
source-git-commit: 5318079d6ad972e66494cd7b7f3bd64359b11012
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 100%

---

# collectHighEntropyUserAgentHints

높은 엔트로피 클라이언트 힌트는 Adobe Analytics에서 디바이스 및 브라우저 식별을 개선하는 데 사용됩니다. 이 옵션은 AppMeasurement.js 버전 2.23.0부터 사용할 수 있습니다. [Google의 블로그](https://web.dev/user-agent-client-hints/)와 [이 개요 및 FAQ](/help/technotes/client-hints.md)에서 클라이언트 힌트에 대해 자세히 알아보십시오.

## Web SDK를 사용하여 높은 엔트로피 힌트 수집

높은 엔트로피 클라이언트 힌트는 Web SDK에 있는 컨텍스트 범주의 일부입니다. 자세한 내용은 [Platform Web SDK 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR)을 참조하십시오.

## Adobe Analytics 확장을 사용하여 높은 엔트로피 힌트 수집

**[!UICONTROL 높은 엔트로피 사용자 에이전트 힌트 수집]**&#x200B;은 Adobe Analytics 확장을 구성할 때 [일반] 아코디언 아래에 있는 확인란입니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/#/@adobepm/data-collection)에 로그인합니다.

1. 원하는 [!UICONTROL 태그 속성]을 클릭합니다.

1. [!UICONTROL 확장] 탭으로 이동한 다음 Adobe Analytics 아래의 [!UICONTROL 구성]을 클릭합니다.

1. [!UICONTROL 일반] 아코디언을 확장하면 [!UICONTROL 높은 엔트로피 사용자 에이전트 힌트] 확인란이 표시됩니다. 기본적으로 선택되어 있지 않습니다.

## AppMeasurement의 collectHighEntropyUserAgentHints

`s.collectHighEntropyUserAgentHints` 변수는 AppMeasurement가 Chromium 브라우저(예: Google Chrome 또는 Microsoft Edge)에서 높은 엔트로피 힌트를 요청하는지 여부를 결정합니다. 이들 힌트는 Adobe Analytics에서 디바이스 및 브라우저 식별을 개선하는 데 사용됩니다.

`true`로 설정하면 모든 높은 엔트로피 힌트가 브라우저에서 요청됩니다.

```js
s.collectHighEntropyUserAgentHints = true;
```
