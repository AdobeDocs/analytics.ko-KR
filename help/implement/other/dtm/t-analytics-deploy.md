---
description: Dynamic Tag Management를 사용하여 배포할 Adobe Analytics 도구를 만듭니다. 이 절차에서는 수동(이전) 구현에 대해 설명합니다.
keywords: Dynamic Tag Management
solution: Experience Cloud,Analytics,Target,Dynamic Tag Management
title: Adobe Analytics 수동 구현(이전)
uuid: d3ad2035-393d-4a77-81f6-e749ee717c09
translation-type: tm+mt
source-git-commit: dfe8409b13fcf67eae6a0c404f83c1209f89ae12

---


# Adobe Analytics 수동 구현(이전)

[!UICONTROL Dynamic Tag Management]를 사용하여 배포할 Adobe Analytics 도구를 만듭니다. 이 절차에서는 수동(이전) 구현에 대해 설명합니다.

자동 구현 관리에 대한 자세한 내용은 [Adobe Analytics 도구 추가](/help/implement/other/dtm/c-aa-tool/analytics-dtm.md).

수동 구성을 자동으로 변경하려면 도구를 편집하고 **[!UICONTROL 자동 구성 활성화를 클릭합니다]**.

1. Analytics 측정 코드를 다운로드 다운로드합니다. 
   1. Analytics에서 **[!UICONTROL 관리자]** > **[!UICONTROL 코드 관리자]**&#x200B;를 클릭합니다.
   1. **[!UICONTROL JavaScript(신규)]**&#x200B;를 클릭하여 코드를 로컬로 다운로드합니다.
1. [!UICONTROL Dynamic Tag Management]에서 [웹 속성을 만듭니다](/help/implement/other/dtm/t-create-web-property.md).

   ![](assets/dtm-property.png)

   웹 속성을 만들면, [!UICONTROL 대시보드]의 [!UICONTROL 웹 속성] 탭에서 편집할 수 있습니다. 웹 속성을 활성화할 필요는 없습니다.에서 보냅니다.

1.  Analytics 도구를 속성에 추가합니다. 
   1. **[!UICONTROL 웹 속성]** 탭에서 속성을 클릭합니다.
   1. **[!UICONTROL 개요]** 탭에서 **[!UICONTROL 도구 추가]**&#x200B;를 클릭합니다.
   1. **[!UICONTROL 도구 유형]** 메뉴에서 **[!UICONTROL Adobe Analytics]**&#x200B;를 선택합니다.

      ![](assets/dtm-add-analytics-tool.png)

   1. 다음 필드를 구성합니다. 

      | 요소 | 설명 |
      |---|---|
      | 도구 유형 | Analytics, Target, Social 등과 같은 Experience Cloud 솔루션. |
      | 도구 이름 | 이 도구의 이름입니다. 이 이름은 [!UICONTROL 설치된 도구] 아래의 [!UICONTROL 개요]에 표시됩니다. |
      | 프로덕션 계정 ID | 데이터 수집을 위한 프로덕션 계정 번호입니다. Dynamic Tag Management는 프로덕션 및 스테이징 환경에서 올바른 계정을 자동으로 설치합니다. |
      | 스테이징 계정 ID | 개발이나 테스트 환경에서 사용되는 번호입니다. 스테이징 계정은 테스트 데이터를 프로덕션과 분리시킵니다. |

1. **[!UICONTROL 도구 만들기를 클릭합니다]**.

   설치된 도구는 [!UICONTROL 개요] 탭에 표시됩니다.

1. 코드를 구성하려면 **[!UICONTROL 설정]**![](assets/settings_gear.png)()을 클릭합니다. 

   적어도, **[!UICONTROL 쿠키]**&#x200B;를 클릭하고, 추적 서버와 SSL 추적 서버를 구성합니다.

1. **[!UICONTROL 일반]**&#x200B;을 클릭하고 [핵심 AppMeasurement 코드를 삽입](/help/implement/other/dtm/c-aa-tool/t-appmeasurement-code.md)합니다.
1. [!DNL Analytics] 데이터를 수집할 [페이지 로드 규칙](/help/implement/other/dtm/c-rules/t-rules-create.md)을 정의합니다.

   이제 규칙을 정의하여 분석 데이터를 수집할 준비가 되었습니다. 먼저 몇 개의 데이터 요소를 정의할 수도 있습니다. 데이터 요소는 페이지에서 규칙을 구성하는 데 사용할 수 있는 데이터를 추출할 수 있도록 해줍니다. 시작하려면, 각 페이지에서 [!DNL Analytics] 데이터를 수집하기 위한 조건이 없는 페이지 로드 규칙을 정의할 수 있습니다.
1. [포함 탭에서 머리글 및 바닥글 코드를 추가](/help/implement/other/dtm/c-headers-footers/t-header-footer-code.md)합니다.

   스테이징의 경우, 기본 Amazon 호스팅 옵션은 그대로 두어도 됩니다. 프로덕션 롤아웃 전에 필요할 경우 변경할 수 있습니다.
1. (선택 사항) 옵션 탭에서 **[!UICONTROL 설정]**![](assets/settings_gear.png)()을 클릭하고 Adobe Analytics 코드를 구성합니다.

   >[!NOTE]
   >
   >[!UICONTROL Adobe Analytics] 페이지의 설정(일반, 쿠키 등)은 `s_code`의 설정을 무시합니다. 이러한 설정이 `s_code`에 있을 경우에는 여기에서 반복할 필요가 없습니다.

