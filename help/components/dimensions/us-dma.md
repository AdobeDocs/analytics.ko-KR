---
title: US DMA
description: 히트의 지정 시장권(DMA)입니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 91%

---


# US DMA

US DMA 차원은 방문자의 지정된 시장권(DMA)을 보고합니다. 이 차원은 [Nielsen](https://www.nielsen.com/us/en/intl-campaigns/dma-maps/)이 만든 미디어 시장을 기반으로 합니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 조회 규칙을 참조합니다. 조회 값은 히트와 함께 전송된 IP 주소를 기반으로 합니다. Adobe는 IP 주소와 DMA 간에 조회를 유지 관리하기 위해 Nielsen과 파트너 관계를 맺고 있습니다. 이 차원은 모든 구현에 대해 즉시 작동합니다. 

>[!TIP]
>
>조직에서 [IP 주소 난독화](/help/admin/admin/general-acct-settings-admin.md)가 충분하지 않은 엄격한 개인 정보 보호 규정을 따르는 경우 지리적 위치 데이터를 완전히 비활성화하도록 요청할 수 있습니다. 보고서 세트에 대해 &#39;지리적 위치&#39;를 해제하려면 보고서 세트 ID로 고객 지원 팀에 연락하여 요청하십시오.

## Dimension 항목

Dimension 항목에는 방문자의 DMA 및 DMA 코드가 포함됩니다. 3자리 코드는 우편 번호가 아니라 Nielsen의 DMA 코드입니다. 값의 예로는 `"Dallas-Ft. Worth (623)"`, `"New York (501)"` 또는 `"Los Angeles (803)"`이 있습니다. The dimension item `"No Metro (0)"` includes all international traffic outside of the United States.

## 보고된 위치와 실제 위치 간의 차이

이 차원은 IP 주소를 기반으로 하므로 일부 시나리오는 보고된 위치와 실제 위치 간의 차이를 보여줄 수 있습니다.

* **기업 프록시를 나타내는 IP 주소**: 이러한 방문자는 사용자가 원격으로 근무하는 경우 실제로 다른 위치에 있을 수 있는데 사용자의 기업 네트워크에서 트래픽이 오는 것처럼 보일 수 있습니다.
* **모바일 IP 주소**: 모바일 IP 타깃팅은 위치와 네트워크에 따라 다양한 수준에서 작동합니다. 이동통신업체 중에는 중앙 또는 지역 거점(point of presence)을 통해 IP 트래픽을 역수송하는 곳도 많습니다.
* **위성 ISP 사용자**: 이러한 사용자는 보통 업링크 위치에서 오는 것처럼 표시되므로 구체적인 위치를 식별하기가 어렵습니다.
* **군대 및 정부 IP**: 세계 각지를 다니며 현재 배치되어 있는 기지나 사무실 대신 홈 위치를 통해 시작하는 사람을 나타냅니다.
