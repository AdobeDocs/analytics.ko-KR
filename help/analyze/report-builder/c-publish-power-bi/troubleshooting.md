---
description: Power BI에서 Report Builder을 사용할 때의 일반적인 문제
title: Power BI 통합 문제 해결
feature: Report Builder
role: User, Admin
exl-id: adb13a0e-99fb-48f5-add2-204d155e467f
source-git-commit: 1ee50c6a2231795b2ad0015a79e09b7c1c74d850
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 51%

---

# Power BI 통합 문제 해결

Power BI에서 Report Builder을 사용할 때 발생하는 일반적인 문제를 연구하고 해결합니다.

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

## 조직 리소스에 액세스하려면 Report Builder 권한을 부여해야 합니다. 이 액세스 권한은 관리자만 부여할 수 있습니다. 관리자에게 권한을 요청하십시오.

Microsoft 관리자가 다음에 있는 &quot;사용자가 애플리케이션을 등록할 수 있음&quot; 설정을 검토하도록 합니다. **[!UICONTROL Microsoft Azure]** > **[!UICONTROL Azure Active Directory]** > **[!UICONTROL 사용자 설정에서 옵션을 사용할 수 있습니다.]**. 이 옵션이 아니오로 설정되어 있으면 해당 관리자가 이러한 유형의 애플리케이션을 등록할 수 있습니다.

사용자는 다음을 사용하여 액세스 권한을 부여할 수 있습니다 [링크](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=logint&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US).

관리자는 다음을 사용하여 각 관리자에 대한 액세스 권한을 부여했습니다 [링크](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=admin_consent&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US).
