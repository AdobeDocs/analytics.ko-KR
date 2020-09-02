---
title: 페이지
description: 페이지 이름.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 71%

---


# 페이지

페이지 차원은 사이트의 페이지 이름을 나열합니다. 사이트의 어느 페이지가 가장 성과가 좋은지 알 수 있도록 해주므로, Adobe Analytics에서 사용되는 가장 일반적인 차원 중 하나입니다.

이 차원은 [사이트 섹션](site-section.md) 및 [서버](server.md) 차원과 관련되어 있습니다. 페이지는 가장 세분화된 차원이고, 서버는 가장 덜 세분화된 차원이며, 사이트 섹션은 그 둘의 사이에 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 페이지 보기 호출( [`pageName` )](/help/implement/validate/query-parameters.md) 의 쿼리 문자열에서 [데이터를`t()`검색합니다](/help/implement/vars/functions/t-method.md). [링크 추적 호출(`tl()`)](/help/implement/vars/functions/tl-method.md) 은 `pageName` 쿼리 문자열이 있어도 항상 이 차원을 제거하십시오.

AppMeasurement는 [`pageName`](/help/implement/vars/page-vars/pagename.md) 변수를 사용하여 이 데이터를 수집합니다. If the `pageName` variable is not defined, it falls back to using the [`pageURL`](/help/implement/vars/page-vars/pageurl.md) variable.

## Dimension 항목

Dimension 항목에는 사이트의 페이지 이름이 포함됩니다. 조직에서 사용할 특정 차원 항목을 결정합니다. 일부 조직에서는 `document.title`을 바로 사용하는 반면, 다른 조직에서는 사용자 지정 탐색 표시를 만듭니다. 어떤 방법을 사용하든 일관된 방법을 사용하고 [솔루션 디자인 문서](/help/implement/prepare/solution-design.md)에 기록하도록 하십시오.

>[!NOTE]
>
>Reports &amp; Analytics에서 전환 지표는 이 차원에 대한 선형 속성을 사용합니다. 예를 들어, 매출은 `purchase` 이벤트 전에 방문에서 본 모든 페이지 간에 분할됩니다. Analysis Workspace는 기본적으로 임의의 속성 모델을 사용하는 옵션과 함께 마지막 속성을 사용합니다.
