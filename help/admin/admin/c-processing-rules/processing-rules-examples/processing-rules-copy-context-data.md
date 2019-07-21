---
description: 처리 규칙을 사용하여 컨텍스트 데이터 변수의 값을 props 및 eVars로 이동합니다.
seo-description: 처리 규칙을 사용하여 컨텍스트 데이터 변수의 값을 props 및 eVars로 이동합니다.
seo-title: Evar에 컨텍스트 데이터 변수 복사
solution: Analytics
subtopic: 처리 규칙
title: Evar에 컨텍스트 데이터 변수 복사
topic: 관리 도구
uuid: 1 Beaec 4 C -71 E 9-49 CE-B 154-78408 CC 532 A 3
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Evar에 컨텍스트 데이터 변수 복사

처리 규칙을 사용하여 컨텍스트 데이터 변수의 값을 props 및 eVars로 이동합니다.

컨텍스트 데이터 변수는 다음 형식으로 AppMeasurement에서 지정됩니다.

```
 s.contextData['search_term']
```

[!UICONTROL 컨텍스트 변수] 목록은 이전 30일 동안 보고서 세트로 전송된 모든 변수를 포함합니다. If you know the context data variable name but have not sent it into the current report suite, you can add a value by typing the variable name and clicking **[!UICONTROL Add variable name context data]**:

![](assets/add-context-variable.png)

다음 규칙 정의는 특정 컨텍스트 데이터 변수를 포함하는 모든 히트의 evar를 채웁니다.

| 규칙 세트 | 값 |
|---|---|
| 조건 | 'search_term' 컨텍스트 데이터가 설정된 경우 |
| 작업 | eVar3 값을 'search_term'으로 덮어쓰기 |

예:

![](assets/set-context-data.png)

구현 도움말에서 [컨텍스트 데이터 변수](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=context_data_variables)를 참조하십시오.
