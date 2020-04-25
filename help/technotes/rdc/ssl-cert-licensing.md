---
title: SSL 인증서 라이센싱
description: 고객 관리 인증서에 대한 인증서 절차
translation-type: tm+mt
source-git-commit: 290838566b86f71902abd303b5c43dd2661d3ce1

---


# SSL/TLS 인증서 라이센싱

Adobe에서는 [Adobe 관리 인증서 프로그램](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html)을 통해 추가 비용 없이 인증서를 관리할 것을 권장합니다.  Adobe 관리 인증서 프로그램은 완전히 자동화되어 있으며 적시에 갱신되므로 인증서 만료로 영향을 받지 않습니다.

[Adobe 관리 인증서 프로그램](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html)을 사용하지 않을 경우에는 자사 쿠키에 사용할 SSL/TLS 인증서를 제공해야 합니다.

자체 인증서를 제공하는 경우 인증서를 구매하고 유지 관리하는 것은 본인의 책임입니다.  자체 SSL/TLS 인증서에 무제한 서버 라이선스가 포함되어 있어야 합니다.

인증서 보안을 위해 Adobe에서 인증서 서명 요청 [CSR]을 가져와 원하는 인증 기관에서 인증서 서명을 받으십시오.  구현을 위해 Adobe에 서명된 인증서를 제공합니다.  이 프로세스를 수행하면 인증서 키의 보안이 유지됩니다.  Adobe 고객 지원 팀이 이 프로세스를 지원합니다.

인증서 유지 관리의 일부로, 인증서가 만료되기 최소 1개월 전에 원하는 인증 기관에 문의하여 갱신된 인증서를 받아 Adobe에 제공합니다.  이 인증서는 이전에 사용한 것과 동일한 CSR을 사용해야 합니다.  CSR의 사본이 필요하거나 새 키를 사용하여 새 CSR을 생성하려는 경우 Adobe에 문의하십시오.

고객 지원 팀은 customercare@adobe.com 또는 1-800-497-0335으로 연락하시면 됩니다.

일반적으로 사용되는 인증 기관으로는 DigiCert, Comodo 및 GeoTrust가 있습니다.
