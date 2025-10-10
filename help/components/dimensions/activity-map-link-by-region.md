---
title: 지역별 Activity Map 링크
description: 링크 및 영역의 연결된 값.
feature: Dimensions
role: User, Admin
exl-id: 33014dc1-da4e-47b7-b73c-3e89e04f3ed6
source-git-commit: bcab98e453247c74b7d96497d34e6aea9ca32bc7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 11%

---

# 지역별 Activity Map 링크

&#39;지역별 Activity Map 링크&#39; [차원](overview.md)에는 [Activity Map 링크](activity-map-link.md)와 [Activity Map 지역](activity-map-link-by-region.md)의 연결이 표시됩니다. 이 차원은 이름이 유사하지만 사이트의 다른 영역에 있는 링크가 있을 때 유용합니다. 예를 들어, 홈 페이지에 모두 &quot;홈&quot;이라는 레이블이 지정된 링크가 여러 개 있는 경우 이 차원을 사용하여 각 사이트 지역의 링크를 구분할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md) `c.a.activitymap.link` 및 `c.a.activitymap.region`에서 데이터를 검색합니다. 이 두 값은 파이프(`|`)로 연결되고 구분됩니다. 구현에서 [Activity Map](/help/analyze/activity-map/overview.md)을 사용하는 경우 이러한 컨텍스트 데이터 변수는 링크를 클릭할 때 자동으로 데이터를 수집합니다.

## 차원 항목

Dimension 항목에는 [Activity Map 링크](activity-map-link.md) 및 [Activity Map 지역](activity-map-link-by-region.md)의 값이 포함됩니다. 조직의 사이트 구조 및 구현은 수집된 정확한 값을 결정합니다.
