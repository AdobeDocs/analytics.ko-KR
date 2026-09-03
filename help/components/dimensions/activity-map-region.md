---
title: Activity Map 영역
description: 클릭한 사이트의 영역입니다.
feature: Dimensions
role: User, Admin
exl-id: e262e537-ce73-492a-8ab3-b88cd77cb8c5
TQID: https://experienceleague.adobe.com/mmLp5-dgKGeovIOMPZxliyhfbpUSMLXca-3Qs6QA0SA
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 249
ht-degree: 5%

---

# Activity Map 영역

&#39;Activity Map 영역&#39; [차원](overview.md)은(는) 사이트에서 가장 많이 클릭한 영역을 표시합니다. 이 차원은 개별 링크 대신 사이트의 중요한 영역에서 클릭을 비교하려는 경우에 유용합니다. 동적 콘텐츠를 제공하는 사이트 영역에도 유용합니다. 예를 들어 순환 뉴스 기사가 있는 첫 페이지가 있는 경우 링크 텍스트가 지속적으로 변경되므로 [Activity Map 링크](activity-map-link.md) 차원을 사용하는 것은 어렵습니다. 그러나 이러한 링크는 동일한 영역을 사용하므로 개별 링크가 매일 변경될 수 있더라도 해당 영역의 성능을 분석할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md) `c.a.activitymap.region`에서 데이터를 검색합니다. 구현에서 [Activity Map](/help/analyze/activity-map/overview.md)을 사용하는 경우, 이 컨텍스트 데이터 변수는 링크를 클릭할 때 자동으로 데이터를 수집합니다.

클릭된 특정 링크에 대해 상위 DOM 요소에서 다음 (순서대로)을 확인하십시오.

* [`ActivityMap.regionIDAttribute`](/help/implement/vars/config-vars/activitymap-regionidattribute.md)이(가) 설정한 특성 값 - 기본적으로 `id` 특성으로 설정됨
* `role="region"` 특성을 사용하는 경우 `aria-label` 특성의 값입니다.
* 의미 체계 요소 `<header>`, `<main>`, `<footer>` 또는 `<nav>`(웹 SDK 전용)

상위 DOM 요소가 위의 기준 중 어느 것도 충족하지 않는 경우 DOM 계층 위쪽으로 계속 재귀적으로 검색합니다. 일치하는 요소가 없으면 값 `BODY`이(가) 반환됩니다.

## 차원 항목

Dimension 항목에는 사이트에서 레이블을 지정한 영역이 포함됩니다. 특정 영역 값은 사용되는 특성과 의미 체계 HTML 요소가 있는지 여부에 따라 달라집니다.
