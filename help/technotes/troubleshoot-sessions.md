---
title: Adobe Analytics에서 세션 문제 해결
description: Adobe Analytics에서 로그아웃되는 문제를 해결하는 방법을 알아봅니다.
seo-title: Adobe Analytics에서 세션 문제 해결
seo-description: Adobe Analytics에서 로그아웃되는 문제를 해결하는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: b5e3801454dafbcc47b93e65f8b5e7c59c3a8081

---


# Adobe Analytics에서 세션 문제 해결

이 페이지는 문제 해결 세션에 대한 것입니다. 즉, 로그인했지만 로그인 상태를 유지할 수 있습니다. If you are having issues logging in to Adobe Analytics, see [Troubleshoot logging in to Adobe Analytics](troubleshoot-login.md).

거의 모든 세션 기반 문제는 조직의 사용자 정의 기업 네트워크에서 비롯됩니다. Adobe Analytics에 로그인했지만 로그인에 문제가 있는 경우 이 문서를 사용하여 원인을 결정하십시오.

## 조직의 네트워크 때문에 문제가 발생하는지 확인

많은 조직은 프록시 서버나 방화벽과 같은 보안을 강화하기 위해 추가적인 네트워크 기능을 배포합니다. 이러한 사용자 지정 기능은 때로 Adobe Analytics에서 활성 세션을 유지하는 기능을 방해할 수 있습니다.

연결되어 있는 기업 네트워크가 Adobe Analytics 사용과 관련된 문제를 초래하는지 확인하려면 회사 네트워크의 외부에 있는 디바이스에서 Experience Cloud 로그인 자격 증명을 사용하십시오. 장치의 예로는 홈 네트워크 또는 모바일 장치의 데이터 계획을 들 수 있습니다. 로그아웃하지 않고 페이지에서 페이지로 이동할 수 있는 경우 조직의 네트워크에서 Adobe Analytics를 로그아웃한 이유가 원인일 수 있습니다.

## IP 풀링 문제

일부 네트워크는 장치의 IP 주소가 조직에서 사용되는 범위 내에서 자주 변경될 수 있는 IP 풀링 (logging) 이라는 사례를 사용합니다. Adobe 보안 관행의 일부로, IP 주소가 중간 세션을 변경하는 경우 해당 세션이 만료됩니다.

조직에서 IP 풀링을 사용하는 경우 다음 지침에 따라 Adobe의 허용 목록에 IP 범위를 추가합니다.

1. 조직의 IT 팀과 협력하여 조직에서 사용되는 IP 범위 목록 확인
2. 고객 지원 담당자가 Adobe 고객 지원 센터에 문의하도록 하고 Adobe에 IP 범위 제공
3. 에이전트가 IP 범위를 허용 목록에 입력하여 두 주소가 모두 제공된 범위에 있을 경우 세션이 만료되지 않도록 합니다.

## 프록시 문제로 인한 문제

Adobe는 Adobe에 요청할 때 인증 헤더를 사용합니다. Bluecoat (현재 Symantec 이 소유) 와 같은 일부 프록시는 Adobe Analytics에서 사용되는 중요한 인증 헤더 정보를 제거합니다. Adobe에서 인증 헤더가 표시되지 않으면 세션이 만료됩니다.

이 문제를 해결하려면 조직의 IT 팀과 협력하여 조직의 프록시를 통한 권한 부여 헤더를 허용하도록 권장합니다.

> [!NOTE] 참고
>
> Analytics 커뮤니티 구성원은 다음 링크를 유용하지만 Adobe가 소유하지 않습니다. 컨텐츠를 볼 때 이 메모를 고려하십시오.

Symantec 프록시 및 인증 헤더에 대한 정보는 다음 내용을 참조하십시오.

* [프록시 또는 ASG 어플라이언스에 대한 프록시 체인 배포의 업스트림 프록시 인증 구성](https://support.symantec.com/en_US/article.TECH246122.html)
* [프록시 서버가 항상 업스트림 서버 인증을 업스트림 전송하도록 허용](https://support.symantec.com/en_US/article.TECH244708.html)
