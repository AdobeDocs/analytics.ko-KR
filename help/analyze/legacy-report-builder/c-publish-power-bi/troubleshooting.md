---
description: Report Builder를 Power BI와 함께 사용할 때의 일반적인 문제입니다.
title: Power BI 통합 문제 해결
feature: Report Builder
role: User, Admin
exl-id: adb13a0e-99fb-48f5-add2-204d155e467f
TQID: https://experienceleague.adobe.com/Q4n08pGcqBwhUl5q3VnWhuVcW9E-tdvv3LoHSLoGleA
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 382
ht-degree: 27%

---

# Power BI 통합 문제 해결

{{legacy-arb}}

Report Builder를 Power BI와 함께 사용할 때의 일반적인 문제를 조사하고 해결합니다.

## Power BI 게시 실패

Power BI 게시가 필요한 예약된 통합 문서는 실행되고 있는 Power BI 서비스에 종속됩니다. 게시 실패의 두 가지 주요 원인은 다음과 같습니다.

* Power BI 서비스가 다운되었을 수 있습니다.
* 통합 문서를 예약한 사용자에게 더 이상 유효한 Microsoft 계정 자격 증명이 없습니다.

각 Report Builder 예약 작업은 예약된 실행당 세 번의 시도를 받습니다.

* 첫 번째 시도 실패 후 &quot;&quot;이 예약된 통합 문서를 Microsoft Power BI에 게시할 수 없습니다. 잠시 후 다시 시도하겠습니다.&quot;
* 두 번째 실패 시도 후에는 메시지가 표시되지 않습니다.
* 세 번째 시도 실패 후 &quot;이 통합 문서를 Power BI에 게시할 수 없습니다.&quot;라는 메시지가 표시됩니다.

## Power BI의 손상된 시각화

Report Builder 요청을 Power BI에 게시한 후 시각화가 중단될 수 있는 주요 이유는 다음과 같습니다.

* 지표 또는 차원 변경과 같은 Report Builder의 요청을 편집한 다음 Power BI에 다시 게시했습니다. 요청을 편집하면 시각화가 손상될 수 있습니다.
* 시각화에 사용된 요청을 삭제했습니다.

>[!IMPORTANT]
>
>Report Builder에서는 관리자가 조직 리소스에 대한 액세스 권한을 부여해야 합니다. 액세스 권한이 필요한 경우 관리자에게 권한 부여를 요청하십시오.
> Microsoft 관리자는 **[!UICONTROL Microsoft Azure]** > **[!UICONTROL Azure Active Directory]** > **[!UICONTROL 사용자 설정 허용 옵션]**&#x200B;에 있는 *사용자가 응용 프로그램을 등록할 수 있음* 설정을 검토할 수 있습니다. 이 옵션이 **아니요**(으)로 설정된 경우 관리자는 이러한 유형의 애플리케이션을 등록할 수 있습니다.

사용자는 [Microsoft Power BI 계정](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&prompt=logint&client_id=8d84f6d8-29a4-4484-a670-589b32400278&redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&locale=en_US)에 로그인하여 액세스 권한을 부여할 수 있습니다.

관리자는 [관리자의 Microsoft Power BI 계정](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&prompt=admin_consent&client_id=8d84f6d8-29a4-4484-a670-589b32400278&redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&locale=en_US)에 로그인하여 모든 사용자에게 액세스 권한을 부여할 수 있습니다.

## API 제한 도달

Power BI의 보고는 Analytics Reporting API와 작동하므로 API 임계값 제한이 적용됩니다.
