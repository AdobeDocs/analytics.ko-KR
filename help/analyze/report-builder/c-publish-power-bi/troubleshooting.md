---
description: Report Builder를 Power BI와 함께 사용할 때의 일반적인 문제입니다.
title: Power BI 통합 문제 해결
feature: Report Builder
role: User, Admin
exl-id: adb13a0e-99fb-48f5-add2-204d155e467f
source-git-commit: fb39f906d6c08713e4dc8211c917b2942502868e
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 68%

---

# Power BI 통합 문제 해결

Report Builder를 Power BI와 함께 사용할 때의 일반적인 문제를 조사하고 해결합니다.

## Power BI 게시 실패

Power BI 게시를 필요로 하는 예약된 통합 문서는 시작하여 실행하는 Power BI 서비스에 의존합니다. 게시 실패에 대한 두 가지 주된 원인은 다음과 같습니다.

* Power BI 서비스가 중단될 수 있습니다.
* 통합 문서를 예약한 사용자에게 더 이상 유효한 Microsoft 계정 자격 증명이 없습니다.

각 Report Builder 예약 작업은 예약된 실행당 세 번을 시도하게 됩니다.

* 첫 번째 시도에 성공하지 못하면 &quot;이 예약된 통합 문서를 Microsoft Power BI에 게시할 수 없습니다. 곧 다시 시도하겠습니다.&quot;라는 메시지가 표시됩니다.
* 두 번째 시도에 성공하지 못하면 메시지가 표시되지 않습니다.
* 세 번째 시도에 성공하지 못하면 &quot;이 통합 문서를 Power BI에 게시할 수 없습니다.&quot;라는 메시지가 표시됩니다.

## Power BI의 손상된 시각화

Report Builder 요청을 Power BI에 게시한 후 시각화가 손상될 수 있는 가장 가능성 있는 원인은 다음과 같습니다.

* 지표나 차원 변경과 같은 요청을 Report Builder에서 편집한 다음, Power BI에 다시 게시했습니다. 요청을 편집하면 시각화가 손상될 수 있습니다.
* 시각화에 사용된 요청을 삭제했습니다.

>[!IMPORTANT]
>
>Report Builder을 사용하려면 관리자가 조직 리소스에 대한 액세스 권한을 부여해야 합니다. 액세스 권한이 필요한 경우 관리자에게 권한 부여를 요청하십시오.
> Microsoft 관리자는 다음을 검토할 수 있습니다. *사용자가 애플리케이션을 등록할 수 있음* 다음에서 설정 찾음: **[!UICONTROL Microsoft Azure]** > **[!UICONTROL Azure Active Directory]** > **[!UICONTROL 사용자 설정에서 옵션을 허용합니다.]**. 이 옵션이 로 설정된 경우 **아니요**&#x200B;그런 다음 관리자는 이러한 유형의 애플리케이션을 등록할 수 있습니다.

사용자는 로그인함으로써 액세스 권한을 부여할 수 있습니다. [Microsoft Power BI 계정](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=logint&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US).

관리자는 모든 사용자에게 로그인하여 액세스 권한을 부여할 수 있습니다. [관리자의 Microsoft Power BI 계정](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=admin_consent&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US).

## API 제한 도달

Power BI의 보고는 Analytics Reporting API와 작동하므로 API 임계값 제한이 적용됩니다. 자세한 내용은 [웹 서비스 오류 코드](https://github.com/AdobeDocs/analytics-1.4-apis/blob/3dda746890743c2098256719d6595109b7748262/docs/getting-started/c_Web_Services_Error_Codes.md).
