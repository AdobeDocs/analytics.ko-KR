---
title: Adobe Analytics의 세션 문제 해결
description: Adobe Analytics에서 로그아웃되는 것과 관련된 문제를 해결하는 방법을 알아봅니다.
feature: Analytics Basics
exl-id: 191250ef-8313-47be-9717-046cce870998
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 100%

---

# Adobe Analytics의 세션 문제 해결

이 페이지는 세션 문제 해결에 대한 것입니다. 즉, 성공적으로 로그인할 수 있지만 로그인 상태를 유지하는 데 문제가 있습니다. Adobe Analytics에 로그인하는 데 문제가 있는 경우 [Adobe Analytics 로그인 문제 해결](troubleshoot-login.md)을 참조하십시오.

거의 모든 세션 기반 문제는 조직의 맞춤형 기업 네트워크에서 비롯됩니다. Adobe Analytics에 로그인할 수 있지만 로그인을 유지하는 데 문제가 있는 경우 이 문서를 참조하여 원인을 파악하십시오.

## 조직의 네트워크 때문에 문제가 발생했는지 확인

많은 조직에서는 보안을 강화하기 위해 프록시 서버 또는 방화벽과 같은 추가 네트워크 기능을 배포합니다. 이러한 사용자 지정은 경우에 따라 Adobe Analytics에서 활성 세션을 유지하는 기능을 방해할 수 있습니다.

연결되어 있는 회사 네트워크로 인해 Adobe Analytics 사용에 문제가 발생할 수 있는지 확인하려면 회사 네트워크 외부의 장치에서 Experience Cloud 로그인 자격 증명을 사용합니다. 장치의 예로는 홈 네트워크 또는 모바일 장치의 데이터 플랜이 있습니다. 로그아웃하지 않고 페이지 간에 성공적으로 이동할 수 있다면, Adobe Analytics에서 로그아웃된 원인이 조직의 네트워크 문제일 수 있습니다.

## 프록시로 인한 문제

Adobe는 Adobe에 요청할 때 인증 헤더를 사용합니다. Edge Secure Web Gateway(이전 Bluecoat)와 같은 일부 프록시는 Adobe Analytics에서 사용하는 중요한 인증 헤더 정보를 제거합니다. Adobe에서 인증 헤더를 확인하지 못하면 세션이 만료됩니다.

이 문제를 해결하려면 조직의 IT 팀과 함께 조직의 프록시를 통해 인증 헤더를 허용하는 것이 좋습니다.

>[!NOTE]
>
>Analytics 커뮤니티의 구성원은 다음 링크가 유용하다고 판단했지만, 그러한 링크는 Adobe가 소유하고 있지 않습니다. 이런 콘텐츠를 볼 때 이 점을 고려하십시오.

프록시 및 인증 헤더에 대한 정보는 다음에서 찾을 수 있습니다.

* [ProxySG 또는 ASG 어플라이언스에서 프록시 체인 배포에 업스트림 프록시 인증 구성](https://knowledge.broadcom.com/external/article/169255/configure-upstream-proxy-authentication.html)
* [ProxySG 어플라이언스 뒤의 서버에 사용자 자격 증명을 전달하는 방법](https://knowledge.broadcom.com/external/article/165859/how-to-forward-user-credentials-to-a-ser.html)
