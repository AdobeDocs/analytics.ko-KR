---
title: trackingServerSecure
description: HTTPS 페이지에서 이미지 요청이 전송되는 위치를 파악합니다.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 100%

---


# trackingServerSecure

Adobe는 방문자가 생성한 이미지 요청을 수신하여 사이트의 데이터를 수집합니다. `trackingServerSecure` 변수는 HTTPS 페이지에서 이미지 요청이 전송되는 위치를 파악합니다. 또한 방문자 쿠키가 저장되어 있는 위치도 파악합니다. 이 변수가 올바르게 정의되지 않으면 구현에서 데이터 손실이 발생할 수 있습니다.

>[!IMPORTANT]
>
>이 값을 변경하면 AppMeasurement가 다른 위치에서 쿠키를 찾습니다. 방문자 쿠키가 새 위치에 설정되면 보고에서 고유 방문자 수가 일시적으로 급증할 수 있습니다.

## Adobe Experience Platform Launch의 SSL 추적 서버

[!UICONTROL SSL 추적 서버]는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 일반] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
4. [!UICONTROL 일반] 아코디언을 확장합니다. 그러면 [!UICONTROL SSL 추적 서버] 필드가 표시됩니다.

이 필드를 비워 두면 기본값은 [`trackingServer`](trackingserver.md) 변수의 값으로 설정됩니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.trackingServerSecure

`s.trackingServerSecure` 변수는 이미지 요청을 보낼 위치를 포함하는 문자열입니다. 거의 항상 사이트의 하위 도메인입니다. 브라우저의 최신 개인 정보 보호 정책은 일반적으로 타사 쿠키를 신뢰할 수 없게 합니다. 이 변수가 비어 있으면 `s.trackingServer` 변수의 값을 사용합니다.

이 변수의 값은 거의 항상 `data.example.com`과 같은 자사 도메인입니다. 자사 쿠키 프로세스에 대한 자세한 내용은 핵심 서비스 사용 안내서에서 [Experience Cloud의 자사 쿠키](https://docs.adobe.com/content/help/ko-KR/core-services/interface/ec-cookies/cookies-first-party.html)를 참조하십시오.

처음 자사 쿠키 구현을 구성하는 개인은 사용하는 도메인과 하위 도메인도 정의합니다. 예:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME 레코드는 일반적으로 `ssl.d1.sc.omtrdc.net`의 하위 도메인을 가리킵니다.
