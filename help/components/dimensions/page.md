---
title: 페이지
description: 페이지 이름.
exl-id: 579963c8-8460-425f-b716-3b30d7a259af
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '212'
ht-degree: 100%

---

# 페이지

페이지 차원은 사이트의 페이지 이름을 나열합니다. 사이트의 어느 페이지가 가장 성과가 좋은지 알 수 있도록 해주므로, Adobe Analytics에서 사용되는 가장 일반적인 차원 중 하나입니다.

이 차원은 [사이트 섹션](site-section.md) 및 [서버](server.md) 차원과 관련되어 있습니다. 페이지는 가장 세분화된 차원이고, 서버는 가장 덜 세분화된 차원이며, 사이트 섹션은 그 둘의 사이에 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 [페이지 조회수 호출 (`t()`)](/help/implement/vars/functions/t-method.md)의 [`pageName` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 검색합니다. [링크 추적 호출 (`tl()`)](/help/implement/vars/functions/tl-method.md)은 `pageName` 쿼리 문자열이 있는 경우에도 항상 이 차원을 제거합니다.

AppMeasurement는 [`pageName`](/help/implement/vars/page-vars/pagename.md) 변수를 사용하여 이 데이터를 수집합니다. `pageName` 변수가 정의되지 않은 경우 [`pageURL`](/help/implement/vars/page-vars/pageurl.md) 변수를 사용하는 방식으로 후퇴합니다.

## 차원 항목

차원 항목에는 사이트의 페이지 이름이 포함됩니다. 조직은 사용자가 사용하려는 특정 차원 항목을 파악합니다. 일부 조직에서는 `document.title`을 바로 사용하는 반면, 다른 조직에서는 사용자 지정 탐색 표시를 만듭니다. 어떤 방법을 사용하든 일관된 방법을 사용하고 [솔루션 디자인 문서](/help/implement/prepare/solution-design.md)에 기록하도록 하십시오.

>[!NOTE]
>
>Reports &amp; Analytics에서 전환 지표는 이 차원에 대한 선형 속성을 사용합니다. 예를 들어, 매출은 `purchase` 이벤트 전에 방문에서 본 모든 페이지 간에 분할됩니다. Analysis Workspace는 기본적으로 임의의 속성 모델을 사용하는 옵션과 함께 마지막 속성을 사용합니다.
