---
title: 서버
description: 서버 이름입니다.
translation-type: tm+mt
source-git-commit: 1869d69566d26aa7d99c520efc2e835901439d48
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 1%

---


# 서버

&#39;서버&#39; 차원은 일반적으로 사이트의 호스트 이름을 나열합니다. 여러 도메인 또는 하위 도메인을 결합하는 보고서 세트의 경우, 이 차원은 성과가 가장 좋은 도메인 또는 하위 도메인을 확인하는 데 유용합니다.

이 차원은 [페이지](page.md) 및 [사이트 섹션](site-section.md) 차원과 관련되어 있습니다. 페이지가 가장 세분화되고, 서버가 가장 적게 세분화되며, 사이트 섹션이 둘 사이입니다.

## 데이터로 이 차원 채우기

이 차원은 이미지 요청의 [`server` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 검색합니다. AppMeasurement는 변수를 사용하여 이 데이터를 [`server`](/help/implement/vars/page-vars/server.md) 수집합니다.

## 차원 값

차원 값에는 사이트의 서버가 포함됩니다. 조직에서 사용할 특정 차원 값을 결정합니다. 일부 조직은 사용자 지정 값 `window.location.hostname`을 작성하는 반면, 다른 조직에서는 사용자 지정 값을 사용합니다. 어떤 방법을 사용하더라도 일관된 컨텐츠를 [솔루션 디자인 문서에](/help/implement/prepare/solution-design.md)기록할 수 있습니다.
