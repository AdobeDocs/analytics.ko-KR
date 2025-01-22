---
description: Activity Map 확장과 인터페이스 탐색 방법에 대해 알아봅니다.
title: Activity Map 확장 인터페이스
uuid: f6734b60-0b77-4f50-a45a-6a6936d1524e
feature: Activity Map
role: User, Admin
exl-id: 461abda1-3238-4a32-b9d3-5a57b00cf0d3
source-git-commit: 13ad9d40ad74a8dffe05d899db54f4d77cbcc34c
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 1%

---

# Activity Map 확장 인터페이스

Activity Map 확장 인터페이스는 두 부분으로 구성됩니다.

* 확장 및 보고서를 구성할 수 있는 상단 패널
* 가장 방문 빈도가 높은 링크를 표시하는 오버레이
* 가장 방문 빈도가 높은 링크에 대한 지표를 표시하는 하단 패널

## 상단 패널

상단 패널에는 Activity Map 오버레이에 대한 기본 컨트롤이 포함되어 있습니다.

![오버레이](../assets/overlay.png)

여기에서는 다음 설정을 제공합니다.

* **표준/라이브 보기**: 표준 보기와 라이브 보기 사이를 전환합니다.
   * 표준 보기: 이전 데이터를 기반으로 오버레이를 표시합니다.
   * 라이브 뷰: 라이브 데이터를 기반으로 오버레이를 표시합니다. 날짜 선택기가 라이브 데이터의 세부기간을 변경할 수 있는 드롭다운으로 변경됩니다.
* **지표 선택기**: 오버레이에서 보고하는 지표를 변경할 수 있습니다. [라이브 보기]를 선택한 경우 [!UICONTROL 링크 클릭 수]만 사용할 수 있습니다.
* **세그먼트 선택기**: 오버레이 내에서 데이터 하위 집합을 보면서 [세그먼트](/help/components/segmentation/seg-overview.md)를 선택할 수 있습니다. 세그먼트는 라이브 보기에서 사용할 수 없습니다.
* **오버레이 시각화 유형**: 오버레이가 링크의 순위를 시각화하는 방법을 변경할 수 있습니다.
   * **[!UICONTROL 버블]**: 상위 링크에는 보고 기간 동안의 숫자 등급을 보여주는 녹색 버블이 표시됩니다. [설정](settings.md)에서 버블 색상을 변경할 수 있습니다.
   * **[!UICONTROL 그라데이션]**: 위쪽 링크는 투명한 빨간색으로 음영 처리되어 나타납니다. 가장 인기 있는 링크는 가장 어두운 빨간색입니다. [설정](settings.md)에서 그라데이션 색을 변경할 수 있습니다.
   * **[!UICONTROL 해제]**: 링크 오버레이를 사용하지 않도록 설정합니다.
* **날짜 선택기**: 보고 기간을 변경할 수 있습니다.

이 패널의 머리글에는 다음 설정이 포함되어 있습니다.

* **상단 패널 확장/축소**: 설정을 가로 또는 세로로 표시하도록 상단 패널을 전환합니다(이중 화살표 아이콘).
* **[!UICONTROL 페이지 세부 정보를 전환합니다]**: 아래쪽 패널(눈 모양 아이콘)을 표시하거나 숨깁니다.
* **[!UICONTROL 설정 표시]**: 변경할 수 있는 설정 메뉴를 엽니다(톱니바퀴 아이콘).
   * **[!UICONTROL 설정]**: 확장의 [설정](settings.md)을 엽니다.
   * **[!UICONTROL 도움말]**: Experience League 설명서를 엽니다(이 페이지).
   * **[!UICONTROL Adobe 커뮤니티]**: [Experience League 커뮤니티](https://experienceleaguecommunities.adobe.com/)를 엽니다.
   * **[!UICONTROL 정보]**: 확장 버전을 표시합니다.
   * **[!UICONTROL 로그아웃]**: 확장에서 로그아웃하므로 다시 로그인해야 합니다.
* **[!UICONTROL Activity Map 종료]**: 확장에 대한 모든 오버레이를 닫습니다(X 아이콘).

## 페이지 오버레이

페이지 오버레이에는 보고 기간 동안 클릭한 가장 방문 빈도가 높은 링크의 위치를 보여 주는 오버레이와 함께 사이트 콘텐츠가 포함되어 있습니다. 상단 패널의 **[!UICONTROL 오버레이 시각화 유형]**&#x200B;에서 버블이나 그라디언트로 표시되도록 이러한 링크 오버레이를 구성할 수 있습니다.

버블 또는 그라디언트를 클릭하면 해당 특정 링크에 대한 세부 정보를 볼 수 있습니다.

![링크 버블](../assets/link-bubble.png)

## 아래쪽 패널

하단 패널은 오버레이에 표시된 링크들의 집계된 보기를 보여줍니다.

* **보고서 유형**: 아래쪽 패널을 전환하여 **[!UICONTROL 페이지에 있는 링크]** 보고서 또는 **[!UICONTROL 페이지 세부 정보]** 보고서를 표시합니다.
* **[!UICONTROL 페이지 이름]**: 현재 [페이지](/help/components/dimensions/page.md) 차원 이름입니다.
* **[!UICONTROL 검색]**: 입력한 텍스트와 일치하는 링크 이름만 표시하도록 보고서를 필터링합니다.
* **[!UICONTROL 다운로드]**: 보고서를 CSV로 내보냅니다. [!UICONTROL 페이지에 있는 링크] 보고서, [!UICONTROL 페이지] 보고서 및 [!UICONTROL 페이지 흐름] 보고서를 동일한 다운로드 파일에 포함할 수 있습니다.
* **[!UICONTROL 보고서 도킹 위치 변경]**: 브라우저 창의 아래쪽 또는 위쪽 부분에 나타나도록 이 패널의 위치를 전환합니다.
* **[!UICONTROL 보고서 닫기]**: 이 패널을 닫습니다. 상단 패널(눈 모양 아이콘)의 **[!UICONTROL 페이지 세부 정보 전환]** 단추를 사용하여 패널을 다시 열 수 있습니다.

**[!UICONTROL 페이지에 있는 링크]** 보고서에는 다음 설정이 있는 기본 작업 영역 보고서가 표시됩니다.

* [Activity Map 링크](/help/components/dimensions/activity-map-link.md) 차원
* [발생 횟수](/help/components/metrics/occurrences.md) 지표(**[!UICONTROL 링크 클릭 수]**)
* 세그먼트로 적용된 현재 [Page](/help/components/dimensions/page.md) 값

![페이지 패널의 링크](../assets/links-on-page.png)

**[!UICONTROL 페이지 세부 정보]** 보고서에 현재 페이지에 초점을 두고 [페이지](/help/components/dimensions/page.md) 차원을 사용하는 [흐름](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) 시각화가 표시됩니다. 현재 페이지에 대한 다음 지표가 왼쪽에 표시됩니다.

* 총 [페이지 보기 수](/help/components/metrics/page-views.md)
* 모든 페이지 보기의 [!UICONTROL %]
* [시작](/help/components/metrics/entries.md) 수
* [종료](/help/components/metrics/exits.md) 수
* [단일 페이지 방문 횟수](/help/components/metrics/single-page-visits.md)
* [!UICONTROL 페이지 평균 클릭 수]
* 평균 [페이지 체류 시간](/help/components/metrics/time-spent.md)
* [다시 로드](/help/components/metrics/reloads.md) 수
* [바운스 비율](/help/components/metrics/bounce-rate.md)
* [!UICONTROL 링크 클릭]

![페이지 세부정보](../assets/page-details.png)
