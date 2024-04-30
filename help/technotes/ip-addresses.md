---
title: Adobe Analytics에서 사용하는 IP 및 도메인
description: 조직 방화벽이 Adobe에서 생성하는 IP 주소를 차단하는 경우 이 목록을 사용하여 방화벽 설정을 업데이트하십시오.
feature: Data Configuration and Collection
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
source-git-commit: ea859717c6a40b4eeeb9eca54b95718859af9c7b
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 32%

---

# Adobe Analytics에서 사용하는 IP 및 도메인

일부 방화벽 구성은 Adobe Analytics이 제품 인터페이스에 의존하는 도메인을 차단합니다. 이 도메인 목록을 사용하여 조직 내에서 제품 액세스를 허용하도록 조직의 네트워크 설정을 변경할 수 있습니다.

## 종속 기술 도메인 허용

Adobe Analytics는 다음 호스트를 사용하여 성능과 제품 경험을 개선합니다. Adobe은 Adobe Analytics을 사용하여 최적의 환경을 제공하기 위해 이러한 도메인을 조직의 방화벽을 통해 허용하는 것을 권장합니다.

| 기술 | 도메인 |
| --- | --- |
| Adobe Analytics 도메인 | `adobe.com`, `adobe.net`, `adobe.io` |
| Adobe Analytics 기존 도메인 | `omniture.com` |
| Amazon AWS | `aaui-879784980514.s3.us-east-2.amazonaws.com` |
| Amazon CloudFront | `d30ln29764hddd.cloudfront.net` |
| Gainsight | `esp.aptrinsic.com`, `esp-m.aptrinsic.com` |
| LaunchDarkly | `app.launchdarkly.com` |
| Microsoft Azure Blob 저장소 | `awaascicdprodva7.blob.core.windows.net` |
| Microsoft Azure CDN | `aauicdnva7.azureedge.net` |

{style="table-layout:auto"}

## Adobe Experience Cloud IP 주소 블록

위의 도메인 외에도 Adobe Analytics은 데이터 수집 및 보고서 내보내기를 위해 여러 IP 주소 블록을 사용합니다.

IP 범위의 전체 목록은 Adobe Experience Cloud IP 주소 를 참조하십시오.

## 중국 성능 최적화 IP 주소

중국 성능 최적화 추가 기능 패키지는 중국 내 방문자의 AppMeasurement 데이터 수집 성능을 개선하는 추가 유료 서비스다. 이 기능 사용에 대한 자세한 내용은 Adobe 계정 팀에 문의하십시오.

>[!IMPORTANT]
>
>Web SDK 데이터 수집에는 중국 RDC를 사용할 수 없습니다. 이러한 서버는 AppMeasurement 라이브러리에만 적용됩니다.

중국의 지역 데이터 수집 서버는 다음 IP 주소를 사용합니다.

| 위치 | 호스트 |
| --- | --- |
| 중국 | `52.80.168.159` |
| 중국 | `52.80.199.104` |
| 중국 | `54.223.199.8` |

{style="table-layout:auto"}
