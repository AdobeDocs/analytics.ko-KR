---
title: IP 로그인 제한 [!UICONTROL 적용을 위한 수명 종료]
description: IP 로그인 제한 적용의 종단 시간 및 [!UICONTROL 의미에 대해 알아봅니다.]
translation-type: tm+mt
source-git-commit: 490a856effac7ec3ff2430dff0ffdcee587bf933

---


# IP 로그인 제한 [!UICONTROL 적용을 위한 수명 종료]

Adobe **[Analytics의 IP 로그인 제한](/help/admin/company/security-manager.md)** 적용 기능을 사용하면 특정 IP 주소(안전한 것으로 간주됨)를 허용 목록에 추가하여 로그인 성공 및 Adobe Analytics 환경에 액세스할 수 있습니다. 대부분의 경우 이 기능은 사용자가 로그인할 수 있는 유일한 보안 IP 주소로 회사 IP 주소를 설정하는 데 사용됩니다. 따라서 Adobe Analytics를 사용하려면 사용자가 회사 사무실에 있거나 VPN을 통해 네트워크에 로그인해야 합니다.

이 기능은 2020년 10월에 사용이 종료됩니다.

## 이 기능을 사용하지 않는 이유는 무엇입니까?

이 기능은 Experience Cloud 로그인 마이그레이션 및/또는 Experience Cloud 로그인으로 인해 일부 상황에서 중단됩니다. 고객 속성 또는 대상 라이브러리를 사용하는 고객의 경우 **[!UICONTROL 중단되는]** 것으로 **[!UICONTROL 알려져 있습니다]**.

또한, 여러 Experience Cloud 솔루션을 소유하고 있는 경우, 이 기능이 존재하지 않거나 Analytics 자체 외부에서 지원되지 않으므로 다른 솔루션과 함께 Experience Cloud에 로그인하여 이 요구 사항을 우회할 수 있습니다. 사용자는 IP 스푸핑을 통해 이 문제를 해결할 수도 있습니다.

마지막으로 Adobe는 SSO(Single-Sign-On) 및 Federated ID를 통해 완벽하게 작동하는 탁월한 대체 솔루션을 제공합니다. 이 기능을 사용하면 사용자의 로그인 경험을 보다 효과적으로 제어하고 보안을 강화할 수 있습니다. 자세한 내용은 아래를 참조하십시오.

## 이 기능의 제거는 어떤 영향을 미칩니까?

IP 로그인 제한 **[!UICONTROL 적용을]** 설정한 모든 고객의 경우 이 기능은 2020년 10월에 제거됩니다. 이때 IP 로그인 제한 사항은 더 이상 적용되지 않습니다. 여전히 IP 주소로 로그인을 제한해야 하는 경우 SSO(Single-Sign-On) 및 Federated ID의 권장 솔루션을 검토하고 구현해야 합니다(자세한 정보 및 리소스).

또한 **[!UICONTROL IP 로그인 제한]** 적용 설정은 Analytics UI의 **[!UICONTROLAdmin &gt; 회사 설정 &gt; 보안 관리자에서]** 제거됩니다(아래 참조).

![](assets/sec-manager2.png)

## 다른 선택사항은 무엇입니까?

위에서 설명한 바와 같이 이 Analytics 기능은 사용이 종료됩니다. SSO 및 Federated ID를 구현할 수 있는 시간을 제공하기 위해 EOL 날짜가 2020년 10월로 연기되었습니다.

SSO와 Federated ID는 모두 IP 로그인 제한 기능보다 뛰어난 솔루션이며 더 많은 제어, 보안 및 기능을 제공합니다. SSO/Federated ID 설정 방법에 대한 자세한 내용은 다음 도움말 설명서를 참조하십시오. IT 부서에서 이를 철저히 읽고 이를 구현하도록 권장합니다.

* [Single Sign-On 및 Experience Cloud](https://spark.adobe.com/page/JeSB8EPEQIvjD/)
* [관리 콘솔 - ID 설정 설명서](https://helpx.adobe.com/enterprise/using/set-up-identity.html)
* [관리 콘솔 - ID 설정 자습서(비디오)](https://helpx.adobe.com/enterprise/how-to/identity-directories-domains.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&ref=helpx.adobe.com)
* [Federated ID 튜토리얼 구성(비디오)](https://helpx.adobe.com/enterprise/how-to/identity-configure-ids.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&ref=helpx.adobe.com)
* [Single Sign-On - 일반적인 질문](https://helpx.adobe.com/enterprise/using/sso-faq.html)
* [Adobe에서 지원하는 ID 유형](https://helpx.adobe.com/enterprise/using/identity.html)

IP 로그인 제한 사항에 대한 지원을 계속 요청하고 Experience Cloud에서 제공하도록 요청하려면 포럼 페이지에서 [이 기능에 대해 투표할 수](https://forums.adobe.com/ideas/11648)있습니다.