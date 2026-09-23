---
title: 브라우저 유형
description: 브라우저를 만든 조직입니다.
feature: Dimensions
exl-id: 2a88ebc6-879e-4e5b-a8e5-40a32d54ac1b
TQID: https://experienceleague.adobe.com/Qb4g-5RXrK42ui4xG86YEv3ozVqmqHrn9Bj5zqXmzPU
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
source-wordcount: '186'
ht-degree: 52%
---
# 브라우저 유형

&#39;브라우저 유형&#39; [차원](overview.md)은(는) 방문자가 사용하는 브라우저를 만든 조직을 나열합니다. 이 차원은 방문자가 주로 사용하는 브라우저를 확인하려는 경우 유용합니다. 동일한 브라우저의 서로 다른 버전을 별도의 차원 항목으로 나열하지 않는다는 점에서 &#39;브라우저&#39; 차원보다 높은 가치를 제공합니다.

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

차원 항목에는 브라우저를 만드는 조직이 포함됩니다. 일반적인 차원 항목에는 `"Google"` ([!DNL Chrome] 작성자), `"Apple"` ([!DNL Safari] 작성자), `"Microsoft"` ([!DNL Edge] 작성자) 및 `"Mozilla"` ([!DNL Firefox] 작성자) 등이 포함됩니다.
