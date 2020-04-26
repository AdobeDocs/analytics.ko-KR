---
title: visitorNameSpace
description: 쿠키 도메인을 결정하던 폐기된 변수입니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# visitorNamespace

>[!IMPORTANT] 이 변수는 사용이 중단되었습니다. 대신 [`trackingServer`](trackingserver.md)를 사용하십시오.

이전 Adobe Analytics 버전에서 AppMeasurement는 `visitorNameSpace` 변수를 사용하여 방문자 쿠키가 저장된 `2o7.net`의 하위 도메인을 파악했습니다. 최신 브라우저에서 개인 정보 보호 정책을 강화하면 타사 쿠키의 신뢰성이 떨어집니다. `trackingServer` 및 [`trackingServerSecure`](trackingserversecure.md) 변수를 도입하면 `visitorNameSpace`가 더 이상 필요하지 않습니다.

>[!TIP] 사이트에서는 자사 쿠키를 사용하는 것이 좋습니다. 자사 쿠키는 이 변수를 사용하지 않습니다.

## Adobe Experience Platform Launch의 방문자 네임스페이스

[!UICONTROL 방문자 네임스페이스]는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 쿠키] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
4. [!UICONTROL 쿠키] 아코디언을 확장합니다. 그러면 [!UICONTROL 방문자 네임스페이스] 필드가 표시됩니다.

이 필드는 사용하지 않는 것이 좋습니다. 대신 `trackingServer` 및 `trackingServerSecure`를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.visitorNamespace

`s.visitorNamespace` 변수는 조직에 대한 고유한 값을 포함하는 문자열입니다. 이전 버전의 Adobe Analytics에서 다운로드할 때 이전 AppMeasurement 라이브러리에서는 이 고유 값을 자동으로 포함했습니다. 현재 AppMeasurement 라이브러리에서는 `trackingServer` 및 `trackingServerSecure`가 설정되어 있는 한 이 변수를 사용하지 않습니다.

조직에서 여전히 이 변수를 필요로 한다면, 조직을 나타내는 값을 선택하십시오. 이 값은 [솔루션 디자인 문서](../../prepare/solution-design.md)에 저장할 수 있습니다.

```js
// If trackingServer is not set, cookies are stored under example.112.2o7.net
s.visitorNameSpace = "example";
```
