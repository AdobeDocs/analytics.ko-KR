---
title: 도메인
description: 방문자가 인터넷에 액세스하기 위해 사용하는 조직 또는 ISP입니다.
translation-type: tm+mt
source-git-commit: c2d371cee2821360ab87240b1a81695798af4f9f
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 7%

---


# 도메인

&#39;도메인&#39; 차원은 방문자가 인터넷에 액세스하기 위해 사용하는 액세스 지점을 보고합니다.

## 이 차원을 데이터로 채우기

Adobe은 [디지털 요소](https://www.digitalelement.com/) 와 파트너 관계를 맺고 액세스 포인트 도메인을 결정합니다. 역추적 DNS 조회를 포함한 여러 가지 방법은 액세스 포인트 도메인을 결정하는 데 사용됩니다. 구성할 필요가 없고 채울 변수가 없습니다. 모든 AppMeasurement 구현에서 기본적으로 작동합니다.

## Dimension 항목

예 차원 항목에는 `comcast.net`, `rr.com`및 `sbcglobal.net`가 포함됩니다 `amazonaws.com`. 이러한 도메인은 액세스 포인트이며 ISP나 조직을 나타내는 도메인이 아닐 수도 있습니다.

액세스 포인트 IP 주소의 소유자가 도메인을 제공하지 않았다는 `None` 의미입니다.
