---
description: Dynamic Tag Management를 사용하여 Adobe Analytics를 배포할 때의 변수에 대한 필드 설명 및 정보입니다.
keywords: Dynamic Tag Management;global variables;server variable;evar;props;dynamic variable prefix;dynamic variable
solution: Experience Cloud,Analytics,Dynamic Tag Management
title: 전역 변수
uuid: d759320a-96ee-4073-b5fd-5257b7033003
translation-type: tm+mt
source-git-commit: e9820869d16b8656ebebe11e397a3d7d8123fbcf

---


# 전역 변수

Dynamic Tag Management를 사용하여 Adobe Analytics를 배포할 때의 변수에 대한 필드 설명 및 정보입니다.

이러한 변수는 모든 페이지 로드 규칙 비콘에서 실행됩니다. 모든 페이지에서 실행되도록 설정된 [페이지 로드 규칙을](/help/implement/c-implement-with-dtm/c-rules/t-rules-page-conditions.md) 사용하여 동일한 효과를 수행할 수 있습니다. 이러한 변수는 [직접 호출](/help/implement/c-implement-with-dtm/c-rules/t-rules-direct-conditions.md) 및 [이벤트 기반](/help/implement/c-implement-with-dtm/c-rules/t-rules-event-conditions.md) 규칙으로 실행되지 않을 수 있습니다.

## 전역 변수 - 필드 설명 {#section_2917F62FCC8D43F982B2612A702DEF81}

**[!UICONTROL *`Property`*]** &gt; ![](assets/settings_gear.png) **[!UICONTROL 편집 도구]** &gt; **[!UICONTROL 전역 변수]**

| 요소 | 설명 |
|--- |--- |
| 서버 | 사전 정의된 변수가 Adobe Analytics의 서버 차원을 채웁니다. [페이지 변수](/help/implement/js-implementation/page-variables/page-variables.md)를 참조하십시오. |
| eVar | [eVar 변수](/help/implement/js-implementation/page-variables/evarn.md)는 사용자 지정 전환 보고서를 작성하는 데 사용됩니다. |
| Prop | [Prop 변수](/help/implement/js-implementation/page-variables/propn.md)는 사용자 지정 트래픽 보고서를 작성하는 데 사용됩니다. |
| 동적 변수 접두사 | 값의 시작 앞부분에 붙는 특수한 접두사입니다. 기본 접두사는 "D="입니다. [동적 변수](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/dynvars-overview.html)를 참조하십시오 |
