---
description: 폴아웃 보고서에 필터를 적용하는 단계에 대해 설명합니다.
title: 요청 마법사를 사용하여 폴아웃 보고서 필터링
feature: Report Builder
role: User, Admin
exl-id: 6134d7d4-7287-4a83-92b6-d250ca15cf69
source-git-commit: ae6ffed05f5a33f032d0c7471ccdb1029154ddbd
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 80%

---

# 요청 마법사를 사용하여 폴아웃 보고서 필터링

{{legacy-arb}}

폴아웃 보고서에 필터를 적용하는 단계에 대해 설명합니다.

이 예에서는 페이지 폴아웃 보고서를 보여 줍니다.

1. Adobe Report Builder에서 **[!UICONTROL 만들기]**&#x200B;를 클릭하여 요청 마법사를 엽니다.
1. 적절한 보고서 세트를 선택합니다.
1. 왼쪽의 트리 보기에서 **[!UICONTROL 경로]** > **[!UICONTROL 페이지]** > **[!UICONTROL 페이지 폴아웃]**&#x200B;을 선택합니다.

   ![Report Builder 디렉터리에 대한 Windows 트리 보기를 보여 주는 스크린샷입니다. 페이지 폴아웃을 선택했습니다.](assets/page_fallout.png)

1. 적절한 [날짜 범위](/help/analyze/legacy-report-builder/data-requests/configuring-report-dates/custom-calendar.md)를 구성합니다.
1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.
1. 마법사 2단계의 **[!UICONTROL 행 레이블]**&#x200B;에서 **[!UICONTROL 체크포인트 정의]** 링크를 클릭합니다. 폴아웃 보고서에서는 패턴이 미리 정의된 경로 보고서와 달리 항상 경로 요소를 정의해야 합니다.

   ![체크포인트 정의 링크를 보여주는 스크린샷](assets/define_checkpoints.png)

1. **[!UICONTROL 필터]** 옵션을 선택합니다.

1. **[!UICONTROL 사이트 섹션 폴아웃 체크포인트 정의]** 대화 상자에서 셀 범위 또는 목록에서 체크포인트를 정의합니다. 그런 다음 **[!UICONTROL 확인]**&#x200B;을 클릭합니다.
1. 셀 범위에서 선택할지 또는 목록에서 선택할지를 결정합니다.
1. 목록에서 선택하는 경우 **[!UICONTROL 추가]**&#x200B;를 클릭하고 폴아웃 경로에 추가할 체크포인트를 선택합니다. 3 및 8 체크포인트 사이에서 정의할 수 있습니다. **[!UICONTROL 더 보기]**&#x200B;를 클릭하여 사용 가능한 요소를 검색합니다.

   필터 세분화에 대한 자세한 내용은 [필터 Dimension](/help/analyze/legacy-report-builder/layout/c-filter-dimensions/filter-dimensions.md)을 참조하세요.

1. **[!UICONTROL 사용 가능한 요소]**&#x200B;를 선택하고 주황색 화살표를 클릭하여 왼쪽 열에서 오른쪽으로 이동합니다.
1. **[!UICONTROL 확인]**&#x200B;을 세 번 클릭하고 **[!UICONTROL 마침]**&#x200B;을 클릭합니다.

   보고서가 새로 고침됩니다.
