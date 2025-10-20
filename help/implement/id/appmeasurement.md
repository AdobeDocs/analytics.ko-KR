---
title: AppMeasurement을 사용한 방문자 식별
description: AppMeasurement을 사용하여 Adobe Analytics을 구현할 때 방문자를 올바르게 식별합니다.
source-git-commit: 779ba5b0a1d71467aaaf3872fd707cc323ae8af2
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# AppMeasurement을 사용한 방문자 식별

AppMeasurement은 데이터 수집을 위한 Adobe Analytics의 레거시 JavaScript 라이브러리입니다. AppMeasurement은 자체적으로 방문자를 식별하는 기본 방법을 제공하지만, 많은 최신 브라우저는 설정하려고 하는 서드파티 쿠키를 거부합니다. Adobe은 모든 구현에서 최신 브라우저 개인 정보 보호 표준을 준수하도록 Adobe Experience Cloud 방문자 ID 서비스 를 사용할 것을 강력히 권장합니다. AppMeasurement의 모든 버전은 방문자 ID 서비스를 구현하는 데 사용되는 JavaScript 라이브러리인 `VisitorAPI.js`과(와) 함께 제공됩니다.

## 방문자 ID 서비스를 사용한 방문자 식별(권장)

다음을 준비했는지 확인합니다.

* [최신 버전의 AppMeasurement](https://github.com/adobe/appmeasurement)을(를) 다운로드합니다. 다운로드한 라이브러리에는 `AppMeasurement.js` 및 `VisitorAPI.js`이(가) 모두 포함되어 있습니다.
* 개발 [보고서 세트 ID](/help/admin/tools/manage-rs/new-rs/new-report-suite.md).
* [`trackingServerSecure`](/help/implement/vars/config-vars/trackingserversecure.md)에 대해 원하는 에지 도메인입니다.
* IMS 조직 ID:
   1. Adobe ID 자격 증명을 사용하여 [experience.adobe.com](https://experience.adobe.com)에 로그인합니다.
   1. Experience Cloud 인터페이스의 모든 곳에서 `[Cmd]` + `[I]`(iOS) 또는 `[Ctrl]` + `[I]`(Windows)을 누릅니다.
   1. **[!UICONTROL 사용자 데이터 디버거]**&#x200B;가 나타납니다. **[!UICONTROL 할당된 조직]** 탭을 선택합니다.
   1. 원하는 IMS 조직을 확장합니다.
   1. **[!UICONTROL ID]** 필드를 찾습니다.

위의 리소스가 있는 경우, 다음 기본 예제 페이지에는 Adobe Analytics으로 데이터를 전송하는 데 필요한 최소 호출이 포함되어 있습니다.

```html
<html>
  <head>
    <title>Example AppMeasurement implementation page</title>
    <script src="AppMeasurement.js"></script>
    <script src="VisitorAPI.js"></script>
  </head>
  <body>
    <h1>Hello world!</h1>
    <script>
      var s = s_gi("examplersid"); // Include development report suite ID here
      s.trackingServerSecure = "example.data.adobedc.net"; // Include edge domain here
      s.visitor = Visitor.getInstance("ADB3LETTERSANDNUMBERS@AdobeOrg"); // Include IMS org ID here
      s.pageName = document.title;
      s.t();
    </script>
  </body>
</html>
```

>[!TIP]
>
>`Visitor`의 사용자 지정 변수에 [`doPlugins`](/help/implement/vars/functions/doplugins.md)의 존재를 할당하여 히트가 방문자 ID 서비스를 사용하는지 추적할 수 있습니다.
>
>```js
>s.doPlugins = function() {
>   s.prop1 = typeof(Visitor) != "undefined" ? "VisitorAPI present" : "VisitorAPI missing";
>};
>```

## `s_vi` 쿠키를 사용하여 방문자 식별(권장되지 않음)

>[!IMPORTANT]
>
>Adobe에서는 방문자를 식별하기 위해 이 방법을 사용하지 않는 것이 좋습니다.

조직에서 방문자 ID 서비스를 사용하지 않는 경우 AppMeasurement은 자체 방문자 ID 양식을 사용합니다. 방문자가 사이트에 처음 도달하면 라이브러리에서 [`s_vi`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) 쿠키를 확인합니다. 이 쿠키는 [`trackingServerSecure`](/help/implement/vars/config-vars/trackingserversecure.md)(HTTPS의 경우) 또는 [`trackingServer`](/help/implement/vars/config-vars/trackingserver.md)(HTTP의 경우)과 일치하는 도메인에서 설정됩니다.

* [관리 인증서 프로그램](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/adobe-managed-cert)에 참여하는 경우 추적 서버는 일반적으로 자사 도메인이므로 `s_vi` 쿠키를 자사 쿠키로 만듭니다.
* 관리 인증서 프로그램에 참여하지 않는 경우 추적 서버는 일반적으로 `adobedc.net`, `omtrdc.net` 또는 `2o7.net`의 하위 도메인이며 `s_vi` 쿠키를 타사 쿠키로 만듭니다. 최신 브라우저 개인 정보 보호 표준으로 인해 서드파티 쿠키는 대부분의 브라우저에서 거부됩니다. 거부되면 AppMeasurement은 대신 자사 대체 쿠키(`fid`)를 설정하려고 합니다.

`trackingServerSecure`을(를) 올바르게 설정하면 추가 방문자 식별 조치가 필요하지 않습니다.

## `visitorID`을(를) 사용하여 방문자 식별(권장되지 않음)

>[!IMPORTANT]
>
>Adobe에서는 방문자를 식별하기 위해 이 방법을 사용하지 않는 것이 좋습니다.

[`visitorID`](/help/implement/vars/config-vars/visitorid.md) 변수를 사용하면 조직에서 방문자를 식별하는 독립적인 제어를 완료할 수 있습니다. `visitorID`을(를) 사용하는 경우 다음 제한 사항에 유의하십시오.

* 모든 히트는 단일 방문자로 계산되려면 동일한 `visitorID` 값을 포함해야 합니다.
   * `visitorID`을(를) 생략한 모든 히트는 자동으로 다른 방문자 식별 방법을 사용하려고 시도하여 별도의 방문자로 취급됩니다.
   * 이전 히트와 다른 `visitorID` 값을 포함하는 모든 히트는 별도의 방문자로 처리됩니다.
   * Adobe에서는 서로 다른 방문자 ID를 함께 사용하여 히트를 연결하는 방법을 제공하지 않습니다.
* 공유 대상, Analytics for Target 및 고객 특성은 `visitorID`을(를) 사용하여 식별된 방문자에서 지원되지 않습니다.

이 변수를 사용하는 구현 지침은 [`visitorID`](/help/implement/vars/config-vars/visitorid.md)을(를) 참조하십시오.
