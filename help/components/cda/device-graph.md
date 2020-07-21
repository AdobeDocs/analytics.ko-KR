---
title: 장치 그래프
description: 장치 그래프를 사용하여 데이터를 결합하는 데 필요한 사전 요구 사항과 제한 사항을 이해합니다.
translation-type: tm+mt
source-git-commit: eb2bee26dd58dcff13b4ddf41c6f6ab337d8d374
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 41%

---


# 장치 그래프

크로스 디바이스 Analytics은 데이터를 서로 연결하는 두 가지 방법을 제공합니다. 이 방법은 Adobe Experience Platform ID 서비스 Co-op 그래프 또는 개인 그래프를 사용하여 데이터를 하나로 묶습니다. CDA는 장치 그래프와 정기적으로 통신하여 장치를 서로 연결합니다.

## Co-op 그래프와 개인 그래프 간의 차이점

Adobe는 ID 서비스의 일부로 두 가지 유형의 장치 그래프를 제공합니다.

* **Co-op 그래프**: 모든 고객이 기여하고 참조할 수 있는 해시된 장치 ID의 저장소 이 유형의 장치 그래프는 공동 작업이므로 일반적으로 비공개 그래프보다 더 많은 장치와 일치합니다.
* **비공개 그래프**: 해시된 장치 ID의 저장소로서 조직만 참조합니다.

## 장치 그래프별 사전 요구 사항

장치 그래프 방법을 사용하여 장치 간 Analytics을 구현하려는 경우 다음이 필요합니다. 조직 내 팀 및 Adobe 계정 관리자와 함께 다음 사항을 모두 충족하도록 하십시오.

>[!IMPORTANT] 모든 전제 조건을 충족하지 못하면 교차 디바이스 분석을 사용할 수 없거나 데이터 결합이 제대로 되지 않을 수 있습니다.

* 모든 전제 조건은 [개요 페이지에 나열되어 있습니다](overview.md).
* 조직이 Adobe Experience Platform ID 서비스 Co-op 그래프 또는 Private 그래프를 사용해야 합니다. Device Co-op 사용 안내서의 [홈 페이지](https://docs.adobe.com/content/help/ko-KR/device-co-op/using/home.html)를 참조하십시오.
* 구현에서 최신 버전의 Experience Cloud ID 서비스를 사용해야 합니다. Experience Cloud ID 서비스 사용 안내서의 [홈 페이지](https://docs.adobe.com/content/help/ko-KR/id-service/using/home.html)를 참조하십시오. Adobe Experience Platform Launch를 사용하는 대부분의 구현에 이미 ECID가 배포되어 있을 수 있습니다.
* Your implementation must call the `setCustomerIDs` function (or SDK equivalent) whenever an individual can be identified, such as when a user logs in or opens an email. 이 요구 사항은 모바일 앱(사용하는 경우)을 비롯한 모든 플랫폼에 적용됩니다. Experience Cloud ID 서비스 사용 안내서의 [`setCustomerIDs`](https://docs.adobe.com/content/help/ko-KR/id-service/using/id-service-api/methods/setcustomerids.html)를 참조하십시오.

## 장치 그래프별 제한 사항

* 기존 Analytics ID는 지원되지 않습니다. Experience Cloud ID가 있는 방문자만 결합됩니다.
* 조직에서 비공개 그래프를 사용하는 경우 새 장치를 연결하는 데 최대 24시간이 걸립니다.
* 조직에서 Co-op 그래프를 사용하는 경우 사이트를 방문하는 새로운 장치를 연결하는 데 최대 2주가 걸릴 수 있습니다. 가장 최근 2주 동안 CDA의 결합 수준은 일반적으로 그 이전까지 날짜 범위의 수준보다 낮습니다.
* 타사 장치 그래프는 지원되지 않습니다.

## 다음 단계

Once your organization meets all requirements met and understands the limitations, you can start [Setting up Cross-Device Analytics](setup.md).

