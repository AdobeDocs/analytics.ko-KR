---
title: Adobe Analytics에서 세션 문제 해결
description: Adobe Analytics에서 로그아웃되는 것과 관련된 문제를 해결하는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Adobe Analytics에서 세션 문제 해결

이 페이지는 세션 문제 해결에 대해 설명합니다. 즉, 성공적으로 로그인할 수 있지만 로그인 상태를 유지하는 데 문제가 있습니다. Adobe Analytics에 로그인하는 데 문제가 있는 경우 Adobe [Analytics 로그인 문제 해결을 참조하십시오](troubleshoot-login.md).

거의 모든 세션 기반 문제는 조직의 맞춤형 기업 네트워크에서 비롯됩니다. Adobe Analytics에 로그인할 수 있지만 로그인하는 데 문제가 있는 경우 이 문서를 사용하여 원인을 확인하십시오.

## 조직의 네트워크 때문에 문제가 발생했는지 확인

많은 조직은 프록시 서버 또는 방화벽과 같은 보안을 강화하기 위해 추가 네트워크 기능을 배포합니다. 이러한 사용자 지정은 경우에 따라 Adobe Analytics에서 활성 세션을 유지하는 기능을 방해할 수 있습니다.

연결되어 있는 회사 네트워크가 Adobe Analytics 사용에 문제를 일으키는지 확인하려면 회사 네트워크 외부의 디바이스에서 Experience Cloud 로그인 자격 증명을 사용하십시오. 장치의 예로는 홈 네트워크 또는 모바일 장치의 데이터 플랜이 있습니다. 로그아웃하지 않고 페이지에서 페이지로 성공적으로 이동할 수 있는 경우 조직의 네트워크가 Adobe Analytics에서 로그아웃되는 이유일 수 있습니다.

## 프록시로 인한 문제

Adobe는 Adobe에 요청할 때 인증 헤더를 사용합니다. Bluecoat(현재 Symantec 소유)와 같은 일부 프록시는 Adobe Analytics에서 사용하는 중요한 인증 헤더 정보를 스트립합니다. Adobe에서 인증 헤더를 볼 수 없으면 세션이 만료됩니다.

이 문제를 해결하려면 조직의 IT 팀과 함께 조직의 프록시를 통해 인증 헤더를 허용하는 것이 좋습니다.

> [!NOTE] Analytics 커뮤니티의 구성원은 다음 링크가 유용하다고 판단했지만, 그러한 링크는 Adobe가 소유하고 있지 않습니다. 이 참고 사항은 콘텐츠를 볼 때 고려하십시오.

Symantec 프록시 및 인증 헤더에 대한 정보는 다음과 같습니다.

* [ProxySG 또는 ASG 어플라이언스의 프록시 체인 배포에서 업스트림 프록시 인증 구성](https://support.symantec.com/en_US/article.TECH246122.html)
* [ProxySG가 항상 업스트림 서버 인증을 전달하도록 허용](https://support.symantec.com/en_US/article.TECH244708.html)
