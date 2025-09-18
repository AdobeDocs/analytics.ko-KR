---
title: trackingServerSecure
description: HTTPS를 통해 Adobe으로 데이터를 전송하는 데 사용되는 도메인.
feature: Appmeasurement Implementation
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
role: Admin, Developer
source-git-commit: 7918b18e73618368543a996ca121b64b7afb33ab
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 13%

---

# trackingServerSecure

`trackingServerSecure` 변수는 AppMeasurement이 HTTPS를 통해 Adobe으로 데이터를 전송하는 데 사용하는 도메인을 결정합니다. 이 변수가 올바르게 정의되지 않으면 구현에서 데이터 손실이 발생할 수 있습니다.

[Adobe Experience Cloud Identity 서비스](https://experienceleague.adobe.com/ko/docs/id-service/using/home) 이전에 이 변수는 타사 쿠키가 설정된 위치도 확인했습니다. Adobe은 가능한 모든 구현에서 ID 서비스를 사용하는 것이 좋습니다.

## Web SDK 확장을 사용한 Edge 도메인

웹 SDK은 [!UICONTROL Edge 도메인]을 사용하여 추적 서버와 보안 추적 서버를 모두 처리합니다. Web SDK 확장을 구성할 때 원하는 [!UICONTROL Edge 도메인] 값을 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 선택합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음 **[!UICONTROL Adobe Experience Platform Web SDK]**&#x200B;에서 [!UICONTROL 구성] 단추를 선택합니다.
1. 원하는 **[!UICONTROL Edge 도메인]** 텍스트 필드를 설정합니다.

자세한 내용은 웹 SDK 설명서의 [Adobe Experience Platform Web SDK 확장 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=ko-KR)을 참조하십시오.

>[!TIP]
>
>조직이 AppMeasurement 또는 Analytics 확장 구현에서 웹 SDK으로 이동하는 경우 이 필드는 `trackingServerSecure`(또는 `trackingServer`)에 포함된 동일한 값을 사용할 수 있습니다.

## Edge 도메인 수동으로 웹 SDK 구현

[`edgeDomain`](https://experienceleague.adobe.com/ko/docs/experience-platform/web-sdk/commands/configure/edgedomain)을(를) 사용하여 SDK을 구성하십시오. 필드는 데이터를 보낼 도메인을 결정하는 문자열입니다.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## Adobe Analytics 확장을 사용한 SSL 추적 서버

[!UICONTROL SSL 추적 서버]는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 일반] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 선택합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음 Adobe Analytics 아래의 **[!UICONTROL 구성]** 단추를 선택합니다.
1. [!UICONTROL 일반] 아코디언을 확장합니다. 그러면 [!UICONTROL SSL 추적 서버] 필드가 표시됩니다.

이 필드를 비워 두면 기본값은 [!UICONTROL 추적 서버]의 값으로 설정됩니다. [!UICONTROL SSL 추적 서버]와 [!UICONTROL 추적 서버]가 모두 비어 있으면 기본값은 `[rsid].data.adobedc.net`입니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.trackingServerSecure

`s.trackingServerSecure` 변수는 Adobe으로 데이터를 보낼 도메인을 포함하는 문자열입니다. 이는 도메인에만 해당되며, 프로토콜, 경로, 포트 및 슬래시를 생략합니다. 이 변수가 비어 있으면 `s.trackingServer` 변수의 값을 사용합니다. `s.trackingServerSecure`과(와) `s.trackingServer`이(가) 모두 비어 있으면 기본값은 `[rsid].2o7.net`입니다.

```js
// Example value when participating in the Adobe-managed certificate program
s.trackingServerSecure = "data.example.com";

// Example value sending data directly to Adobe
s.trackingServerSecure = "example.data.adobedc.net";
```

## `trackingServerSecure`의 값을 결정할 때 고려 사항

`trackingServerSecure`(또는 `edgeDomain`)에 사용하는 값은 여러 요인에 따라 다릅니다.

* [Adobe 관리 인증서 프로그램](https://experienceleague.adobe.com/ko/docs/core-services/interface/data-collection/adobe-managed-cert)에 참여
* [Adobe Experience Cloud ID 서비스](https://experienceleague.adobe.com/ko/docs/id-service/using/home)를 구현하고 올바르게 설정한 경우

**조직에서 Adobe 관리 인증서 프로그램에 참여하는 경우** 값을 인증서를 설정할 때 선택한 자사 도메인으로 설정하십시오. 일반적으로 이 값은 조직이 소유한 하위 도메인입니다. 예, `data.example.com`. 조직의 CNAME 레코드는 해당 데이터를 Adobe으로 리디렉션합니다.

**인증서 프로그램에 참여하지 않는 경우** 값을 `data.adobedc.net`의 하위 도메인으로 설정하십시오. Adobe에서는 일관성을 유지하기 위해 조직의 회사 ID를 사용하는 것이 좋습니다. 예, `example.data.adobedc.net`. 회사 ID를 확인하려면 다음 단계를 수행하십시오.

1. Adobe ID 자격 증명을 사용하여 [experience.adobe.com](https://experience.adobe.com)에 로그인합니다.
1. Experience Cloud 인터페이스의 모든 곳에서 `[Cmd]` + `[I]`(iOS) 또는 `[Ctrl]` + `[I]`(Windows)을 누릅니다.
1. **[!UICONTROL 사용자 데이터 디버거]**&#x200B;가 나타납니다. **[!UICONTROL 할당된 조직]** 탭을 선택합니다.
1. 원하는 IMS 조직을 확장합니다.
1. **[!UICONTROL 테넌트]** 필드를 찾습니다. 이 값은 `data.adobedc.net`의 권장 하위 도메인입니다.

>[!NOTE]
>
>`example.data.adobedc.net`보다 더 아래의 하위 도메인은 사용하지 마십시오. 예를 들어 `custom.example.data.adobedc.net`은 올바른 추적 서버가 아닙니다.

이전 구현에는 `sc.omtrdc.net` 또는 `2o7.net` 같은 값이 있을 수 있습니다. 이 도메인들은 주로 이전 버전의 Adobe Analytics에서 사용되었으며 여전히 유효합니다.

Adobe은 조직 전체에서 일관성을 유지하기 위해 [솔루션 디자인 문서](../../prepare/solution-design.md)에서 이 정보를 유지할 것을 적극 권장합니다.

## 방문자 ID 서비스를 사용하지 않을 경우의 결과

Adobe은 모든 구현에서 [Adobe Experience Cloud ID 서비스](https://experienceleague.adobe.com/ko/docs/id-service/using/home)를 사용할 것을 강력히 권장합니다. ID 서비스는 다음과 같은 여러 가지 방법으로 구현할 수 있습니다.

* 수동 AppMeasurement 구현에서는 `VisitorAPI.js`을(를) 사용하고 `getInstance` 메서드를 호출합니다. 자세한 내용은 [Analytics용 Experience Cloud Identity 서비스 구현](https://experienceleague.adobe.com/ko/docs/id-service/using/implementation/setup-analytics)을 참조하십시오.
* Adobe Analytics 태그 확장을 사용하는 구현은 [Adobe Experience Cloud ID 서비스 태그 확장](https://experienceleague.adobe.com/ko/docs/experience-platform/tags/extensions/client/id-service/overview)을 사용합니다. 추가되면 추가 구성이 필요하지 않습니다.
* 모든 형식의 웹 SDK(`alloy.js` 또는 Web SDK 태그 확장)를 사용하는 구현에는 기본적으로 ID 서비스가 활성화되어 있습니다. `edgeDomain` 값을 설정하는 외에 구성이 필요하지 않습니다.

**구현에서 ID 서비스를 사용하지 않는 경우** 구현에 미치는 영향을 고려하십시오.

* ID 서비스를 사용하지 않는 경우 `trackingServerSecure`이(가) 쿠키 위치를 결정합니다. 이 변수를 타사 도메인으로 설정하면 대부분의 최신 브라우저가 타사 쿠키를 거부하므로 AppMeasurement은 대체 쿠키를 사용해야 합니다.
* 내부 링크 추적 및 Activity Map의 신뢰성이 떨어질 수 있습니다.
