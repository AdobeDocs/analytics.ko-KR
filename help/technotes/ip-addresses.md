---
title: Adobe Analytics에서 사용하는 IP 주소
description: 조직 방화벽이 Adobe에서 생성하는 IP 주소를 차단하는 경우 이 목록을 사용하여 방화벽 설정을 업데이트하십시오.
feature: Data Configuration and Collection
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
source-git-commit: 5ac6da2eb53d2748e8838ef2c6334a771abc26c9
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 35%

---

# Adobe Analytics에서 사용하는 IP 주소

일부 방화벽 구성은 Adobe 데이터 수집 서버나 데이터에 액세스하는 서버에서 오는 IP 주소를 차단합니다. 이 범위 목록을 사용하여 액세스를 허용하고 조직 내에서 데이터를 전송할 수 있도록 조직의 방화벽 설정을 변경할 수 있습니다.

중국 성능 최적화 추가 기능 패키지를 제외하고 Adobe Analytics에서 사용하는 모든 IP 주소는 Adobe Experience Cloud에서 사용하는 [IP 주소](https://experienceleague.adobe.com/ko/docs/core-services/interface/data-collection/ip-addresses)의 일부입니다.

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

>[!MORELIKETHIS]
>
>[Adobe Experience Cloud에서 사용하는 IP 주소](https://experienceleague.adobe.com/ko/docs/core-services/interface/data-collection/ip-addresses)
>
>[Adobe Analytics에서 사용하는 도메인](domains.md)
