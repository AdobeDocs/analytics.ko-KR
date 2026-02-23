---
description: Analysis Workspace에서 날짜 비교를 사용하는 방법을 알아보십시오. 이를 통해 날짜 범위가 포함된 모든 열을 가져와 공통 날짜 비교를 만들 수 있습니다.
title: 날짜 비교
feature: Date Ranges
role: User, Admin
exl-id: ea7a42ef-89de-4f70-b468-8a5cf69fea05
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 100%

---

# 날짜 비교

Analysis Workspace의 날짜 비교를 사용하여 날짜 범위가 포함된 열을 가져오고 전년 대비, 사분기 대비, 전월 대비 등과 같은 일반 날짜 비교를 만들 수 있습니다.

## 기간 비교

분석하려면 컨텍스트가 필요하며, 해당 컨텍스트를 이전 기간에서 제공하는 경우가 종종 있습니다. 예를 들어 *작년 이맘때보다 얼마나 좋아질까요/나빠질까요?*&#x200B;라는 질문은 비즈니스를 이해하는 데 기본적인 질문입니다. 날짜 비교에 *차이점* 열이 자동으로 포함되는데, 이 열은 지정된 기간과 비교한 백분율 변경을 표시합니다.

1. 기간을 비교할 차원 및 지표를 사용하여 [자유 형식 테이블](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md)을 만듭니다.
1. 패널 또는 열에서 기간을 설정하여 비교 시간대를 결정하고, 이것이 순환 시간 비교인지 고정 시간 비교인지 결정합니다.

   순환 시간 비교를 생성하려면, 패널 또는 컬럼의 날짜 범위를 순환 날짜 범위(예: **[!UICONTROL 지난 7일]**, **[!UICONTROL 지난 30일]** 등)로 설정합니다.

   고정 시간 비교를 생성하려면, 패널 또는 열의 날짜 범위를 사용자 지정 날짜 범위로 설정합니다.
1. 표 행의 컨텍스트 메뉴를 열고 **[!UICONTROL 기간 비교]**&#x200B;를 선택합니다.

   ![기간 비교가 선택된 테이블 행](assets/compare-time.png)

   >[!NOTE]
   >
   >이 컨텍스트 메뉴 선택 사항은 지표 행, 날짜 범위 행 및 시간 차원 행에 대해 비활성화됩니다.

1. 테이블의 날짜 범위를 설정한 방법에 따라 비교에 대한 다음 옵션이 제공됩니다.

   | 옵션 | 설명 |
   |---|---|
   | **[!UICONTROL 이 날짜 범위 이전 *x*주 / 월 / 분기 / 년]** | 이 날짜 범위 바로 이전의 선택한 날짜 범위와 비교합니다. |
   | **[!UICONTROL 작년부터 이 날짜 범위까지 x주/개월/분기/년]** | 1년 전의 같은 날짜 범위와 비교합니다. |
   | **[!UICONTROL 이 날짜 범위에 해당하는 사용자 정의 날짜 범위]** | 사용자 정의 날짜 범위를 정의할 수 있습니다. |

   >[!NOTE]
   >
   >사용자 정의 일수를 선택한 경우, 예를 들어 10월 7일 ~ 10월 20일(14일 범위)을 선택한 경우 **[!UICONTROL 이 날짜 범위부터 14일 전]**&#x200B;과 **[!UICONTROL 이 날짜 범위에 해당하는 사용자 정의 날짜 범위]**, 이렇게 2가지 옵션만 제공됩니다.

1. 결과 비교 모양은 다음과 같습니다.

   ![날짜 범위와 변화율을 비교한 자유 형식 테이블입니다.](assets/compare-time-result.png)

   [퍼센트 변경] 열의 행은 음수 값인 경우 빨간색으로 표시되고 양수 값인 경우 녹색으로 표시됩니다.

## 비교할 기간 열 추가

이제 테이블의 각 열에 기간을 추가하여 캘린더에 설정된 기간과 다른 기간을 추가할 수 있습니다.

1. 테이블에서 열을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL 기간 열 추가]**&#x200B;를 선택합니다.

   ![](assets/add-time-period-column.png)

1. 테이블의 날짜 범위를 설정한 방법에 따라 비교에 대한 다음 옵션이 제공됩니다.

   | 옵션 | 설명 |
   |---|---|
   | **[!UICONTROL 이 날짜 범위 이전 *x*주 / 월 / 분기 / 년]** | 이 날짜 범위로부터 주/달 전 등을 비교합니다. |
   | **[!UICONTROL 작년부터 이 날짜 범위까지 *x*주/개월/분기/년]** | 1년 전의 같은 날짜 범위를 추가합니다. |
   | **[!UICONTROL 이 날짜 범위에 해당하는 사용자 정의 날짜 범위]** | 사용자 정의 날짜 범위를 만들 수 있습니다. |

   >[!NOTE]
   >
   >사용자 정의 일수를 선택한 경우, 예를 들어 10월 7일 ~ 10월 20일(14일 범위)을 선택한 경우 **[!UICONTROL 이 날짜 범위부터 14일 전]**&#x200B;과 **[!UICONTROL 이 날짜 범위에 해당하는 사용자 정의 날짜 범위]**, 이렇게 2가지 옵션만 제공됩니다.

1. 선택한 열 맨 위에 기간이 삽입됩니다.

   ![현재 캘린더 기간과 지난 달의 발생 건수를 보여 주는 자유 형식 테이블입니다.](assets/add-time-period-column2.png)

1. 원하는 만큼 여러 번 열을 추가하고 다른 날짜 범위를 조합할 수 있습니다.

1. 또한 각 열을 정렬하여 정렬하는 열에 따라 일 순서를 변경할 수 있습니다.

## 열 날짜를 같은 행의 시작으로 정렬

각 열의 날짜가 같은 행에서 시작하도록 맞출 수 있습니다.

예를 들어 지난주(2024년 10월 5일 종료)와 그 이전 주의 일별 비교를 수행합니다. 기본적으로 왼쪽 열은 9월 22일부터 시작하고 오른쪽 열은 9월 29일부터 시작합니다.

![날짜가 정렬되지 않았습니다](assets/not-align-dates.png)

자유 형식 테이블 시각화에서 열 날짜를 같은 행에서 시작하도록 정렬하려면 [설정](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md#settings-1)에서 **[!UICONTROL 각 열의 날짜를 모두 같은 행에서 시작하도록 정렬]**&#x200B;을 활성화할 수 있습니다.

![](assets/align-dates.png)

이 옵션을 사용할 때 다음 사항을 고려합니다.

* 이 설정은 모든 새 프로젝트에서 기본적으로 활성화됩니다.

* 이 설정은 전체 테이블에 적용됩니다. 예를 들어 테이블 내 분류에 대한 이 설정을 변경하면 전체 테이블의 설정이 적용됩니다.


<!--
# Date comparison

Date comparison in Analysis Workspace lets you take any column containing a date range and create a common date comparison, such as: year-over-year, quarter-over-quarter, month-over-month, etc.


>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Date comparison](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/using-date-ranges-and-comparisons-in-analysis-workspace){target="_blank"} for a demo video.

>[!ENDSHADEBOX]



## Compare time periods {#section_C4E36BFE0F5C4378A74E705747C9DEE4}

>[!NOTE]
>[!UICONTROL Compare Time Periods] leverages advanced Calculated Metrics. As a result, it is available only to customers with Analytics Select, Prime, and Ultimate SKUs. 

Analysis requires context, and often that context is provided by a previous time period. For example, the question "How much better or worse are we doing than at this time last year?" is fundamental to understanding your business. Date Comparison automatically include a "difference" column, which shows the percentage change compared to a specified time period.

1. Create a Freeform table, with any dimensions and metrics you want to compare over a time period.
1. Right-click a table row and select **[!UICONTROL Compare time periods]**.

   ![](assets/compare-time.png)

   >[!NOTE]
   >
   >This right-click option is disabled for metric rows, date range rows, and time dimension rows.

1. Depending on how you have set the table's date range, you have these options for comparison: 

   |  Option  | Description  |
   |---|---|
   | **[!UICONTROL Prior week/month/quarter/year to this date range]** | Compares to the week/month/etc. immediately before this date range.  |
   | **[!UICONTROL This week/month/quarter/year last year to this date range]** | Compares to the same date range a year ago.  |
   | **[!UICONTROL Custom date range to this date range]** | Lets you select a custom date range.  |

   >[!NOTE]
   >
   >When you select a custom number of days, for example October 7 - October 20 (a 14-day range), you will get only 2 options: **[!UICONTROL Prior 14 days before this date range]**, and **[!UICONTROL Custom date range to this date range]**.

1. The resulting comparison looks like this:

   ![](assets/compare-time-result.png)

   Rows in the Percent Change column appear red for negative values and green for positive values.

1. (Optional) As in any other Workspace projects, you can create visualizations based on these time comparisons. For example, here is a Bar graph:

   ![](assets/compare-time-barchart.png)

   Note that in order to show the percentage change in the bar chart, you have to have the [!UICONTROL Percentages] setting checked in the [!UICONTROL Visualization Settings].

## Add a time period column for comparison {#section_93CC2B4F48504125BEC104046A32EB93}

You can now add a time period to each column in a table, enabling you to add a time period that is different from the one your calendar is set to. This is another way you can compare dates.

1. Right-click a column in the table and select **[!UICONTROL Add time period column]**. 

   ![](assets/add-time-period-column.png)

1. Depending on how you have set the table's date range, you have these options for comparison: 

   |  Option  | Description  |
   |---|---|
   | **[!UICONTROL Prior week/month/quarter/year to this date range]** | Adds a column with the week/month/etc. immediately before this date range.  |
   | **[!UICONTROL This week/month/quarter/year last year to this date range]** | Adds the same date range a year ago.  |
   | **[!UICONTROL Custom date range to this date range]** | Lets you select a custom date range.  |

   >[!NOTE]
   >
   >When you select a custom number of days, for example October 7 - October 20 (a 14-day range), you will get only 2 options: **[!UICONTROL Prior 14 days before this date range]**, and **[!UICONTROL Custom date range to this date range]**.

1. The time period will be inserted on top of the column you selected:

   ![](assets/add-time-period-column2.png)

1. You can add as many time columns as you want, as well as mix and match different date ranges:

   ![](assets/add-time-period-column4.png)

1. In addition, you can sort on each column, which will change the order of days depending on the column you are sorting on.

## Align column dates to start on the same row {#section_5085E200082048CB899C3F355062A733}

You can align the dates from each column to all start on the same row. 

For example, when you choose to align the dates, if you do a month-over-month comparison between October and September 2016, the left column will start with October 1 and the right column will start with September 1:

![](assets/add-time-period-column3.png)

>[!NOTE]
>
>Consider the following when using this option:
>
>* This setting is enabled by default for all new projects.
>
>* This setting applies to the entire table. For example, if you change this setting for a breakdown within the table, it will change the setting for the entire table.
>

To enable this setting, if it is not already enabled:

1. In the table where you want to align column dates, select the **Settings** icon in the table header.

1. On the [!UICONTROL **Settings**] tab, select **[!UICONTROL Align Dates from each column to all start on the same row (applies to entire table)]**.

![](assets/date-comparison-setting.png)


-->