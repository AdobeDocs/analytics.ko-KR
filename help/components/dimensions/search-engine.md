---
title: 검색 엔진
description: 방문자가 사이트에 도달하기 위해 사용한 검색 엔진입니다.
feature: Dimensions
exl-id: 2815f1fa-d938-4d2b-b864-c4ed834f3ed3
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 93%

---

# 검색 엔진

&#39;검색 엔진&#39; [차원](overview.md)은(는) 방문자가 사이트에 도달하기 위해 사용하는 검색 엔진을 보고합니다. 레퍼러는 다음 두 항목을 모두 충족해야 검색 엔진으로 분류할 수 있습니다.

* 참조 도메인이 Adobe에 의해 유효한 검색 엔진으로 인식됩니다.
* 키워드 쿼리 문자열 매개 변수가 참조 URL에 있습니다. 쿼리 문자열 매개 변수는 비워 둘 수 있습니다 (개인 정보 보호 방침으로 인해 여러 검색 엔진이 있는 경우).

유료 검색과 자연어 검색을 구분하려면 [유료 검색 감지](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/paid-search-detection.md)가 필요합니다. 검색 엔진에 여러 차원을 사용할 수 있습니다.

* **검색 엔진**: 유료 검색인지 또는 자연어 검색인지에 상관없이 사이트에 도달하기 위해 사용되는 검색 엔진입니다.
* **검색 엔진 - 유료**: 사이트에 도달하기 위해 사용된 검색 엔진으로서 유료 검색 감지와 일치합니다.
* **검색 엔진 - 자연어**: 사이트에 도달하기 위해 사용된 검색 엔진으로서 유료 검색 감지와 일치하지 않습니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 여러 조회 테이블을 참조합니다. 각 값은 히트의 [레퍼러](referrer.md)를 기반으로 하는데, 이것은 [내부 URL 필터](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md)에 따라 달라집니다. 레퍼러 차원과 내부 URL 필터가 올바로 구성되어 있는지 확인하십시오.

## 차원 항목

차원 항목에는 사이트에 도달하기 위해 사용되는 검색 엔진이 포함됩니다. 값의 예로는 `"Google"`, `"Microsoft Bing"` 및 `"DuckDuckGo"`이 있습니다. `"Unspecified"` 차원 항목은 모든 비검색 트래픽입니다.
