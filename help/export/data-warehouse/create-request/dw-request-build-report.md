---
description: Data Warehouse 요청을 만드는 방법을 설명하는 단계입니다.
title: Data Warehouse 요청에 대한 보고서 작성
feature: Data Warehouse
exl-id: 34e84e39-e3b1-4184-898a-3fd222ff4d38
source-git-commit: 6a7bbf5103eb6e7f8a3738d27d1fbb189d951a99
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 42%

---

# Data Warehouse 요청에 대한 보고서 작성

Data Warehouse 요청을 만들 때 사용할 수 있는 다양한 구성 옵션이 있습니다. 다음 정보는 요청에 대한 보고서를 작성하는 방법을 설명합니다.

요청 만들기를 시작하는 방법과 다른 중요 구성 옵션 링크에 대한 자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md)을 참조하십시오.

Data Warehouse 요청에 대한 보고서를 작성하려면 다음 작업을 수행하십시오.

1. **[!UICONTROL 도구]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **추가**]&#x200B;를 선택하여 Adobe Analytics에서 요청 만들기를 시작하십시오.

   자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md)를 참조하십시오.

1. 새 Data Warehouse 요청 페이지에서 [!UICONTROL **보고서 작성**] 탭을 선택합니다.

   ![보고서 탭 빌드](assets/build-report.png)

1. 왼쪽 상단 모서리에서 Data Warehouse 보고서를 작성할 때 사용할 보고서 세트를 선택합니다.

   세그먼트 빌더에서 만든 모든 세그먼트가 Data Warehouse와 호환되는 것은 아닙니다. 호환되지 않는 세그먼트가 포함된 가상 보고서 세트를 선택하면 오류가 표시됩니다.

   세그먼트 내에서 지원되는 함수 목록을 보려면 [Data Warehouse 세그먼트 호환성](/help/components/segmentation/seg-reference/seg-compatibility.md)을 참조하세요.

1. 세그먼트, 지표 및 차원을 빌더로 드래그합니다. 빌드하는 보고서는 Data Warehouse 요청에 포함되는 데이터를 결정합니다.

1. [!UICONTROL **보고서 대상**] 탭에서 Data Warehouse 요청을 계속 구성합니다. 자세한 내용은 [Data Warehouse 요청에 대한 보고 대상 구성](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)을 참조하십시오.

<!--

Keep any of this? It was in the Overview article:

The following table describes the fields and options on the [!UICONTROL Data Warehouse Request] tab.

<table id="table_7325A2466866460E8B0AF7D696152713"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Request Name</span> </td> 
   <td colname="col2"> Identifies the request. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Reporting Date</span> </td> 
   <td colname="col2"> <p>The date and granularity of the request. </p> 
    <ul id="ul_C00F4529BD9E4113B517A61751B1DD5C"> 
     <li id="li_4D7C26812DF94ED7B64F985309541F46"> <span class="wintitle"> Custom</span>: A date range you configure in the calendar. </li> 
     <li id="li_2B272087006847148A936350D1B2D523"> <span class="wintitle"> Preset</span>: A preset range. The preset range is relative to the report date. </li> 
     <li id="li_745989965BB94D489FF7046587E13C42"> <span class="wintitle"> Granularity</span>: The time granularity. Valid values are None, Hour, Day, Week, Month, Quarter, and Year. </li> 
    </ul> <p>Data Warehouse reporting on virtual report suites supports the alternative time zone configured on the virtual report suite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Available Segments</span> </td> 
   <td colname="col2"> <p>Lets you select the part of the visitor population you want to examine and generate complex segments. You can load pre-configured segments, create new segments, and store segment components in a library to use in building additional segments. </p> <p>You can now stack segments. When selecting multiple segments, the preview area, the Request Manager, and the Request Detail popup show a comma-separated list of names (e.g., Segment1, Segment2). </p> <p>See the <a href="/help/components/segmentation/seg-home.md"> Segmentation Guide</a> for more information. </p> <p>Note:  You cannot include both a segment filter and a breakdown on the same segment, in the same Data Warehouse report. Doing so will result in an error. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Breakdowns</span> </td> 
   <td colname="col2"> <p>Lets you categorize data using breakdowns. Segments and breakdowns differ in that a segment filters data out of a data set, while a breakdown compartmentalizes data across all valid values for the breakdown. </p> You can also break down a report by one or more segments. However, you cannot include both a segment filter and a breakdown on the same segment, in the same Data Warehouse report. Doing so will result in an error. <p> For example, use segments to remove a gender from the data set, and use a breakdown to see data separated by gender. </p> <p>When a Data Warehouse request is submitted with multiple multi-value dimensions (e.g., various Mobile Reports), an exponential number of rows can be generated from a single hit. The number of rows that can be output from a single hit is capped at 100 (previously 1,000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Metrics</span> </td> 
   <td colname="col2">Lets you add metrics that you want to report on. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> Metrics Sort</span> </td> 
   <td colname="col2">Provides ranked breakdown reports, sorted by descending metric value, similar to what is displayed in the Reports &amp; Analytics user interface, Data Workbench, etc. <a href="/help/export/data-warehouse/sorting-by-metric.md"  > More...</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Schedule Delivery</span> </td> 
   <td colname="col2"> <p>Lets you schedule requests for automatic delivery at selected intervals, or as a one-time report. If you use the default format, the report arrives in an email as a .csv file. </p> <p>To add the date range, include <span class="filepath"> %R</span> in the filename. This value represents the date values requested in the report. For example, if you request data from May 1, 2013 through May 7, 2013, the <span class="filepath"> %R</span> shows a filename including the date range of 20130501 - 20130507. </p> </td> 
  </tr> 
 </tbody> 
</table>

-->
