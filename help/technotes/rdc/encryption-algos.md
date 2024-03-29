---
title: 지원되는 HTTPS 암호화 알고리즘
description: TLS 암호화 보안 설정 및 인증서 유형입니다.
feature: Regional Data Collection
exl-id: f1cbb0cb-fd65-4f22-8594-0d97b6906698
source-git-commit: 1ca7f750387fd9ae034d10ebf3e47190cf33d4b7
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 25%

---

# 지원되는 HTTPS 암호화 알고리즘

## 암호화 보안 수준

Adobe는 자사 데이터 수집에서의 보안에 대한 다양한 고객 요구 사항에 부합하는 두 가지의 암호 보안 수준을 제공합니다. 이러한 수준은 Adobe 서버와의 HTTPS 연결에 대해 지원되는 암호화 알고리즘을 결정합니다. Adobe은 현재 보안 방침에 따라 지원되는 알고리즘 집합을 정기적으로 검토하고 업데이트합니다. 암호 보안 설정을 변경하려면 고객 지원 센터에 문의하십시오.

&#39;Standard&#39;에는 TLS 1.2 이상 및 128비트 이상의 암호화가 필요합니다. 보안 암호화를 유지하면서 가장 광범위한 장치 호환성을 제공하도록 설계되었습니다.

&#39;높은&#39; 암호화 보안 수준에는 TLS 1.2 이상이 필요하며 더 약한 암호기에 대한 지원을 제거합니다. 강력한 암호화를 원하며 이전 장치의 지원에 관심이 없는 고객을 위해 설계되었습니다.

다음 클라이언트는 암호 보안 집합을 &quot;높음&quot;으로 설정하여 연결할 수 없는 것으로 알려져 있습니다.

* Windows 8.1 이하(2018년에 마지막으로 업데이트됨)
* Windows Phone 8.1 이하(2016년에 마지막으로 업데이트됨)
* OS X 10.10 이하(2017년에 마지막으로 업데이트됨)
* iOS 8.4 이하(2015년에 마지막으로 업데이트됨)

## 지원되는 HTTPS 인증서 유형

Adobe은 다양한 고객 요구 사항을 충족하는 RSA 및 ECC 인증서 유형을 모두 지원합니다. RSA 인증서는 클라이언트에 대해 보다 광범위하게 지원되지만 ECC 인증서는 서버 및 클라이언트 측에서 적은 처리량을 사용합니다. Adobe 관리 인증서의 경우 RSA 및 ECC 가 모두 제공됩니다. 고객 관리 인증서의 경우 RSA 및 ECC 가 모두 권장됩니다. 최신 클라이언트는 RSA와 ECC를 모두 지원합니다. 다음 클라이언트는 RSA 인증서만 지원하는 것으로 알려져 있습니다.

* Windows Vista 및 이전 버전(2012년에 마지막으로 업데이트됨)
* Windows Phone 8.0 이하(2014년에 마지막으로 업데이트됨)
* OS X 10.8 이하(2013년에 마지막으로 업데이트됨)
* iOS 5.1 이하(2012년에 마지막으로 업데이트됨)
* Android 4.3 및 이전(2013년에 마지막으로 업데이트됨)
