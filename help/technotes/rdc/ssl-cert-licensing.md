---
title: SSL 인증서 라이센싱
seo-title: Adobe Analytics SSL 인증서 라이센싱
description: null
seo-description: null
translation-type: tm+mt
source-git-commit: 1fdd14497171dbf5850ec1b1d873a06931d58435

---


# SSL 인증서 라이센싱

퍼스트 파티 쿠키를 사용하고 있고 보안 트래픽을 측정하는 경우, RDC 구현을 위해 충분한 SSL 인증서 라이센스를 제공해야 합니다.

SSL 인증서는 최대 10개 서버상의 설치를 지원해야 합니다. 이러한 인증서들은 전 세계 로드 밸런서에 설치되어 있습니다. Adobe가 추가적으로 온라인 데이터 수집 센터를 제공하기 때문에 SSL 인증서가 변경되어야 합니다. 이러한 변경이 장기적으로 인증서 라이센싱에 미치는 영향은 사용자의 인증서 라이센스의 유형에 따라 다릅니다.

* 서버 기반 라이센스: RDC 배포에 필요한 라이센스 요구사항이 시간이 흐르면서 증가합니다.
* 볼륨 기반 라이센스: 라이센스 요구사항이 인프라 변경의 영향을 받지 않지만 시간이 흐르면서 트래픽 볼륨이 변화합니다.
* 무제한 라이센스: 라이센스 요구사항이 장기적으로 봤을 때 비교적 안정적으로 유지됩니다.

자신의 인증서를 제공하는 경우 인증서를 구매하고 유지 관리하는 것은 본인의 책임입니다. 인증서 제공자의 계약을 확인하여 여러 데이터 센터에 SSL 인증서를 설치할 수 있는지 확인합니다.

또는 Adobe에서 [Adobe 관리 인증서 프로그램](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html)을 통해 추가 비용 없이 인증서를 관리해드릴 수도 있습니다.
