---
title: 참조 도메인
description: 방문자가 사이트에 클릭스루하기 전에 있었던 도메인.
translation-type: tm+mt
source-git-commit: 1869d69566d26aa7d99c520efc2e835901439d48
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 1%

---


# 참조 도메인

&#39;참조 도메인&#39; 차원은 방문자가 사이트에 도달하기 위해 클릭스루하는 도메인을 보고합니다. 이 차원은 트래픽이 가장 많은 타사 사이트를 파악하는 데 유용합니다. 외부 사이트에 링크가 있어야 하며, 차원 값이 표시되려면 방문자가 링크를 클릭해야 합니다.

>[!IMPORTANT] 이 차원을 사용하려면 보고서 세트의 [내부 URL 필터를](/help/admin/admin/internal-url-filter-admin.md) 구성해야 합니다. 내부 URL 필터를 구성하지 않으면 내부 도메인을 포함하거나 외부 도메인이 표시되지 않을 수 있습니다.

## 데이터로 이 차원 채우기

이 차원은 Analytics 인터페이스에 구성되어야 하며 이미지 요청의 데이터입니다.

* 구현 내에서 이 차원은 이미지 요청의 [`r` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 검색합니다. AppMeasurement는 브라우저에서 JavaScript 변수를 사용하여 이 데이터 `document.referrer` 를 수집합니다. AppMeasurement 라이브러리(예: Adobe Experience Platform Launch)를 사용하는 경우 이 차원은 기본적으로 작동합니다. API를 통해 AppMeasurement 외부에 데이터 수집 메서드를 사용하는 경우 이미지 요청에 `r` 쿼리 문자열 매개 변수를 포함해야 합니다.
* Analytics 인터페이스 내에서 보고서 세트의 [내부 URL 필터를 구성해야 합니다](/help/admin/admin/internal-url-filter-admin.md). 내부 URL 필터를 구성하지 않으면 내부 도메인을 포함하거나 외부 도메인이 표시되지 않을 수 있습니다.

Adobe는 방문에 대한 참조 도메인을 유지합니다. 방문자가 한 방문 내에 다른 도메인에 있는 링크를 클릭하여 나가는 경우, 새 값이 업데이트되어 나머지 방문 동안 유지됩니다. 원래 값만 보려는 경우 [원래 참조 도메인을 참조하십시오](original-referring-domain.md).

## 차원 값

차원 값에는 방문자가 사이트에 클릭스루하는 도메인이 포함됩니다. 히트에 레퍼러 데이터(설정되거나 지속된)가 없으면 차원 값 아래에 그룹화됩니다 `"Typed/Bookmarked"`. 이 차원 값은 방문자가 수동으로 브라우저 주소를 주소 표시줄에 입력하거나 책갈피를 클릭하는 등 레퍼러 값이 없음을 의미합니다.
