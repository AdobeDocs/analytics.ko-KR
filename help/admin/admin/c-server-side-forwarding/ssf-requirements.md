---
description: 서버측 전달을 구현하려면 이러한 Experience Cloud 솔루션, 서비스 및 코드 요구 사항을 충족해야 합니다. 이러한 요구 사항에는 코드 버전을 확인하는 방법과 최신 코드 라이브러리를 얻을 수 있는 곳에 대한 지침도 포함되어 있습니다.
seo-description: 서버측 전달을 구현하려면 이러한 Experience Cloud 솔루션, 서비스 및 코드 요구 사항을 충족해야 합니다. 이러한 요구 사항에는 코드 버전을 확인하는 방법과 최신 코드 라이브러리를 얻을 수 있는 곳에 대한 지침도 포함되어 있습니다.
seo-title: 서버측 전달을 위한 요구 사항
solution: Audience Manager
title: 서버측 전달을 위한 요구 사항
uuid: E 52 C 9292-B 2 ED -4782-9594-C 813 E 4 F 894 E 1
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# 서버측 전달을 위한 요구 사항

서버측 전달을 구현하려면 이러한 Experience Cloud 솔루션, 서비스 및 코드 요구 사항을 충족해야 합니다. 이러한 요구 사항에는 코드 버전을 확인하는 방법과 최신 코드 라이브러리를 얻을 수 있는 곳에 대한 지침도 포함되어 있습니다.

## 솔루션 요구 사항

서버 측 전달은 [Analytics](https://www.adobe.com/data-analytics-cloud/analytics.html)와 [Audience Manager](https://www.adobe.com/data-analytics-cloud/audience-manager.html) 및/또는 [ Audiences](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)에서 작동합니다.

## 서비스 요구 사항

Server-side forwarding requires the [Identity Service](https://marketing.adobe.com/resources/help/en_US/mcvid/). ID 서비스는 Experience Cloud의 모든 솔루션에서 사이트 방문자를 식별하는 범용 ID를 제공합니다. 서버 측 전달이 작동하려면 ID 서비스를 구현해야 합니다.

## 코드 버전

서버 측 전달에는 아래 나열된 코드 라이브러리 버전 1.5 이상이 필요합니다. 더 좋은 방법은 이러한 최소 요구 사항보다는 최신 버전을 사용하는 것입니다.

* `AppMeasurement.js`
* `AppMeasurement_Module_AudienceManagement.js`
* `VistorAPI.js`

### 코드 라이브러리 버전 확인

브라우저가 수행한 HTTP 요청을 모니터하는 도구에서 AppMeasurement 및 Visitor API 코드의 버전 번호를 표시할 수 있습니다. `AppMeasurement_Module_AudienceManagement.js` does not contain or return a version id. 다음 예제는 버전 ID가 `AppMeasurement.js` 및 `VisitorAPI.js` 코드처럼 표시되는 코드 라이브러리를 보여줍니다.

* `AppMeasurement.js`: [Adobe Debugger](https://marketing.adobe.com/resources/help/en_US/sc/implement/debugger.html) 는 다음과 같이 appmeasurement 버전을 반환합니다. `Version of Code | JS-1.5.1`. 다른 도구는 다른 레이블을 사용할 수 있지만 값은 항상 `JS-X.X.X` 패턴을 따르며, 여기서 `X`는 버전 번호입니다.
* `VisitorAPI.js`: 매개 변수를 `d_visid_ver` 찾습니다. It will show you the Visitor ID service like this: `d_visid_ver: 1.5.5`. 1.5.2 버전보다 오래된 방문자 API 코드에는 버전 번호가 포함되지 않았습니다. 모니터링 결과가 버전 번호를 반환하지 않으면 이전 코드 라이브러리를 사용하고 있는 것이므로 업그레이드해야 합니다.