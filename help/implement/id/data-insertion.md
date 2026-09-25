---
title: 데이터 삽입 API를 사용한 방문자 식별
description: 데이터 삽입 API를 사용하여 서버측 방문자를 식별하고 직접 Adobe Analytics 데이터 수집을 수행합니다.
feature: Implementation Basics
role: Admin, Developer, Leader
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
    internal-label: Functions
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
    internal-label: Variables
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 7fcd738b7eb13c13d5f9f23d625287988c803220
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%
---
# 데이터 삽입 API를 사용한 방문자 식별

[데이터 삽입 API](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/)는 AppMeasurement 또는 Web SDK과 같은 클라이언트측 라이브러리가 없는 Adobe Analytics 수집 서버로 히트를 보냅니다. ID를 관리할 라이브러리가 없으므로 직접 이미지 요청의 경우 브라우저에서, 서버측 수집의 경우 서버에서 방문자 ID를 직접 설정합니다.

>[!NOTE]
>
>이 페이지는 방문자 ID를 다룹니다. 요청을 직접 작성하고 보내는 방법은 Adobe Developer에서 [데이터 삽입 API 설명서](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/)를 참조하십시오.

Adobe은 표준 [작업 순서](overview.md): `vid`, `aid`, `mid`, `fid`, 마지막으로 IP 주소 및 사용자 에이전트를 사용하여 방문자를 식별합니다. 데이터 삽입 API를 사용하면 일반적으로 ECID(`mid`), Analytics 방문자 ID(`aid`) 또는 사용자 지정 방문자 ID(`vid`) 중 하나를 직접 설정합니다.

## ECID 사용(권장)

ECID(`mid`(으)로 전송됨)는 Adobe Analytics, Adobe Target 및 Adobe Audience Manager에서 공유되는 최신 교차 솔루션 방문자 식별자입니다. Adobe은 가능한 모든 곳에서 사용할 것을 권장합니다.

[방문자 ID 서비스](https://experienceleague.adobe.com/kr/docs/id-service/using/home)&#x200B;(`VisitorAPI.js`)를 사용하여 ECID를 얻습니다. 브라우저에서 [`getInstance`](https://experienceleague.adobe.com/ko/docs/id-service/using/id-service-api/methods/getinstance)을(를) 사용하여 IMS 조직 ID로 서비스를 초기화한 다음 [`getMarketingCloudVisitorID`](https://experienceleague.adobe.com/ko/docs/id-service/using/id-service-api/methods/getmcvid)을(를) 사용하여 ECID를 읽습니다.

```js
var visitor = Visitor.getInstance("YOUR_ORG_ID@AdobeOrg");
var ecid = visitor.getMarketingCloudVisitorID();
```

각 히트에 대한 해당 값을 `mid` 쿼리 매개 변수로 보내고 IMS 조직 ID를 `mcorgid` 매개 변수로 보내면 ECID가 올바르게 확인됩니다. 데이터가 Audience Manager으로 전송되는 경우 [`getLocationHint`](https://experienceleague.adobe.com/ko/docs/id-service/using/id-service-api/methods/getlocationhint)에서 지역도 `aamlh` 매개 변수로 전송합니다. 자신의 고객 식별자를 방문자와 연결하려면 [`setCustomerIDs`](https://experienceleague.adobe.com/ko/docs/id-service/using/id-service-api/methods/setcustomerids)을(를) 사용합니다.

서버측 수집의 경우 클라이언트에서 ECID를 가져와서 각 히트를 전송할 서버에 전달합니다. 클라이언트 없이 서버측에서 ECID를 완전히 생성하려면 ID 서비스의 [직접 통합](https://experienceleague.adobe.com/ko/docs/id-service/using/implementation/direct-integration)을 사용하십시오.

## Analytics 방문자 ID 사용

Analytics 방문자 ID(`aid`)가 [`s_vi`](https://experienceleague.adobe.com/ko/docs/core-services/interface/data-collection/cookies/analytics) 쿠키에 저장되어 있습니다. 식별자 없이 히트가 도착하면 수집 서버가 `aid`을(를) 할당하고 해당 식별자가 포함된 쿠키를 설정하려고 시도합니다. 일부 [응답 형식](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/response-types)은(는) 이 식별자도 응답 본문에 포함합니다.

* **클라이언트측(직접 이미지 요청).** 브라우저는 서버가 반환한 `s_vi` 쿠키를 저장하고 나중에 다시 요청할 때마다 동일한 수집 도메인으로 보냅니다. 그런 다음 자신을 설정할 `aid` 없이 방문자가 자동으로 인식됩니다. 이 모델은 쿠키에 따라 다르므로, 쿠키 기반 ID와 동일한 내구성 제한을 따릅니다. 자사 및 타사 쿠키 동작은 [AppMeasurement을 사용한 방문자 식별](appmeasurement.md)을, Adobe에서 사용할 식별자를 선택하는 방법은 [작업 순서](overview.md)을 참조하십시오. Adobe에서는 지속적인 ID를 위해 ECID를 사용하는 것이 좋습니다.

  >[!NOTE]
  >
  >`s_vi` 쿠키에서 직접 방문자 ID를 읽는 경우 쿠키는 ID를 추가 데이터(예: `[CS]v1|<id>[CE]`)로 래핑합니다. — `<id>` 부분만 추출합니다. 방문자 응답에서 ID를 읽으면 구문 분석 없이 ID를 직접 반환합니다.

* **서버측.** 서버에 쿠키 Jar가 없으므로 사용자에게 입력된 `aid`을(를) 직접 저장하고 다시 보냅니다.

  1. 저장된 `aid`에서 사용자를 찾습니다.
  1. 쿼리 매개 변수가 있으면 `aid` 쿼리 매개 변수로 보내십시오.
  1. 그렇지 않으면 식별자 없이 히트를 보내 할당된 `aid`을(를) 반환하는 응답 형식을 요청한 다음 다음에 저장하십시오.

  식별자가 없는 첫 번째 히트는 서버가 반환하는 `aid`에 이미 귀속되므로 ID가 있기 전에 해당 히트를 보내도 데이터가 손실되지 않습니다. ID(JavaScript의 경우 `3`, XML의 경우 `11`, JSON의 경우 `10`) 및 요청 형식을 반환하는 응답 형식에 대해서는 데이터 삽입 API 설명서의 [응답 형식](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/response-types)을(를) 참조하십시오.

  서버측 요청은 방문자 쿠키를 전달하지 않으며, 자체 IP 주소 및 사용자 에이전트는 발신자에 속합니다. 히트의 특성을 올바르게 지정하려면 방문자의 실제 IP 주소(`X-Forwarded-For` 헤더)와 사용자 에이전트(`User-Agent` 헤더)도 전달하십시오.

## 사용자 지정 방문자 ID 사용

사용자가 완전히 제어하는 영구 식별자가 이미 있는 경우 모든 히트에서 해당 식별자를 [`visitorID`](/help/implement/vars/config-vars/visitorid.md)(`vid`)(으)로 보내고 자체 ID를 끝까지 보낼 수 있습니다. 이는 안정적인 장치 식별자를 제공하는 비브라우저 플랫폼에 적합합니다. 예를 들어 Unity 응용 프로그램은 장치 식별자를 `vid`(으)로 보낼 수 있습니다.

>[!IMPORTANT]
>
>모든 히트에서 안정적인 값을 보장할 수 있는 경우에만 `vid`을(를) 사용합니다.
>
>* **브라우저가 적합하지 않습니다.** 브라우저에 안정적으로 채울 수 있는 영구 식별자가 없으므로 브라우저 집합 `vid`이(가) 조각화되거나 충돌합니다. 대신 쿠키 기반 클라이언트측 모델을 사용하십시오.
>* **인증 식별자를 주의하십시오.** 사용자가 로그인하기 전에는 식별자가 없으며 사용자가 로그아웃하면 이후 히트는 다른 방문자에게 연결됩니다. 이러한 작업은 한 사람의 활동을 여러 방문자에게 분할합니다.

사용자 지정 방문자 ID의 형식 및 제약 조건에 대해서는 [`visitorID`](/help/implement/vars/config-vars/visitorid.md)을(를) 참조하십시오.
