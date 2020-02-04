---
title: trackingServerSecure
description: 위치 이미지 요청이 HTTPS 페이지에서 전송되었는지 확인합니다.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# trackingServerSecure

Adobe는 방문자가 생성한 이미지 요청을 수신하여 사이트의 데이터를 수집합니다. 이 `trackingServerSecure` 변수는 HTTPS를 통해 이미지 요청이 전송되는 위치를 결정합니다. 또한 위치 방문자 쿠키가 저장되어 있는지 결정합니다. 이 변수가 올바르게 정의되지 않은 경우 구현에서 데이터 손실을 경험할 수 있습니다.

> [!IMPORTANT] 이 값을 변경하면 AppMeasurement가 다른 위치에서 쿠키를 찾습니다. 방문자 쿠키가 새 위치에 설정되면 고유 방문자 수가 일시적으로 보고서에서 급증할 수 있습니다.

## Adobe Experience Platform Launch의 SSL 추적 서버

[!UICONTROL SSL 추적] 서버는 Adobe Analytics [!UICONTROL 확장을 구성할 때] 일반 아코디언 아래에 있는 필드입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 확장 [!UICONTROL 탭으로 이동한] 다음 Adobe [!UICONTROL Analytics에서 구성] 단추를 클릭합니다.
4. [ [!UICONTROL SSL 추적 서버] ] [!UICONTROL 필드를 표시하는 [일반] 아코디언을] 확장합니다.

이 필드를 비워 두면 `trackingServer` 변수의 값이 기본값으로 설정됩니다.

## s.trackingServerSecure in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.trackingServerSecure` 변수는 이미지 요청을 보낼 위치를 포함하는 문자열입니다. 거의 항상 사이트의 하위 도메인입니다. 브라우저의 최신 개인 정보 보호 정책은 일반적으로 서드 파티 쿠키를 신뢰할 수 없게 합니다. 이 변수가 비어 있으면 `s.trackingServer` 변수의 값을 사용합니다.

이 변수의 값은 거의 항상 퍼스트 파티 도메인과 같은 `data.example.com`것입니다. 퍼스트 [파티 쿠키 프로세스에 대한 자세한 내용은](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html) 핵심 서비스 사용 안내서의 Experience Cloud의 퍼스트 파티 쿠키를 참조하십시오.

퍼스트 파티 쿠키 구현을 처음에 구성하는 개인 역시 사용된 도메인과 하위 도메인을 정의합니다. 예:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME 레코드는 일반적으로 하위 도메인을 `ssl.d1.sc.omtrdc.net`가리킵니다.
