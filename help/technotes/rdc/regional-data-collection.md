---
title: 지역 데이터 수집
description: 지역 데이터 수집 정보
translation-type: tm+mt
source-git-commit: 09b453c1b4cd8555c5d1718759003945f5c230c5
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 77%

---


# 지역 데이터 수집

Adobe Experience Cloud는 RDC(지역 데이터 수집)를 사용하므로 최종 사용자와 Adobe Experience Cloud 간의 상호 작용이 최종 사용자에게 가까운 위치에서 발생할 수 있습니다. 이렇게 하면 사이트/앱 성능이 향상되고 데이터가 가능한 한 빨리 수집되므로 최종 사용자 환경이 최적화됩니다. 디지털 속성의 데이터가 DCC(데이터 수집 센터)에 지역적으로 수집되면 보안 연결을 통해 DPC(데이터 처리 센터)로 전달되며, 여기서 처리되고 Adobe Experience Cloud의 제품에서 사용할 수 있게 됩니다.

>[!IMPORTANT]
>
>중국 RDC(China Performance Optimization) 애드온 패키지는 Adobe Analytics의 유료 애드온입니다. 중국 본토의 Adobe의 성능 최적화를 통해 중국 내 고객은 전 세계 다른 위치가 아니라 중국 에지 노드로 데이터를 직접 전송할 수 있습니다. 이렇게 하면 중국 외부의 노드로 데이터를 전송할 때보다 페이지 로드 시간과 데이터 정확도가 향상됩니다. 자세한 내용은 Adobe 영업 담당자에게 문의하십시오.

현재 RDC에는 다음 위치(변경될 수 있음)가 포함되어 있습니다.

## 타사 및 HTTP 데이터 수집

| RDC 유형 | 데이터 수집 센터 |
|---------------------|-------------------|
| 기본값 | 오리건, 버지니아, 아일랜드, 파리, 뭄바이, 싱가포르, 도쿄, 시드니 |

Note: If your Analytics image request is sent to the `adobedc`, `2o7.net` or `omtrdc.net` endpoints, then you have third-party data collection. 요청 URL에 종단점이 표시되면 이를 확인할 수 있습니다.

## 자사 HTTPS 데이터 수집

| RDC 유형 | 데이터 수집 센터 |
|---------------------|-------------------|
| 글로벌(기본값) | 오리건, 버지니아, 아일랜드, 파리, 뭄바이, 싱가포르, 도쿄, 시드니 |
| 아메리카만 | 오리건, 버지니아 |
| 유럽만 | 아일랜드, 파리 |
| 아시아 태평양만 | 뭄바이, 싱가포르, 도쿄, 시드니 |

참고: Experience Edge Global은 최종 사용자에게 최고의 성능을 제공합니다.  대체 RDC 유형을 사용하려면 Adobe 고객 지원 팀에 문의하십시오.

## RDC 작동 방식

다음 목록에서는 Adobe에서 사용하는 데이터 수집 프로세스에 대해 설명하고 있습니다.

1. DNS는 방문자에게 가장 가까운 데이터 수집 센터의 IP 주소에 대한 수집 호스트 이름을 자동으로 확인합니다.
1. 방문자가 이 위치로 데이터를 보냅니다.
1. 데이터는 보안 연결을 통해 데이터 처리 센터로 즉시 전달되어 처리되고, Adobe Experience Cloud의 제품에 사용할 수 있게 됩니다.
