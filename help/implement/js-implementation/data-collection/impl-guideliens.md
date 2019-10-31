---
description: 이 지침을 따르면 동일한 쿠키 도메인을 사용하므로, 다양한 구현 유형 간에 방문을 추적할 수 있게 됩니다.
keywords: Analytics 구현
seo-description: 이 지침을 따르면 동일한 쿠키 도메인을 사용하므로, 다양한 구현 유형 간에 방문을 추적할 수 있게 됩니다.
seo-title: 구현 안내서
solution: Analytics
title: 구현 안내서
topic: 개발자 및 구현
uuid: 2917f4af-19bd-4666-ae4b-056e7e33f642
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 구현 안내서

이 지침을 따르면 동일한 쿠키 도메인을 사용하므로, 다양한 구현 유형 간에 방문을 추적할 수 있게 됩니다.

* **RSID:**[!UICONTROL  보고서 세트 ID]
* **VNS:** 방문자 이름 공간. [!DNL 2o7.net]방문자 ID[!DNL omtrdc.net] 쿠키를 저장하는 데 사용되는 [!UICONTROL  또는 ]의 하위 도메인입니다.
* **COOKIEDOMAIN:** VNS + trackingServer. 데이터 센터와 RDC 구성에 따라 매우 달라질 수 있습니다. [데이터 수집 도메인에](https://helpx.adobe.com/contact/enterprise-support.ec.html#analytics) 대해 잘 모르는 경우 고객 지원 센터에 문의하십시오.

## Javascript

```javascript
var s_account="RSID" 
s.visitorNamespace="VNS" 
s.trackingServer="VNS.COOKIEDOMAIN.net" 
```

## AppMeasurement

```javascript
var s_account="RSID" 
s.visitorNamespace="VNS" 
s.trackingServer="VNS.COOKIEDOMAIN.net" 
```

## 하드 코딩된 이미지 요청

```javascript
<img border="0" alt="" src="https://VNS.COOKIEDOMAIN.net/b/ss/RSID/5?ns=VNS" width="1" height="1" /> 

<!-- Note that the visitor namespace is defined twice in hardcoded image requests; once in the http subdomain, and another using the ns= query string parameter! -->
```

자사 쿠키 구현을 사용하는 경우에는 `VNS.COOKIEDOMAIN.net`을 사용 중인 자사 쿠키로 교체할 수 있습니다. 예를 들어 `adobe.com`의 자사 쿠키는 `metrics.adobe.com`과 비슷한 주소로 교체됩니다.
