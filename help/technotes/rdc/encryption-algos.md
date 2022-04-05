---
title: 지원되는 HTTPS 암호화 알고리즘
description: 2022년 6월 23일부터 암호 보안 수준이 “높음”으로 설정되어 있는 고객에 대해 SHA1 또는 CBC를 활용하는 TLS 1.2 암호에 대한 지원이 중단될 예정입니다.
feature: Regional Data Collection
exl-id: f1cbb0cb-fd65-4f22-8594-0d97b6906698
source-git-commit: a1ae98d6907960135c1dfa03ed10738eac8bec0d
workflow-type: ht
source-wordcount: '273'
ht-degree: 100%

---

# 지원되는 HTTPS 암호화 알고리즘

Adobe는 자사 데이터 수집에서의 보안에 대한 다양한 고객 요구 사항에 부합하는 두 가지의 암호 보안 수준을 제공합니다. 이러한 수준은 당사 서버와의 HTTPS 연결에 지원되는 암호화 알고리즘을 결정합니다. 고객은 최신 암호화 알고리즘만을 지원하는 “표준”으로 전환됩니다. “높음” 수준을 사용하면 이러한 연결을 더 중요하게 생각하는 고객에게 더 적은 수의 암호화 알고리즘만 지원됩니다. 두 보안 수준 모두에 대해 Adobe는 현재 보안 사례를 기반으로 지원되는 알고리즘 세트를 정기적으로 업데이트합니다. 보안 수준 설정을 변경하고자 하는 경우 고객 지원 센터에 문의해 주십시오.

2022년 6월 23일부터 암호 보안 수준이 “높음”으로 설정되어 있는 고객에 대해 SHA1 또는 CBC를 활용하는 TLS 1.2 암호에 대한 지원이 중단될 예정입니다. 이 변경은 이전 운영 체제를 사용하는 최종 사용자에 대한 보안 데이터 수집에 영향을 줍니다.

다음은 더 이상 지원되지 않는 TLS 1.2 암호 목록입니다.

* TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
* TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
* TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
* TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
* TLS_RSA_WITH_AES_128_CBC_SHA
* TLS_RSA_WITH_AES_256_CBC_SHA

다음은 현재 암호화 표준에 대한 지원 부족으로 인해 이 변경의 영향을 받게 되는 클라이언트 목록입니다.

* Windows 8.1 이하(2018년에 마지막으로 업데이트됨)
* Windows Phone 8.1 이하(2016년에 마지막으로 업데이트됨)
* OS X 10.10 이하(2017년에 마지막으로 업데이트됨)
* iOS 8.4 이하(2015년에 마지막으로 업데이트됨)

Android 디바이스는 이 변경의 영향을 받지 않습니다.

암호 보안 수준이 “표준”으로 설정되어 있는 고객은 이 변경의 영향을 받지 않습니다.
