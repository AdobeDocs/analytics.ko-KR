---
title: '[!UICONTROL IP 로그인 제한 적용]의 사용 종료'
description: 수명 종료 시간 및 [!UICONTROL Enforce IP 로그인 제한]에 대한 의미
translation-type: tm+mt
source-git-commit: 940638b77f800b471f1ce4097a8ca6de98d518d3

---


# 사용 종료 [!UICONTROL Enforce IP login restrictions]

Adobe Analytics의 **[IP 로그인 제한 적용](/help/admin/company/security-manager.md)**기능을 사용하면 안전한 것으로 간주되는 특정 IP 주소를 허용 목록에 추가하여 Adobe Analytics 환경에 성공적으로 로그인하고 액세스할 수 있습니다. 많은 경우 이 기능은 사용자가 로그인할 수 있는 유일한 보안 IP 주소로서 회사 IP 주소를 설정하는 데 사용됩니다. 따라서 Adobe Analytics를 사용하려면 사용자가 회사 사무실에 있거나 VPN을 통해 네트워크에 로그인해야 합니다.

이 기능은 2021년 1월에 사용이 종료됩니다.

## 이 기능을 종료하는 이유는 무엇입니까?

이 기능은 Experience Cloud 로그인 마이그레이션 및/또는 Experience Cloud 로그인으로 인해 일부 상황에서 중단됩니다. 또는 를 사용하는 고객의 경우 중단되는 것으로 **[!UICONTROL Customer Attributes]** 알려져 **[!UICONTROL Audience Library]**&#x200B;있습니다.

또한, 여러 Experience Cloud 솔루션이 있을 경우 이 기능이 존재하지 않거나 Analytics 자체 외부에서 지원되지 않는다면 다른 솔루션 중 하나를 사용하여 Experience Cloud에 로그인함으로써 이 요구 사항을 우회할 수 있습니다. 사용자는 IP 스푸핑을 통해 이 문제를 처리할 수도 있습니다.

마지막으로, Adobe에서는 단일 사인온 및 Federated ID를 통해 잘 작동하면서도 훨씬 뛰어난 대체 솔루션을 제공합니다. 이 기능을 사용하면 사용자의 로그인 환경을 보다 효과적으로 제어하고 보안을 강화할 수 있습니다. 자세한 내용은 아래 내용을 참조하십시오.

## 이 기능을 제거하면 어떤 영향이 있습니까?

설정한 모든 고객의 경우 이 **[!UICONTROL Enforce IP login restrictions]** 기능은 2021년 1월에 제거됩니다. 이때 여전히 존재하는 IP 로그인 제한이 더 이상 적용되지 않습니다. 여전히 IP 주소로 로그인을 제한해야 하는 경우에는 단일 사인온 및 Federated ID의 권장 솔루션을 검토하고 구현해야 합니다(자세한 정보 및 리소스는 아래에 있음).

Additionally, the **[!UICONTROL Enforce IP login restrictions]** setting will be removed from the **[!UICONTROLAdmin > Company Settings > Security Manager]** in the Analytics UI (as shown below).

![](assets/sec-manager2.png)

## 다른 선택 사항은 무엇입니까?

위에 서술했듯이 이 Analytics 기능은 종료될 예정입니다. SSO 및 Federated ID를 구현할 수 있는 시간을 제공하기 위해 EOL 날짜가 2021년 1월로 연기되었습니다.

SSO와 Federated ID는 모두 현재 사용 중인 IP 로그인 제한 기능보다 뛰어난 솔루션이며 더 효과적인 제어, 보안 및 기능을 제공하게 됩니다. SSO/Federated ID 설정 방법에 대한 자세한 내용은 다음 도움말 설명서를 참조하십시오. 이 설명서를 완전히 읽고 IT 부서와 함께 구현할 것을 권장합니다.

* [단일 사인온 및 Experience Cloud](https://spark.adobe.com/page/JeSB8EPEQIvjD/)
* [Admin Console - ID 설정 설명서](https://helpx.adobe.com/kr/enterprise/using/set-up-identity.html)
* [Admin Console - ID 설정 자습서(비디오)](https://helpx.adobe.com/kr/enterprise/how-to/identity-directories-domains.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&amp;ref=helpx.adobe.com)
* [Federated ID 자습서 구성(비디오)](https://helpx.adobe.com/kr/enterprise/how-to/identity-configure-ids.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&amp;ref=helpx.adobe.com)
* [단일 사인온 - 일반적인 질문](https://helpx.adobe.com/kr/enterprise/using/sso-faq.html)
* [Adobe에서 지원하는 ID 유형](https://helpx.adobe.com/kr/enterprise/using/identity.html)

IP 로그인 제한에 대한 지원에 대해 계속 이야기하고 Experience Cloud에서 제공하도록 요청하려면 [포럼 페이지](https://forums.adobe.com/ideas/11648)에서 이 기능에 대해 투표할 수 있습니다.