---
description: '처리 규칙은 컨텍스트 데이터 변수에 따라 이벤트를 트리거할 수 있습니다. '
subtopic: Processing rules
title: 컨텍스트 데이터 변수를 사용하여 이벤트 설정
feature: 관리 도구
uuid: 4a6018eb-03e2-4ec8-874b-e48bf716e103
exl-id: f0af0e23-c08a-4f82-85b4-25064eeaa3c6
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 95%

---

# 컨텍스트 데이터 변수를 사용하여 이벤트 설정

처리 규칙은 컨텍스트 데이터 변수에 따라 이벤트를 트리거할 수 있습니다. 

컨텍스트 데이터 변수는 다음 형식으로 AppMeasurement에서 지정됩니다.

```
 s.contextData['search_term']
```

[!UICONTROL 컨텍스트 변수] 목록은 이전 30일 동안 보고서 세트로 전송된 모든 변수를 포함합니다. 컨텍스트 데이터 변수 이름은 알지만, 현재 보고서 세트로 보내지 않았다면 변수 이름을 입력하고 **[!UICONTROL 변수 이름 컨텍스트 데이터 추가]**&#x200B;를 클릭하여 값을 추가할 수 있습니다.

![](assets/add-context-variable.png)

다음 규칙 정의는 [컨텍스트 데이터 변수를 eVar 규칙에 복사](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md)에서 확장하여 특정 컨텍스트 데이터 변수를 포함하는 모든 히트에 대해서도 이벤트를 설정합니다.

| 규칙 세트 | 값 |
|---|---|
| 조건 | &#39;search_term&#39; 컨텍스트 데이터가 설정된 경우 |
| 작업 | 이벤트 &#39;검색&#39; 설정 |

예:

![](assets/processing_rule_set_event.png)

구현 도움말에서 [컨텍스트 데이터 변수](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/contextdata.html)를 참조하십시오.
