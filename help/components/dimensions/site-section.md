---
title: 사이트 섹션
description: 사이트 섹션의 이름입니다.
translation-type: tm+mt
source-git-commit: 1869d69566d26aa7d99c520efc2e835901439d48
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# 사이트 섹션

&#39;사이트 섹션&#39; 차원은 사이트에 있는 사이트 섹션의 이름을 나열합니다. 대규모 사이트의 경우 페이지를 섹션으로 그룹화하는 것이 유용합니다. 이 차원은 상위 보기 또는 상위 수행 사이트 섹션을 보는 데 유용합니다.

이 차원은 [페이지](page.md) 및 [서버](server.md) 차원과관련되어 있습니다. 페이지가 가장 세분화되고, 서버가 가장 적게 세분화되며, 사이트 섹션이 둘 사이입니다.

## 데이터로 이 차원 채우기

이 차원은 이미지 요청의 [`ch` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 검색합니다. AppMeasurement는 변수를 사용하여 이 데이터를 [`channel`](/help/implement/vars/page-vars/channel.md) 수집합니다.

## 차원 값

차원 값에는 사이트의 사이트 섹션 이름이 포함됩니다. 조직에서 사용할 특정 차원 값을 결정합니다. 어떤 방법을 사용하더라도 일관된 컨텐츠를 [솔루션 디자인 문서에](/help/implement/prepare/solution-design.md)기록할 수 있습니다.
