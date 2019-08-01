---
description: 통합 코드를 사용하려면 통합 모듈이 Adobe Analytics 배포 내에 있어야 합니다.
seo-description: 통합 코드를 사용하려면 통합 모듈이 Adobe Analytics 배포 내에 있어야 합니다.
seo-title: 통합 모듈 포함
title: 통합 모듈 포함
uuid: e 574 f 3 db -49 fa -4 f 72-bbcf-fd 98540 d 3198
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Including the Integrate Module{#including-the-integrate-module}

통합 코드를 사용하려면 통합 모듈이 Adobe Analytics 배포 내에 있어야 합니다.

배포의 일부로 통합 모듈이 아직 없는 경우 구현 유형에 따라 다음 단계를 완료하십시오.

## For AppMeasurement v1.0+ {#section-f28d090bf2404cabaae34cd9c66fc575}

1. **[!UICONTROL Analytics]** &gt; **[!UICONTROL 관리]** &gt; **[!UICONTROL 코드 관리자에서 다운로드한 appmeasurement zip 파일의 압축을 풉니다]**.

1. Open the file named [!DNL AppMeasurement_Module_Integrate.js].
1. Copy and paste the contents of this file into your primary [!DNL AppMeasurement.js] file.

   >[!NOTE]
   >
   >파일 내에서 이 줄 주석을 변경하지 마십시오.

## For Legacy Code (H-code) {#section-bba8ad8c715e4f97883e7de3269f681a}

1. [지원] 탭 아래에 있는 데이터 커넥터 UI 내의 "리소스" 영역에서 통합 모듈을 다운로드합니다.

   ![](assets/h_code.png)

1. Copy and paste the contents of that file into your [!DNL s_code] file.

   >[!NOTE]
   >
   >파일 내에서 이 줄 주석을 변경하지 마십시오.

