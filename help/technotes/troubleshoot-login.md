---
title: Adobe Analytics 로그인 문제 해결
description: Adobe Analytics에 로그인할 수 없는 경우 취해야 할 단계입니다.
exl-id: e670a043-c55b-4717-9b60-613ea4d04382
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '609'
ht-degree: 100%

---

# Adobe Analytics 로그인 문제 해결

Adobe Analytics는 여러 인증 방법을 사용하여 로그인합니다.

* Experience Cloud를 통한 Adobe ID
* 레거시 Analytics ID
* Single Sign-On

**정기적으로 Analytics에 액세스하며 로그인 문제가 발생하기 시작하는 경우 브라우저의 쿠키와 캐시를 지우면 대부분의 문제가 해결됩니다.**

때때로 가용성 문제가 로그인 기능에 영향을 미칠 수 있습니다. 진행 중인 인시던트에 대해서는 [status.adobe.com](https://status.adobe.com)를 확인하십시오. 그렇지 않으면 조직의 인증 방법에 따라 적절한 섹션을 사용하십시오.

## Adobe ID

Experience Cloud를 사용하여 Adobe Analytics에 로그인할 때 발생하는 문제를 해결합니다.

1. [experience.adobe.com](https://experience.adobe.com)으로 이동합니다. 이 사이트에 액세스할 수 없는 경우 조직에서 방화벽을 통해 이 도메인을 허용하지 않을 수 있습니다. 조직의 IT 팀과 협력하여 허용을 받으십시오. IT 팀에 제공할 수 있는 유용한 정보는 [Adobe Experience Cloud에서 사용되는 IP 및 도메인](https://helpx.adobe.com/analytics/kb/adobe-ip-addresses.html)을 참조하십시오.

2. Adobe ID를 사용하여 인증: **[!UICONTROL Adobe ID로 로그인]**&#x200B;을 클릭합니다. 로그인할 수 없는 경우 이메일 주소를 올바르게 입력했는지 다시 확인하십시오. 다른 방법은 **[!UICONTROL 암호 재설정]**&#x200B;을 클릭하고 안내에 따라 Adobe ID 비밀번호를 재설정하는 것입니다.

3. 인증 후 Analytics 액세스: 오른쪽 상단의 9-그리드 아이콘을 클릭한 다음 분석을 클릭합니다. 이 옵션이 없거나 회색으로 표시된 경우 조직 내 제품 관리자와 협력하여 Analytics에 액세스할 수 있는 올바른 권한이 있는지 확인하십시오.

## 레거시 Analytics ID

조직의 사용자가 로그인을 시도할 때 다음 오류를 수신할 수 있습니다.

*이 계정은 로그인 시도 실패 횟수가 너무 많아 보안 규정에 따라 잠겼습니다.*

브라우저의 쿠키/캐시를 지워도 문제가 해결되지 않으면 조직의 Analytics 관리자와 협력하여 사용자의 암호를 재설정하십시오.

>[!IMPORTANT]
>
>사용자 암호를 재설정하는 다음의 단계는 Adobe ID가 아닌 레거시 Analytics ID에만 적용됩니다. 조직에서 Adobe ID를 사용하는 경우 [adminconsole.adobe.com](https://adminconsole.adobe.com)에서 사용자 계정을 관리할 수 있습니다.

1. 관리 권한이 있는 계정으로 Adobe Analytics에 로그인합니다.
2. **[!UICONTROL 관리자]** > **[!UICONTROL 사용자 관리]**&#x200B;로 이동합니다.
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
