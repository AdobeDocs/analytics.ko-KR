---
title: 구성 요소 개요
description: Adobe Analytics이 제공하는 구성 요소와 보고 시 이러한 구성 요소를 사용하는 방법을 알아봅니다.
feature: Components
role: User, Admin
exl-id: e2c98c77-64ee-4349-956a-3ab092e36017
source-git-commit: ff38740116ac6f12033ebdc17cffa3250a30f3f7
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 98%

---

# 구성 요소 개요

구성 요소는 시각화(예: 자유 형식 테이블)에서 사용하거나 보고 기능을 보완하는 Adobe Analytics의 기능입니다.

메인 Adobe Analytics 인터페이스에서 구성 요소를 관리하는 방법:

1. 상단 막대에서 **[!UICONTROL 구성 요소]**&#x200B;를 선택합니다.
1. **[!UICONTROL 구성 요소]**&#x200B;를 선택하여 관리할 수 있는 구성 요소의 개요를 확인하거나 메뉴에서 관리하려는 구성 요소를 바로 선택합니다.

다음 구성 요소를 관리할 수 있습니다.

* [세그먼트](/help/components/segmentation/seg-home.md): 강력하고 집중적인 대상자 세그먼트를 작성, 관리, 공유하고 보고서에 적용합니다. 세그먼트를 사용하여 특성 또는 상호 작용에 따라 사용자 하위 세트를 식별할 수 있습니다.
* [계산된 지표](/help/components/c-calcmetrics/cm-overview.md): 보고에 사용할 새 구성 요소로 지표 및 공식 사용
* [날짜 범위](calendar-date-ranges/custom-date-ranges.md): Analysis Workspace에서 제공하는 날짜 범위 사용자 정의 및 세분화입니다.
* [예약된 프로젝트](../curate-share/t-schedule-report.md): 예약된 프로젝트를 관리합니다.
* [위치](../../../components/locations/locations-manager.md): 프로젝트를 내보낼 위치를 관리합니다.
* [경고](/help/components/c-alerts/intellligent-alerts.md): 변경된 백분율이나 특정 데이터 포인트에 따라 알림을 받을 수 있도록 해 줍니다.
* [주석](annotations/overview.md): 컨텍스트 데이터 뉘앙스와 인사이트를 조직에 전달합니다.
* [환경 설정](/help/analyze/analysis-workspace/user-preferences.md): Analysis Workspace 환경 설정을 관리합니다.



## Analysis Workspace 구성 요소

Analysis Workspace의 구성 요소는 Workspace 프로젝트 패널 및 시각화에 드래그 앤 드롭할 수 있는 지표, 차원, 세그먼트 및 날짜 범위로 구성됩니다. 계산된 지표나 사용자 정의 날짜 범위와 같은 생성된 사용자 정의 구성 요소가 이 패널에 추가됩니다.

구성 요소 패널에 액세스하려면 버튼 패널의 ![Curate](/help/assets/icons/Curate.svg) **[!UICONTROL 구성 요소]**&#x200B;를 선택합니다.

![왼쪽 레일의 구성 요소 아이콘이 강조 표시된 Workspace 패널](assets/components.png)

프로젝트의 구성 요소를 사용하는 방법에 대한 자세한 내용은 [프로젝트 만들기](/help/analyze/analysis-workspace/home.md)를 참조하십시오.


## 구성 요소 관리 {#actions}

Analysis Workspace의 **[!UICONTROL 구성 요소]** 메뉴를 사용하여 새 구성 요소를 빠르게 만들 수 있습니다. 자세한 내용은 [Analysis Workspace 메뉴](/help/analyze/analysis-workspace/home.md#menu)를 참조하십시오.

(개별적으로 또는 두 개 이상을 선택하여) 구성 요소를 관리할 수 있습니다.

1. 하나 이상의 구성 요소를 선택합니다.

1. 컨텍스트 메뉴 또는 ![MoreVertical](/help/assets/icons/MoreVertical.svg) 구성 요소 작업 버튼(구성 요소 상단)에서 다음 작업 중 하나를 선택합니다.


   >[!TIP]
   >
   >**[!UICONTROL Shift 키]**&#x200B;를 누르거나 **[!UICONTROL Command]**(macOS) 또는 **[!UICONTROL Ctrl]**(Windows) 키를 누른 상태에서 여러 구성 요소를 선택할 수 있습니다.


   ![태그, 즐겨찾기, 승인, 공유 및 삭제가 표시된 구성 요소 작업 목록입니다.](assets/component-menu.png)

   | 구성 요소 작업 | 설명 |
   |--- |--- |
   | ![레이블](/help/assets/icons/Label.svg) [!UICONTROL **태그**] | 구성 요소에 태그를 적용하여 구성 요소를 구성하거나 관리합니다. 그런 다음 ![Filter](/help/assets/icons/Filter.svg) 필터를 선택하거나 `#`을 입력하여 왼쪽 패널에서 태그로 검색할 수 있습니다. 태그는 구성 요소 관리자에서 필터 역할도 합니다. |
   | ![Star](/help/assets/icons/Star.svg) [!UICONTROL **즐겨찾기**] | 구성 요소를 즐겨찾기 목록에 추가합니다. 태그와 마찬가지로 왼쪽 패널에서 즐겨찾기로 검색하고 구성 요소 관리자에서 즐겨찾기별로 필터링할 수 있습니다. |
   | ![StarOutline](/help/assets/icons/StarOutline.svg) **[!UICONTROL 즐겨찾기에서 제거]** | 즐겨찾기 목록에서 구성 요소를 제거합니다. |
   | ![체크 표시](/help/assets/icons/Checkmark.svg) [!UICONTROL **승인**] | 구성 요소를 승인됨으로 표시하여 해당 구성 요소가 조직에서 승인되었음을 사용자에게 알립니다. 태그와 마찬가지로 왼쪽 패널에서 승인됨으로 검색하고 승인됨별로 필터링할 수 있습니다. ![체크 표시](/help/assets/icons/Checkmark.svg)는 승인된 구성 요소를 식별합니다. |
   | ![공유](/help/assets/icons/ShareAlt.svg) [!UICONTROL **공유**] | 조직의 사용자와 구성 요소를 공유합니다. 이 옵션은 세그먼트 또는 계산된 지표와 같은 사용자 정의 구성 요소에만 사용할 수 있습니다. |
   | ![삭제](/help/assets/icons/Delete.svg) [!UICONTROL **삭제**] | 더 이상 필요하지 않은 구성 요소를 삭제하십시오. 이 옵션은 세그먼트 또는 계산된 지표와 같은 사용자 정의 구성 요소에만 사용할 수 있습니다. |

사용자 정의 구성 요소는 해당 구성 요소 관리자를 통해 관리할 수도 있습니다. 예를 들어 [세그먼트 관리](/help/components/segmentation/segmentation-workflow/seg-manage.md)를 참조하십시오.

## 구성 요소 목록 관리

Analysis Workspace의 왼쪽 패널에 있는 구성 요소 목록을 검색하고, 필터링하고, 정렬하여 특정 구성 요소를 찾을 수 있습니다.

### 검색

1. 왼쪽 패널에서 **구성 요소** ![Components icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Curate_18_N.svg)를 선택합니다.

2. 검색 필드에 프로젝트에서 사용하려는 구성 요소의 이름을 입력하기 시작합니다.

   색상과 아이콘은 구성 요소 유형을 식별합니다. **차원**(![차원 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Data_18_N.svg))은 주황색, **세그먼트**(![세그먼트 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg))는 파란색, **날짜 범위**(![날짜 범위 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg))는 보라색, **지표**(![지표 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg))는 녹색입니다.<br/>Adobe 아이콘(![AdobeLogo](/help/assets/icons/AdobeLogoSmall.svg))은 계산된 지표 템플릿 또는 세그먼트 템플릿 중 하나를 나타냅니다. 계산기 아이콘(![Calculator icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg))은 조직의 관리자가 만든 계산된 지표를 나타냅니다.

3. 드롭다운 메뉴에서 구성 요소를 선택합니다.

### 필터링

1. 왼쪽 패널에서 **구성 요소** 아이콘(![Components icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Curate_18_N.svg))을 선택합니다.

2. **필터**(![데이터 사전 필터 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg))를 선택하거나 검색 필드에 `#`를 입력합니다.

3. 다음 필터 옵션 중 하나를 선택하여 구성 요소 목록을 필터링합니다.

   | 아이콘 | 필터 옵션 | 설명 |
   |---------|---|----------|
   | ![체크 표시](/help/assets/icons/Checkmark.svg) | **[!UICONTROL 승인됨]** | 관리자가 승인함으로 표시한 구성 요소만 표시합니다. |
   | ![Star](/help/assets/icons/Star.svg) | **[!UICONTROL 즐겨찾기]** | 즐겨찾기 목록에 있는 구성 요소만 표시합니다. <br/>즐겨찾기 목록에 구성 요소를 추가하는 방법에 대한 자세한 내용은 [구성 요소 관리](#manage-components)를 참조하십시오. |
   | ![Dimensions](/help/assets/icons/Dimensions.svg) | **[!UICONTROL 차원]** | 차원인 구성 요소만 표시합니다. |
   | ![Event](/help/assets/icons/Event.svg) | **[!UICONTROL 지표]** | 지표인 구성 요소만 표시합니다. |
   | ![Segmentation](/help/assets/icons/Segmentation.svg) | **[!UICONTROL 세그먼트]** | 세그먼트인 구성 요소만 표시합니다. |
   | ![Calendar](/help/assets/icons/Calendar.svg) | **[!UICONTROL 날짜 범위]** | 날짜 범위인 구성 요소만 표시합니다. |
   | ![레이블](/help/assets/icons/Label.svg) | **[!UICONTROL *태그 이름&#x200B;*]** | 선택한 특정 태그가 있는 구성 요소만 표시합니다. Adobe 템플릿에 제공되는 전용 태그는 Adobe의 [기본 계산된 지표](/help/components/c-calcmetrics/cm-reference/default-calcmetrics.md)입니다. |

   필터의 ![CrossSize75](/help/assets/icons/CrossSize75.svg)를 선택하여 필터를 제거합니다.

4. [구성 요소 목록 정렬](#sort-the-component-list)에 설명된 대로 선택적으로 구성 요소 목록을 정렬할 수 있습니다.

### 정렬

<!-- {{release-limited-testing-section}}-->

1. (선택 사항) [구성 요소 목록 필터링](#filter-the-component-list)에 설명된 대로 구성 요소 목록에 필터를 적용합니다.

2. 왼쪽 패널에서 **구성 요소** ![Components icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Curate_18_N.svg)를 선택합니다.

3. **정렬** 아이콘(![Sort components icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SortOrderDown_18_N.svg))을 선택한 후 다음 필터 옵션 중 하나를 선택하여 구성 요소 목록을 정렬합니다.

다음 정렬 옵션을 사용할 수 있습니다.

{{components-sort-options}}

## 액세스 권한

Analysis Workspace에서 관리자는 보고 시 사용자에게 표시될 구성 요소를 [선정](/help/analyze/analysis-workspace/curate-share/curate.md)할 수 있습니다.


<!--
# Components overview

Components in Analysis Workspace consist of dimensions, metrics, segments, and date ranges that you can drag-and-drop onto a project. 

To access the Components menu, click the **[!UICONTROL Components]** icon in the left rail. You can switch among ![WebPage](/help/assets/icons/WebPage.svg)[panels](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=ko), [visualizations](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html?lang=ko), and components from the left rail icons or by using [hotkeys](/help/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.md).

![](assets/component-overview.png)

You can also adjust the [View density settings](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html?lang=ko) for the project to see more values in the left rail at once by going to **[!UICONTROL Project > Project Info & Settings > View Density]**.

## Dimensions {#dimensions}

[**Dimensions**](https://experienceleague.adobe.com/docs/analytics/components/dimensions/overview.html?lang=ko) are text attributes that describe your visitor behavior and can be viewed, broken down, and compared in your analysis. They can be found in the left Component rail (orange section) and are typically applied as rows of a table. 

Examples of dimensions include [!UICONTROL Page Name], [!UICONTROL Marketing Channels], [!UICONTROL Device Type], and [!UICONTROL Products]. Dimensions are provided by Adobe and are captured through your custom implementation (eVar, Props, classifications, etc).

Each dimension also contains **dimension items** within it. Dimension items can be found in the left Component rail by clicking the right-arrow next to any dimension name (items are yellow).

Examples of dimension items include [!UICONTROL Homepage] (within the [!UICONTROL Page] dimension), [!UICONTROL Paid Search] (within the [!UICONTROL Marketing Channel] dimension), [!UICONTROL Tablet] (within the [!UICONTROL Mobile Device Type] dimension), and so on.

![](assets/dimensions.png)

## Metrics {#metrics}

[**Metrics**](https://experienceleague.adobe.com/docs/analytics/components/metrics/overview.html?lang=ko) are quantitative measures about visitor behavior. They can be found in the left Component rail (green section) and are typically applied as columns of a table.

Examples of metrics include [!UICONTROL Page views], [!UICONTROL Visits], [!UICONTROL Orders], [!UICONTROL Average Time spent], and [!UICONTROL Revenue/Order]. Metrics are provided by Adobe, or captured through your custom implementation ([!UICONTROL Success events]), or created using the [Calculated metric builder](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html?lang=ko).

![](assets/metrics.png)

## Segments {#segments}

[**Segments**](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/segments/t-freeform-project-segment.html?lang=ko) are audience filters that are applied to your analysis. They can be found in the left Component rail (blue section) and are typically applied at the top of a panel or above metric columns in a table. 

Examples of segments include [!UICONTROL Mobile Device Visitors], [!UICONTROL Visits from Email], and [!UICONTROL Authenticated Hits]. Segments are provided by Adobe, or created in the [panel dropzone](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=ko), or created using the [Segment builder](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=ko).

![](assets/segments.png)

## Date Ranges {#date-ranges}

[**Date Ranges**](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html?lang=ko) are the range of dates you conduct your analysis across. They can be found in the left Component rail (purple section) and are typically applied in the calendar of each panel.

You can make the date range components relative to the panel calendar. For additional information, see [About relative panel date ranges](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#relative-panel-dates).

Examples of date ranges include July 2019, [!UICONTROL Last 4 weeks], and [!UICONTROL This month]. Date ranges are provided by Adobe, applied in the [panel calendar](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=ko), or created using the [Date range builder](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html?lang=ko).

![](assets/date-ranges.png)


## Manage components {#actions}

You can manage components directly in the left rail. 

1. Right-click a component.

   Or
   
   Select a component, then select the **Action** (3-dot) icon at the top of the component list.

   >[!TIP]
   >
   >   You can select multiple components by holding Shift, or by holding Command (on Mac) or Ctrl (on Windows).


   ![](assets/component-actions.png)

   | Component action | Description |
   |--- |--- |
   | [!UICONTROL **Tag**] | Organize or manage components by applying tags to them. You can then search by tag in the left rail by clicking the filter or typing #. Tags also act as filters in the component managers. |
   | [!UICONTROL **Favorite**] | Add the component to your list of favorites. Like tags, you can search by Favorites in the left rail and filter by them in the component managers. |
   | [!UICONTROL **Approve**] | Mark components as Approved to signal to your users that the component is organization-approved. Like tags, you can search by Approved in the left rail and filter by them in the component managers. |
   | [!UICONTROL **Share**] | Share components to users in your organization. This option is available for custom components only, such as segments or calculated metrics. |
   | [!UICONTROL **Delete**] | Delete components that you no longer need. This option is available for custom components only, such as segments or calculated metrics. |

Custom components can also be managed through their respective Component managers. For example, the [Segment Manager](/help/components/segmentation/segmentation-workflow/seg-manage.md).

## Search, filter, and sort the component list

You can search, filter, and sort the component list in the left rail of Analysis Workspace to quickly locate a particular component. 

### Search the component list

1. Select the **Components** icon ![Components icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Curate_18_N.svg) in the left rail.

2. In the search field, begin typing the name of the component you want to use in your project.

   The type of component can be identified by both color and icon. **Dimensions** ![Dimension icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Data_18_N.svg) are orange, **Segments** ![Segment icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) are blue, **Date ranges** ![Date range icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg) are purple, and **Metrics** ![Metric icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg) are green. The Adobe icon indicates either a calculated metric template or a segment template, and the calculator icon ![Calculator icon](assets/calculated-metric-icon-created.png) indicated a calculated metric that was created by an Analytics administrator in your organization. 

3. Select the component when it appears in the drop-down list.

### Filter the component list

1. Select the **Components** icon ![Components icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Curate_18_N.svg) in the left rail.

2. Select the **Filter** icon ![Data Dictionary Filter icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg).

   Or

   Type the pound sign (#) in the search field.

3. Select any of the following filter options to filter the list of components:

   |Option | Function |
   |---------|----------|
   | [!UICONTROL **Approved**] | Show only components that are marked as Approved by an administrator. |
   | [!UICONTROL **Favorites**] | Show only components that are in your list of Favorites. For information about adding components to your list of favorites, see [Components overview](/help/analyze/analysis-workspace/components/analysis-workspace-components.md). |
   | [!UICONTROL **Dimensions**] | Show only components that are Dimensions. |
   | [!UICONTROL **Metrics**] | Show only components that are Metrics. |
   | [!UICONTROL **Segments**] | Show only components that are Segments.  |
   | [!UICONTROL **Date ranges**] | Show only components that are Date Ranges. |
   | [!UICONTROL **Show all**] | Show all components. This option is available only for administrators. |
   | [!UICONTROL **Unapproved**] | Show only components that are not yet marked as Approved by an administrator. As an administrator, this is helpful when identifying components that require your review and approval. This option is available only for administrators. |

4. (Optional) To further hone the list, you can sort the component list, as described in [Sort the component list](#sort-the-component-list).

### Sort the component list

1. (Optional) Apply any filters to the component list, as described in [Filter the component list](#filter-the-component-list).

2. Select the **Components** icon ![Components icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Curate_18_N.svg) in the left rail.

3. Select the **Sort** icon ![Sort components icon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SortOrderDown_18_N.svg), then select any of the following filter options to sort the list of components:

   {{components-sort-options}}

-->