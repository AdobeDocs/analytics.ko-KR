---
title: 사이트 섹션
description: 사이트 섹션의 이름입니다.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '137'
ht-degree: 100%

---


# 사이트 섹션

사이트 섹션 차원은 사이트에 있는 사이트 섹션의 이름을 나열합니다. 대형 사이트의 경우 페이지를 섹션으로 그룹화하는 것이 도움이 되는데, 이 차원은 상위 보기 또는 상위 성능 사이트 섹션을 보는 데 유용합니다.

이 차원은 [페이지](page.md) 및 [서버](server.md) 차원과 관련되어 있습니다. 페이지는 가장 세분화된 차원이고, 서버는 가장 덜 세분화된 차원이며, 사이트 섹션은 그 둘의 사이에 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 이미지 요청의 [`ch` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 검색합니다. AppMeasurement는 [`channel`](/help/implement/vars/page-vars/channel.md) 변수를 사용하여 이 데이터를 수집합니다.

## 차원 항목

차원 항목에는 사이트의 사이트 섹션 이름이 포함됩니다. 조직은 사용자가 사용하려는 특정 차원 항목을 파악합니다. 어떤 방법을 사용하든 일관된 방법을 사용하고 [솔루션 디자인 문서](/help/implement/prepare/solution-design.md)에 기록하도록 하십시오.
