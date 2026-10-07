---
description: 서버측 전달을 구현하려면 이러한 CX Enterprise 솔루션, 서비스 및 코드 요구 사항을 충족해야 합니다. 이러한 요구 사항에는 코드 버전을 확인하는 방법과 최신 코드 라이브러리를 가져올 위치에 대한 지침도 포함되어 있습니다.
solution: Analytics
title: 서버측 전달 요구 사항
feature: Report Suite Settings
exl-id: af0cf85a-381e-46d2-a4fd-9a5b073c8a8d
role: Admin
TQID: 'https://experienceleague.adobe.com/1GCflxlY4IpT-pPTr93FuOmxkJLC4baJe3Z2SGjj1So'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
    internal-label: Admin Tools
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
subfeature_v2:
  - id: c354699e-6555-4397-8706-1a9a89984069
    internal-label: Server side forwarding
  - id: fab61dd8-112a-4e5e-ad5f-fb0240b7a60b
    internal-label: Report Suite settings
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 319f78bb5f8c2449a7263e3f1c378c49656889a7
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 47%
---
# 서버측 전달 요구 사항

서버측 전달을 구현하려면 이러한 CX Enterprise 솔루션, 서비스 및 코드 요구 사항을 충족해야 합니다. 이러한 요구 사항에는 코드 버전을 확인하는 방법과 최신 코드 라이브러리를 가져올 위치에 대한 지침도 포함되어 있습니다.

## 솔루션 요구 사항

서버측 전달은 [Analytics](https://www.adobe.com/kr/data-analytics-cloud/analytics.html)와 [Audience Manager](https://www.adobe.com/kr/data-analytics-cloud/audience-manager.html) 및/또는 [Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=ko)에서 작동합니다.

## 서비스 요구 사항

서버측 전달을 사용하려면 [ID 서비스](https://experienceleague.adobe.com/kr/docs/id-service/using/home)가 필요합니다. ID 서비스는 CX Enterprise의 모든 솔루션에서 사이트 방문자를 식별하는 범용 ID를 제공합니다. 서버측 전달이 작동하려면 ID 서비스를 구현해야 합니다.

## 코드 버전

서버측 전달에는 아래 나열된 코드 라이브러리 버전 1.5 이상이 필요합니다. 가장 좋은 방법으로서, 이러한 필요한 최소 버전보다 최신 버전을 사용하는 것이 좋습니다.

* `AppMeasurement.js`
* `AppMeasurement_Module_AudienceManagement.js`
* `VistorAPI.js`

### 코드 라이브러리 버전 확인

브라우저가 수행한 HTTP 요청을 모니터링하는 도구에서 AppMeasurement 및 Visitor API 코드의 버전 번호를 표시할 수 있습니다. `AppMeasurement_Module_AudienceManagement.js`는 버전 ID를 포함하지 않거나 반환하지 않습니다. 다음 예제는 버전 ID가 `AppMeasurement.js` 및 `VisitorAPI.js` 코드처럼 표시되는 코드 라이브러리를 보여 줍니다.

* `AppMeasurement.js`: `/b/ss/examplersid/1/JS-X.X.X/s234234238479`과(와) 같이 응답 형식 뒤에 버전이 요청 URL에 나타납니다. 요청을 디코딩하는 [디버깅 도구](/help/implement/validate/debugging-tools.md)에서 다른 레이블을 사용할 수 있지만 값은 항상 `JS-X.X.X` 패턴을 따릅니다. 여기서 `X`은(는) 버전 번호입니다.
* `VisitorAPI.js`: `d_visid_ver` 매개 변수를 찾습니다. 다음과 같은 방문자 ID 서비스를 표시합니다. `d_visid_ver: 1.5.5`. 버전 1.5.2 이전의 방문자 API 코드에는 버전 번호가 포함되어 있지 않습니다. 모니터링 결과가 버전 번호를 반환하지 않는 경우 이전 코드 라이브러리를 사용하고 있으며 업그레이드해야 할 수도 있습니다.
