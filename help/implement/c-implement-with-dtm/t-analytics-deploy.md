---
description: 다이내믹 태그 관리를 사용하여 배포할 Adobe Analytics 도구를 만듭니다. 이 절차에서는 수동(이전) 구현에 대해 설명합니다.
keywords: 다이내믹 태그 관리
seo-description: 다이내믹 태그 관리를 사용하여 배포할 Adobe Analytics 도구를 만듭니다. 이 절차에서는 수동(이전) 구현에 대해 설명합니다.
seo-title: Adobe Analytics 수동 구현(이전)
solution: Experience Cloud,Analytics,Target,다이내믹 태그 관리
title: Adobe Analytics 수동 구현(이전)
uuid: d3ad2035-39 파섹
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Adobe Analytics 수동 구현(이전)

Create an Adobe Analytics tool for deployment using [!UICONTROL Dynamic Tag Management]. 이 절차에서는 수동(이전) 구현에 대해 설명합니다.

자동 구현 관리에 대한 자세한 내용은 [Adobe Analytics 도구 추가](../../implement/c-implement-with-dtm/c-aa-tool/analytics-dtm.md#concept_FBA6679A0B79490F8296437F11E5E4F8).

수동 구성을 자동으로 변경하려면 도구를 편집하고 **[!UICONTROL 자동 구성 활성화를 클릭합니다]**.

1. Analytics 측정 코드를 다운로드 다운로드합니다. 
   1. Analytics에서 관리 **[!UICONTROL &gt; 코드]** 관리자를 **[!UICONTROL 클릭합니다]**.
   1. Click **[!UICONTROL JavaScript (new)]** to download the code locally.
1. 다이내믹 [!UICONTROL 태그 관리에서]웹 속성을 [만듭니다](../../implement/c-implement-with-dtm/t-create-web-property.md#task_960467FBB7A54499AC228CB3AA3C4123).

   ![](assets/dtm-property.png)

   웹 속성을 만들면, [!UICONTROL 대시보드]의 [!UICONTROL 웹 속성] 탭에서 편집할 수 있습니다. 웹 속성을 활성화할 필요는 없습니다.에서 보냅니다.

1.  Analytics 도구를 속성에 추가합니다. 
   1. On the **[!UICONTROL Web Properties]** tab, click the property.
   1. On the **[!UICONTROL Overview]** tab, click **[!UICONTROL Add a Tool]**.
   1. From the **[!UICONTROL Tool Type]** menu, select **[!UICONTROL Adobe Analytics]**.

      ![](assets/dtm-add-analytics-tool.png)

   1. 다음 필드를 구성합니다. 

      | 요소 | 설명 |
      |---|---|
      | 도구 유형 | Analytics, Target, Social 등과 같은 Experience Cloud 솔루션. |
      | 도구 이름 | 이 도구의 이름입니다. 이 이름은 [!UICONTROL 설치된 도구] 아래의 [!UICONTROL 개요]에 표시됩니다. |
      | 프로덕션 계정 ID | 데이터 수집을 위한 프로덕션 계정 번호입니다. 다이내믹 태그 관리는 프로덕션 및 스테이징 환경에서 올바른 계정을 자동으로 설치합니다. |
      | 스테이징 계정 ID | 개발이나 테스트 환경에서 사용되는 번호입니다. 스테이징 계정은 테스트 데이터를 프로덕션과 구별합니다. |

1. **[!UICONTROL 도구 만들기를 클릭합니다]**.

   설치된 도구는 [!UICONTROL 개요] 탭에 표시됩니다.

1. To configure the code, click **[!UICONTROL Settings]** ![](assets/settings_gear.png).

   적어도, **[!UICONTROL 쿠키]를 클릭하고, 추적 서버와 SSL 추적 서버를 구성합니다.**

1. 일반을 **[!UICONTROL 클릭하고]** 핵심 AppMeasurement 코드를 [삽입합니다](../../implement/c-implement-with-dtm/c-aa-tool/t-appmeasurement-code.md#task_068D72664B2743359A64ADB8692D3658).
1. [데이터를 수집할](../../implement/c-implement-with-dtm/c-rules/t-rules-create.md#task_B7FB5ED415AF430C952265AC2835C0DB) 페이지 로드 규칙을 [!DNL Analytics]정의합니다.

   이제 규칙을 정의하여 분석 데이터를 수집할 준비가 되었습니다. 먼저 몇 개의 데이터 요소를 정의할 수도 있습니다. 데이터 요소는 페이지에서 규칙을 구성하는 데 사용할 수 있는 데이터를 추출할 수 있도록 해줍니다. 시작하려면, 각 페이지에서 [!DNL Analytics] 데이터를 수집하기 위한 조건이 없는 페이지 로드 규칙을 정의할 수 있습니다.
1. [[포함] 탭에서 머리글 및 바닥글 코드를 추가](../../implement/c-implement-with-dtm/c-headers-footers/t-header-footer-code.md#task_43C8DD699A514638B0620775C06423E5)합니다.

   스테이징의 경우, 기본 Amazon 호스팅 옵션은 그대로 두어도 됩니다. 프로덕션 롤아웃 전에 필요할 경우 변경할 수 있습니다.
1. (Optional) Click **[!UICONTROL Settings]** ![](assets/settings_gear.png) on the Options tab, and configure the Adobe Analytics code.

   >[!NOTE]
   >
   >The settings on the [!UICONTROL Adobe Analytics] page (General, Cookies, and so on) override settings in your `s_code`. 이러한 설정이 `s_code`에 있을 경우에는 여기에서 반복할 필요가 없습니다.

