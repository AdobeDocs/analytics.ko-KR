---
description: 경로 지정 보고서에 필터를 적용하는 단계에 대해 설명합니다.
title: 요청 마법사를 사용하여 경로 보고서 필터링
topic: Report builder
uuid: 9b22d5b5-7ae8-49a2-90ae-0c1075562bbe
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 요청 마법사를 사용하여 경로 보고서 필터링

경로 지정 보고서에 필터를 적용하는 단계에 대해 설명합니다.

이 예제에서는 사이트 섹션 경로를 사용합니다.

1. In Adobe Report Builder, click **[!UICONTROL Create]** to open the Request Wizard.
1. 적절한 보고서 세트를 선택합니다.
1. 왼쪽의 트리 보기에서 **[!UICONTROL Paths]** > **[!UICONTROL Site Sections]** > **[!UICONTROL Site Section Paths]**&#x200B;를 선택합니다.

   ![](assets/site_section_path_1.png)

1. 해당 날짜를 지정합니다.
1. 클릭 **[!UICONTROL Next]**.
1. 마법사의 2단계에서 **[!UICONTROL Row Labels]**&#x200B;링크를 클릭합니다 **[!UICONTROL Top 1-10 (pattern applied)]** . 경로 보고서에는 기본적으로 패턴이 적용되어 있습니다.

   ![](assets/site_section_path_2.png)

1. **[!UICONTROL Filter]** 옵션을 선택합니다.

   ![](assets/filter_option.png)

1. 대화 **[!UICONTROL Define 'Site Section Paths' Path Pattern]** 상자에서
   1. 첫 번째 보고서의 시작 등급 
   1. 이 보고서에 표시하려는 항목 수 
1. Click **[!UICONTROL Edit]** to define a path pattern.
1. If you want a custom pattern, drag and drop any **[!UICONTROL Pattern Objects]** from the list on the left into the **[!UICONTROL Pattern Build Canvas]** on the right.

   ![](assets/custom_pattern.png)

1. You can also select a predefined pattern from the **[!UICONTROL Select a Pattern]** drop-down list and modify it. 사용 가능한 패턴은 다음과 같습니다. 

   ![](assets/select_a_pattern.png)

   일부 패턴인 시작 경로의 다음 항목 패턴, 종료 경로의 이전 항목 패턴, 다음 항목 패턴은 Report Builder에만 국한됩니다.
1. 미리 정의한 패턴을 편집하려면
   1. 패턴을 선택합니다. 예를 들어 **[!UICONTROL Exited Site Pattern]**&#x200B;다음을 선택합니다. ![](assets/exited_site_pattern.png)

   1. 종료하기 전에 사용자가 이동하는 사이트 섹션 경로를 정의해야 합니다. 클릭 **[!UICONTROL Specific Item(s): 0 selected]**. 셀 범위에서 선택하거나(기존 요청을 편집하는 경우) 섹션 목록에서 선택하여 이 경로를 정의할 수 있습니다.
   1. To select from a range of cells from a previous request, select **[!UICONTROL From range of cells]** and click the cell selector icon. 그런 후 보고서에서 셀을 선택합니다. ![](assets/choose_site_section_paths.png)

   1. To select from a list of site sections, select **[!UICONTROL From list]** and click **[!UICONTROL Add]**.
   1. Move elements from the **[!UICONTROL Available Elements]** column to the **[!UICONTROL Selected Elements]** column by selecting them and clicking the orange arrow. 클릭합니다. **[!UICONTROL OK]**![](assets/move_site_section_elements.png)

   1. To save the pattern you just established, click **[!UICONTROL Save]**.
   1. 세 **[!UICONTROL OK]** 번 클릭한 다음 을 클릭합니다 **[!UICONTROL Finish]**. 필터링한 패턴 요청이 생성됩니다.
