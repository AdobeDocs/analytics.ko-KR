---
title: 모바일 라이프사이클 차원
description: Mobile SDK를 사용하여 수집된 데이터를 기반으로 한 Dimension.
feature: Dimensions
exl-id: b7ba45d7-7d30-48a3-a747-ea9fbb253abb
source-git-commit: d940428e1cbe1be6d8263e986e8b641ec18aace1
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 57%

---

# 모바일 라이프사이클 차원

*이 페이지 참조 데이터는 Adobe Experience Platform Mobile SDK를 통해 일반적으로 추적되었습니다. 사용자 에이전트를 사용하는 모바일 장치에 대한 자세한 내용은 [모바일 조회 차원](mobile-dimensions.md). Mobile SDK를 사용하여 추적한 지표에 대해서는 를 참조하십시오. [모바일 라이프사이클 지표](../metrics/lifecycle-metrics.md).*

| 라이프사이클 차원 이름 | 설명 | 컨텍스트 데이터 변수 |
| --- | --- | --- |
| [!UICONTROL 첫 번째 실행 날짜] | | TBD |
| [!UICONTROL 디바이스 이름 (SDK)] | | `a.DeviceName` |
| [!UICONTROL 운영 체제 버전 (SDK)] | | `a.OSVersion` |
| [!UICONTROL 해결 방법(SDK)] | | `a.Resolution` |
| [!UICONTROL 고객 확보 소스] | | `a.referrer.campaign.source` |
| [!UICONTROL 앱 ID] | | `a.AppID` |
| [!UICONTROL 고객 확보 미디어] | | `a.referrer.campaign.medium` |
| [!UICONTROL 고객 확보 용어] | | `a.referrer.campaign.term` |
| [!UICONTROL 고객 확보 콘텐츠] | | `a.refferer.campaign.content` |
| [!UICONTROL 고객 확보 이름] | | `a.referrer.campaign.name` |
| [!UICONTROL 위치 (10km까지)] | | `a.loc.lat.a` + `a.loc.lon.a` |
| [!UICONTROL 위치 (100m까지)] | | `a.loc.lat.b` + `a.loc.lon.b` |
| [!UICONTROL 위치 (1m까지)] | | `a.loc.lat.c` + `a.loc.lon.c` |
| [!UICONTROL 관심 영역 이름] | | `a.loc.poi` |
| [!UICONTROL 관심 영역 중앙까지의 거리] | | `a.loc.dist` |
| [!UICONTROL 시작 번호] | | `a.Launches` |
| [!UICONTROL 최초 사용 이후 일 수] | | `a.DaysSinceFirstUse` |
| [!UICONTROL 동작 이름] | | TBD |
| [!UICONTROL 라이프타임 값(evar)] | | `a.ltv.amount` |
| [!UICONTROL 비콘 Major] | | TBD |
| [!UICONTROL 비콘 Minor] | | TBD |
| [!UICONTROL 비콘 UUID] | | TBD |
| [!UICONTROL 비콘 Proximity] | | TBD |
| [!UICONTROL 마지막 사용 이후 일 수] | | `a.DaysSinceFirstUse` |
| [!UICONTROL 시간 (SDK)] | | `a.HourOfDay` |
| [!UICONTROL 요일 (SDK)] | | `a.DayOfWeek` |
| [!UICONTROL 관심 영역 ID] | | TBD |

{style="table-layout:auto"}

<!-- Missing: Install Date -->
