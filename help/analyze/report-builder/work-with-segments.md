---
title: Report Builder에서 세그먼트 작업
description: Report Builder에서 세그먼트를 사용하는 방법을 알아봅니다.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 2691fde0-59c6-45a7-80a5-8e5e221adce2
source-git-commit: c3fe537967473754a3b5fe88c7b383647b2c742e
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 6%

---

# 세그먼트를 사용한 작업

새 데이터 블록을 만들거나 **[!UICONTROL 명령]** 패널에서 **[!UICONTROL 데이터 블록 편집]**&#x200B;을 선택하면 세그먼트를 적용할 수 있습니다.

## 데이터 블록에 세그먼트 적용

세그먼트를 전체 데이터 블록에 적용하려면 세그먼트를 더블 선택하거나 구성 요소 목록에서 테이블의 세그먼트 섹션으로 세그먼트를 드래그 앤 드롭합니다.

## 개별 지표에 필터 적용

세그먼트를 사용하여 필터를 개별 지표에 적용하려면 다음을 수행합니다.

* **[!UICONTROL 세그먼트]**&#x200B;에서 테이블의 지표로 하나 이상의 세그먼트를 끌어다 놓습니다.

* 또는

   1. ![테이블](/help/assets/icons/MoreSmall.svg) 창에서 특정 지표에 대해 **[!UICONTROL MoreSmall]**&#x200B;을 선택한 다음 **[!UICONTROL 지표 필터링]**&#x200B;을 선택합니다.

      지표를 표시하는 ![세그먼트 탭](./assets/filter-metric.png){zoomable="yes"}

   1. **[!UICONTROL 세그먼트]** 드롭다운 메뉴에서 하나 이상의 세그먼트를 선택하십시오. 세그먼트가 **[!UICONTROL 적용된 세그먼트]** 목록에 추가됩니다.

      ![적용된 세그먼트](assets/segments-applied.png)
   1. ![적용된 세그먼트](/help/assets/icons/CrossSize75.svg) 목록에서 세그먼트를 제거하려면 **[!UICONTROL CrossSize75]**&#x200B;을(를) 선택하십시오. 또는 **[!UICONTROL 모두 지우기]**&#x200B;를 선택하여 **[!UICONTROL 적용된 세그먼트]** 목록에서 모든 세그먼트를 제거합니다.
   1. **[!UICONTROL 적용]**&#x200B;을 선택합니다.

적용된 필터를 보려면 테이블 창에서 지표 위로 마우스를 이동하거나 선택합니다. 세그먼트가 적용된 지표에는 세그먼트 아이콘이 표시됩니다.


## 세그먼트 빠른 편집

**[!UICONTROL 빠른 편집]** 패널을 사용하여 기존 데이터 블록의 세그먼트를 추가, 제거 또는 바꿀 수 있습니다.

스프레드시트에서 셀 범위를 선택하면 **[!UICONTROL 빠른 편집]** 패널의 **[!UICONTROL 세그먼트]** 링크에 해당 선택 항목의 데이터 블록이 사용하는 세그먼트의 요약 목록이 표시됩니다.

**[!UICONTROL 빠른 편집]** 패널을 사용하여 세그먼트를 편집하려면:

1. 하나 이상의 데이터 블록에서 셀 범위를 선택합니다.

1. **[!UICONTROL 세그먼트]** 링크를 선택하여 **[!UICONTROL 빠른 편집]** **[!UICONTROL 세그먼트]** 패널을 시작합니다.


### 세그먼트 추가 또는 제거

추가/제거 옵션을 사용하여 세그먼트를 추가하거나 제거할 수 있습니다.

1. **[!UICONTROL 빠른 편집]** **[!UICONTROL 세그먼트]** 패널에서 **[!UICONTROL 추가/제거]** 탭을 선택합니다.


   1. **[!UICONTROL 세그먼트]** 드롭다운 메뉴에서 하나 이상의 세그먼트를 선택하십시오. 세그먼트가 **[!UICONTROL 적용된 세그먼트]** 목록에 추가됩니다.
   1. ![적용된 세그먼트](/help/assets/icons/CrossSize75.svg) 목록에서 세그먼트를 제거하려면 **[!UICONTROL CrossSize75]**&#x200B;을(를) 선택하십시오.
   1. **[!UICONTROL 적용]**&#x200B;을 선택합니다.

Report Builder에 적용된 세그먼트 변경 사항을 확인하는 메시지가 표시됩니다.

### 세그먼트 바꾸기

기존 세그먼트를 다른 세그먼트로 대체하여 데이터 세그먼트 방식을 변경할 수 있습니다.

1. **[!UICONTROL 빠른 편집]** **[!UICONTROL 세그먼트]** 패널에서 **[!UICONTROL 바꾸기]** 탭을 선택합니다.

1. **검색 목록** 검색 필드를 사용하여 특정 세그먼트를 찾습니다.

1. 바꿀 세그먼트를 하나 이상 선택합니다.

1. 다음으로 바꾸기 드롭다운 메뉴에서 하나 이상의 세그먼트를 검색하여 **[!UICONTROL 다음으로 바꾸기]** 목록에 세그먼트를 추가하십시오.

1. **[!UICONTROL 적용]**&#x200B;을 선택합니다.

Report Builder은 세그먼트 목록을 업데이트하여 대체 항목을 반영합니다.

## 셀에서 데이터 블록 세그먼트 정의

데이터 블록은 셀의 세그먼트를 참조할 수 있습니다. 여러 데이터 블록이 세그먼트에 대해 동일한 셀을 참조할 수 있으므로 한 번에 여러 데이터 블록에 대해 세그먼트를 쉽게 전환할 수 있습니다.

셀에서 세그먼트를 적용하려면

1. [새 데이터 블록을 만들거나](create-a-data-block.md#create-a-data-block) 기존 데이터 블록을 편집합니다.
1. 세그먼트를 정의하려면 **[!UICONTROL 세그먼트]** 탭을 선택하십시오.
1. ![DataViewSelector](/help/assets/icons/DataViewSelector.svg)를 선택합니다.

   ![셀에서 세그먼트 선택](assets/select-segment-from-cell.png){zoomable="yes"}

1. 데이터 블록이 세그먼트를 참조할 셀을 선택합니다.

1. 세그먼트를 셀에 추가하려면 더블 선택합니다. 또는 하나 이상의 세그먼트를 **[!UICONTROL 포함된 세그먼트]** 섹션으로 끌어다 놓습니다.

1. 참조 셀을 만들려면 **[!UICONTROL 적용]**&#x200B;을 선택하십시오.

1. **세그먼트** 탭에서 새로 만든 참조 셀 세그먼트를 데이터 블록에 추가합니다.

   ![Sheet1!J1(모든 데이터) 세그먼트를 표시하는 세그먼트 탭이 표에 추가되었습니다.](assets/segment-from-cell-applied.png){zoomable="yes"}

1. **[!UICONTROL 마침]**&#x200B;을 선택합니다.

참조 셀을 다른 데이터 블록에 세그먼트로 적용하려면 **[!UICONTROL 테이블]** 탭의 **[!UICONTROL 세그먼트]** 목록에 있는 세그먼트 중 하나로 셀 참조를 사용합니다.

### 참조 셀을 사용하여 데이터 블록 세그먼트 변경

1. 스프레드시트에서 참조 셀을 선택합니다.

1. **[!UICONTROL 빠른 편집]** 메뉴의 **[!UICONTROL 셀의 세그먼트]**&#x200B;에서 링크를 선택하십시오.

   ![Sheet1!J1(모든 데이터)을 표시하는 셀 링크의 세그먼트](assets/select-segment-from-cell-in-sheet.png){zoomable="yes"}

1. 드롭다운 메뉴에서 세그먼트를 선택합니다.

1. **[!UICONTROL 적용]**&#x200B;을 선택합니다.

<!--
You can apply segments when you create a new data block or when you select the **Edit data block** option from the COMMANDS panel.

## Apply segments to a data block

To apply a segment to the entire data block, double-click a segment or drag and drop filters from the components list into the Segments section of the Table.

## Apply segments to individual metrics

To apply segments to individual metrics, drag and drop a segment onto a metric in the table. You can also click the **...** icon to the right of a metric in the Table pane and then select **[!UICONTROL Segment metric]**. To view applied segments, hover over or select a metric in the Table pane. Metrics with applied segments display a filter icon.

![Segments tab displaying metrics.](./assets/filter_by.png)

## Quick edit segments

You can use the Quick edit panel to add, remove, or replace segments for existing data blocks.

When you select a range of cells in the spreadsheet, the **[!UICONTROL Segments]** link in the Quick edit panel displays a summary list of the segments used by the data blocks in that selection.

To edit segments using the Quick edit panel

1. Select a range of cells from one or multiple data blocks.

    ![Quick Edit segment panel showing segment options for report suites, date range, and segments.](./assets/select_multiple_dbs.png)

1. Click the link underneath **[!UICONTROL Segments]** to launch the Quick edit - Filters panel.

    ![the Segments panel showing the Add Segments field and Segments Applied lists.](./assets/quick_edit_filters.png)

### Add or remove a segment

You can add or remove segments using the Add/Remove options.

1. Select the **[!UICONTROL Add/Remove]** tab in the Quick edit-segments panel.

    All segments applied to the selected data blocks are listed in the Quick Edit-segments panel. Segments applied to all data blocks in the selection are listed under the **[!UICONTROL Applied to all selected data blocks]** heading. Segments applied to some but not all data blocks are listed under the **[!UICONTROL Applied to 1 or more selected data blocks]** heading.

    When multiple segments are present in the selected data blocks, you can search for specific segments using the **[!UICONTROL Add Filter]** search field.

    ![The Add Segments field.](./assets/add_filter.png)

1. Add segments by selecting segments from the **[!UICONTROL Add segment]** drop down menu.

    The list of searchable segments includes all segments accessible to the report suites that are present in one or more of the selected data blocks as well as all the segments that are available globally in the organization.

    Adding a segment applies the segment to all data blocks in the selection.

1. To remove segments, click the delete icon **x** to the right of segments in the **[!UICONTROL Segments applied]** list.

1. Click **[!UICONTROL Apply]** to save changes and return to the hub panel.

    Report Builder displays a message to confirm the applied segment changes.

### Replace a segment

You can replace an existing segment with another segment to change how the data is segmented.

1. Select the **[!UICONTROL Replace]** tab in the Quick edit-segment panel.

    ![Select the Replace tab.](./assets/replace_filter.png)

1. Use the **[!UICONTROL Search list]** search field to locate specific segments.

1. Choose one or more segments that you want to replace.

1. Search for one or more segments in the Replace with field.

    Selecting a filter adds it to the **[!UICONTROL Replace with]**... list.

1. Click **[!UICONTROL Apply]**.

    Report Builder updates the list of segments to reflect the replacement.

### Define data block segments from cell

Data blocks can reference segments from a cell. Multiple data blocks can reference the same cell for segments, allowing you to easily switch segments for multiple data blocks at a time.

To apply segments from a cell

1. Navigate to Step 2 in either the data block creation or editing process. See [Create a Data Block](./create-a-data-block.md).
1. Click the **[!UICONTROL Segments]** tab to define filters.
1. Click **[!UICONTROL Create segment from cell]**.

    ![Create segment from cell icon.](./assets/create-filter-from-cell.png)

1. Select the cell from which you want the data blocks to reference a segment.
   
1. Add the segment choice you wish to add to the cell by either double clicking the segment, or by dragging and dropping it into the **[!UICONTROL Segments Included]** section. 
   
   Note: Only one choice may be selected for the given cell at one time.

    ![The Add segment from cell window showing the Filters included.](./assets/select-filters.png)

1. Click **[!UICONTROL Apply]** to create the reference cell.

1. From the **[!UICONTROL Segments]** tab, add the newly created reference cell segments to your data block.

    ![Segments tab showing Sheet1!J1(All Data) segment added to the table.](./assets/reference-cell-filter.png)

1. Click **[!UICONTROL Finish]**.

    Now this cell can be referenced by other data blocks in their segments. To apply the reference cell as a segment to other data blocks, simply add the cell reference to their segments from the Segments tab. 

#### Use the reference cell to change data block segments

1. Select the reference cell in your spreadsheet.

1. Click the link under **[!UICONTROL Segments from Cell]** in the Quick Edit menu.

    ![Segments from cell link showing Sheet1!J1 (All Data)](./assets/filters-from-cell-link.png)

1. Select your segment from the drop-down menu.

    ![Segments drop down menu](./assets/filter-drop-down.png)

1. Click **[!UICONTROL Apply]**.
-->