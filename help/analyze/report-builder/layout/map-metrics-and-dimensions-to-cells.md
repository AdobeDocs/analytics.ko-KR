---
description: 항목을 스프레드시트에 매핑하기 전에 스프레드시트가 보호되지 않도록 하십시오. 워크시트에 대한 보호 스키마로 인해 사용자 작업이 불가능할 경우에는 스프레드시트에서 셀을 선택할 수 없게 됩니다. 이 경우 먼저 시트의 보호를 해제한 다음 셀 매핑을 추가합니다.
seo-description: 항목을 스프레드시트에 매핑하기 전에 스프레드시트가 보호되지 않도록 하십시오. 워크시트에 대한 보호 스키마로 인해 사용자 작업이 불가능할 경우에는 스프레드시트에서 셀을 선택할 수 없게 됩니다. 이 경우 먼저 시트의 보호를 해제한 다음 셀 매핑을 추가합니다.
seo-title: 지표와 차원을 셀에 매핑
solution: Analytics
title: 지표와 차원을 셀에 매핑
topic: Report Builder
uuid: 50893 E 1 C -5 F 2 C -4558-8001-41 E 70 D 74 D 6 E 7
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 지표와 차원을 셀에 매핑

항목을 스프레드시트에 매핑하기 전에 스프레드시트가 보호되지 않도록 하십시오. 워크시트에 대한 보호 스키마로 인해 사용자 작업이 불가능할 경우에는 스프레드시트에서 셀을 선택할 수 없게 됩니다. 이 경우 먼저 시트의 보호를 해제한 다음 셀 매핑을 추가합니다.

매핑할 영역과 셀의 수는 선택하는 지표, 세부기간, 날짜 범위 및 설정한 필터에 따라 다릅니다. 예를 들어, [!UICONTROL 사이트 지표] &gt; [!UICONTROL 트래픽 보고서]를 선택하고, [!UICONTROL 주] 세부기간을 설정하고 [!UICONTROL 지난 2주]에 대한 날짜 범위를 설정하면, [!UICONTROL 요청 마법사: 2단계]에서 세 개의 셀을 매핑하라는 메시지가 표시됩니다([!UICONTROL 사용자 지정 레이아웃] 사용 시). 요청은 첫째 주에 대한 데이터와 둘째 주에 대한 데이터를 검색하며 여기서 각 데이터 포인트 값은 페이지 보기의 값과 같습니다. 세 번째 셀은 [!UICONTROL 서식 선택 사항]을 사용하여 구성할 수 있는 행 머리글로 사용됩니다.

실수로 스프레드시트에서 호환하지 않는 위치를 매핑하는 경우 Report Builder가 오류를 표시합니다.

다음 섹션에는 추가 정보가 포함됩니다.

* [셀 범위 선택](../../../analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_1E37FB46DA194FB7A1050B8833A48AC6)
* [셀 선택 기술](../../../analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_760421C3D7F84D67A639174710C93B22)
* [매핑 시 문제](../../../analyze/report-builder/layout/map-metrics-and-dimensions-to-cells.md#section_CC1BCF841291447EB3A994EB08F3A099)

## Select a Range of Cells {#section_1E37FB46DA194FB7A1050B8833A48AC6}

[!UICONTROL 요청 마법사: 2단계]에서, 트렌드 요청에 대해 [!UICONTROL 사용자 지정 레이아웃]을 활성화하면 요청을 셀 범위에 매핑할 수 있습니다.

**[!UICONTROL 범위 선택기]** ![select_ cell_ icon. png를 클릭합니다.](assets/select_cell_icon.png)

을 클릭합니다.

* ** All Cells in Range:** Requires you to select a group of cells for a [!UICONTROL Custom Layout] style request.

* ** First Cell of Range:** Lets you select the top-left cell of the range, and displays the [!UICONTROL Range] orientation to specify the horizontal or vertical orientation of input and output cells (column or row). 이 선택 사항을 사용하여 Report Builder가 자동으로 셀을 선택하도록 하십시오.

* ** 범위 방향: ** 셀 범위를 열 또는 행으로 방향을 지정할 수 있습니다.
* **범위의 위쪽 셀 위치 선택:** 셀 참조를 표시합니다.

## Techniques for selecting cells {#section_760421C3D7F84D67A639174710C93B22}

**[!UICONTROL 범위 선택]** 아이콘 ![select_ cell_ icon. png를 클릭하여 데이터를 선택합니다.](assets/select_cell_icon.png)

을 클릭하고 스프레드시트의 원하는 셀 범위를 마우스로 클릭한 채 드래그하여 데이터를 선택합니다. 연속적인 선택은 검정색 테두리로 표시됩니다.

![](assets/twenty_cells.gif)

분리되어 선택된 행들은 각 행 둘레에 흰색의 가는 테두리로 표시됩니다.

![](assets/twoXten_cells_highlighted.gif)

한 요청에서 분리된 행들을 매핑하려면 [!UICONTROL Control] 키를 사용한 다음, 원하는 셀에서 커서로 클릭하여 드래그합니다. 요청이 모두 40개의 셀이 있는 하나의 연속적인 영역이 아니라 각각 10개의 셀이 있는 네 개의 영역을 호출하는 경우 이렇게 하게 됩니다.

![](assets/map4.png)

셀을 선택한 후, **[!UICONTROL 범위 선택]양식에서 다시**[!UICONTROL 범위 선택기]를 클릭하여 [!UICONTROL 요청 마법사: 2단계]로 돌아갑니다.

## Issues when mapping {#section_CC1BCF841291447EB3A994EB08F3A099}

실수로 이미 활성 상태의 매핑이 있는 셀에 매핑하도록 선택하면 범위 선택기 아이콘 옆 텍스트 상자에 아무런 셀 참조도 표시되지 않습니다. [!UICONTROL 확인]을 클릭하면, Report Builder는 "선택한 범위가 다른 요청의 범위와 교차합니다. 택 내용을 변경하십시오"라는 오류를 표시합니다.

* 여전히 이 셀을 사용해야 한다면 원하는 셀(들)을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL 요청 삭제를 선택합니다]**.

이 메시지가 표시되지 않도록 하려면 두 가지 방법이 있을 수 있습니다. 

*  요청과 매핑이 있는 셀에 서식을 추가하여 보고서의 형식을 계획합니다.
* 매핑이 들어 있는 스프레드시트의 영역에 대해 테스트합니다.

임베딩된 요청이 있는 영역에 대해 테스트하기 위해서는 다음을 수행할 수 있습니다.

* [!UICONTROL 요청 관리자]를 실행하고 테이블에 나열된 개별 요청을 클릭합니다. 요청을 클릭하면 요청이 매핑된 스프레드시트의 셀이 강조 표시됩니다.
* 새 매핑에 사용할 스프레드시트의 셀을 선택하고 [!UICONTROL 시트에서]를 클릭합니다. [!UICONTROL 요청 관리자]가 선택한 셀을 교차할 출력 항목이 있는 목록의 요청을 선택합니다. 선택한 요청이 없으면 셀을 사용할 수 있습니다.

* 스프레드시트에서 셀을 선택하고 컨텍스트 메뉴를 마우스 오른쪽 단추로 클릭한 다음 [!UICONTROL 요청 편집]을 사용할 수 있는지 확인합니다. 사용할 수 있으면 이 셀과 연결된 요청이 있습니다.

