---
title: trackingServerSecure
description: HTTPS 페이지에서 이미지 요청이 전송되는 위치를 파악합니다.
feature: Appmeasurement Implementation
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 66%

---

# trackingServerSecure

Adobe는 방문자가 생성한 이미지 요청을 수신하여 사이트의 데이터를 수집합니다. `trackingServerSecure` 변수는 HTTPS 페이지에서 이미지 요청이 전송되는 위치를 파악합니다. 또한 방문자 쿠키가 저장되어 있는 위치도 파악합니다. 이 변수가 올바르게 정의되지 않으면 구현에서 데이터 손실이 발생할 수 있습니다.

>[!WARNING]
>
>이 값을 변경하면 AppMeasurement가 다른 위치에서 쿠키를 찾습니다. 방문자 쿠키가 새 위치에 설정되면 보고에서 고유 방문자 수가 일시적으로 급증할 수 있습니다.

## Web SDK 확장을 사용한 Edge 도메인

웹 SDK은 [!UICONTROL Edge 도메인]을 사용하여 추적 서버와 보안 추적 서버를 모두 처리합니다. Web SDK 확장을 구성할 때 원하는 [!UICONTROL Edge 도메인] 값을 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음 [!UICONTROL Adobe Experience Platform Web SDK] 아래의 **[!UICONTROL 구성]** 단추를 클릭합니다.
1. 원하는 **[!UICONTROL Edge 도메인]** 텍스트 필드를 설정합니다.

자세한 내용은 웹 SDK 설명서의 [Adobe Experience Platform Web SDK 확장 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=ko-KR)을 참조하십시오.

>[!TIP]
>
>조직이 AppMeasurement 또는 Analytics 확장 구현에서 웹 SDK으로 이동하는 경우 이 필드는 `trackingServerSecure`(또는 `trackingServer`)에 포함된 동일한 값을 사용할 수 있습니다.

## Edge 도메인 수동으로 웹 SDK 구현

[`edgeDomain`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR)을(를) 사용하여 SDK을 구성하십시오. 필드는 데이터를 보낼 도메인을 결정하는 문자열입니다.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## Adobe Analytics 확장을 사용한 SSL 추적 서버

[!UICONTROL SSL 추적 서버]는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 일반] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
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
