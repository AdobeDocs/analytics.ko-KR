---
title: trackingServer
description: 이미지 요청이 전송되는 위치를 파악합니다.
exl-id: bcc23286-4dd5-45ac-ac6f-7b60e95cb798
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '398'
ht-degree: 100%

---

# trackingServer

Adobe는 방문자가 생성한 이미지 요청을 수신하여 사이트의 데이터를 수집합니다. `trackingServer` 변수는 이미지 요청이 전송되는 위치를 파악합니다. 이 변수가 올바르게 정의되지 않으면 구현에서 데이터 손실이 발생할 수 있습니다.

>[!IMPORTANT]
>
>이 값을 변경하면 AppMeasurement가 다른 위치에서 쿠키를 찾습니다. 방문자 쿠키가 새 위치에 설정되면 보고에서 고유 방문자 수가 일시적으로 급증할 수 있습니다.

## Adobe Experience Platform Launch의 추적 서버

추적 서버는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 일반] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
4. [!UICONTROL 일반] 아코디언을 확장합니다. 그러면 [!UICONTROL 추적 서버] 필드가 표시됩니다.

이 필드를 비워 두면 기본값은 `[rsid].data.adobedc.net`로 설정됩니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.trackingServer

`s.trackingServer` 변수는 데이터를 보낼 위치를 포함하는 문자열입니다.

## trackingServer의 값 확인

이 변수의 값은 자사 쿠키를 사용하는지 또는 서드파티 쿠키를 사용하는지에 따라 달라집니다. 여러분의 구현에서는 자사 쿠키를 사용하는 것이 좋습니다.

### 자사 쿠키

자사 쿠키 구현을 사용하는 경우 조직의 누군가가 이미 자사 쿠키 프로세스를 완료했을 수 있습니다. 자사 쿠키 프로세스에 대한 자세한 내용은 핵심 서비스 사용 안내서에서 [Experience Cloud의 자사 쿠키](https://docs.adobe.com/content/help/ko-KR/core-services/interface/ec-cookies/cookies-first-party.html)를 참조하십시오.

처음 자사 쿠키 구현을 구성하는 개인은 사용하는 도메인과 하위 도메인도 정의합니다. 예:

```js
s.trackingServer = "data.example.com";
```

### 서드파티 쿠키

>[!TIP]
>
>최신 브라우저에서 개인 정보 보호 정책을 강화하면 서드파티 쿠키의 신뢰성이 떨어집니다. 자사 쿠키 워크플로에 따라 설정하는 것이 좋습니다.

서드파티 쿠키 구현을 사용하는 경우 `trackingServer`의 값은 `data.adobedc.net`의 하위 도메인입니다.  예:

```js
s.trackingServer = "example.data.adobedc.net";
```

Adobe Analytics를 사용하는 다른 조직에서 선택할 가능성이 없고 조직에 고유한 하위 도메인을 선택하십시오.  조직에 할당된 방문자 네임스페이스가 권장됩니다.  조직의 모든 구현에서 동일한 추적 서버를 사용하도록 합니다. 이렇게 하면 [솔루션 디자인 문서](../../prepare/solution-design.md)에서 이 정보를 유지하는 데 도움이 될 수 있습니다.

조직이 이미 `sc.omtrdc.net` 또는 `2o7.net` 도메인에서 서드파티 추적 서버를 사용하고 있을 수 있습니다.  이 도메인들은 주로 이전 버전의 Adobe Analytics에서 사용되었으며 여전히 유효합니다.

>[!NOTE]
>
> `example.data.adobedc.net`보다 더 아래의 하위 도메인은 사용하지 마십시오. 예를 들어 `custom.example.data.adobedc.net`은 올바른 추적 서버가 아닙니다.
