---
title: 크로스 디바이스 방문자 식별 FAQ
description: 크로스 디바이스 방문자 식별 FAQ
feature: Implementation Basics
exl-id: da972fee-fe6e-45b2-af01-50674989c375
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 100%

---

# 크로스 디바이스 방문자 식별 FAQ

교차 장치 방문자 식별 FAQ

+++크로스 디바이스 방문자 식별과 크로스 디바이스 분석 간의 차이점은 무엇입니까?
크로스 디바이스 방문자 식별에서는 몇 가지 주요 제한 사항이 있지만 `visitorID` 변수를 사용하여 디바이스를 서로 연결하는데, 몇 가지 주요 제한 사항이 있습니다. 이 식별 방법의 가장 큰 제한 사항 중 하나는 디바이스가 이미 인식되어 있지 않은 경우 인증되지 않은 히트는 구분된다는 것입니다. 이러한 인증되지 않은 히트는 고유 방문자 수를 부풀릴 수 있습니다.

크로스 디바이스 분석은 Adobe의 최신 크로스 디바이스 방문자 식별 방법입니다. 여기에서는 Experience Cloud ID 서비스 및 디바이스 그래프를 사용하여 서로 다른 디바이스들에서의 방문을 소급하여 통합합니다. CDA를 사용하려면 동일한 방문자가 사용하는 디바이스를 판별하는 `setCustomerIDs` 함수를 사용해야 합니다.
+++

+++크로스 디바이스 방문자 식별은 세그먼트를 어떻게 처리합니까?
크로스 디바이스 방문자 식별에서는 세그먼트를 다른 기능과 유사하게 처리합니다. 각 개별 히트를 살펴보고 세그먼트 기준과 일치하는지 확인하고 일치하는 경우 데이터에 해당 히트를 포함하십시오. 방문 및 방문자 기반 컨테이너를 사용하는 세그먼트는 여전히 방문자 ID를 봅니다. 구현이 가능한 모든 곳에서 `visitorID` 변수를 사용하여 세그먼테이션의 고유 방문자를 일관되게 식별하도록 하십시오.
+++
