---
description: AND/OR 검색 표현식과 함께 부울 로직을 사용하여 구성하는 등급 및 조건부 필터.
title: 가장 자주 사용하는 필터링
uuid: 558fa592-41be-4e66-8705-81262afe1fc7
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 99%

---


# 가장 자주 사용하는 필터링

AND/OR 검색 표현식과 함께 부울 로직을 사용하여 구성하는 등급 및 조건부 필터.

가장 자주 사용하는 필터는 [!UICONTROL Includs All], [!UICONTROL Includes Any] 또는 [!UICONTROL Excludes All]과 같은 조건 또는 조건 그룹과 함께 [!UICONTROL Page does not contain ]*`<product name>`*과 같이 AND/OR 조건이 있는 부울 로직을 사용하여 구성하는 표현식 필터입니다. 이 통합 문서 또는 다른 통합 문서에서 다른 요청에 대해 이러한 표현식을 [저장](/help/analyze/report-builder/layout/c-filter-dimensions/saved-filters.md)할 수 있습니다.

**가장 자주 사용하는 필터를 만드는 방법**

1. 요청을 만들거나 편집하고 [!UICONTROL 요청 마법사: 2단계]로 진행합니다.

   ![단계 정보](assets/dimension_filter.png)

1. [!UICONTROL 요청 마법사: 2단계]에서, 그리드에서 차원 옆에 있는 링크를 클릭한 다음 **[!UICONTROL 필터]**&#x200B;를 선택합니다.
1.  [!UICONTROL 페이지 선택] 양식에서 **[!UICONTROL 가장 자주 사용]**&#x200B;을 활성화한 후 다음 선택 사항을 구성합니다.

   **시작 등급:** 차원의 시작 등급. 기본 등급 1은 보고된 데이터 목록에서 맨 위에 있는 항목을 가리킵니다. 예를 들어 [!UICONTROL 페이지] 차원의 경우, 시작 표시 1은 사이트에서 가장 요청을 많이 받는 한 페이지임을 가리킵니다. 10 또는 다른 값을 시작 등급 셀로 지정할 수 있으며 이렇게 되면 최상위 보고서로서 10으로 시작하는 보고서가 만들어집니다. 지표는 활동이 가장 큰 라인 항목이 목록에서 먼저 보고되도록 내림차순으로 배열됩니다. 하나의 요청에 50,000개가 넘는 페이지 이름이 필요하지만 보고할 페이지는 수천 개만 보유하고 있을 경우 요청을 복사하고 시작 등급을 변경하여 50,000개의 블록에서 적절한 데이터를 검색할 수 있습니다.

   **항목 수:** ([!UICONTROL 피벗 레이아웃]만 해당) 날짜 범위 동안 특정 지표에 대해 보고되는 항목의 수를 정의합니다. 일부 지표의 경우 한 지표에 대해 수백 개의 항목이 나열될 수 있는 반면 어떤 지표들에 대해서는 단 몇 개만 표시됩니다. 예를 들어, [!UICONTROL 사이트 섹션] 차원의 경우, 항목 수 25는 보고서가, 가장 많이 방문한 25개의 페이지를 보여줌을 가리킵니다.

   화살표를 사용하면 시트에 있는 첫 번째 데이터 포인트의 [!UICONTROL 시작 등급]과 [!UICONTROL 항목 수]를 변경할 수 있습니다. 기본적으로 [!UICONTROL 시작 등급]은 1로 설정되며 [!UICONTROL 항목 수]는 10으로 설정됩니다. 이 값들은 특정 지표들에 대해 최소값 1에서부터 최대값 50,000까지 조정할 수 있습니다. 각 지표에는 [!UICONTROL 항목 수]에 대한 자체 상한선이 있습니다. 이 필드에 음수 값이나 0은 사용할 수 없습니다. [!UICONTROL 시작 등급]을 15로 선택하고 [!UICONTROL 항목 수]를 10으로 선택하면 이 지표에 대한 데이터 요청은 10개의 가장 많이 방문한 페이지를 반환하며, 여기에서 제일 많이 방문한 첫 번째 페이지는 특정 데이터 범위에 대해 목록에서 15번입니다. 15번에서 25번까지 등급이 지정된 가장 많이 요청 받은 페이지는 모두 내림차순으로 나열됩니다.

   >[!NOTE]
   >
   >필터를 기존 요청에 적용하면 표시된 데이터가 변경됩니다. 상위 10개 [!UICONTROL 페이지]를 $A$1부터 $A$10까지의 셀들에 매핑했고 여기서[!UICONTROL 시작 등급]은 1이고 [!UICONTROL 항목 수]는 10이라고 가정해 보십시오. 이 값들을 변경하여 [!UICONTROL 시작 등급]에 1을 표시하고 [!UICONTROL 항목 수]에 3만 표시하면 이전에 $A$4부터 $A$10까지의 셀들을 채우던 데이터는 더 이상 표시되지 않게 됩니다.

1. 검색 표현식을 만들려면 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

   ![단계 정보](assets/expressions_define_filter.png)

1. [!UICONTROL 필터 정의] 양식에서 필요한 조건을 적절히 구성합니다.

   ![select_cell_icon.png](assets/select_cell_icon.png): 셀의 값에 정의된 조건을 찾을 수 있도록 해줍니다.

   **조건 추가:** 표현식에 조건을 추가합니다. 추가할 수 있는 조건 수에는 제한이 없습니다.

1. **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

   ![단계 정보](assets/choose_page_02.png)

1. [!UICONTROL 페이지 선택] 양식에서 **[!UICONTROL 저장]**&#x200B;을 클릭하여 표현식을 저장합니다.
1. **[!UICONTROL 확인]**&#x200B;을 클릭합니다.
