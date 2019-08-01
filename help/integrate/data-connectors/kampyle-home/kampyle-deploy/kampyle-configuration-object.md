---
description: 통합 마법사를 완료한 후에는 통합 구성 개체를 웹 속성에 배포해야 합니다.
seo-description: 통합 마법사를 완료한 후에는 통합 구성 개체를 웹 속성에 배포해야 합니다.
seo-title: 통합 구성 개체 배포
solution: Analytics
title: 통합 구성 개체 배포
uuid: E 951 C 864-2914-4324-9 F 03-5069 D 4 F 75 D 99
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Deploy the Integration Configuration Object{#deploy-the-integration-configuration-object}

통합 마법사를 완료한 후에는 통합 구성 개체를 웹 속성에 배포해야 합니다.

대부분의 경우 통합 구성 개체를 배포하는 가장 쉬운 방법은 Adobe Analytics 배포 코드에 포함하는 것입니다.

>[!NOTE]
>
>Adobe tagmanager 또는 다이내믹 태그 관리를 사용하여 Adobe Analytics를 배포하는 경우 해당 도구를 통해 통합 구성 개체를 쉽게 추가할 수 있습니다.

1. Navigate to the **[!UICONTROL Resources]** &gt; **[!UICONTROL Support]** tab of the integration.
1. **[!UICONTROL Kampyle 통합 코드 (JS)]** 리소스를 다운로드하고 저장합니다. 이 코드는 다음과 비슷합니다.

   ```
   /* Kampyle:  Integration configuration settings */
     window.k_sc_param = { "version":1.1 }
   ```

1. 다음 방법 중 하나를 사용하여 코드를 배포합니다.

       | ** Adobe tagmanager 또는 다이내믹 태그 관리를 사용합니다.** | 태그 관리 인터페이스를 사용하여 코드를 추가합니다. |
       |---|---|
       | **In all other cases** | Deliver the code to the organizational resource that is responsible for updating your Adobe Analytics deployment code.  |
   
