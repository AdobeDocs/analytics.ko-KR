---
description: 통합 마법사를 완료한 후에는 연결될 각 Qualtrics 설문 조사에 대한 통합을 활성화해야 합니다.
seo-description: 통합 마법사를 완료한 후에는 연결될 각 Qualtrics 설문 조사에 대한 통합을 활성화해야 합니다.
seo-title: Qualtrics Research Suite에서 통합 활성화
solution: Analytics
subtopic: Qualtrics
title: Qualtrics Research Suite에서 통합 활성화
topic: Data connectors
uuid: 2 CC 6 FA 4 A-D 17 E -4560-BD 5 B -1790851 D 6274
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Enabling the Integration in Qualtrics Research Suite{#enabling-the-integration-in-qualtrics-research-suite}

통합 마법사를 완료한 후에는 연결될 각 Qualtrics 설문 조사에 대한 통합을 활성화해야 합니다.

1. Qualtrics Research Suite에 로그인합니다.
1. **[!UICONTROL 내 설문 조사]** 탭에서 통합하려는 설문 조사의 **[!UICONTROL 편집]** 단추를 클릭합니다.
1. **[!UICONTROL 고급 옵션]** 메뉴를 클릭하고 **[!UICONTROL Adobe Analytics]**&#x200B;를 선택합니다. (이 옵션이 표시되지 않는 경우 관리자에게 권한 얻기에 대해 문의하십시오.)

   ![](assets/advanced_options.png)

1. Select the Adobe Analytics Configuration, then click **[!UICONTROL Save]**. 구성을 사용할 수 없는 경우 Adobe 통합 마법사를 아직 완료하지 않았을 수 있습니다.
   1. The **[!UICONTROL Include Partial Responses]** checkbox can be used to indicate that you’d like to capture data into Adobe Analytics after each partial survey screen is completed. 선택하지 않으면 완료된 설문 조사에 대해서만 데이터가 전송됩니다.
   1. The **[!UICONTROL Send Timestamp With Beacon]** checkbox should be used only when integrating with a Report Suite that is configured to receive time-stamped data (not common).
   ![](assets/integration_config.png)

