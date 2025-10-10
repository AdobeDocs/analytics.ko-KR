---
description: 클릭한 링크 이름입니다.
title: Activity Map 링크
uuid: 67864bf9-33cd-46fa-89a8-4d83d3b81152
feature: Dimensions
role: User, Admin
exl-id: 6aef3a0f-d0dd-4c84-ad44-07b286edbe18
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 8%

---

# Activity Map 링크

&#39;Activity Map 링크&#39; [차원](overview.md)은(는) 클릭한 가장 인기 있는 링크를 표시합니다. 이 차원을 사용하면 링크를 클릭한 위치에 관계없이 사이트에서 가장 많이 사용되는 링크를 비교할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md) `c.a.activitymap.link`에서 데이터를 검색합니다. 구현에서 [Activity Map](/help/analyze/activity-map/overview.md)을 사용하는 경우, 이 컨텍스트 데이터 변수는 링크를 클릭할 때 자동으로 데이터를 수집합니다.

클릭한 특정 링크에 대해 Activity Map은 다음 링크를 (순서대로) 검색합니다.

1. `s_objectID` 변수
1. 링크의 내부 텍스트
1. 이미지에 대한 `alt` 특성
1. `title` 특성
1. 이미지에 대한 `src` 특성
1. 양식에 대한 `action` 특성

클릭된 요소에 위의 기준이 포함되어 있지 않으면 Activity Map은 해당 클릭에 대한 데이터를 수집하지 않습니다.

## 차원 항목

Dimension 항목에는 방문자가 클릭하는 링크 텍스트 또는 기타 링크 속성이 포함됩니다. 조직의 사이트 구조 및 구현은 수집된 정확한 값을 결정합니다.
