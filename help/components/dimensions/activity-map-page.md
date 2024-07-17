---
title: Activity Map 페이지
description: 링크를 클릭할 때의 페이지 이름입니다.
feature: Dimensions
role: User, Admin
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 6%

---

# Activity Map 페이지

&#39;Activity Map 페이지&#39; [차원](overview.md)은(는) 링크를 클릭할 때 방문자가 있었던 페이지를 표시합니다. 이 차원을 사용하여 가장 많이 클릭되는 링크가 포함된 페이지를 결정할 수 있습니다. 이 차원은 표시할 링크를 결정하기 위해 Activity Map 오버레이에서도 사용됩니다.

## 이 차원을 데이터로 채우기

이 차원은 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md) `c.a.activitymap.page`에서 데이터를 검색합니다. 구현에서 [Activity Map](/help/analyze/activity-map/overview.md)을 사용하는 경우, 이 컨텍스트 데이터 변수는 링크를 클릭할 때 자동으로 데이터를 수집합니다.

클릭한 특정 링크에 대해 이 컨텍스트 데이터 변수는 [Page](page.md) 차원의 값을 수집합니다. 페이지 차원에 값이 없으면 대신 [페이지 URL](page-url.md) 차원이 사용됩니다(페이지 차원이 사용하는 대체 항목과 유사). Activity Map 데이터는 일반적으로 링크를 클릭한 후 다음 히트에서 전송됩니다. 이 차원을 사용하면 데이터를 전송할 때 페이지 값 대신 링크를 클릭했을 때의 페이지 값을 결정할 수 있습니다.

## 차원 항목

Dimension 항목에는 [Page](page.md) 차원에 있는 모든 값이 포함됩니다.
