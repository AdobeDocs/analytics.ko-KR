---
title: 도메인
description: 방문자가 인터넷에 액세스하는 데 사용하는 조직 또는 ISP입니다.
feature: Dimensions
exl-id: 292dc256-e9e7-47be-8586-774f1c047011
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 52%

---

# 도메인

&#39;도메인&#39; [차원](overview.md)은(는) 방문자가 인터넷에 액세스하는 데 사용하는 액세스 지점을 보고합니다.

## 이 차원을 데이터로 채우기

Adobe는 [Digital Element](https://www.digitalelement.com/)와 협력하여 액세스 포인트 도메인을 결정합니다. 역방향 DNS 조회를 비롯한 여러 방법을 사용하여 액세스 포인트 도메인을 확인합니다. 또한 구성할 필요가 없으며 채울 변수가 없습니다.

* AppMeasurement 구현의 경우 이 차원은 즉시 작동합니다.
* 웹 SDK 구현의 경우 [!UICONTROL 데이터 스트림을 구성]할 때 [네트워크 조회](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=ko)를 사용하도록 설정하십시오.

## 차원 항목

차원 항목 예에는 `comcast.net`, `rr.com`, `sbcglobal.net` 및 `amazonaws.com`이 포함됩니다. 이러한 도메인은 액세스 지점이며 ISP 또는 조직을 나타내는 도메인일 필요는 없습니다.

`None`의 차원 값은 액세스 지점 IP 주소의 소유자가 도메인을 제공하지 않았음을 의미합니다.
