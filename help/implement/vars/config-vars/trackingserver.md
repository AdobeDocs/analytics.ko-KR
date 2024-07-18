---
title: trackingServer
description: 이미지 요청이 전송되는 위치를 파악합니다.
feature: Variables
exl-id: bcc23286-4dd5-45ac-ac6f-7b60e95cb798
role: Admin, Developer
source-git-commit: 284f121428ce9d682b42309dd85cfd117285a7e5
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 52%

---

# trackingServer

Adobe는 방문자가 생성한 이미지 요청을 수신하여 사이트의 데이터를 수집합니다. `trackingServer` 변수는 이미지 요청이 전송되는 위치를 파악합니다. 이 변수가 올바르게 정의되지 않으면 구현에서 데이터 손실이 발생할 수 있습니다.

>[!WARNING]
>
>이 값을 변경하면 AppMeasurement가 다른 위치에서 쿠키를 찾습니다. 방문자 쿠키가 새 위치에 설정되면 보고에서 고유 방문자 수가 일시적으로 급증할 수 있습니다.

## 웹 SDK 확장을 사용한 Edge 도메인

Web SDK는 [!UICONTROL Edge 도메인]을 사용하여 추적 서버와 보안 추적 서버를 모두 처리합니다. Web SDK 확장을 구성할 때 원하는 [!UICONTROL Edge 도메인] 값을 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음 [!UICONTROL Adobe Experience Platform Web SDK] 아래의 **[!UICONTROL 구성]** 단추를 클릭합니다.
1. 원하는 **[!UICONTROL Edge 도메인]** 텍스트 필드를 설정합니다.

자세한 내용은 웹 SDK 설명서의 [Adobe Experience Platform 웹 SDK 확장 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=ko-KR)을 참조하십시오.

>[!TIP]
>
>조직이 AppMeasurement 또는 Analytics 확장 구현에서 웹 SDK로 이동하는 경우 이 필드는 `trackingServerSecure`(또는 `trackingServer`)에 포함된 동일한 값을 사용할 수 있습니다.

## Edge 도메인 수동으로 웹 SDK 구현

[`edgeDomain`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR)을(를) 사용하여 SDK를 구성합니다. 필드는 데이터를 보낼 도메인을 결정하는 문자열입니다.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## Adobe Analytics 확장을 사용한 추적 서버

추적 서버는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 일반] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
4. [!UICONTROL 일반] 아코디언을 확장합니다. 그러면 [!UICONTROL 추적 서버] 필드가 표시됩니다.

이 필드를 비워 두면 기본값은 `[rsid].data.adobedc.net`로 설정됩니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.trackingServer

`s.trackingServer` 변수는 데이터를 보낼 위치를 포함하는 문자열입니다.

## `trackingServer`의 값을 결정하기 위한 고려 사항

Adobe의 추적 서버 도메인(예: `adobedc.net`)을 사용하도록 선택하거나 특수 프로세스를 통해 사이트 도메인(예: `data.mydomain.com`)과 일치하는 추적 서버를 설정할 수 있습니다(CNAME 구현이라고도 함). 사이트 도메인과 일치하는 추적 서버가 있으면 구현의 다른 측면에 따라 몇 가지 이점이 있을 수 있습니다. 추적 서버가 현재 페이지의 도메인과 일치하지 않으면, AppMeasurement에서 설정한 쿠키를 서드파티로 설정해야 합니다. 브라우저가 서드파티 쿠키를 지원하지 않는 경우 이러한 불일치는 특정 Analytics 기능을 방해할 수 있습니다.

- 식별자 설정: Experience Cloud ID 서비스를 사용하는 경우 추적 서버는 쿠키가 설정되는 방식에 영향을 주지 않습니다. 그러나 Analytics 레거시 식별자(`s_vi` 쿠키)를 사용하고 있고 수집 서버가 현재 도메인과 일치하지 않으면 쿠키를 서드파티로 설정해야 합니다. 이 경우 서드파티 쿠키가 브라우저에 의해 차단되면 Analytics는 표준 `s_vi` 쿠키 대신 자사 대체 ID(`s_fid`)를 설정합니다.
- 링크 추적은 내부 링크에 대해 작동하지 않습니다.
- Activity Map은 내부 링크에 대해 작동하지 않습니다.
- 쿠키 확인.

### 자사 쿠키

자사 쿠키 구현을 사용하는 경우 조직의 누군가가 이미 자사 쿠키 프로세스를 완료했을 수 있습니다. 자사 쿠키 프로세스에 대한 자세한 내용은 핵심 서비스 사용 안내서에서 [Experience Cloud의 자사 쿠키](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=ko-KR)를 참조하십시오.

처음 자사 쿠키 구현을 구성하는 개인은 사용하는 도메인과 하위 도메인도 정의합니다. 예:

```js
s.trackingServer = "data.example.com";
```

### 서드파티 추적 서버

>[!TIP]
>
>최신 브라우저에서 개인정보 보호정책을 강화하면 서드파티 쿠키의 신뢰성이 떨어집니다. 자사 쿠키 워크플로에 따라 설정하는 것이 좋습니다.

서드파티 쿠키 구현을 사용하는 경우 `trackingServer`의 값은 `data.adobedc.net`의 하위 도메인입니다. 예:

```js
s.trackingServer = "example.data.adobedc.net";
```

Adobe Analytics를 사용하는 다른 조직에서 선택할 가능성이 없고 조직에 고유한 하위 도메인을 선택하십시오.  조직에 할당된 방문자 네임스페이스가 권장됩니다.  조직의 모든 구현에서 동일한 추적 서버를 사용하도록 합니다. 이렇게 하면 [솔루션 디자인 문서](../../prepare/solution-design.md)에서 이 정보를 유지하는 데 도움이 될 수 있습니다.

조직이 이미 `sc.omtrdc.net` 또는 `2o7.net` 도메인에서 서드파티 추적 서버를 사용하고 있을 수 있습니다.  이 도메인들은 주로 이전 버전의 Adobe Analytics에서 사용되었으며 여전히 유효합니다.

>[!NOTE]
>
>`example.data.adobedc.net`보다 더 아래의 하위 도메인은 사용하지 마십시오. 예를 들어 `custom.example.data.adobedc.net`은 올바른 추적 서버가 아닙니다.
