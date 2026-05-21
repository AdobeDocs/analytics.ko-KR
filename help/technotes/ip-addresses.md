---
title: Adobe Analytics에서 사용하는 IP 주소
description: 조직 방화벽이 Adobe에서 생성하는 IP 주소를 차단하는 경우 이 목록을 사용하여 방화벽 설정을 업데이트하십시오.
feature: Data Configuration and Collection
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
TQID: https://experienceleague.adobe.com/-4XZdprTBXpIaFnHeXBQsAr5YoZMW4ocnZRY50bHGUs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 9e2c89f4188c723b4623a6e7859b74ede15e155b
workflow-type: tm+mt
source-wordcount: 204
ht-degree: 32%

---

# Adobe Analytics에서 사용하는 IP 주소

일부 방화벽 구성은 Adobe 데이터 수집 서버나 데이터에 액세스하는 서버에서 오는 IP 주소를 차단합니다. 이 범위 목록을 사용하여 액세스를 허용하고 조직 내에서 데이터를 전송할 수 있도록 조직의 방화벽 설정을 변경할 수 있습니다.

중국 성능 최적화 추가 기능 패키지를 제외하고 Adobe Analytics에서 사용하는 모든 IP 주소는 [CX Enterprise에서 사용하는 IP 주소](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/ip-addresses)의 일부입니다.

## 중국 성능 최적화 IP 주소

중국 성능 최적화 추가 기능 패키지는 중국 내 방문자를 위해 AppMeasurement 데이터 수집 성능을 개선하는 추가 유료 서비스입니다. 이 기능 사용에 대한 자세한 내용은 Adobe 계정 팀에 문의하십시오.

>[!IMPORTANT]
>
>웹 SDK 데이터 수집에는 중국 RDC를 사용할 수 없습니다. 이러한 서버는 AppMeasurement 라이브러리에만 적용됩니다.

중국의 지역 데이터 수집 서버는 다음 IP 주소를 사용합니다.

| 위치 | 호스트 |
| --- | --- |
| 중국 | `52.80.168.159` |
| 중국 | `52.80.199.104` |
| 중국 | `54.223.199.8` |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>[CX Enterprise에서 사용하는 IP 주소](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/ip-addresses)
>
>[Adobe Analytics에서 사용하는 도메인](domains.md)
