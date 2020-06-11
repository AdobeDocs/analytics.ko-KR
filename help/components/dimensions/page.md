---
title: 페이지
description: 페이지 이름.
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---


# 페이지

&#39;페이지&#39; 차원은 사이트의 페이지 이름을 나열합니다. 사이트 내 어느 페이지가 가장 성과가 좋은 지에 대한 통찰력을 제공하므로 Adobe Analytics에서 사용되는 가장 일반적인 차원 중 하나입니다.

이 차원은 [사이트 섹션](site-section.md) 및 [서버](server.md) 차원과 관련되어 있습니다. 페이지가 가장 세분화되고, 서버가 가장 적게 세분화되며, 사이트 섹션이 둘 사이입니다.

## 데이터로 이 차원 채우기

이 차원은 이미지 요청의 [`pageName` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 검색합니다. AppMeasurement는 변수를 사용하여 이 데이터를 `pageName` 수집합니다. 변수가 `pageName` 정의되지 않은 경우 페이지의 URL을 사용하는 것으로 돌아갑니다.

## 차원 값

차원 값에는 사이트의 페이지 이름이 포함됩니다. 조직에서 사용할 특정 차원 값을 결정합니다. 어떤 조직들은 직접 사용하는 반면, 다른 조직들은 `document.title`맞춤형 곡창들을 만들어 냅니다. 어떤 방법을 사용하더라도 일관된 컨텐츠를 [솔루션 디자인 문서에](/help/implement/prepare/solution-design.md)기록할 수 있습니다.

>[!NOTE] 보고 및 분석에서 전환 지표는 이 차원에 대한 선형 속성을 사용합니다. For example, revenue is split between all pages viewed in a visit before a `purchase` event. 분석 작업 공간은 기본적으로 속성 모델을 사용하는 옵션과 함께 마지막 속성을 사용합니다.
