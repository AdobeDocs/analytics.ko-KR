---
title: 페이지 URL
description: 페이지의 URL입니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 92%

---


# 페이지 URL

페이지 URL 차원은 사이트의 URL을 나열합니다.

>[!IMPORTANT]
>
>이 차원은 Data Warehouse에서만 사용할 수 있습니다. 다른 Analytics 솔루션에서 URL 차원을 사용하려면 [eVar](evar.md)를 사용하십시오.

## 이 차원을 데이터로 채우기

이 차원은 이미지 요청의 [`g` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 검색합니다. AppMeasurement는 [`pageURL`](/help/implement/vars/page-vars/pageurl.md) 변수를 사용하여 이 데이터를 수집합니다.

## eVar를 URL로 채우기

연결된 문자열 `window.location.hostname + window.location.pathname`으로 eVar를 설정하는 것이 좋습니다. 이 문자열은 일반적으로 프로토콜, 쿼리 문자열 및 앵커 태그를 생략하므로 `window.location.href`보다 잘 작동합니다.

eVar가 Data Warehouse의 &#39;페이지 URL&#39; 차원과 정확히 일치하도록 하려면 [동적 변수](/help/implement/vars/page-vars/dynamic-variables.md)를 사용하고 각 히트에서 eVar를 `D=g`로 설정할 수 있습니다. 페이지 URL이 모든 [`tl()`](/help/implement/vars/functions/tl-method.md) 호출에 대해 제거되므로 이 방법은 사용자 지정 링크 히트에 대해서는 작동하지 않습니다.

## Dimension 항목

Dimension 항목에는 사이트의 페이지 URL이 포함됩니다.
