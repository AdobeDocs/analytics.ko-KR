---
description: '처리 규칙은 컨텍스트 데이터 변수에 따라 이벤트를 트리거할 수 있습니다. '
seo-description: '처리 규칙은 컨텍스트 데이터 변수에 따라 이벤트를 트리거할 수 있습니다. '
seo-title: 컨텍스트 데이터 변수를 사용하여 이벤트 설정
solution: Analytics
subtopic: 처리 규칙
title: 컨텍스트 데이터 변수를 사용하여 이벤트 설정
topic: 관리 도구
uuid: 4a6018eb-03e2-4ec8-874b-e48bf716e103
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 컨텍스트 데이터 변수를 사용하여 이벤트 설정

처리 규칙은 컨텍스트 데이터 변수에 따라 이벤트를 트리거할 수 있습니다. 

컨텍스트 데이터 변수는 다음 형식으로 AppMeasurement에서 지정됩니다.

```
 s.contextData['search_term']
```

[!UICONTROL 컨텍스트 변수] 목록은 이전 30일 동안 보고서 세트로 전송된 모든 변수를 포함합니다. If you know the context data variable name but have not sent it into the current report suite, you can add a value by typing the variable name and clicking **[!UICONTROL Add variable name context data]**:

![](assets/add-context-variable.png)

다음 규칙 정의는 컨텍스트 데이터 변수 [복사를 eVar](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md) 규칙으로 확장하여 특정 컨텍스트 데이터 변수를 포함하는 모든 히트에 대해서도 이벤트를 설정합니다.

| 규칙 세트 | 값 |
|---|---|
| 조건 | 'search_term' 컨텍스트 데이터가 설정된 경우 |
| 작업 | 이벤트 '검색' 설정 |

예:

![](assets/processing_rule_set_event.png)

구현 도움말에서 [컨텍스트 데이터 변수](https://marketing.adobe.com/resources/help/en_US/sc/implement/context_data_variables.html)를 참조하십시오.
