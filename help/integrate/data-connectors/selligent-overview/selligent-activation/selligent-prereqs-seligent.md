---
description: 통합을 배포하기 전에 귀하의 Selligent 계정에서 제공하는 필요한 정보를 나열합니다.
seo-description: 통합을 배포하기 전에 귀하의 Selligent 계정에서 제공하는 필요한 정보를 나열합니다.
seo-title: Selligent에 대한 전제 조건
solution: Analytics
title: Selligent에 대한 전제 조건
uuid: 3 a 43 a 1 c 0-5 f 51-4 bc 8-b 6 b 9-0 c 46 aa 00 ba 9 f
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Prerequisites for Selligent{#prerequisites-for-selligent}

통합을 배포하기 전에 귀하의 Selligent 계정에서 제공하는 필요한 정보를 나열합니다.

**유효한 기본 계정**

이 데이터 커넥터 통합을 사용하려면 유효한 계정이 있어야 합니다.

**계정 정보**

이 통합 설정 중에 귀하의 Selligent 계정에 대한 다음 정보가 필요합니다.

* **Adobe 서비스 URL**:

   URL는 Selligent 마케팅 솔루션에 로그온하는 데 사용되는 URL에서 파생될 수 있습니다. URL의 "/simweb/login. aspx" 부분을 "/automation/omniture. asmx" 로 바꿉니다.

   예: http://<client-specific install url>/automation/omniture.asmx

* **쿼리 문자열 매개 변수:** 이것은 메시지 ID 및 수신자 ID (방문자 ID) 에 대한 랜딩 페이지 URL에 추가됩니다. 항상 메시지 ID와 수신자 ID는 mid 및 rid 입니다.

* **통합 토큰** Simweb 내에서 관리자 도구를 실행하고 **[!UICONTROL 구성]** &gt; **[!UICONTROL 시스템 설정]** &gt; **[!UICONTROL 일반]** 탭 &gt; **[!UICONTROL 시스템으로 이동합니다]**. **[!UICONTROL 보안]**&#x200B;아래에서 통합 토큰을 찾을 수 있습니다.

   ![](assets/selligent-integration_token.png)

