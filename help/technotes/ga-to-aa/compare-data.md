---
title: Adobe Analytics 데이터와 서드파티 제품 비교
description: Adobe Analytics의 데이터를 다른 Analytics 솔루션에서 수집한 데이터와 직접 비교할 때 선택할 수 있는 옵션을 이해합니다.
feature: Third-party Integration
exl-id: b4f85088-7ffd-45dc-bdd1-c0fc8dc3b332
source-git-commit: 34ba0e09cd909951a777b0ad3da080958633f97e
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 88%

---

# Adobe Analytics 데이터와 서드파티 제품 비교

온라인에서 사용할 수 있는 다양한 분석 솔루션이 있습니다. 이러한 각 솔루션은 자체 방법을 사용하여 코드를 구현하고 데이터를 수집합니다. 다양한 제품들이 각 제품에서 사용되는 페이지 보기, 방문, 고유 방문자 및 기타 지표를 구성하는 항목에 대한 자체 정의를 가지고 있습니다.

정의, 데이터 구조 및 구현이 이렇게 광범위하게 서로 다르기 때문에 **Adobe 고객 지원 센터는 서드파티 분석 도구와의 차이를 해결하지는 않습니다.**

Adobe Analytics와 서드파티 분석 도구 간에 큰 차이가 발생하는 경우 다음 리소스를 사용할 수 있습니다.

* **디버거를 사용한 자체 감사**: [Adobe의 디버거](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=ko-KR)나 다른 패킷 모니터를 사용하여 사이트의 페이지를 확인할 수 있습니다. 디버거를 사용하면 구현의 유효성을 검사하여 이미지 요청이 올바른 변수로 올바로 실행되는지 확인할 수 있습니다.
* **데이터 피드를 사용한 자체 감사**: Adobe에서는 각 날의 모든 원시 데이터를 포함하는 [데이터 피드](/help/export/analytics-data-feed/data-feed-overview.md) 수신 옵션을 조직에 제공합니다. 그러면 조직은 이 데이터를 사용하여 서드파티 분석 도구와 비교하여 불일치를 결정할 수 있습니다.
* **Adobe Consulting을 통한 감사 및 데이터 유효성 검사 지원**: 공식 Adobe 담당자가 사이트에서 전체 구현 감사를 수행하려면 Adobe 계정 팀에 문의하십시오. 회사의 계약에 따라 사이트를 감사할 수 있는 구현 컨설턴트와 회의를 예약할 수 있습니다.
