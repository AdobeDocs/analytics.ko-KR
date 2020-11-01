---
title: 페이지 URL
description: 페이지의 URL입니다.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 69%

---


# 페이지 URL

페이지 URL 차원은 사이트의 URL을 나열합니다.

>[!IMPORTANT]
>
>이 차원은 Data Warehouse에서만 사용할 수 있습니다. 다른 Analytics 솔루션에서 URL 차원을 사용하려면 모든 히트에서 값을 [eVar](evar.md) 로 복사하는 것이 좋습니다.

## 이 차원을 데이터로 채우기

This dimension retrieves data from the [`g` and `-g` query strings](/help/implement/validate/query-parameters.md) in [Page view calls (`t()`)](/help/implement/vars/functions/t-method.md). [링크 추적 호출(`tl()`)](/help/implement/vars/functions/tl-method.md) 은 `g` 쿼리 문자열이 있어도 항상 이 차원을 제거하십시오.

경우에 따라 URL이 255바이트보다 길 수 있습니다. AppMeasurement는 이미지 요청에 있는 URL의 처음 255바이트에 대해 `g` 쿼리 문자열 매개 변수를 사용합니다. URL이 255바이트보다 긴 경우 URL의 나머지 부분은 `-g` 쿼리 문자열 매개 변수에 저장됩니다. URL의 프로토콜 및 쿼리 문자열은 이 변수에 포함됩니다.

AppMeasurement는 페이지의 URL에 따라 이 데이터를 자동으로 수집합니다. 변수를 사용하여 수집된 값을 대체할 수 [`pageURL`](/help/implement/vars/page-vars/pageurl.md) 있습니다.

## eVar를 URL로 채우기

연결된 문자열 `window.location.hostname + window.location.pathname`으로 eVar를 설정하는 것이 좋습니다. 이 문자열은 일반적으로 프로토콜, 쿼리 문자열 및 앵커 태그를 생략하므로 `window.location.href`보다 잘 작동합니다.

eVar가 Data Warehouse의 &#39;페이지 URL&#39; 차원과 정확히 일치하도록 하려면 [동적 변수](/help/implement/vars/page-vars/dynamic-variables.md)를 사용하고 각 히트에서 eVar를 `D=g`로 설정할 수 있습니다.

## 차원 항목

차원 항목에는 사이트의 페이지 URL이 포함됩니다.
