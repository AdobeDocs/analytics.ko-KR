---
title: RDC 환경 특성
seo-title: Adobe Analytics RDC 환경 특성
description: null
seo-description: null
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# RDC 환경 특성

RDC(Regional Data Collection) 환경에는 아래에 설명된 특성이 포함되어 있습니다.

## 성능 향상

RDC를 사용할 때의 현재 응답 시간은 Adobe Analytics [요청 성능을 참조하십시오](https://marketing.adobe.com/resources/help/en_US/whitepapers/performance/).

일반적으로 사용자는 다음과 같이 RDC를 사용하여 응답 시간이 개선되었습니다.

| 지역 | RDC로 절약되는 응답 시간 |
| --- | --- |
| 아시아 | 36% |
| 오스트레일리아 | 5% |
| 중국 및 러시아 | 41% |
| 일본 | 41% |
| 유럽 | 83% |
| 영국 제도 | 94% |
| 중유럽 및 동유럽 | 84% |
| 북유럽 | 73% |
| 서유럽 | 89% |
| 북미 | 38% |
| 캐나다 | 26% |
| 미국 중부 | 48% |
| 미국 동부 | 46% |
| 미국 서부 | 20% |
| 글로벌 | 50% |

## 자사 또는 타사 쿠키

구현의 종류에 따라 사용자는 퍼스트 파티 또는 서드 파티 쿠키를 사용할 것입니다. 퍼스트 파티 쿠키에 대한 더 자세한 내용은  [여기](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/fpcookies_overview.html)에서 확인하십시오.

## 보안 페이지

사이트에 https 프로토콜을 사용하는 페이지가 포함된 경우 보안 페이지가 있습니다. Adobe Analytics에서 추적하는 대부분의 페이지 보기는 https 프로토콜을 사용하여 보호됩니다. 보안 페이지는 추적에 SSL 인증서가 필요합니다. 웹 속성이 타사 쿠키를 사용하는 경우, 보안 페이지는 Adobe가 소유한 SSL 인증서를 사용하므로 FPSSL 구현 없이 데이터를 Adobe 데이터 수집 서버로 안전하게 전송할 수 있습니다.

## DNS 변경(CNAME 업데이트)

[CNAME](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/fpcookies_cname.html) 업데이트는 회사의 DNS 서버에 변경 사항을 적용하는 것을 의미합니다. 일반적으로 IT 담당자 또는 네트워크 작업 팀이 이 프로세스를 다루고 있습니다. 사용자의 시나리오에 이러한 변경이 필요한 경우, 고객 지원 센터에 연락해서 새로운 Adobe 호스트 이름을 요청해야 합니다.
