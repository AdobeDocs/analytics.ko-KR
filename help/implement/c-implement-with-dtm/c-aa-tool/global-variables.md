---
description: 다이내믹 태그 관리를 사용하여 Adobe Analytics를 배포할 때의 변수에 대한 필드 설명 및 정보입니다.
keywords: 다이내믹 태그 관리; 전역 변수; server 변수; Evar; prop; 동적 변수 접두사; 동적 변수
seo-description: 다이내믹 태그 관리를 사용하여 Adobe Analytics를 배포할 때의 변수에 대한 필드 설명 및 정보입니다.
seo-title: 전역 변수
solution: Marketing Cloud, 분석, 다이내믹 태그 관리
title: 전역 변수
uuid: D 759320 A -96 EE -4073-B 5 FD -5257 B 7033003
translation-type: tm+mt
source-git-commit: 3489f00bd7dddefda0420fc361056416f6f10d3f

---


# 전역 변수

다이내믹 태그 관리를 사용하여 Adobe Analytics를 배포할 때의 변수에 대한 필드 설명 및 정보입니다.

모든 페이지 로드 규칙 비콘을 클릭하면 이러한 변수가 작동합니다. 모든 페이지에서 작동하도록 설정된 [페이지 로드 규칙](../../../implement/c-implement-with-dtm/c-rules/t-rules-page-conditions.md#task_69B41CB230EE4530A755D91233F73706)을 사용해도 동일한 결과를 얻을 수 있습니다. These variables might not fire in [Direct-Call](../../../implement/c-implement-with-dtm/c-rules/t-rules-direct-conditions.md#task_85EB8F01775A402BA53B8298F0AADA09) and [Event-Based](../../../implement/c-implement-with-dtm/c-rules/t-rules-event-conditions.md#task_A122DE72110F4579A91F9D96D92D39FC) rules.

## 전역 변수 - 필드 설명 {#section_2917F62FCC8D43F982B2612A702DEF81}

**[!UICONTROL *`Property`*]** &gt; ![](assets/settings_gear.png)**[!UICONTROL 편집 도구]** &gt; **[!UICONTROL 전역 변수]**

| 요소 | 설명 |
|--- |--- |
| 서버 | 사전 정의된 변수는 Adobe Analytics의 서버 차원을 채웁니다. [페이지 변수 참조](/help/implement/js-implementation/c-variables/page-variables.md) |
| eVar | [Evar 변수는](/help/implement/js-implementation/c-variables/page-variables.md) 사용자 지정 전환 보고서를 작성하는 데 사용됩니다. |
| Prop | [prop 변수는](/help/implement/js-implementation/c-variables/page-variables.md) 사용자 지정 트래픽 보고서를 작성하는 데 사용됩니다. |
| 동적 변수 접두사 | 값의 시작 앞부분에 붙는 특수한 접두사입니다. 기본 접두사는 "D="입니다. [동적 변수](/help/implement/js-implementation/c-variables/dynvars-overview.md)를 참조하십시오 |
