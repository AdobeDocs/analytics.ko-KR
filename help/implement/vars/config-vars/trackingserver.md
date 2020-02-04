---
title: trackingServer
description: 위치 이미지 요청이 전송되었는지 확인합니다.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# trackingServer

Adobe는 방문자가 생성한 이미지 요청을 수신하여 사이트의 데이터를 수집합니다. 이 `trackingServer` 변수는 이미지 요청이 전송되는 위치를 결정합니다. 이 변수가 올바르게 정의되지 않은 경우 구현에서 데이터 손실을 경험할 수 있습니다.

> [!IMPORTANT] 이 값을 변경하면 AppMeasurement가 다른 위치에서 쿠키를 찾습니다. 방문자 쿠키가 새 위치에 설정되면 고유 방문자 수가 일시적으로 보고서에서 급증할 수 있습니다.

## Adobe Experience Platform Launch의 추적 서버

추적 서버는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 일반] 아코디언 아래의 필드입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 확장 [!UICONTROL 탭으로 이동한] 다음 Adobe [!UICONTROL Analytics에서 구성] 단추를 클릭합니다.
4. [추적 [!UICONTROL 서버] ] [!UICONTROL 필드를 표시하는 [일반] 아코디언을] 확장합니다.

이 필드를 비워 두면 기본값이 로 `[rsid].112.2o7.net`설정됩니다.

## s.trackingServer in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.trackingServer` 변수는 데이터를 보낼 위치를 포함하는 문자열입니다.

> [!TIP] 일부 구현은 데이터를 `2o7.net`가리킵니다. 유효한 데이터 수집 도메인이지만 지역 데이터 수집은 사용하지 않습니다. 이미지를 사용한 구현은 이미지 요청 응답 시간이 약간 더 `2o7.net` 높습니다.

## trackingServer의 값 확인

이 변수의 값은 퍼스트 파티 쿠키 또는 타사 쿠키를 사용하는지에 따라 달라집니다. 구현에서 퍼스트 파티 쿠키를 사용하는 것이 좋습니다.

### 자사 쿠키

퍼스트 파티 쿠키 구현을 사용하는 경우 조직의 누군가가 이미 퍼스트 파티 쿠키 프로세스를 완료했을 수 있습니다. 퍼스트 [파티 쿠키 프로세스에 대한 자세한 내용은](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html) 핵심 서비스 사용 안내서의 Experience Cloud의 퍼스트 파티 쿠키를 참조하십시오.

퍼스트 파티 쿠키 구현을 처음에 구성하는 개인 역시 사용된 도메인과 하위 도메인을 정의합니다. 예:

```js
s.trackingServer = "data.example.com";
```

일반적으로 CNAME 레코드는 이미 설정되고 `sc.omtrdc.net`가리키게 됩니다. 도메인도 `2o7.net` 유효한 CNAME 대상이며, 주로 이전 버전의 Adobe Analytics에서 사용됩니다.

### 타사 쿠키

> [!TIP] 최신 브라우저에서 개인 정보 보호 정책을 강화하면 타사 쿠키의 신뢰성이 떨어집니다. 퍼스트 파티 쿠키 워크플로우에 따라 설정하는 것이 좋습니다.

타사 쿠키 구현을 사용하는 경우 의 값은 `trackingServer` 의 하위 도메인입니다 `sc.omtrdc.net`. 예:

```js
s.trackingServer = "example.sc.omtrdc.net";
```

Adobe Analytics를 사용하는 다른 조직에서 선택할 가능성이 없는 조직 고유의 하위 도메인을 선택하십시오. 조직의 모든 구현에서 동일한 추적 서버를 사용해야 합니다. 이 정보는 [솔루션 디자인 문서에서](../../prepare/solution-design.md)유지하는 데 도움이 될 수 있습니다.
