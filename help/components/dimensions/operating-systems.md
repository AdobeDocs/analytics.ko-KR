---
title: 운영 체제
description: 방문자의 운영 체제입니다.
feature: Dimensions
exl-id: e3911ae0-d242-4da2-a4bc-b2f4877f9dd2
TQID: https://experienceleague.adobe.com/WM6GQ-AhLmtudRWXF6lOez6DaVxMBU3rSaEb2UdsXdc
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
subfeature_v2:
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 34%
---
# 운영 체제

운영 체제 [차원](overview.md)은(는) 방문자가 사용한 운영 체제와 버전을 보여 줍니다. 웹 속성에 OS별 기능이 있는 경우 이 차원을 통해 가장 일반적인 운영 체제를 파악할 수 있습니다.

## 이 차원을 데이터로 채우기

Adobe은 `User-Agent` HTTP 헤더에서 이 차원을 파생하여 Adobe이 [DeviceAtlas](https://deviceatlas.com/)와(과) 협력하여 유지 관리하는 내부 조회 테이블에 대해 이 차원을 일치시킵니다. 설정할 변수가 없습니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(사용자 에이전트에서 파생) |
| **웹 SDK/XDM 필드** | 없음(사용자 에이전트에서 파생) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 해당 없음 |

* AppMeasurement 구현의 경우 이 차원은 즉시 작동합니다.
* 웹 SDK 구현의 경우 [데이터 스트림을 구성](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=ko)할 때 [!UICONTROL 장치 조회]를 사용하도록 설정하십시오.

## 차원 항목

차원 항목에는 방문자가 사용하는 운영 체제가 포함됩니다. 예로는 `"Windows 10"`, `"OS X 10.15.7"` 및 `"Android 9"`가 있습니다.

## 정확한 OS 버전 추적

업계에서 클라이언트 힌트로 전환함에 따라 일부 운영 체제 버전이 잠재적으로 혼동될 수 있습니다. 예를 들어 높은 엔트로피 클라이언트 힌트를 수집하지 않는 경우 &quot;Windows 10&quot; 및 &quot;Windows 11&quot;을 모두 &quot;Windows 10&quot; 아래에 그룹화할 수 있습니다. 자세한 내용은 기술 정보 안내서의 [클라이언트 힌트](/help/technotes/client-hints.md)를 참조하십시오.
