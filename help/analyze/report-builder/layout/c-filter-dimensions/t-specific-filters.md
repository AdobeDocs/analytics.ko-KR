---
description: 특정 차원 용어를 적용하는 필터.
title: 특정 필터
topic: Report builder
uuid: b3a8187a-3d59-4da0-abca-e933664332e3
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 특정 필터

특정 차원 용어를 적용하는 필터.

정확한 기준을 만족하는 필터를 만들어 특정 차원 항목에서 검색할 수 있습니다. 예를 들어, page in [!DNL homepage.htm], [!DNL contact_us.html], [!DNL corporate_info.html]과 같은 필터 유형을 만들 수 있습니다.

**특정 필터 만드는 방법**

1. 요청을 만들거나 편집한 다음 [!UICONTROL Request Wizard: Step 2]로 진행합니다.

   ![단계 결과](assets/dimension_filter.png)

1. On the [!UICONTROL Request Wizard: Step 2], click the link next to the dimension in the grid, then choose **[!UICONTROL Filter]**.

   ![단계 결과](assets/choose_page_specific01.png)

1. Enable **[!UICONTROL Specific]**, then enable one of the following options:

   * **셀 범위에서:** 셀에서 데이터를 선택할 수 있도록 해줍니다. 다음 항목을 선택할 수 있습니다.
   * **범위의 모든 셀:** 범위의 모든 셀을 매핑할 수 있도록 해줍니다. 설명 텍스트가 선택해야 하는 셀 그룹의 수를 알려줍니다. 셀 그룹을 두 개 이상 매핑하려면 Ctrl 키를 눌러 연속적으로 선택합니다. 매핑해야 하는 범위에 셀이 하나만 있을 경우 이 선택 사항은 사용할 수 있는 유일한 선택 사항입니다.
   * **범위의 첫 번째 셀:** 범위의 상단 왼쪽 셀만 선택한 다음 데이터의 방향을 선택합니다. 그리고 요청에 여러 기간이 있을 경우에는 기간의 방향을 선택하고 기간 사이에 있는 설정된 셀 수를 건너뛸지 여부를 선택합니다.
   * **목록에서:** 데이터를 추가할 수 있는 목록에서 데이터를 선택할 수 있도록 해줍니다.
1. If you enable **[!UICONTROL From List]**, select any available listed items or click **[!UICONTROL Add]**.

   When you click **[!UICONTROL Add]**, the [!UICONTROL Select From List] form displays a list of available dimension values for the current request date range, limited to the first 10,000 items. You can search across these items or click **[!UICONTROL More ...]**, which displays the [!UICONTROL Search Form], so that you can create a more detailed search for dimensions.
1. 에서 [!UICONTROL Select From List]을 클릭합니다 **[!UICONTROL OK]**.
1. On the [!UICONTROL Choose Page] form, save your Specific filter if you want, then click **[!UICONTROL OK]**.
