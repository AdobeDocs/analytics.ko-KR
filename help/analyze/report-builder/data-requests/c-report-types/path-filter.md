---
description: 경로 지정 보고서에 필터를 적용하는 단계에 대해 설명합니다.
title: 요청 마법사를 사용하여 경로 보고서 필터링
uuid: 9b22d5b5-7ae8-49a2-90ae-0c1075562bbe
feature: Report Builder
role: 비즈니스 전문가, 관리자
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 99%

---


# 요청 마법사를 사용하여 경로 보고서 필터링

경로 지정 보고서에 필터를 적용하는 단계에 대해 설명합니다.

이 예제에서는 사이트 섹션 경로를 사용합니다.

1. Adobe Report Builder에서 **[!UICONTROL 만들기]**&#x200B;를 클릭하여 요청 마법사를 엽니다.
1. 적절한 보고서 세트를 선택합니다.
1. 왼쪽의 트리 보기에서 **[!UICONTROL 경로]** > **[!UICONTROL 사이트 섹션]** > **[!UICONTROL 사이트 섹션 경로]**&#x200B;를 선택합니다.

   ![](assets/site_section_path_1.png)

1. 해당 날짜를 지정합니다.
1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.
1. 마법사 2단계의 **[!UICONTROL 행 레이블]**&#x200B;에서 **[!UICONTROL 상위 1-10(패턴이 적용됨)]** 링크를 클릭합니다. 경로 보고서에는 기본적으로 패턴이 적용되어 있습니다.

   ![](assets/site_section_path_2.png)

1. **[!UICONTROL 필터]** 옵션을 선택합니다.

   ![](assets/filter_option.png)

1. **[!UICONTROL &#39;사이트 섹션 경로&#39; 경로 패턴 정의]** 대화 상자에서 다음을 지정할 수 있습니다.
   1. 첫 번째 보고서의 시작 등급 
   1. 이 보고서에 표시하려는 항목 수 
1. **[!UICONTROL 편집]**&#x200B;을 클릭하여 경로 패턴을 정의합니다.
1. 사용자 지정 패턴을 원하는 경우 왼쪽 목록의 **[!UICONTROL 패턴 개체]**&#x200B;를 오른쪽의 **[!UICONTROL Pattern Builder 캔버스]**&#x200B;로 드래그하여 놓습니다.

   ![](assets/custom_pattern.png)

1. **[!UICONTROL 패턴 선택]** 드롭다운 목록에서 미리 정의한 패턴을 선택하고 수정할 수 있습니다. 사용 가능한 패턴은 다음과 같습니다. 

   ![](assets/select_a_pattern.png)

   일부 패턴인 시작 경로의 다음 항목 패턴, 종료 경로의 이전 항목 패턴, 다음 항목 패턴은 Report Builder에만 국한됩니다.
1. 미리 정의한 패턴을 편집하려면
   1. 패턴을 선택합니다. 예를 들어 **[!UICONTROL 종료한 사이트 패턴]**&#x200B;을 선택합니다.![](assets/exited_site_pattern.png)

   1. 종료하기 전에 사용자가 이동하는 사이트 섹션 경로를 정의해야 합니다. **[!UICONTROL 특정 항목: 0개 선택함]**&#x200B;을 클릭합니다. 셀 범위에서 선택하거나(기존 요청을 편집하는 경우) 섹션 목록에서 선택하여 이 경로를 정의할 수 있습니다.
   1. 이전 요청의 셀 범위에서 선택하려면 **[!UICONTROL 셀 범위에서]**&#x200B;를 선택하고 셀 선택기 아이콘을 클릭합니다. 그런 후 보고서에서 셀을 선택합니다. ![](assets/choose_site_section_paths.png)

   1. 사이트 섹션 목록에서 선택하려면 **[!UICONTROL 목록에서]**&#x200B;를 선택하고 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
   1. **[!UICONTROL 사용 가능한 요소]** 열의 요소를 선택한 후 주황색 화살표를 클릭하여 **[!UICONTROL 선택한 요소]** 열로 이동합니다. **[!UICONTROL 확인]**&#x200B;을 클릭합니다. ![](assets/move_site_section_elements.png)

   1. 막 설정한 패턴을 저장하려면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
   1. **[!UICONTROL 확인]**&#x200B;을 세 번 클릭한 다음 **[!UICONTROL 마침]**&#x200B;을 클릭합니다. 필터링한 패턴 요청이 생성됩니다.
