---
title: US DMA
description: 히트의 지정 시장권 (DMA)입니다.
feature: Dimensions
exl-id: 156d5755-2e93-4240-bde3-1d537422b7bf
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 64%

---

# US DMA

&#39;US DMA&#39; [차원](overview.md)은(는) 방문자의 지정된 DMA(시장 지역)를 보고합니다. 이 차원은 [Nielsen](https://www.nielsen.com/dma-regions/)이 만든 미디어 시장을 기반으로 합니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 조회 규칙을 참조합니다. 조회 값은 히트와 함께 전송된 IP 주소를 기반으로 합니다. Adobe은 IP 주소와 DMA 간에 조회를 유지 관리하기 위해 Nielsen과 파트너 관계를 맺고 있습니다.

* AppMeasurement 구현의 경우 이 차원은 즉시 작동합니다.
* 웹 SDK 구현의 경우 [!UICONTROL 데이터 스트림을 구성]할 때 [지역 조회](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html)를 사용하도록 설정하십시오.

## 차원 항목

Dimension 항목에는 방문자의 DMA와 DMA 코드가 포함됩니다. 3자리 코드는 우편 번호가 아니라 Nielsen의 DMA 코드입니다. 값의 예로는 `"Dallas-Ft. Worth (623)"`, `"New York (501)"` 또는 `"Los Angeles (803)"`이 있습니다. 차원 항목 `"No Metro (0)"`은 미국 외부의 모든 국제 트래픽을 포함합니다.

## 보고된 위치와 실제 위치 간의 차이

이 차원은 IP 주소를 기반으로 하므로 일부 시나리오는 보고된 위치와 실제 위치 간의 차이를 보여 줄 수 있습니다.

* **기업 프록시를 나타내는 IP 주소**: 이러한 방문자는 사용자가 원격으로 근무하는 경우 실제로 다른 위치에 있을 수 있는데 사용자의 기업 네트워크에서 트래픽이 오는 것처럼 보일 수 있습니다.
* **모바일 IP 주소**: 모바일 IP 타깃팅은 위치와 네트워크에 따라 다양한 수준에서 작동합니다. 일부 이동통신사는 중앙 또는 지역 거점(point of presence)을 통해 IP 트래픽을 역수송합니다.
* **위성 ISP 사용자**: 이러한 사용자는 보통 업링크 위치에서 오는 것처럼 표시되므로 구체적인 위치를 식별하기가 어렵습니다.
* **군대 및 정부 IP**: 세계 각지를 다니며 현재 배치되어 있는 기지나 사무실 대신 홈 위치를 통해 시작하는 사람을 나타냅니다.
* **개인 정보 보호를 위해 IP 주소를 숨기는 프록시**: Apple의 개인 릴레이와 같은 서비스는 중개 또는 프록시를 통해 임의로 데이터를 전송하여 실제 IP 주소를 숨깁니다. 그런 다음 이 프록시는 Adobe으로 전달하기 전에 다른 IP 주소를 대체합니다.
