---
description: Analysis Workspace에서 캘린더 및 데이터 범위를 사용하여 날짜 범위를 지정합니다.
title: 날짜 범위 개요
feature: Date Ranges
role: User, Admin
exl-id: fbf4bc18-65ba-4e39-96c1-4c41a8e3baa9
source-git-commit: ff38740116ac6f12033ebdc17cffa3250a30f3f7
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 100%

---


# 날짜 범위 개요

Workspace 프로젝트에서는 일반적으로 [패널의 캘린더](/help/analyze/analysis-workspace/c-panels/panels.md#calendar)를 사용하여 해당 패널의 시각화 날짜 범위를 지정합니다.

날짜 범위 구성 요소를 사용하면 패널의 캘린더 설정을 정의할 수 있습니다.


## 날짜 범위 사용

날짜 범위 구성 요소를 사용하여 패널의 캘린더를 다시 정의할 수 있습니다.

또는 자유 형식 테이블의 날짜 범위를 지표나 차원으로 사용할 수 있습니다.

![날짜 범위 사용](assets/date-ranges-usage.png)

- **지표**. 예를 들어 특정 지표에 대해 두 달 간의 차원을 비교합니다.
- **차원**. 날짜 범위 차원에 대해 다양한 차원 항목의 지표를 비교합니다.

>[!NOTE]
>
>자유 형식 테이블에서 날짜 범위를 사용하는 경우, 해당 날짜 범위는 자유 형식 테이블이 속한 패널에 지정된 캘린더보다 우선합니다.
>

날짜 범위는 [모든 구성 요소를 사용](/help/analyze/analysis-workspace/components/analysis-workspace-components.md#analysis-workspace-components)하는 것과 같은 방식으로 사용합니다. ![캘린더](/help/assets/icons/Calendar.svg) **[!UICONTROL 날짜 범위]** 구성 요소 패널에서 날짜 범위를 끌어서 다음 위치에 구성 요소를 놓습니다.

- **[!UICONTROL 캘린더]**: 현재 캘린더 구성을 날짜 범위로 ![전환](/help/assets/icons/Switch.svg) **[!UICONTROL 대체]**&#x200B;합니다.
- **지표 열 머리글**: 지표를 ![전환](/help/assets/icons/Switch.svg) **[!UICONTROL 대체]**&#x200B;하거나 지표로 날짜 범위를 ![추가](/help/assets/icons/Add.svg)**[!UICONTROL 추가&#x200B;]**하거나 지표를 날짜 범위 구성 요소를 사용하여 지표를 ![필터](/help/assets/icons/Filter.svg)**[!UICONTROL &#x200B;필터링&#x200B;]**합니다.
- **차원 열 머리글**: 현재 차원을 ![전환](/help/assets/icons/Switch.svg) **[!UICONTROL 대체]**&#x200B;합니다. 새로운 차원은 이제 **[!UICONTROL 날짜 범위]**&#x200B;입니다. 차원이 날짜 범위이면 차원 항목으로 날짜 범위를 ![추가](/help/assets/icons/Add.svg)**[!UICONTROL 추가&#x200B;]**할 수 있습니다.
- **차원 항목**: 날짜 범위에 따라 특정 차원 항목을 ![분류](/help/assets/icons/Breakdown.svg) **[!UICONTROL 분류]**&#x200B;합니다.

자유 형식 테이블 시각화에 날짜 범위 열을 직접 추가할 수도 있습니다.

1. 지표 열의 컨텍스트 메뉴에서 선택합니다.

   - **[!UICONTROL 기간 열 추가]**. 현재 캘린더를 기반으로 제안된 옵션 중에서 선택하거나 [사용자 정의 날짜 범위](#custom-date-ranges)를 만들 수 있습니다.
   - **[!UICONTROL 기간 비교]**. 현재 캘린더를 기반으로 제안된 옵션 중에서 선택하거나 [사용자 정의 날짜 범위](#custom-date-ranges)를 만들 수 있습니다.

1. 선택에 따라 날짜 범위 열이 자유 형식 테이블에 추가됩니다.

## 기본 날짜 범위

Analysis Workspace는 다양한 기본 날짜 범위를 제공합니다.


| 일 | 주 | 월 | 분기 | 년 |
|---|---|---|---|---|
| 오늘 | 이번 주 | 이번 달 | 이번 분기 | 올해 |
| 어제 | 이번 주 (오늘 제외) | 이번 달 (오늘 제외) | 이번 분기 (오늘 제외) | 올해 (오늘 제외) |
| 2일 전 | 2주 전 | 2개월 전 |   |  |
| 3일 전 | 3주 전 | 3개월 전 |  | |
| 지난 7일 | 지난주 | 지난 달 | 지난 분기 | 지난 해 |
| 지난 14일 | 최근 2주 전체 | 최근 2개월 전체 | 지난 4분기 전체 | |
| 지난 30일 | 최근 3주 전체 | 최근 3개월 전체 | | |
| 지난 60일 | 최근 4주 전체 | 최근 6개월 전체 | | |
| 지난 90일 | 최근 12주 전체 | 최근 12개월 전체 | | |
| 지난 7일 전체 | 최근 52주 전체 | 최근 13개월 전체 | | |
| 지난 14일 전체 | | | | |
| 지난 30일 전체 | | | | |
| 지난 90일 전체 | | | | |

<table style="table-layout:fixed">

## 사용자 정의 날짜 범위

고유한 사용자 정의 날짜 범위를 만들 수 있습니다. 날짜 범위를 만들 수 있는 다양한 옵션은 [날짜 범위 만들기](create.md)를 참조하십시오. 그런 다음 [날짜 범위 빌더](create.md#date-range-builder)에 날짜 범위를 작성, 수정 및 저장합니다.

[날짜 범위 관리자](manage.md)를 사용하여 날짜 범위를 관리합니다.



<!--
# Calendar and date ranges overview {#date-range}

>[!CONTEXTUALHELP]
>id="components_dateranges_endtime"
>title="End time"
>abstract="End times always include 59 seconds."



In the calendar, you can specify dates and date ranges, or select a preset.


>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Calendar and date ranges overview](https://video.tv.adobe.com/v/23973?quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]


Calendar selections apply at the panel level, but you have the option to apply them to all panels. When you click a date range in Workspace, the interface displays the current calendar month and the previous calendar month. You can adjust these two calendars by clicking the right and left arrows in each respective upper corner.

![Calendar](assets/aw_calendar2.png){width="60%"} 

## Select and apply date ranges {#select-apply}

The first click on a calendar starts a date range selection. The second click completes a date range selection, which becomes highlighted. If the `Shift` key is held down (or right-click is used), it appends to the currently selected range.

You can also drag dates (and time dimensions) into a Workspace project. You can select specific days, weeks, months, years, or a rolling date.

[Using Date Ranges and Calendar in Analysis Workspace](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/using-dates-in-analysis-workspace.html?lang=ko) (4:07)

| Setting | Description |
|--- |--- |
|Selected Days|Selected days/weeks/months/years.|
|Make date range components relative to panel calendar| If disabled, any date range components used within a table, visualization, or panel drop zone override the panel calendar. <p>If enabled, any date range components used within a table, visualization, or panel drop zone are in relation to the panel date range. For example, if the panel date range is set to November 1 through November 30, and a Last Week date range component is used in a freeform table, the information in the freeform table refers to the last week in October. |
|Use rolling dates| Rolling dates allow you to generate a dynamic report that looks forward or backward for a set period of time based on when you ran the report. For example, if you want to report on all Orders placed "Last Month" (based on the Created Date field) and ran that report in December, you'd see orders placed in November. If you ran that same report in January, you'd see orders placed in December.<ul><li>**[!UICONTROL Date Preview]**: Indicates what time period the rolling calendar encompasses.</li><li>**[!UICONTROL Start]**: You can choose among current day, current week, current month, current quarter, current year.</li><li>**[!UICONTROL End]**: You can choose among current day, current week, current month, current quarter, current year.</li></ul>To view an example, see [Custom date ranges](/help/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.md). <br>Selected by default.|
|Date Range|Lets you pick a preset date range. Last 30 days is the default. **[!UICONTROL This week/month/quarter/year (excluding today)]** lets you choose from date ranges that do not include partial-day data from today.|
|Apply to All Panels|Lets you not only change the selected date range for the current panel, but also for all other panels within the project.|
|Apply|Applies the date range to this panel only.|

## About relative panel date ranges {#relative-panel-dates}

If you're working in Workspace, you can make the date range components relative to the panel calendar. 
Three common use cases where you'll see relative panel dates take effect are Combo charts, Key metrics summary, and Freeform table date ranges.

To use relative panel date ranges

1. Select the **Workspace** tab.
1. Select **Blank project**.
1. Add dimensions, metrics, and segments from the left rail. 
1. Click the panel date range field to toggle the relative panel date range setting.
1. Select **Make date range components relative to panel calendar**.
    * Select the option to make the date range components relative to the panel calendar.
        If relative dates are selected, then rolling dates will be based on the start date of the panel calendar and not today's date.
    * If this option isn't selected, then rolling dates will be based on today's date.

    ![relative panel dates](assets/relative-date-selected.png){width="60%"} 

1. Click **Apply**.
    The relative dates are shown in the upper-right.

    ![relative dates in freeform ](assets/relative-date-range1.png)

## Guidelines for relative panel date ranges {#guidelines}

Keep in mind the following guidelines when using relative panel date ranges.

### Formulas and relative date ranges {#formula-relative-dates}

If you have relative dates selected, all date formulas will use the panel's start date as the starting point.

### Custom calendars and relative date ranges {#custom-calendar-formulas}

When you use a week-based custom calendar and you add months or years, the formula calculates the offset of the day in the given period. The actual date may be different because of the offset. The formula chooses the day landing in the same place in the custom calendar. For example, the third Friday of the third week in a custom calendar.

### About segments that use rolling dates and relative panel date ranges {#segments-relative-dates}

If you build a segment or use a segment with a rolling date, for example, the Last 7 Days or the Last 2 Weeks, and you click on the segment preview, it will start the rolling date from *Today* instead of the panel start date. As a result the preview for the segment will not match when you actually use the segment in the table. The preview is impacted, not the segment itself. 

## Guidelines for panel date ranges and previews {#guidelines-panel-dates}

* Starting with the February release, component and data previews will be based on the panel date range and not the last 90 days. 
* All components listed in the left rail will be available based on the panel date range. 
* All date previews in the segment and calculated metric builders will be based on the panel date range (unless accessed from the component managers, which do not have an associated panel, they will still be based on the last 90 days). 
* Any data previews will display data or components based on the panel date range.

-->