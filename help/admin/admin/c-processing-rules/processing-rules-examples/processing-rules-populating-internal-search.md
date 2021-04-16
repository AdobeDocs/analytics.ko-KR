---
description: 'q와 같은 일반적인 변수를 사용하는 경우, 검색어를 채우기 위해 처리 규칙을 사용하여 해당 값으로 내부 검색어 evar를 채울 수 있습니다. '
subtopic: Processing rules
title: 쿼리 문자열 매개 변수를 사용하여 내부 검색어 채우기
feature: 관리 도구
uuid: 05ae2b0a-8797-468c-8f59-643beac614c5
exl-id: bc7cc712-0f2a-4260-a82c-ad0e48149e73
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 100%

---

# 쿼리 문자열 매개 변수를 사용하여 내부 검색어 채우기

q와 같은 일반적인 변수를 사용하는 경우, 검색어를 채우기 위해 처리 규칙을 사용하여 해당 값으로 내부 검색어 evar를 채울 수 있습니다. 

쿼리 문자열 값은 처리 규칙에서 읽도록 유니코드 또는 UTF-8로 인코딩해야 합니다.

| 규칙 세트 | 값 |
|---|---|
| 조건 | 쿼리 문자열 매개 변수 q가 설정된 경우 |
| 작업 | 내부 검색어 값을 쿼리 문자열 매개 변수 q로 덮어쓰기 |

예:

![](assets/populate-internal-search-terms.png)
