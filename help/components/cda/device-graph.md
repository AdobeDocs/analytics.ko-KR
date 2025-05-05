---
title: Device Graph
description: Device Graph를 사용하여 데이터 결합의 사전 요구 사항과 제한 사항을 이해합니다.
exl-id: b8408a7d-6aff-4fff-b535-f10d422bcf0d
feature: CDA
role: Admin
source-git-commit: cc0b8703d6b6488adf9a2ea41a51001538d1cbee
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 60%

---


# Device Graph

{{available-existing-customers}}

교차 디바이스 분석은 개인 그래프를 사용하여 데이터를 함께 결합할 수 있습니다. 개인 그래프는 조직에 고유한 해시된 장치 ID의 저장소입니다. CDA는 Device Graph와 정기적으로 통신하여 디바이스들을 함께 연결합니다.

## Device Graph별 사전 요구 사항

Device Graph 방법을 사용하여 크로스 디바이스 분석을 구현하려는 경우 다음 조건을 충족해야 합니다. 조직 내의 팀 및 Adobe 계정 팀과 함께 다음 사항을 모두 충족하는지 확인합니다.

>[!WARNING]
>
>모든 사전 요구 사항을 충족하지 못하면 크로스 디바이스 분석을 사용할 수 없거나 데이터 결합이 제대로 되지 않을 수 있습니다.
>

* [개요 페이지](overview.md)에 나열되어 있는 모든 사전 요구 사항.
* 조직은 [Adobe Experience Platform ID 서비스 개인 그래프](https://business.adobe.com/products/experience-platform/identity-service.html)를 사용해야 합니다. ID 서비스 사용 안내서의 [홈 페이지](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=ko-KR)도 참조하세요.
* 구현은 최신 버전의 ECID(Experience Cloud ID 서비스)를 사용해야 합니다. ID 서비스 사용 안내서에서 [홈 페이지](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ko)를 참조하세요. Adobe Experience Platform에서 [태그](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ko)를 사용하는 대부분의 구현에 이미 ID 서비스가 배포되어 있을 수 있습니다.
* 구현은 사용자가 로그인하거나 이메일을 여는 경우와 같이 개인을 식별할 수 있을 때마다 이 `setCustomerIDs` 함수 (또는 그에 상응하는 SDK 항목)를 호출해야 합니다. 이 요구 사항은 모바일 앱 (사용하는 경우)을 비롯한 모든 플랫폼에 적용됩니다. ID 서비스 사용 안내서에서 [`setCustomerIDs`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html?lang=ko-KR)을(를) 참조하십시오.

## Device Graph에 해당하는 제한 사항

* 기존 Analytics ID는 지원되지 않습니다. Experience Cloud ID가 있는 방문자만 결합됩니다.
* 조직에서 개인 그래프를 사용하는 경우 새 디바이스를 결합하는 데 최대 24시간이 걸립니다.
* 서드파티 디바이스 그래프는 지원되지 않습니다.

## 다음 단계

조직이 모든 요구 사항을 충족하고 제한 사항을 이해하면 [크로스 디바이스 분석 설정](setup.md)을 시작할 수 있습니다.
