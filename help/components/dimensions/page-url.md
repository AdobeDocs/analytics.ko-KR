---
title: 페이지 URL
description: 페이지의 URL입니다.
exl-id: 7c0ec494-d79b-4b65-9161-bdc48485af84
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '221'
ht-degree: 100%

---

# 페이지 URL

페이지 URL 차원은 사이트의 URL을 나열합니다.

>[!IMPORTANT]
>
>이 차원은 Data Warehouse에서만 사용할 수 있습니다. 다른 Analytics 솔루션에서 URL 차원을 사용하려면 모든 히트에서 값을 [eVar](evar.md)에 복사하는 것이 좋습니다.

## 이 차원을 데이터로 채우기

이 차원은 [페이지 조회수 호출 (`t()`)](/help/implement/vars/functions/t-method.md)의 [`g` 및 `-g` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 검색합니다. [링크 추적 호출 (`tl()`)](/help/implement/vars/functions/tl-method.md)은 `g` 쿼리 문자열이 있는 경우에도 항상 이 차원을 제거합니다.

경우에 따라 URL이 255바이트보다 길 수 있습니다. AppMeasurement는 이미지 요청에 있는 URL의 처음 255바이트에 대해 `g` 쿼리 문자열 매개 변수를 사용합니다. URL이 255바이트보다 긴 경우 URL의 나머지 부분은 `-g` 쿼리 문자열 매개 변수에 저장됩니다. URL의 프로토콜 및 쿼리 문자열은 이 변수에 포함됩니다.

AppMeasurement는 페이지의 URL을 기반으로 이 데이터를 자동으로 수집합니다. [`pageURL`](/help/implement/vars/page-vars/pageurl.md) 변수를 사용하여 수집된 값을 재정의할 수 있습니다.

## eVar를 URL로 채우기

연결된 문자열 `window.location.hostname + window.location.pathname`으로 eVar를 설정하는 것이 좋습니다. 이 문자열은 일반적으로 프로토콜, 쿼리 문자열 및 앵커 태그를 생략하므로 `window.location.href`보다 잘 작동합니다.

eVar가 Data Warehouse의 “페이지 URL” 차원과 정확히 일치하도록 하려면 [동적 변수](/help/implement/vars/page-vars/dynamic-variables.md)를 사용하고 각 히트에서 eVar를 `D=g`로 설정할 수 있습니다.

## 차원 항목

차원 항목에는 사이트의 페이지 URL이 포함됩니다.
