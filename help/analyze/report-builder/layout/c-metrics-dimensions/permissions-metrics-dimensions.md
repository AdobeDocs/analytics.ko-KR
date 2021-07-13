---
description: 이제 Adobe Report Builder에는 Analytics 관리 도구의 권한 부여 설정과 유사한 권한 부여 설정이 포함됩니다.
title: 차원 및 지표의 사용자 액세스 권한
uuid: b561407d-c4fa-4f1e-8b16-5ca46fcbf36f
feature: Report Builder
role: User, Admin
exl-id: 53cfdcf4-31c3-40ab-aca4-8f0f9be6fe13
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 100%

---

# 차원 및 지표의 사용자 액세스 권한

이제 Adobe Report Builder에는 Analytics 관리 도구의 권한 부여 설정과 유사한 권한 부여 설정이 포함됩니다.

관리자가 아닌 사용자는 이전에 액세스 권한이 없는 차원 및 지표를 가리키는 요청이 있는 통합 문서를 만들었을 수 있습니다. 이러한 권한이 이제 적용됩니다.

예를 들어 액세스 권한이 없는 차원이나 지표를 포함하는 요청을 새로 고치면 제한된 권한 오류가 나타납니다.

![](assets/arb_restrc_perm.png)

유지 관리하는 **각** Report Builder 통합 문서에 대한 다음 지침을 따르십시오.

1. 통합 문서를 엽니다.
1. 모든 요청 새로 고침.
1. 사용자 액세스 권한 오류가 표시되면 **[!UICONTROL CSV 파일 열기]**&#x200B;를 클릭하여 제한된 권한 오류 목록에 액세스할 수 있습니다.
1. 파일 “AllRestrictedPermissionErrors.xlsx”를 만들고 CSV 파일의 제한된 권한 오류 목록을 복사한 후 이 파일에 붙여넣습니다.
1. Report Builder 통합 문서를 닫습니다.

모든 통합 문서를 처리했으면 “AllRestrictedPermissionErrors.xlsx”에서 제한된 권한 오류의 포괄적 목록이 표시됩니다. 이 목록을 Adobe Analytics 사용자 액세스 관리자로 보내 지표 및 차원에 대한 액세스 권한을 요청하십시오.
