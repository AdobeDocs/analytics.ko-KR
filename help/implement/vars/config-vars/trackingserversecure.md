---
title: trackingServerSecure
description: HTTPS 페이지에서 이미지 요청이 전송되는 위치를 파악합니다.
feature: Variables
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 61%

---

# trackingServerSecure

Adobe는 방문자가 생성한 이미지 요청을 수신하여 사이트의 데이터를 수집합니다. `trackingServerSecure` 변수는 HTTPS 페이지에서 이미지 요청이 전송되는 위치를 파악합니다. 또한 방문자 쿠키가 저장되어 있는 위치도 파악합니다. 이 변수가 올바르게 정의되지 않으면 구현에서 데이터 손실이 발생할 수 있습니다.

>[!WARNING]
>
>이 값을 변경하면 AppMeasurement가 다른 위치에서 쿠키를 찾습니다. 방문자 쿠키가 새 위치에 설정되면 보고에서 고유 방문자 수가 일시적으로 급증할 수 있습니다.

## 웹 SDK 확장을 사용한 Edge 도메인

웹 SDK는 [!UICONTROL Edge 도메인] 추적 서버와 보안 추적 서버를 모두 처리하도록 합니다. 원하는 을 설정할 수 있습니다 [!UICONTROL Edge 도메인] 값을 설정하는 것이 좋습니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 원하는 태그 속성을 클릭합니다.
1. 로 이동합니다. [!UICONTROL 확장] 탭을 클릭한 다음 **[!UICONTROL 구성]** 버튼 아래 [!UICONTROL Adobe Experience Platform Web SDK].
1. 원하는 을 설정합니다 **[!UICONTROL Edge 도메인]** 텍스트 필드.

자세한 내용은 [Adobe Experience Platform 웹 SDK 확장 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html) 를 참조하십시오.

>[!TIP]
>
>조직에서 AppMeasurement 또는 Analytics 확장 구현에서 웹 SDK로 이동하는 경우 이 필드에 포함된 동일한 값을 사용할 수 있습니다 `trackingServerSecure` 또는 `trackingServer`).

## 웹 SDK를 수동으로 구현하는 Edge 도메인

를 사용하여 SDK 구성 [`edgeDomain`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR?lang=ko-KR). 필드는 데이터를 보낼 도메인을 결정하는 문자열입니다.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## Adobe Analytics 확장을 사용하는 SSL 추적 서버

[!UICONTROL SSL 추적 서버]는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 일반] 아코디언 아래의 필드입니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
4. [!UICONTROL 일반] 아코디언을 확장합니다. 그러면 [!UICONTROL SSL 추적 서버] 필드가 표시됩니다.

이 필드를 비워 두면 기본값은 [`trackingServer`](trackingserver.md) 변수의 값으로 설정됩니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.trackingServerSecure

`s.trackingServerSecure` 변수는 이미지 요청을 보낼 위치를 포함하는 문자열입니다. 거의 항상 사이트의 하위 도메인입니다. 브라우저의 최신 개인정보 보호정책은 일반적으로 서드파티 쿠키를 신뢰할 수 없게 합니다. 이 변수가 비어 있으면 `s.trackingServer` 변수의 값을 사용합니다.

이 변수의 값은 거의 항상 `data.example.com`과 같은 자사 도메인입니다. 자사 쿠키 프로세스에 대한 자세한 내용은 핵심 서비스 사용 안내서에서 [Experience Cloud의 자사 쿠키](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=ko-KR)를 참조하십시오.

처음 자사 쿠키 구현을 구성하는 개인은 사용하는 도메인과 하위 도메인도 정의합니다. 예:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME 레코드는 일반적으로 `data.adobedc.net`, `sc.adobedc.net` 또는 `2o7.net`의 하위 도메인을 가리킵니다.
