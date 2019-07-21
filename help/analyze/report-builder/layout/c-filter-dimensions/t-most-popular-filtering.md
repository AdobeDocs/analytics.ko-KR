---
description: AND/OR 검색 표현식과 함께 부울 로직을 사용하여 구성하는 등급 및 조건부 필터.
seo-description: AND/OR 검색 표현식과 함께 부울 로직을 사용하여 구성하는 등급 및 조건부 필터.
seo-title: 가장 빈도가 높은 필터링
solution: Analytics
title: 가장 빈도가 높은 필터링
topic: Report Builder
uuid: 558 FA 592-41 BE -4 E 66-8705-81262 AFE 1 FC 7
translation-type: tm+mt
source-git-commit: dcddb02157ac3e62781b602c5e6c7de3ef79b4fc

---


# 가장 빈도가 높은 필터링

AND/OR 검색 표현식과 함께 부울 로직을 사용하여 구성하는 등급 및 조건부 필터.

Most Popular filters are expression filters that you configure using Boolean logic with AND/OR conditions, such as [!UICONTROL Page does not contain]*`<product name>`* with conditions or groups of conditions like [!UICONTROL Includes All], [!UICONTROL Includes Any], or [!UICONTROL Excludes All]. You can [save](../../../../analyze/report-builder/layout/c-filter-dimensions/saved-filters.md#concept_562AC2C5628247909FBA5E1867BB6AE5) these expressions for other request in this workbook, or in other workbooks.

**가장 자주 사용하는 필터를 만드는 방법**

1. Create or edit a request, and advance to the [!UICONTROL Request Wizard: Step 2].

   ![단계 정보](assets/dimension_filter.png)

1. On the [!UICONTROL Request Wizard: Step 2], click the link next to the dimension in the grid, then choose **[!UICONTROL Filter]**.
1.  [!UICONTROL 페이지 선택]**양식에서[!UICONTROL 가장 인기 있음]**&#x200B;을 활성화한 후 다음 선택 사항을 구성합니다. 

   **시작 등급:** 차원의 시작 등급. 기본 등급 1은 보고된 데이터 목록에서 맨 위에 있는 항목을 가리킵니다. 예를 들어 [!UICONTROL 페이지] 차원의 경우, 시작 표시 1은 사이트에서 가장 요청을 많이 받는 한 페이지임을 가리킵니다. 10 또는 다른 값을 시작 등급 셀로 지정할 수 있으며 이렇게 되면 최상위 보고서로서 10으로 시작하는 보고서가 만들어집니다. 지표는 활동이 가장 큰 라인 항목이 목록에서 먼저 보고되도록 내림차순으로 배열됩니다. 하나의 요청에 50,000개가 넘는 페이지 이름이 필요하지만 보고할 페이지는 수천 개만 보유하고 있을 경우 요청을 복사하고 시작 등급을 변경하여 50,000개의 블록에서 적절한 데이터를 검색할 수 있습니다.

   **항목 수:**([!UICONTROL 피벗 레이아웃]만 해당) 날짜 범위 동안 특정 지표에 대해 보고되는 항목의 수를 정의합니다. 일부 지표의 경우 한 지표에 대해 수백 개의 항목이 나열될 수 있는 반면 어떤 지표들에 대해서는 단 몇 개만 표시됩니다. 예를 들어, [!UICONTROL 사이트 섹션] 차원의 경우, 항목 수 25는 보고서가, 가장 많이 방문한 25개의 페이지를 보여줌을 가리킵니다.

   화살표를 사용하면 시트에 있는 첫 번째 데이터 포인트의 [!UICONTROL 시작 등급]과 [!UICONTROL 항목 수]를 변경할 수 있습니다. 기본적으로 [!UICONTROL 시작 등급]은 1로 설정되며 [!UICONTROL 항목 수]는 10으로 설정됩니다. 이 값들은 특정 지표들에 대해 최소값 1에서부터 최대값 50,000까지 조정할 수 있습니다. 각 지표에는 [!UICONTROL 항목 수]에 대한 자체 상한선이 있습니다. 이 필드에 음수 값이나 0은 사용할 수 없습니다. [!UICONTROL 시작 등급]을 15로 선택하고 [!UICONTROL 항목 수]를 10으로 선택하면 이 지표에 대한 데이터 요청은 10개의 가장 많이 방문한 페이지를 반환하며, 여기에서 제일 많이 방문한 첫 번째 페이지는 특정 데이터 범위에 대해 목록에서 15번입니다. 15번에서 25번까지 등급이 지정된 가장 많이 요청 받은 페이지는 모두 내림차순으로 나열됩니다.

   >[!NOTE]
   >
   >필터를 기존 요청에 적용하면 표시된 데이터가 변경됩니다. 상위 10개 [!UICONTROL 페이지]를 $A$1부터 $A$10까지의 셀들에 매핑했고 여기서[!UICONTROL 시작 등급]은 1이고 [!UICONTROL 항목 수]는 10이라고 가정해 보십시오. 이 값들을 변경하여 [!UICONTROL 시작 등급]에 1을 표시하고 [!UICONTROL 항목 수]에 3만 표시하면 이전에 $A$4부터 $A$10까지의 셀들을 채우던 데이터는 더 이상 표시되지 않게 됩니다.

1. To create a search expression, click **[!UICONTROL Add]**.

   ![단계 정보](assets/expressions_define_filter.png)

1. [!UICONTROL 필터 정의] 양식에서 필요한 조건을 적절히 구성합니다.

   ![select_cell_icon.png](assets/select_cell_icon.png): 셀의 값에 정의된 조건을 찾을 수 있도록 해줍니다.

   ** 조건 추가: ** 표현식에 조건을 추가합니다. 추가할 수 있는 조건 수에는 제한이 없습니다.

1. **[!UICONTROL 확인을 클릭합니다]**.

   ![단계 정보](assets/choose_page_02.png)

1. [!UICONTROL 페이지 선택]**양식에서[!UICONTROL 저장]**&#x200B;을 클릭하여 표현식을 저장합니다.
1. **[!UICONTROL 확인을 클릭합니다]**.
