---
description: 서버측 전달을 구현하려면 이러한 Experience Cloud 솔루션, 서비스 및 코드 요구 사항을 충족해야 합니다. 이러한 요구 사항에는 코드 버전을 확인하는 방법과 최신 코드 라이브러리를 얻을 수 있는 곳에 대한 지침도 포함되어 있습니다.
solution: Audience Manager
title: 서버 측 전달 요구 사항
uuid: e52c9292-b2ed-4782-9594-c813e4f894e1
exl-id: af0cf85a-381e-46d2-a4fd-9a5b073c8a8d
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 93%

---

# 서버 측 전달 요구 사항

서버측 전달을 구현하려면 이러한 Experience Cloud 솔루션, 서비스 및 코드 요구 사항을 충족해야 합니다. 이러한 요구 사항에는 코드 버전을 확인하는 방법과 최신 코드 라이브러리를 얻을 수 있는 곳에 대한 지침도 포함되어 있습니다.

## 솔루션 요구 사항

서버 측 전달은 [Analytics](https://www.adobe.com/kr/data-analytics-cloud/analytics.html)와 [Audience Manager](https://www.adobe.com/kr/data-analytics-cloud/audience-manager.html) 및/또는 [Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html)에서 작동합니다.

## 서비스 요구 사항

서버 측 전달을 사용하려면 [ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html)가 필요합니다. ID 서비스는 Experience Cloud의 모든 솔루션에서 사이트 방문자를 식별하는 범용 ID를 제공합니다. 서버 측 전달이 작동하려면 ID 서비스를 구현해야 합니다.

## 코드 버전

서버 측 전달에는 아래 나열된 코드 라이브러리 버전 1.5 이상이 필요합니다. 더 좋은 방법은 이러한 최소 요구 사항보다는 최신 버전을 사용하는 것입니다.

* `AppMeasurement.js`
* `AppMeasurement_Module_AudienceManagement.js`
* `VistorAPI.js`

### 코드 라이브러리 버전 확인

브라우저가 수행한 HTTP 요청을 모니터링하는 도구에서 AppMeasurement 및 Visitor API 코드의 버전 번호를 표시할 수 있습니다. `AppMeasurement_Module_AudienceManagement.js`는 버전 ID를 포함하지 않거나 반환하지 않습니다. 다음 예제는 버전 ID가 `AppMeasurement.js` 및 `VisitorAPI.js` 코드처럼 표시되는 코드 라이브러리를 보여줍니다.

* `AppMeasurement.js`: [Adobe Debugger](https://experienceleague.adobe.com/docs/analytics/implementation/validate/debugger.html)가 다음과 같은 AppMeasurement 버전을 반환합니다. `Version of Code | JS-1.5.1` 다른 도구는 다른 레이블을 사용할 수 있지만 값은 항상 `JS-X.X.X` 패턴을 따르며, 여기서 `X`는 버전 번호입니다.
* `VisitorAPI.js`: `d_visid_ver` 매개 변수를 찾습니다. 다음과 같은 방문자 ID 서비스를 표시합니다. `d_visid_ver: 1.5.5`. 1.5.2 버전보다 오래된 방문자 API 코드에는 버전 번호가 포함되지 않았습니다. 모니터링 결과가 버전 번호를 반환하지 않으면 이전 코드 라이브러리를 사용하고 있는 것이므로 업그레이드해야 합니다.
