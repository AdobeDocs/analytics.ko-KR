---
description: Analysis Workspace에서 프로젝트에서 구성 요소를 사용하는 방법을 알아봅니다.
title: 프로젝트에서 구성 요소 사용
feature: Workspace Basics
role: User, Admin
exl-id: fb56e794-67e3-4f85-960e-b90684300fa0
source-git-commit: 35f2812c1a1a4eed090e04d67014fcebf88a80ec
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 80%

---

# 프로젝트에서 구성 요소 사용

구성 요소는 Analysis Workspace에서 모든 프로젝트의 실제 데이터를 구성합니다. 구성 요소는 차원, 지표, 세그먼트 및 날짜 범위로 구성됩니다. 시각화나 패널로 구성 요소를 드래그하여 프로젝트에 구성 요소를 추가할 수 있습니다.

추가할 수 있는 구성 요소 유형에 대한 자세한 내용은 [구성 요소 개요](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)를 참조하십시오.

>[!TIP]
>
>각 구성 요소에 대한 정보는 ![InfoOutline](/help/assets/icons/InfoOutline.svg)을 사용합니다. 자세한 내용은 [구성 요소 정보](#component-info)를 참조하십시오.

## 프로젝트에 구성 요소 추가

1. [Analysis Workspace에서 프로젝트 만들기](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md).

1. Analysis Workspace의 프로젝트에 [패널 추가](/help/analyze/analysis-workspace/c-panels/panels.md#create-a-panel) 또는 [시각화 추가](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)합니다. 빈 프로젝트에 구성 요소를 추가하면 자유 형식 테이블 시각화가 이미 생성됩니다.

1. 버튼 패널에서 ![조정](/help/assets/icons/Curate.svg) **[!UICONTROL 구성 요소]**&#x200B;를 선택합니다. 왼쪽 패널에서 사용 가능한 모든 구성 요소를 볼 수 있습니다. 자세한 내용은 [인터페이스](/help/analyze/analysis-workspace/home.md#interface)를 참조하십시오.

1. 추가하려는 구성 요소를 스크롤하거나 검색한 다음 프로젝트 내의 패널이나 시각화로 드래그합니다.

1. 선택 사항으로 구성요소를 패널 헤더의 세그먼트 드롭 영역으로 드래그할 수 있습니다. 이 드래그 앤 드롭 기능은 구성 요소를 세그먼트로 정의하고 해당 세그먼트를 패널 내의 모든 콘텐츠에 적용합니다.
패널의 세그먼트 드롭 영역을 사용하여 패널을 세그먼트화하는 방법에 대한 자세한 내용은 [패널 개요](/help/analyze/analysis-workspace/c-panels/panels.md#drop-zone)의 [드롭 영역](/help/analyze/analysis-workspace/c-panels/panels.md)을 참조하십시오.

1. 자세한 내용은 다음 섹션을 참조하십시오.

   * [프로젝트에 차원 추가](#add-dimensions-to-a-project)

   * [프로젝트에 지표 추가](#add-metrics-to-a-project)

   * [프로젝트에 세그먼트 추가](#add-segments-to-a-project)

   * [프로젝트에 날짜 범위 추가](#add-date-ranges-to-a-project)

### 프로젝트에 차원 추가

[차원](/help/components/dimensions/overview.md)은(는) 일반적으로 문자열 값을 포함하는 Adobe Analytics의 변수입니다. 반면에, [지표](/help/components/c-calcmetrics/cm-overview.md)는 차원에 연결된 숫자 값을 포함합니다. 기본 보고서는 숫자 값 (지표) 열에 대해 문자열 값 (차원) 행을 보여 줍니다.

1. Analysis Workspace에서 [프로젝트에 구성 요소 추가](#add-components-to-a-project)에 설명된 대로 차원을 추가하기 시작합니다.

1. 다음 방법 중 하나를 선택하여 차원을 추가하고 분석하려는 데이터 유형을 결정합니다.

   ![차원 추가](assets/add-dimension.gif)

   * Analysis Workspace에서 차원을 시각화(예: 자유 형식 테이블)로 끌어다 놓습니다.

   * [프로젝트에 세그먼트 추가](#add-filters-to-a-project)에 설명된 대로 왼쪽 패널에서 세그먼트 드롭 영역으로 하나 이상의 차원을 드래그하여 빠른 세그먼트를 만듭니다.

1. Analysis Workspace에서 다른 구성 요소와 함께 차원 및 차원 항목을 선택적으로 세분화할 수 있습니다. 자세한 내용은 [Workspace에서 차원 분류](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md)를 참조하십시오.

Analysis Workspace에서 차원을 사용하는 방법에 대한 자세한 내용은 [차원 미리 보기](/help/analyze/analysis-workspace/components/dimensions/view-dimensions.md), [차원 분류](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md) 및 [차원 시간 분할](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md)을 참조하십시오.

### 프로젝트에 지표 추가

지표를 사용하면 Analysis Workspace에서 데이터 포인트를 수량화할 수 있습니다. 이들은 일반적으로 시각화에서 열로 사용되며 차원에 연결됩니다.

Analysis Workspace에서 프로젝트에 지표를 추가하려면 다음 작업을 수행하십시오.

1. [프로젝트에 구성 요소 추가](#add-components-to-a-project)에 설명된 대로 Analysis Workspace에서 프로젝트에 지표를 추가하기 시작합니다.



1. Analysis Workspace에 지표를 추가하려면 다음 방법 중 하나를 선택합니다.

   ![지표 추가](assets/add-metric.gif)

   * 지표를 빈 자유 형식 테이블의 지표 드롭 영역으로 드래그하면 해당 지표가 프로젝트의 날짜 기간 동안 추세를 보여 줍니다.

   * 각 차원 항목에 대한 해당 지표를 보려면 차원이 존재할 때 지표를 드래그하십시오.

   * 기존 지표 헤더 위로 지표를 드래그하여 대체합니다.

   * 새 지표를 추가하려면 기존 지표 헤더의 왼쪽이나 오른쪽으로 지표를 끌어다 놓습니다.

   * 기존 지표 헤더 위나 아래로 지표를 드래그하여 지표가 겹치도록 만듭니다.


지표에 대한 자세한 내용은 [지표](/help/analyze/analysis-workspace/components/apply-create-metrics.md)를 참조하십시오.

### 프로젝트에 세그먼트 추가

[세그먼트](/help/components/segmentation/seg-overview.md)를 사용하면 특성이나 특정 상호 작용에 따라 개인, 세션 또는 이벤트의 하위 집합을 식별할 수 있습니다.

Analysis Workspace에서 세그먼트를 다음과 같은 방법으로 사용할 수 있습니다.

* 패널에 세그먼트 추가
패널에 세그먼트를 추가하면 세그먼트가 패널 내의 모든 콘텐츠에 적용됩니다.
패널의 세그먼트 드롭 영역을 사용하여 패널을 세그먼트화하는 방법에 대한 자세한 내용은 [패널 개요](/help/analyze/analysis-workspace/c-panels/panels.md#drop-zone)의 [드롭 영역](/help/analyze/analysis-workspace/c-panels/panels.md)을 참조하십시오.

* 시각화에 세그먼트 추가
자유 형식 테이블의 열에 세그먼트를 추가하면 세그먼트가 테이블 열 내의 모든 콘텐츠에 적용됩니다. 또한 폴아웃 시각화의 일부로 세그먼트를 추가할 수도 있습니다.

* 구성 요소에서 세그먼트 사용
[계산된 지표](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md), [주석](/help/analyze/analysis-workspace/components/annotations/create-annotations.md#annotation-builder) 또는 [세그먼트](/help/components/segmentation/segmentation-workflow/seg-build.md)와 같은 구성 요소를 정의할 때 세그먼트를 정의의 일부로 사용할 수 있습니다.


### 프로젝트에 날짜 범위 추가

[날짜 범위](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md)는 Analysis Workspace의 보고 기간을 결정합니다. 그리고 데이터 범위는 프로젝트 내의 패널과 일부 시각화(예: 자유 형식 테이블)에 적용할 수도 있습니다.

각 패널에는 기본적으로 날짜 범위가 포함됩니다. 패널의 날짜 범위를 업데이트하는 방법에는 여러 가지가 있습니다. Analysis Workspace에서 패널의 날짜 범위를 업데이트하는 방법 중 하나는 왼쪽 패널에서 날짜 범위 구성 요소를 끌어오는 것입니다.

1. 원할 경우, [프로젝트에 구성 요소 추가](#add-components-to-a-project)에 설명된 대로 Analysis Workspace에서 프로젝트에 날짜 범위를 추가합니다.

1. 다음 위치의 왼쪽 패널에서 날짜 범위를 끌어서 놓습니다.

   * 현재 날짜 범위를 선택하여 패널의 날짜 범위를 수정합니다.

     ![날짜 범위 놓기](assets/add-date-range.gif)

   * 자유 형식 테이블 시각화의 지표 또는 차원. 자세한 내용은 [날짜 범위 사용](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#use-date-ranges)을 참조하십시오.

Analysis Workspace에서 날짜 범위를 사용하고 관리하는 방법에 대한 자세한 내용은 [날짜 범위 개요](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md)를 참조하십시오.

## 구성 요소 정보

구성 요소 위에 마우스를 가져다 대면 ![자세한 정보](/help/assets/icons/InfoOutline.svg)가 표시됩니다. ![InfoOutline](/help/assets/icons/InfoOutline.svg)을(를) 선택하면 구성 요소에 대한 추가 정보가 포함된 팝업이 표시됩니다.

![구성 요소 정보](assets/component-info.png)

액세스 제어에 따라 다음과 같은 작업을 수행할 수 있습니다.

* 구성 요소에 대한 ![책갈피](/help/assets/icons/Bookmark.svg) [!UICONTROL 데이터 사전] 정의에 액세스합니다.
* 구성 요소가 정의된 ![편집](/help/assets/icons/Edit.svg) 구성 요소 빌더에 액세스합니다.




<!--
# Use components in Analysis Workspace

Components make up the actual data of any project in Analysis Workspace. Components consist of dimensions, metrics, segments, and date ranges. You can add components to a project by dragging them into visualizations or panels.

For overview information about the types of components you can add, see [Components overview](/help/analyze/analysis-workspace/components/analysis-workspace-components.md).

>[!TIP]
>
>For information about each component, select the Info icon next to a component's name in the left rail of Analysis Workspace, or see the [Analytics Components Guide](/help/components/home.md).

## Begin adding components to a project

1. [Create a project in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md) if you haven't already.

1. [Add a panel](/help/analyze/analysis-workspace/c-panels/panels.md) or [add a visualization](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel) to the project in Analysis Workspace. 

   If you add a component to a blank project, a freeform table visualization is automatically created.

1. Select the **[!UICONTROL Components]** icon in the left rail.

   ![](assets/build-components.png)

1. Scroll to or search for the component you want to add, then drag it to a panel or visualization within your project. 

1. (Optional) Drag a component to the segment drop zone in a panel header. 

   Segments apply to all content within the panel.

   For information about how you can use the segment drop zone on a panel to filter your panel, see [Drop zone](/help/analyze/analysis-workspace/c-panels/panels.md#drop-zone) in [Panels overview](/help/analyze/analysis-workspace/c-panels/panels.md).

   ![drop a segment in the drop zone](assets/segment-dropzone.png)

1. For more detailed information, continue with one of the following sections, depending on the component type you are adding:

   * [Add dimensions to a project](#add-dimensions-to-a-project)

   * [Add metrics to a project](#add-metrics-to-a-project)

   * [Add segments to a project](#add-segments-to-a-project)

   * [Add date ranges to a project](#add-date-ranges-to-a-project)

## Add dimensions to a project

[Dimensions](/help/components/dimensions/overview.md) are variables in Adobe Analytics that typically contain string values. Common dimensions include [Page](/help/components/dimensions/page.md), [Referring domain](/help/components/dimensions/referring-domain.md), or an [eVar](/help/components/dimensions/evar.md). In contrast, [metrics](/help/components/metrics/overview.md) contain numeric values that tie to a dimension. A basic report shows rows of string values (dimension), against a column of numeric values (metric).

1. Start adding a dimension to your project in Analysis Workspace, as described in [Begin adding components to a project](#begin-adding-components-to-a-project).

1. Choose one of the following methods to add dimensions and determine the type of data you want to analyze:

   * Drag a dimension to a visualization (such as a freeform table) in Analysis Workspace.

     ![Add dimensions to a project](assets/add-dimensions.png)
   
   * Drag one or more dimensions from the left rail onto the segment drop zone to create an ad hoc segment, as described in [Add segments to a project](#add-segments-to-a-project).

     ![drop a segment in the drop zone](assets/segment-dropzone.png)

1. (Optional) You can break down dimensions and dimension items in Analysis Workspace with other components. 

   For more information, see [Break down dimensions](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md).

For more information about how to use dimensions in Analysis Workspace, see [Preview dimensions](/help/analyze/analysis-workspace/components/dimensions/view-dimensions.md), [Break down dimensions](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md), and [Time-parting dimensions](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md).

## Add metrics to a project

[Metrics](/help/analyze/analysis-workspace/components/apply-create-metrics.md) allow you to quantify data points in Analysis Workspace. They are most commonly used as columns in a visualization and tied to dimensions.

To add a metric to a project in Analysis Workspace:

1. Start adding a metric to your project in Analysis Workspace, as described in [Begin adding components to a project](#begin-adding-components-to-a-project).

1. Choose one of the following methods to add a metric in Analysis Workspace:

   * Drag a metric to the metric drop zone in an empty Freeform table to see that metric trended over the project's date period. 

     ![Add a metric to a project](assets/add-metrics.png)

   * Drag a metric when a dimension is present to see that metric compared to each dimension item. 

   * Drag a metric on top of an existing metric header to replace it.

   * Drag a metric next to a header to see both metrics side-by-side.

For more information about how to use metrics in Analysis Workspace, see [Metrics](/help/analyze/analysis-workspace/components/apply-create-metrics.md).

## Add segments to a project

[Segments](/help/components/segmentation/seg-overview.md) allow you to identify subsets of visitors based on characteristics or specific interactions.

You can use segments in Analysis Workspace in any of the following ways:

### Add segments to a panel

When you add segments to a panel, the segments apply to all content within the panel.

For information about how you can use the segment drop zone on a panel to filter your panel, see [Drop zone](/help/analyze/analysis-workspace/c-panels/panels.md#drop-zone) in [Panels overview](/help/analyze/analysis-workspace/c-panels/panels.md).

### Add segments to a column in a freeform table

When you add segments to a column in a freeform table, the segments apply to all content within the table column.

### Use segments when creating calculated metrics

In the Calculated metric builder, you can apply segments within your metric definition. 

For more information, see [Segmented metrics](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md).

## Add date ranges to a project

[Date ranges](/help/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.md) determine the reporting time frame in Analysis Workspace, and can be applied to one or more panels within a project.

Each panel includes a date range by default. There are multiple ways to update a date range for a panel. One way to update a date range for a panel in Analysis Workspace is to drag a date range component from the left rail:

1. Start adding a date range to your project in Analysis Workspace, as described in [Begin adding components to a project](#begin-adding-components-to-a-project).

1. Drag a date range from the left rail onto the current date range in the upper-right portion of the panel.

     ![drop a date range](assets/daterange-drop.png)

For more information about how to use calendars and date ranges in Analysis Workspace, see [Calendar and date ranges overview](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md).

-->