---
title: 지원되는 HTTPS 암호화 알고리즘
description: 2022년 6월 23일에 암호화 보안 수준이 "높음"으로 설정된 고객의 경우 SHA1 또는 CBC를 활용하는 TLS 1.2 암호기에 대한 지원을 제거합니다.
feature: Regional Data Collection
source-git-commit: ce607610516a94e4d0fbbc53a1f8f53f5977a777
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# 지원되는 HTTPS 암호화 알고리즘

Adobe은 자사 데이터 수집에서 보안을 위해 다양한 고객 요구 사항을 충족하는 두 가지 암호화 보안 수준을 제공합니다. 이러한 수준은 Adobe 서버와의 HTTPS 연결에 대해 지원되는 암호화 알고리즘을 결정합니다. 고객은 기본적으로 &#39;Standard&#39;로, 최신 암호화 알고리즘만 지원합니다. &#39;높음&#39;은 이러한 연결에 대해 더 관심이 있는 고객을 위해 더 작은 암호화 알고리즘 목록을 지원합니다. 두 보안 수준의 경우 Adobe은 현재 보안 방침에 따라 지원되는 알고리즘 집합을 정기적으로 업데이트합니다. 암호 보안 설정을 변경하려면 고객 지원 센터에 문의하십시오.

2022년 6월 23일에 암호화 보안 수준이 &quot;높음&quot;으로 설정된 고객의 경우 SHA1 또는 CBC를 활용하는 TLS 1.2 암호기에 대한 지원을 제거합니다.  이 변경 사항은 이전 운영 체제에서 최종 사용자를 위한 보안 데이터 수집에 영향을 줍니다.

다음 TLS 1.2 암호기는 더 이상 지원되지 않습니다.

* TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
* TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
* TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
* TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
* TLS_RSA_WITH_AES_128_CBC_SHA
* TLS_RSA_WITH_AES_256_CBC_SHA

다음 클라이언트는 현재 암호화 표준에 대한 지원이 없으므로 이러한 변경의 영향을 받는 것으로 알려져 있습니다.

* Windows 8.1 및 이전 버전(2018년에 마지막으로 업데이트됨)
* Windows Phone 8.1 및 이전(2016년에 마지막으로 업데이트됨)
* OS X 10.10 이하(2017년에 마지막으로 업데이트됨)
* iOS 8.4 및 이전(2015년 마지막 업데이트)

Android 장치는 이 변경의 영향을 받지 않습니다.

암호화 보안 수준이 &quot;표준&quot;으로 설정된 고객은 이러한 변경의 영향을 받지 않습니다.

