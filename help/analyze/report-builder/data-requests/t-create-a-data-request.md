---
description: 기본 Report Builder 데이터 요청을 만드는 절차.
title: 데이터 요청 만들기
topic: Report builder
uuid: 5d0151f1-e23d-43eb-84a4-96ae06c3a564
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Report Builder 데이터 요청 만들기

기본 데이터 요청을 만드는 절차.

1. In Excel, click **[!UICONTROL Create]**.
1. 창에서 [!UICONTROL Request Wizard: Step 1] 보고서 세트를 [](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md)선택합니다.
1. 세그먼트를 선택하여 요청에 적용합니다(선택 사항). 세그먼트를 한 개 이상 선택하면 선택한 세그먼트가 목록 맨 위로 이동합니다.

   Report Builder는 Adobe Analytics가 세그먼트를 사용하는 방법과 같게 세그먼트를 사용합니다. [Analytics 세그멘테이션 안내서](https://marketing.adobe.com/resources/help/ko_KR/analytics/segment/)를 참조하십시오. 1. 배포에 사용할 [게시 목록](/help/analyze/report-builder/data-requests/allow-publishing-list-overrides.md)을 선택합니다(선택 사항).
1. [보고서 유형](/help/analyze/report-builder/data-requests/c-report-types/select-report-types.md)을 선택합니다.
1. [날짜 범위](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md)를 및 보고서 [세부기간](/help/analyze/report-builder/data-requests/configuring-report-dates/granularity.md)을 지정합니다.
1. 클릭 **[!UICONTROL Next]**.
1. [레이아웃 - 요청 마법사 2단계](/help/analyze/report-builder/layout/layout.md) 창에서 다음 레이아웃을 지정합니다.

   | 요소 | 설명 |
   |---|---|
   | 피벗 레이아웃 | 표준 Excel 테이블과 유사하게, 레이아웃용 행, 열 및 지표 그리드를 제공합니다. 이 레이아웃을 사용하여 원본 요청 내에 분류 요청을 추가할 수 있습니다. |
   | 사용자 지정 레이아웃 | Provides most of the functionality of the [!UICONTROL Pivot Layout] but lets you choose where each item in the grid should be located in the spreadsheet. 이 레이아웃에서는 이전 릴리스에서 사용할 수 있는 유연성을 제공합니다. |

1. On the [!UICONTROL Metrics] tab, double-click (or drag) metrics in the tree to add them to the [!UICONTROL Metrics] grid.
1. On the [!UICONTROL Dimensions] tab, double-click (or drag) dimensions to the [!UICONTROL Row Labels] grid.

   보고서 세트의 구성과 1단계에서 선택한 기본 보고서에 따라 2단계에서 [차원](https://marketing.adobe.com/resources/help/ko_KR/reference/dimensions.html)을 사용할 수 있습니다. The dimensions are items that correlate, sub-relate, or are a classification of the original report type metric you selected on the [!UICONTROL Request Wizard: Step 1] window. 2단계에서 두 개 이상의 차원을 추가하면 데이터 요청에서 분류가 만들어집니다.

   자세한 내용은 [지표 및 차원 추가](/help/analyze/report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md)를 참조하십시오.
