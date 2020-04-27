---
description: 폴아웃 보고서에 필터를 적용하는 단계에 대해 설명합니다.
title: 요청 마법사를 사용하여 폴아웃 보고서 필터링
topic: Report builder
uuid: 269e900e-23bd-48d8-9bac-69e3167a9c18
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 요청 마법사를 사용하여 폴아웃 보고서 필터링

폴아웃 보고서에 필터를 적용하는 단계에 대해 설명합니다.

이 예에서는 페이지 폴아웃 보고서를 보여줍니다.

1. In Adobe Report Builder, click **[!UICONTROL Create]** to open the Request Wizard.
1. 적절한 보고서 세트를 선택합니다.
1. 왼쪽의 트리 보기에서 **[!UICONTROL Paths]** > **[!UICONTROL Page]** > **[!UICONTROL Page Fallout]**&#x200B;를 선택합니다.

   ![](assets/page_fallout.png)

1. 적절한 [날짜 범위](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md)를 구성합니다.
1. 클릭 **[!UICONTROL Next]**.
1. 마법사의 2단계에서 **[!UICONTROL Row Labels]**&#x200B;링크를 클릭합니다 **[!UICONTROL Define Checkpoints]** . 폴아웃 보고서에서는 패턴이 미리 정의된 경로 보고서와 달리 항상 경로 요소를 정의해야 합니다. 

   ![](assets/define_checkpoints.png)

1. **[!UICONTROL Filter]** 옵션을 선택합니다.

1. 대화 **[!UICONTROL Define Site Section Fallout Checkpoints]** 상자에서 셀 범위 또는 목록에서 체크포인트를 정의합니다. 그런 다음 **[!UICONTROL OK]**&#x200B;를 클릭합니다.
1. 셀 범위에서 선택할지 또는 목록에서 선택할지를 결정합니다.
1. If you select from a list, click **[!UICONTROL Add]** to select checkpoints to add to the fallout path. 3 및 8 체크포인트 사이에서 정의할 수 있습니다. (Search for available elements by clicking **[!UICONTROL More]**.)

   필터 세분화에 대한 자세한 내용은 [필터 차원](/help/analyze/report-builder/layout/c-filter-dimensions/filter-dimensions.md)을 참조하십시오. 1. Move **[!UICONTROL Available Elements]** from the left column to the right by selecting them and clicking the orange arrow.
1. 세 **[!UICONTROL OK]** 번 클릭한 다음 을 클릭합니다 **[!UICONTROL Finish]**.

   보고서가 새로 고침됩니다.
