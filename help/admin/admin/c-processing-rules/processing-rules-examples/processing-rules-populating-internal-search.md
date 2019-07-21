---
description: 'q와 같은 일반적인 변수를 사용하는 경우, 검색어를 채우기 위해 처리 규칙을 사용하여 해당 값으로 내부 검색어 evar를 채울 수 있습니다. '
seo-description: 'q와 같은 일반적인 변수를 사용하는 경우, 검색어를 채우기 위해 처리 규칙을 사용하여 해당 값으로 내부 검색어 evar를 채울 수 있습니다. '
seo-title: 쿼리 문자열 매개 변수를 사용하여 내부 검색어 채우기
solution: Analytics
subtopic: 처리 규칙
title: 쿼리 문자열 매개 변수를 사용하여 내부 검색어 채우기
topic: 관리 도구
uuid: 05 AE 2 B 0 A -8797-468 C -8 F 59-643 BEAC 614 C 5
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

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

