---
description: Dynamic Tag Management를 사용하여 Adobe Analytics를 배포할 때의 변수에 대한 필드 설명 및 정보입니다.
keywords: Dynamic Tag Management;전역 변수;서버 변수;evar;props;동적 변수 접두어;동적 변수
solution: Experience Cloud,Analytics
title: 전역 변수
uuid: d759320a-96ee-4073-b5fd-5257b7033003
exl-id: e78e9ff4-bfce-4fa0-8d53-fd33ed3052fd
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '150'
ht-degree: 100%

---

# 전역 변수

Dynamic Tag Management를 사용하여 Adobe Analytics를 배포할 때의 변수에 대한 필드 설명 및 정보입니다.

이러한 변수는 모든 페이지 로드 규칙 비콘에서 실행됩니다. 모든 페이지에서 실행되도록 설정된 [페이지 로드 규칙을](/help/implement/other/dtm/c-rules/t-rules-page-conditions.md) 사용하여 동일한 효과를 수행할 수 있습니다. 이러한 변수는 [직접 호출](/help/implement/other/dtm/c-rules/t-rules-direct-conditions.md) 및 [이벤트 기반](/help/implement/other/dtm/c-rules/t-rules-event-conditions.md) 규칙으로 실행되지 않을 수 있습니다.

## 전역 변수 - 필드 설명 {#section_2917F62FCC8D43F982B2612A702DEF81}

**[!UICONTROL *`Property`*]**> ![](assets/settings_gear.png)**[!UICONTROL &#x200B;편집 도구&#x200B;]**>**[!UICONTROL &#x200B;전역 변수&#x200B;]**

| 요소 | 설명 |
|--- |--- |
| 서버 | 사전 정의된 변수가 Adobe Analytics의 서버 차원을 채웁니다. [서버](../../../vars/page-vars/server.md)를 참조하십시오. |
| eVar | [eVar 변수](../../../vars/page-vars/evar.md)는 사용자 지정 전환 보고서를 작성하는 데 사용됩니다. |
| Prop | [Prop 변수](../../../vars/page-vars/prop.md)는 사용자 지정 트래픽 보고서를 작성하는 데 사용됩니다. |
| 동적 변수 접두사 | 값의 시작 앞부분에 붙는 특수한 접두사입니다. 기본 접두사는 &quot;D=&quot;입니다. 참조: [동적 변수] (../../../vars/page-vars/dynamic-variables.md) |
