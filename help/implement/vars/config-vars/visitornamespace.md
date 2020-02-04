---
title: visitorNameSpace
description: 쿠키 도메인을 결정한 폐기 변수.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# visitorNamespace

> [!IMPORTANT] 이 변수는 사용이 중단되었습니다. 대신 `trackingServer` 사용하십시오.

이전 버전의 Adobe Analytics에서 AppMeasurement는 이 `visitorNameSpace` 변수를 사용하여 방문자 쿠키가 저장된 `2o7.net` 하위 도메인을 파악했습니다.  최신 브라우저에서 개인 정보 보호 정책을 강화하면 타사 쿠키의 신뢰성이 떨어집니다. 변수 `trackingServer` 및 `trackingServerSecure` 변수가 도입되면 `visitorNameSpace` 더 이상 필요하지 않습니다.

> [!TIP] 사이트에서 퍼스트 파티 쿠키를 사용하는 것이 좋습니다. 퍼스트 파티 쿠키는 이 변수를 사용하지 않습니다.

## Adobe Experience Platform 론치의 방문자 네임스페이스

[!UICONTROL 방문자] 네임스페이스는 Adobe Analytics [!UICONTROL 확장을 구성할 때 쿠키] 아코디언 아래에 있는 필드입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 확장 [!UICONTROL 탭으로 이동한] 다음 Adobe [!UICONTROL Analytics에서 구성] 단추를 클릭합니다.
4. [ [!UICONTROL 방문자 네임스페이스] ] [!UICONTROL 필드를 표시하는 쿠키] 아코디언을 확장합니다.

Adobe는 이 필드를 사용하지 않도록 권장합니다. 를 `trackingServer` `trackingServerSecure` 대신 사용하십시오.

## s.visitorNamespace in AppMeasurement and Launch custom code editor

이 `s.visitorNamespace` 변수는 조직당 고유한 값을 포함하는 문자열입니다. 이전 버전의 Adobe Analytics에서 다운로드할 때 이전 AppMeasurement 라이브러리에는 이 고유 값이 자동으로 포함되었습니다. 현재 AppMeasurement 라이브러리는 설정되지 `trackingServer` 않은 경우 이 변수를 사용하지 `trackingServerSecure` 않습니다.

조직에서 여전히 이 변수를 필요로 하는 경우, 조직을 나타내는 값을 선택하십시오. 이 값을 [솔루션 디자인 문서에](../../prepare/solution-design.md)저장할 수 있습니다.

```js
// If trackingServer is not set, cookies are stored under example.112.2o7.net
s.visitorNameSpace = "example";
```
