---
title: Adobe Analytics 로그인 문제 해결
description: Adobe Analytics에 로그인할 수 없는 경우 취해야 할 단계입니다.
feature: Analytics Basics
exl-id: e670a043-c55b-4717-9b60-613ea4d04382
TQID: https://experienceleague.adobe.com/akXZpx8BUywqvI2NGvk9dqIBL-pHEAza1-I05pC89io
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: a421fb65-2c82-457a-921c-28c46b697a39
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 9e2c89f4188c723b4623a6e7859b74ede15e155b
workflow-type: tm+mt
source-wordcount: 607
ht-degree: 88%

---

# Adobe Analytics 로그인 문제 해결

Adobe Analytics는 여러 인증 방법을 사용하여 로그인합니다.

* Adobe ID - CX Enterprise
* 레거시 Analytics ID
* Single Sign-On

**정기적으로 Analytics에 액세스하며 로그인 문제가 발생하기 시작하는 경우 브라우저의 쿠키와 캐시를 지우면 대부분의 문제가 해결됩니다.**

때때로 가용성 문제가 로그인 기능에 영향을 미칠 수 있습니다. 진행 중인 인시던트에 대해서는 [status.adobe.com](https://status.adobe.com/ko-kr)를 확인하십시오. 그렇지 않으면 조직의 인증 방법에 따라 적절한 섹션을 사용하십시오.

## Adobe ID

CX Enterprise를 사용한 Adobe Analytics 로그인 관련 문제를 해결합니다.

1. [Adobe CX Enterprise](https://experience.adobe.com)&#x200B;(으)로 이동합니다. 이 사이트에 액세스할 수 없는 경우 조직에서 방화벽을 통해 이 도메인을 허용하지 않을 수 있습니다. 조직의 IT 팀과 협력하여 허용을 받으십시오. IT 팀에 제공할 수 있는 유용한 정보는 [Adobe Analytics에서 사용하는 IP 주소](/help/technotes/ip-addresses.md)를 참조하십시오.

2. Adobe ID를 사용하여 인증: **[!UICONTROL Adobe ID로 로그인]**&#x200B;을 클릭합니다. 로그인할 수 없는 경우 이메일 주소를 올바르게 입력했는지 다시 확인하십시오. 다른 방법은 **[!UICONTROL 암호 재설정]**&#x200B;을 클릭하고 안내에 따라 Adobe ID 비밀번호를 재설정하는 것입니다.

3. 인증 후 Analytics 액세스: 오른쪽 상단의 9-그리드 아이콘을 클릭한 다음 분석을 클릭합니다. 이 옵션이 없거나 회색으로 표시된 경우 조직 내 제품 관리자와 협력하여 Analytics에 액세스할 수 있는 올바른 권한이 있는지 확인하십시오.

## 레거시 Analytics ID

조직의 사용자가 로그인을 시도할 때 다음 오류를 수신할 수 있습니다.

*이 계정은 로그인 시도 실패 횟수가 너무 많아 보안 규정에 따라 잠겼습니다.*

브라우저의 쿠키/캐시를 지워도 문제가 해결되지 않으면 조직의 Analytics 관리자와 협력하여 사용자의 암호를 재설정하십시오.

>[!IMPORTANT]
>
>사용자의 암호를 재설정하는 다음의 단계는 Adobe ID의 암호가 아닌 레거시 Analytics ID에만 적용됩니다. 조직에서 Adobe ID의 계정을 사용하는 경우 [adminconsole.adobe.com](https://adminconsole.adobe.com)에서 사용자 계정을 관리할 수 있습니다.

1. 관리 권한이 있는 계정으로 Adobe Analytics에 로그인합니다.
2. **[!UICONTROL 관리자]** > **[!UICONTROL 모든 관리자]** > **[!UICONTROL 사용자 관리]**&#x200B;로 이동합니다.
3. **[!UICONTROL 사용자]** 탭을 클릭한 다음 원하는 사용자 옆에 있는 **[!UICONTROL 편집]**&#x200B;을 클릭합니다.
4. 암호를 임의의 값으로 변경하고 **[!UICONTROL 다음 로그인시 사용자가 암호를 변경해야 함]** 확인란을 선택합니다.
5. 사용자에게 새 암호를 알립니다.

## Single Sign-On

SSO (Single Sign-On) 문제를 해결하려면 조직의 관리자에게 문의하십시오.

## 만료된 로그인

조직의 사용자가 로그인을 시도할 때 다음 오류를 수신할 수 있습니다.

*오류: 이 로그인이 만료되었습니다.*

이 오류는 의도한 대로 작동합니다. Adobe Analytics는 관리자에게 사용자 계정이 유효한 날짜 범위를 설정할 수 있는 기능을 제공합니다. 현재 날짜가 계정의 유효한 날짜 범위를 벗어난 경우 로그인할 수 없습니다. 조직의 Analytics 관리자와 협력하여 로그인의 유효한 날짜 범위를 확장하십시오. Adobe 고객 지원 센터는 사용자 계정의 유효한 로그인 날짜 범위를 변경할 권한이 없습니다.

## 기타 로그인 문제

위 단계 중 어느 것도 작동하지 않으면 로그인 문제의 범위를 확인하십시오.

* 다른 브라우저를 사용할 때 문제가 발생합니까, 아니면 모든 브라우저에 걸쳐 문제가 발생합니까?
* 네트워크의 다른 시스템에서 문제가 발생합니까, 아니면 여러 시스템에 걸쳐 문제가 발생합니까?
* 모바일 데이터 연결, 라이브러리 또는 홈 네트워크와 같은 다른 네트워크를 사용하여 로그인해 보십시오. 네트워크 전체에 문제가 있습니까?

네트워크 내에서 문제가 격리된 경우 조직의 IT 팀과 협력하여 문제를 해결하십시오. 단일 네트워크로 제한되지 않는 경우 Adobe 고객 지원 센터에 문의하십시오.
