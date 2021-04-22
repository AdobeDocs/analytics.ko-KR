---
title: 레퍼러
description: 방문자가 사이트를 클릭스루하기 전에 있었던 URL입니다.
exl-id: 146f0327-c73c-40f5-8cc1-584e31d163a2
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '448'
ht-degree: 100%

---

# 레퍼러

레퍼러 차원은 방문자가 사이트에 도달하기 위해 클릭스루할 때 있었던 URL을 보고합니다. 이 차원은 사이트로 들어오는 트래픽이 가장 많은 특정 URL을 이해하는 데 유용합니다. 링크는 외부 URL에 있어야 하며, 방문자가 링크를 클릭하여 차원 항목을 표시해야 합니다.

>[!IMPORTANT]
>
>이 차원을 사용하려면 보고서 세트의 [내부 URL 필터](/help/admin/admin/internal-url-filter-admin.md)를 구성해야 합니다. 내부 URL 필터를 구성하지 않으면 내부 URL이 포함되거나 외부 URL이 표시되지 않을 수 있습니다.

동일한 보고서가 Analysis Workspace와 Data Warehouse 간에 다른 결과를 보여줄 수 있습니다. Analysis Workspace는 내부 URL 필터와 일치하는 값을 제외하고 각 개별 페이지에 대한 레퍼러를 보고합니다. Data Warehouse는 방문의 첫 번째 레퍼러만 보고하고 내부 URL 필터는 무시합니다.

## 이 차원을 데이터로 채우기

이 차원에서는 Analytics 인터페이스에서의 구성과 이미지 요청의 데이터가 필요합니다.

* 구현 내에서 이 차원은 이미지 요청의 [`r` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 검색합니다. AppMeasurement는 브라우저에서 JavaScript 변수 `document.referrer`를 사용하여 이 데이터를 수집합니다. [`referrer`](/help/implement/vars/page-vars/referrer.md) 변수 재정의를 사용하여 변수를 수동으로 설정할 수 있습니다. AppMeasurement 라이브러리를 사용하는 경우 (Adobe Experience Platform Launch 등을 통해) 이 차원은 즉시 작동합니다. AppMeasurement 외부의 데이터 수집 방법을 사용하는 경우 (API 등을 통해)에는 이미지 요청에 `r` 쿼리 문자열 매개 변수를 포함해야 합니다.
* Analytics 인터페이스 내에서는 보고서 세트의 [내부 URL 필터](/help/admin/admin/internal-url-filter-admin.md)를 구성해야 합니다. 내부 URL 필터를 구성하지 않으면 내부 URL이 포함되거나 외부 URL이 표시되지 않을 수 있습니다.

## 차원 항목

차원 항목에는 방문자가 사이트를 클릭스루하는 URL이 포함됩니다. 히트에 레퍼러 데이터가 없으면 이 히트는 차원 항목 `"Typed/Bookmarked"` 아래에 그룹화됩니다. 이 차원 항목은 방문자가 수동으로 브라우저 주소를 주소 표시줄에 입력하거나 책갈피를 클릭하는 등의 경우와 같이 레퍼러 값이 없음을 의미합니다. Analytics를 수용하지 않는 리디렉션에 대해서도 `"Typed/Bookmarked"` 차원 항목이 나타납니다. 기술 정보 사용 안내서에서 [리디렉션 및 별칭](/help/technotes/redirects.md)을 참조하십시오.

### `googleusercontent.com`을 포함하는 차원 항목

사용자는 도메인 `googleusercontent.com`이 있는 차원 항목을 볼 수 있습니다.

* **캐시된 페이지**: Google의 스파이더는 오프라인 상태가 될 경우에 대비해 끊임없이 웹을 크롤링하고 페이지 사본을 저장합니다. 이러한 캐시된 페이지는 &quot;캐시됨&quot; 링크를 클릭하여 대부분의 검색 결과 옆에서 사용할 수 있습니다. 사용자가 이 링크를 클릭하고 Google에서 캐시한 콘텐츠를 볼 때에는 `webcache.googleusercontent.com`이 일반적인 차원 항목입니다.
* **번역된 페이지**: Google은 강력하고 편리한 번역 서비스를 제공합니다. 이 서비스를 사용하여 사이트를 보는 경우 `translate.googleusercontent.com`에서 사이트가 전송됩니다. 이 차원 항목은 사용자가 링크를 클릭하여 원래 콘텐츠로 돌아가는 경우 나타납니다.
