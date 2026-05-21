---
title: 모바일 라이프사이클 차원
description: Mobile SDK을 사용하여 수집된 데이터를 기반으로 하는 차원입니다.
feature: Dimensions
exl-id: b7ba45d7-7d30-48a3-a747-ea9fbb253abb
TQID: https://experienceleague.adobe.com/VUN8x5eMzIfJ9VGw76v2pWfKWU7b-ct-kI6liwWTObw
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 180
ht-degree: 25%

---

# 모바일 라이프사이클 차원

*이 페이지 참조 데이터는 Adobe Experience Platform Mobile SDK을 통해 일반적으로 추적됩니다. 사용자 에이전트를 사용하는 모바일 장치에 대한 자세한 내용은 [모바일 조회 차원](mobile-dimensions.md)을 참조하십시오. Mobile SDK을 사용하여 추적한 지표에 대해서는 [모바일 라이프사이클 지표](../metrics/lifecycle-metrics.md).*&#x200B;를 참조하십시오.

| 라이프사이클 차원 이름 | 설명 | 컨텍스트 데이터 변수 |
| --- | --- | --- |
| [!UICONTROL 첫 번째 실행 날짜] | | |
| [!UICONTROL 장치 이름(SDK)] | | `a.DeviceName` |
| [!UICONTROL 운영 체제 버전(SDK)] | | `a.OSVersion` |
| [!UICONTROL 해상도(SDK)] | | `a.Resolution` |
| [!UICONTROL 획득 Source] | | `a.referrer.campaign.source` |
| [!UICONTROL 앱 ID] | | `a.AppID` |
| [!UICONTROL 획득 Medium] | | `a.referrer.campaign.medium` |
| [!UICONTROL 획득 용어] | | `a.referrer.campaign.term` |
| [!UICONTROL 획득 콘텐츠] | | `a.refferer.campaign.content` |
| [!UICONTROL 획득 이름] | | `a.referrer.campaign.name` |
| [!UICONTROL 위치(10km까지)] | 방문자의 위도와 경도로, 소수점 첫 번째 자리까지 정확합니다. 예: `040.9` `-111.9`. | `a.loc.lat.a` + `a.loc.lon.a` |
| [!UICONTROL 위치(100m까지)] | 방문자의 위도와 경도로 소수점 세 번째 자리까지 정확합니다. 예: `040.932` `-111.931`. | `a.loc.lat.a` + `a.loc.lat.b` + `a.loc.lon.a` + `a.loc.lon.b` |
| [!UICONTROL 위치(1m까지)] | 방문자의 위도와 경도로 소수점 다섯 번째 자리까지 정확합니다. 예: `040.93231` `-111.93152`. | `a.loc.lat.a` + `a.loc.lat.b` + `a.loc.lat.c` + `a.loc.lon.a` + `a.loc.lon.b` + `a.loc.lon.c` |
| [!UICONTROL 관심 영역 이름] | | `a.loc.poi` |
| [!UICONTROL 관심 영역 중앙까지의 거리] | | `a.loc.dist` |
| [!UICONTROL 시작 번호] | | `a.Launches` |
| [!UICONTROL 최초 사용 이후 일 수] | | `a.DaysSinceFirstUse` |
| [!UICONTROL 작업 이름] | | |
| [!UICONTROL 수명 값(evar)] | | `a.ltv.amount` |
| [!UICONTROL 비콘 Major] | | |
| [!UICONTROL 비콘 Minor] | | |
| [!UICONTROL 비콘 UUID] | | |
| [!UICONTROL 비콘 Proximity] | | |
| [!UICONTROL 마지막 사용 이후 일 수] | | `a.DaysSinceFirstUse` |
| [!UICONTROL 시간(SDK)] | | `a.HourOfDay` |
| [!UICONTROL 요일(SDK)] | | `a.DayOfWeek` |
| [!UICONTROL 관심 영역 ID] | | |

{style="table-layout:auto"}

<!-- Missing: Install Date -->
