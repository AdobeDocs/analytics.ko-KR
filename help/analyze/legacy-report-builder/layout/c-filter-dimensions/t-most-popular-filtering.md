---
description: AND/OR 검색 표현식과 함께 부울 로직을 사용하여 구성하는 등급 및 조건부 필터.
title: 가장 자주 사용하는 필터링
uuid: 558fa592-41be-4e66-8705-81262afe1fc7
feature: Report Builder
role: User, Admin
exl-id: 31587740-6caa-40cb-bb24-d7a15181f642
TQID: https://experienceleague.adobe.com/TLo2RytIM7ZQlpFMqXsTdoz7vFAXnwqoTJGHDG7gWLg
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 33%

---

# 가장 자주 사용하는 필터링

{{legacy-arb}}

AND/OR 검색 표현식과 함께 부울 로직을 사용하여 구성하는 등급 및 조건부 필터.

가장 자주 사용하는 필터는 [!UICONTROL Includs All], [!UICONTROL Includes Any] 또는 [!UICONTROL Excludes All]과 같은 조건 또는 조건 그룹과 함께 [!UICONTROL Page does not contain &#x200B;]*`<product name>`*과 같이 AND/OR 조건이 있는 부울 로직을 사용하여 구성하는 표현식 필터입니다. 이 통합 문서 또는 다른 통합 문서에서 다른 요청에 대해 이러한 표현식을 [저장](/help/analyze/legacy-report-builder/layout/c-filter-dimensions/saved-filters.md)할 수 있습니다.

**가장 자주 사용하는 필터를 만드는 방법**

1. 요청을 만들거나 편집하고 [!UICONTROL 요청 마법사: 2단계]로 진행합니다.

1. [!UICONTROL 요청 마법사: 2단계]에서 그리드에서 차원 옆에 있는 링크를 클릭한 다음 **[!UICONTROL 필터]**&#x200B;를 선택합니다.

   ![응용 프로그램, 사용자 및 프로젝트별로 필터링할 수 있는 옵션이 있는 필터 정의 대화 상자를 표시하는 스크린샷입니다.](/help/admin/tools/assets/filter.png)

1. [!UICONTROL 페이지 선택] 양식에서 **[!UICONTROL 가장 자주 사용]**&#x200B;을 활성화한 후 다음 선택 사항을 구성합니다.

   **시작 등급:** 차원의 시작 등급입니다. 기본 순위 1은 보고된 데이터 목록의 최상위 항목을 나타냅니다. 예를 들어, [!UICONTROL 페이지] 차원의 경우 1의 시작 표시는 사이트에서 가장 많이 요청한 단일 페이지를 나타냅니다. 10 또는 다른 값을 시작 등급 셀로 지정하여 10으로 시작하는 보고서를 가장 높게 생성할 수 있습니다. 지표는 활동이 가장 큰 라인 항목이 목록에서 먼저 보고되도록 내림차순으로 정렬됩니다. 한 요청에 50,000개 이상의 페이지 이름이 필요하지만 보고할 페이지가 수천 개 이상인 경우 요청을 복사하고 시작 등급을 변경하여 50,000개 블록의 적절한 데이터를 검색할 수 있습니다.

   **항목 수:** ([!UICONTROL 피벗 레이아웃]만 해당) 날짜 범위 동안 특정 지표에 대해 보고되는 항목의 수를 정의합니다. 일부 지표에는 지표에 대한 수백 개의 항목이 나열될 수 있지만, 다른 지표에는 몇 개만 표시될 수 있습니다. 예를 들어 차원 [!UICONTROL 사이트 섹션]의 경우 25개의 항목 수는 보고서에 가장 많이 방문한 25개의 페이지가 표시됨을 나타냅니다.

   화살표를 사용하면 시트의 첫 번째 데이터 포인트에서 [!UICONTROL 시작 순위] 및 [!UICONTROL 항목 수]를 변경할 수 있습니다. 기본적으로 [!UICONTROL 시작 순위]는 1로 설정되고 [!UICONTROL 항목 수]는 10으로 설정됩니다. 이러한 값은 특정 지표에 대해 최소 1개에서 최대 50,000개까지 조정할 수 있습니다. 각 지표에는 [!UICONTROL 항목 수]에 대한 자체 한도가 있습니다. 이 필드에는 음수 값이나 0이 허용되지 않습니다. [!UICONTROL 시작 등급]을 15로 선택하고 [!UICONTROL 항목 수]를 10으로 선택하는 경우 지표에 대한 데이터 요청은 가장 많이 방문한 10개 페이지를 반환합니다. 여기서 가장 많이 방문한 첫 번째 페이지는 특정 날짜 범위의 목록에서 15번입니다. 15위부터 25위까지 가장 많이 요청된 페이지가 모두 내림차순으로 나열됩니다.

   >[!NOTE]
   >
   >필터를 기존 요청에 적용하면 표시된 데이터가 변경됩니다. 상위 10개의 [!UICONTROL 페이지]을(를) $A$1에서 $A$10 사이의 셀에 매핑했다고 가정합니다. [!UICONTROL 시작 순위]의 경우 1이고 [!UICONTROL 항목 수]의 경우 10입니다. 이 값을 [!UICONTROL 시작 순위]에 대해 1을 표시하고 [!UICONTROL 항목 수]에 대해 3만 표시하도록 변경하면 이전에 $A$4에서 $A$10까지의 셀에 입력된 데이터가 더 이상 표시되지 않습니다.

1. 검색 표현식을 만들려면 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

1. [!UICONTROL 필터 정의] 양식에서 필요한 조건을 적절히 구성합니다.


   ![필터 정의 대화 상자를 표시하는 스크린샷입니다.](assets/expressions_define_filter.png)

   셀 선택 아이콘을 사용하면 셀 값에 정의된 조건을 찾을 수 있습니다. ![셀 선택 아이콘](assets/select_cell_icon.png)

   **조건 추가** 링크를 사용하면 표현식에 조건을 추가할 수 있습니다. 추가할 수 있는 조건 수에는 제한이 없습니다.

1. **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

   오른쪽 하단에 [확인] 단추가 있는 필터 정의 대화 상자의 ![스크린샷입니다.](assets/choose_page_02.png)

1. [!UICONTROL 페이지 선택] 양식에서 **[!UICONTROL 저장]**&#x200B;을 클릭하여 표현식을 저장합니다.
1. **[!UICONTROL 확인]**&#x200B;을 클릭합니다.
