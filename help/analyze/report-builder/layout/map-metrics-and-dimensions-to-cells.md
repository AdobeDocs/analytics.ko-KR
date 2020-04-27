---
description: 항목을 스프레드시트에 매핑하기 전에 스프레드시트가 보호되지 않도록 하십시오. 워크시트에 대한 보호 스키마로 인해 사용자 작업이 불가능할 경우에는 스프레드시트에서 셀을 선택할 수 없게 됩니다. 이 경우 먼저 시트의 보호를 해제한 다음 셀 매핑을 추가합니다.
title: 지표 및 차원을 셀에 매핑
topic: Report builder
uuid: 50893e1c-5f2c-4558-8001-41e70d74d6e7
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 지표 및 차원을 셀에 매핑

항목을 스프레드시트에 매핑하기 전에 스프레드시트가 보호되지 않도록 하십시오. 워크시트에 대한 보호 스키마로 인해 사용자 작업이 불가능할 경우에는 스프레드시트에서 셀을 선택할 수 없게 됩니다. 이 경우 먼저 시트의 보호를 해제한 다음 셀 매핑을 추가합니다.

매핑할 영역과 셀의 수는 선택하는 지표, 세부기간, 날짜 범위 및 설정한 필터에 따라 다릅니다. 예를 들어 [!UICONTROL Site Metric] > > [!UICONTROL Traffic Report]를 선택하고 [!UICONTROL Week] 세부기간을 설정하고 날짜 범위를 [!UICONTROL Last 2 Weeks]설정하는 경우 에 세 개의 셀을 매핑하라는 메시지가 표시됩니다(사용 시 [!UICONTROL Custom Layout]) [!UICONTROL Request Wizard: Step 2]. 요청은 첫째 주에 대한 데이터와 둘째 주에 대한 데이터를 검색하며 여기서 각 데이터 포인트 값은 페이지 보기의 값과 같습니다. Your third cell serves as the row heading, which you can configure using [!UICONTROL Format Options].

실수로 스프레드시트에서 호환하지 않는 위치를 매핑하는 경우 Report Builder가 오류를 표시합니다.

다음 섹션에는 추가 정보가 포함됩니다.

* [셀 범위 선택](/help/analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_1E37FB46DA194FB7A1050B8833A48AC6)
* [셀 선택 기술](/help/analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_760421C3D7F84D67A639174710C93B22)
* [매핑 시 문제](/help/analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_CC1BCF841291447EB3A994EB08F3A099)

## 셀 범위 선택 {#section_1E37FB46DA194FB7A1050B8833A48AC6}

On the [!UICONTROL Request Wizard: Step 2], when you enable [!UICONTROL Custom Layout] for a trended request, you can map the request to a range of cells.

select_ **[!UICONTROL Range Selector]** cell_icon.png를 ![클릭합니다.](assets/select_cell_icon.png)

를 클릭합니다.

* **범위의 모든 셀:** 스타일 요청에 대한 셀 그룹을 선택해야 합니다. [!UICONTROL Custom Layout]
* **범위의 첫 번째 셀:** 범위의 왼쪽 위 셀을 선택하고, [!UICONTROL Range] 방향을 표시하여 입력 및 출력 셀의 가로 또는 세로 방향(열 또는 행)을 지정합니다. 이 선택 사항을 사용하여 Report Builder가 자동으로 셀을 선택하도록 하십시오.
* **범위 방향:** 셀 범위를 열 또는 행으로 방향을 정하도록 합니다.
* **범위의 위쪽 셀 위치 선택:** 셀 참조를 표시합니다.

## 셀 선택 기술 {#section_760421C3D7F84D67A639174710C93B22}

You select the data by clicking the **[!UICONTROL Range Selection]** icon  ![select_cell_icon.png](assets/select_cell_icon.png)

을 클릭하고 스프레드시트의 원하는 셀 범위를 마우스로 클릭한 채 드래그하여 데이터를 선택합니다. 연속적인 선택은 검정색 테두리로 표시됩니다.

![](assets/twenty_cells.gif)

분리되어 선택된 행들은 각 행 둘레에 흰색의 가는 테두리로 표시됩니다.

![](assets/twoXten_cells_highlighted.gif)

한 요청에서 분리된 행들을 매핑하려면 [!UICONTROL Control] 키를 사용한 다음, 원하는 셀에서 커서로 클릭하여 드래그합니다. 요청이 모두 40개의 셀이 있는 하나의 연속적인 영역이 아니라 각각 10개의 셀이 있는 네 개의 영역을 호출하는 경우 이렇게 하게 됩니다.

![](assets/map4.png)

셀을 선택한 후 양식에서 을 **[!UICONTROL Range Selector]** 다시 클릭하여 [!UICONTROL Range Selection] 폼으로 돌아갑니다 [!UICONTROL Request Wizard: Step 2].

## 매핑 시 문제 {#section_CC1BCF841291447EB3A994EB08F3A099}

실수로 이미 활성 상태의 매핑이 있는 셀에 매핑하도록 선택하면 범위 선택기 아이콘 옆 텍스트 상자에 아무런 셀 참조도 표시되지 않습니다. When you click [!UICONTROL OK], report builder displays the error, &quot;The range selected intersects another request&#39;s range. 택 내용을 변경하십시오&quot;라는 오류를 표시합니다.

* If you still need to use the cell, right-click on the desired cell or cells, and select **[!UICONTROL Delete Request]**.

이 메시지가 표시되지 않도록 하려면 두 가지 방법이 있을 수 있습니다. 

*  요청과 매핑이 있는 셀에 서식을 추가하여 보고서의 형식을 계획합니다.
* 매핑이 들어 있는 스프레드시트의 영역에 대해 테스트합니다.

임베딩된 요청이 있는 영역에 대해 테스트하기 위해서는 다음을 수행할 수 있습니다.

* Launch the [!UICONTROL Request Manager] and click on individual requests listed in the table. 요청을 클릭하면 요청이 매핑된 스프레드시트의 셀이 강조 표시됩니다.
* Select cells in the spreadsheet you intend to use for a new mapping and click [!UICONTROL From Sheet]. The [!UICONTROL Request Manager] selects the request in the list which has an output item that intersects the selected cell. 선택한 요청이 없으면 셀을 사용할 수 있습니다.
* Select cells in the spreadsheet, right-click in the context menu and verify if [!UICONTROL Edit Request] is available. 사용할 수 있으면 이 셀과 연결된 요청이 있습니다.
