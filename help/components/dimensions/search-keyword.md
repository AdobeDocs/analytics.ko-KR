---
title: 검색 키워드
description: 방문자가 사이트에 도달하기 위해 사용한 검색 키워드입니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 78%

---


# 검색 키워드

검색 키워드 차원은 방문자가 사이트에 도달하기 위해 사용하는 검색 키워드를 보고합니다.

>[!IMPORTANT]
>
>개인 정보 보호 정책이 강화됨에 따라 대부분의 검색 엔진이 더 이상 검색 키워드를 전달하지 않습니다. Hits where Adobe recognizes a search engine but is missing a keyword groups under the dimension item `"Keyword unavailable"`.

레퍼러는 다음 두 항목을 모두 충족해야 검색 키워드로 분류할 수 있습니다.

* 참조 도메인이 Adobe에 의해 유효한 [검색 엔진](search-engine.md)으로 인식됩니다.
* 키워드 쿼리 문자열 매개 변수가 참조 URL에 있습니다. If the keyword query string exists but does not contain a value, it groups under the dimension item `"Keyword unavailable"`.

유료 검색과 자연어 검색을 구분하려면 [유료 검색 감지](/help/admin/admin/paid-search-detection/paid-search-detection.md)가 필요합니다. 검색 키워드에 여러 차원을 사용할 수 있습니다.

* **검색 키워드**: 유료 검색인지 또는 자연어 검색인지에 상관없이 사이트에 도달하기 위해 사용되는 검색 키워드입니다.
* **검색 키워드 - 유료**: 사이트에 도달하기 위해 사용된 검색 키워드로서 유료 검색 감지와 일치합니다.
* **검색 키워드 - 자연어**: 사이트에 도달하기 위해 사용된 검색 키워드로서 유료 검색 감지와 일치하지 않습니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 여러 조회 테이블을 참조합니다. 각 값은 히트의 [레퍼러](referrer.md)를 기반으로 하는데, 이것은 [내부 URL 필터](/help/admin/admin/internal-url-filter-admin.md)에 따라 달라집니다. 레퍼러 차원과 내부 URL 필터가 올바로 구성되어 있는지 확인하십시오.

## Dimension 항목

Dimension 항목에는 사이트에 도달하는 데 사용되는 검색 키워드가 포함됩니다. The `"Unspecified"` dimension item is all non-search traffic.
