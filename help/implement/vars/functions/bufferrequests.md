---
title: bufferRequests
description: 페이지를 즉시 언로드하는 브라우저에 대한 링크 추적 요청 캡처의 안정성을 향상시킵니다.
feature: Appmeasurement Implementation
exl-id: f103deb4-f449-4325-b1a0-23e58a3c9ba0
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 6%

---

# bufferRequests

`bufferRequests()` 메서드를 사용하면 이미지 요청을 Adobe으로 보내는 대신 현재 페이지에서 캐시할 수 있습니다. 이 메서드를 트리거하는 것은 브라우저가 [`navigator.sendBeacon()`](https://developer.mozilla.org/ko-KR/docs/Web/API/Navigator/sendBeacon)을(를) 지원하지 않거나 페이지를 언로드할 때 이미지 요청을 취소하는 시나리오에서 유용합니다. Safari와 같은 많은 버전의 WebKit 브라우저는 일반적으로 링크를 클릭할 때 이미지 요청을 중지하는 동작을 보여 줍니다. `bufferRequests()` 메서드는 모든 버전의 AppMeasurement v2.25.0 이상에서 사용할 수 있습니다.

동일한 브라우저 세션의 후속 페이지에서 [`t()`](t-method.md) 또는 [`tl()`](tl-method.md)을(를) 호출했지만 해당 페이지에서 `bufferRequests()`이(가) 아직 호출되지 않은 경우 해당 페이지의 이미지 요청과 함께 모든 버퍼된 요청이 전송됩니다. 버퍼된 요청은 현재 페이지의 이미지 요청이 마지막으로 전송되는 올바른 순서로 전송됩니다.

>[!TIP]
>
>버퍼된 요청의 타임스탬프는 데이터가 전송되는 페이지와 공유됩니다. 버퍼된 요청이 기록되는 정확한 시간 내에 더 정밀하게 하려면 요청을 버퍼링하기 전에 [`timestamp`](../page-vars/timestamp.md) 페이지 변수를 설정할 수 있습니다. 이 변수를 사용하는 경우 [타임스탬프 선택 사항](/help/technotes/timestamps-optional.md)이 활성화되어 있는지 확인하십시오. 그렇지 않으면 타임스탬프가 지정된 모든 히트가 영구적으로 손실됩니다.

## 제한 사항

`bufferRequests()` 메서드를 호출할 때는 다음 제한 사항에 유의하십시오. 이 메서드는 [`Window.sessionStorage`](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API)을(를) 사용하므로 다음과 같은 제한 사항이 많이 적용됩니다.

* 대상 링크는 동일한 도메인과 하위 도메인에 있어야 합니다. 버퍼된 요청은 도메인 또는 하위 도메인 간에 동일하게 Adobe Analytics 구현이 있더라도 작동하지 않습니다. 또한 이 제한은 버퍼된 요청을 사용하여 종료 링크를 추적할 수 없음을 의미합니다.
* 대상 링크는 현재 페이지와 동일한 프로토콜을 사용해야 합니다. HTTP와 HTTPS 간에는 버퍼된 요청을 보낼 수 없습니다.
* 버퍼된 요청은 `bufferRequests()`을(를) 먼저 호출하지 않고 `t()` 또는 `tl()`을(를) 호출하거나 브라우저나 탭을 닫을 때까지 저장됩니다. 해당 데이터를 Adobe으로 보내기 전에 브라우저 세션이 종료되면 전송되지 않은 버퍼된 요청이 영구적으로 손실됩니다.
* 브라우저가 [웹 저장소 API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) 또는 [JSON API](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON)을(를) 지원하지 않는 경우 브라우저 콘솔에 경고가 출력되고 AppMeasurement은 `t()` 메서드를 사용하여 이미지 요청을 즉시 전송하려고 시도합니다.

## 웹 SDK의 버퍼된 요청

웹 SDK은 현재 요청을 버퍼링하는 기능을 제공하지 않습니다.

## Adobe Analytics 확장을 사용한 버퍼된 요청

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.bufferRequests()

`t()` 또는 `tl()`을(를) 호출하기 전에 `bufferRequests()` 메서드를 호출하십시오. `bufferRequests()`이(가) 호출되면 후속 추적 호출이 Adobe 데이터 수집 서버로 전송되는 대신 세션 저장소에 기록됩니다.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// Flag the request to be buffered
s.bufferRequests();

// The t() or tl() method then writes the data to session storage instead of sending it to Adobe
s.tl(true,"o","Example link click");

// On a subsequent page, the tracking call sends both the above link tracking call and the page view call
s.t();
```
