---
title: collectHighEntropyUserAgentHints
description: 'collectHighEntropyUserAgentHints 변수를 사용하여 Adobe이 Chromium 브라우저(예: Google Chrome 및 Microsoft Edge)에서 높은 엔트로피 힌트를 요청할지 여부를 결정합니다.'
source-git-commit: 9c386dd26e31b8b2dc2b4a52ae502f9505ec467d
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---


# collectHighEntropyUserAgentHints

Adobe Analytics은 높은 엔트로피 클라이언트 힌트를 사용하여 장치 및 브라우저 식별을 개선합니다. 에서 클라이언트 힌트에 대해 자세히 알아보십시오 [이 개요 및 FAQ](/help/technotes/client-hints.md) 뿐만 아니라 [Google 블로그](https://web.dev/user-agent-client-hints/).

## 웹 SDK를 사용하여 높은 엔트로피 힌트를 수집합니다

높은 엔트로피 클라이언트 힌트는 웹 SDK의 컨텍스트 카테고리의 일부입니다. 자세한 내용은 [Platform Web SDK 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=en) 자세한 내용

## Adobe Analytics 확장을 사용하여 높은 엔트로피 힌트를 수집합니다

**[!UICONTROL 높은 엔트로피 사용자 에이전트 힌트 수집]** Adobe Analytics 확장을 구성할 때 일반 아코디언 아래의 확인란입니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/#/@adobepm/data-collection) adobeID 자격 증명 사용.

1. 원하는 을 클릭합니다 [!UICONTROL 태그 속성].

1. 로 이동합니다. [!UICONTROL 확장] 탭을 클릭한 다음 [!UICONTROL 구성] Adobe Analytics 아래에 있습니다.

1. 를 확장합니다. [!UICONTROL 일반] 아코디언을 표시합니다. [!UICONTROL 높은 엔트로피 사용자 에이전트 힌트 수집] 확인란을 선택합니다. 기본적으로 선택되어 있지 않습니다.

## AppMeasurement의 collectHighEntropyUserAgentHints

다음 `s.collectHighEntropyUserAgentHints` 변수는 AppMeasurement가 Chromium 브라우저(예: Google Chrome 및 Microsoft Edge)에서 높은 엔트로피 힌트를 요청하는지 여부를 결정합니다. 이러한 힌트는 Adobe Analytics에서 장치 및 브라우저 식별을 개선하기 위해 사용합니다.

TRUE로 설정하면 브라우저에서 모든 높은 엔트로피 힌트가 요청됩니다.

`s.collectHighEntropyUserAgentHints = TRUE`

`s.collectHighEntropyUserAgentHints = FALSE`