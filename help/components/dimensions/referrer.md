---
title: 레퍼러
description: 방문자가 사이트를 클릭스루하기 전에 있었던 URL.
translation-type: tm+mt
source-git-commit: 6778dd290424651dc959224daa0eef8ebd8196e5
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 5%

---


# 레퍼러

&#39;레퍼러&#39; 차원은 방문자가 사이트에 도달하기 위해 클릭스루할 때 있었던 URL을 보고합니다. 이 차원은 사이트 트래픽이 가장 많은 특정 URL을 이해하는 데 유용합니다. 외부 URL에 링크가 있어야 하며, 방문자가 차원 항목을 표시하려면 링크를 클릭해야 합니다.

>[!IMPORTANT]
>
>이 차원을 사용하려면 보고서 세트의 [내부 URL 필터를](/help/admin/admin/internal-url-filter-admin.md) 구성해야 합니다. 내부 URL 필터를 구성하지 않으면 내부 URL이 포함되거나 외부 URL이 표시되지 않을 수 있습니다.

동일한 보고서는 Analysis Workspace과 Data warehouse 간에 다른 결과를 표시할 수 있습니다. Analysis Workspace은 내부 URL 필터와 일치하는 값을 제외하고 각 개별 페이지에 대한 레퍼러를 보고합니다. Data warehouse은 방문의 첫 번째 레퍼러만 보고하고 내부 URL 필터를 무시합니다.

## 데이터로 이 차원 채우기

이 차원에서는 Analytics 인터페이스 및 이미지 요청의 데이터를 구성해야 합니다.

* 구현 내에서 이 차원은 이미지 요청의 [`r` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 검색합니다. AppMeasurement는 브라우저에서 JavaScript 변수를 사용하여 이 데이터 `document.referrer` 를 수집합니다. AppMeasurement 라이브러리(예: Adobe Experience Platform Launch을 통해)를 사용하는 경우 이 차원은 기본적으로 작동합니다. API를 통해 AppMeasurement 외부에 데이터 수집 메서드를 사용하는 경우 이미지 요청에 `r` 쿼리 문자열 매개 변수를 포함해야 합니다.
* Analytics 인터페이스 내에서 보고서 세트의 [내부 URL 필터를 구성해야 합니다](/help/admin/admin/internal-url-filter-admin.md). 내부 URL 필터를 구성하지 않으면 내부 URL이 포함되거나 외부 URL이 표시되지 않을 수 있습니다.

## Dimension 항목

Dimension 항목에는 방문자가 사이트를 클릭스루하는 URL이 포함됩니다. 히트에 레퍼러 데이터가 없는 경우 차원 항목 아래에 그룹화됩니다 `"Typed/Bookmarked"`. 이 차원 항목은 방문자가 브라우저 주소를 주소 표시줄에 수동으로 입력하거나 책갈피를 클릭하는 경우와 같이 레퍼러 값이 없음을 의미합니다.

### Dimension 항목 `googleusercontent.com`

사용자는 도메인이 있는 차원 항목을 볼 수 있습니다 `googleusercontent.com`.

* **캐시된 페이지**: 구글의 스파이더는 오프라인일 경우에 대비해 끊임없이 웹을 탐색하고 페이지 사본을 저장한다. 이러한 캐시된 페이지는 &quot;캐시됨&quot; 링크를 클릭하여 대부분의 검색 결과 옆에 있습니다. 사용자가 이 링크를 클릭하고 Google에서 캐시한 컨텐츠를 보면 일반적인 차원 항목 `webcache.googleusercontent.com` 이 됩니다.
* **번역된 페이지**: Google은 강력하고 편리한 번역 서비스를 제공합니다. 이 서비스를 사용하여 사이트를 보는 경우 `translate.googleusercontent.com`에서 사이트가 전송됩니다. 이 차원 항목은 사용자가 링크를 클릭하여 원래 컨텐츠로 돌아가는 경우 나타납니다.
