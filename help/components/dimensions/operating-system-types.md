---
title: 운영 체제 유형
description: 버전에 관계없이 운영 체제를 보여 줍니다.
feature: Dimensions
exl-id: 0afd5261-98e8-4247-865a-1b8844c53ff4
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 55%

---

# 운영 체제 유형

운영 체제 유형 [차원](overview.md) 특정 버전에 관계없이 방문자가 사용한 지배적인 OS를 보여줍니다. 이 차원은 가장 일반적인 특정 운영 체제와 버전뿐만 아니라 방문자가 사용하는 일반적인 OS 플랫폼을 파악하는 데 유용합니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 조회 테이블을 참조합니다. 조회 값은 이미지 요청에 있는 `User-Agent` HTTP 헤더를 기반으로 합니다. 와 파트너 Adobe [DeviceAtlas](https://deviceatlas.com/) 사용자 에이전트와 운영 체제 유형 간의 조회를 유지 관리합니다.

* AppMeasurement 구현의 경우 이 차원은 즉시 작동합니다.
* 웹 SDK 구현의 경우 다음을 활성화합니다 [!UICONTROL 장치 조회] 조건 [데이터스트림 구성](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=ko-KR).

## 차원 항목

Dimension 항목에는 사용된 운영 체제의 유형이 포함됩니다. 예로는 `"Microsoft Windows"`, `"Apple Macintosh"`, `"Google Android"` 및 `"Apple iOS"`가 있습니다.
