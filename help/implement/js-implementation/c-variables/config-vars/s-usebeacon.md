---
title: useBeacon
description: useBeacon을 사용하면 AppMeasurement가 브라우저 sendBeacon API를 사용하도록 할 수 있습니다
keywords: Analytics 구현
seo-description: useBeacon을 사용하면 AppMeasurement가 브라우저 sendBeacon API를 사용하도록 할 수 있습니다
translation-type: tm+mt
source-git-commit: f89d909e539cee2b78798c165fcb405773418056

---


# s.useBeacon

이 `s.useBeacon` 변수는 다음 요청에서 브라우저의 sendBeacon API를 사용하도록 [합니다](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/sendBeacon). 을 `s.sendBeacon` 사용하면 HTTP 요청을 페이지의 컨텍스트 외부로 보낼 수 있습니다. 페이지를 언로드하기 전에 정보를 전송하려는 종료 링크 및 기타 상황에 유용합니다.

이 값을 설정하면 AppMeasurement가 실행되는 다음 요청에만 적용됩니다. 요청이 실행되면, `s.useBeacon` false로 재설정됩니다. 이 변수는 `s.t()` 및 `s.tl()` 이미지 요청 모두에 적용됩니다.

이 `s.useBeacon` 변수를 사용하려면 AppMeasurement 2.17.0 이상이 필요합니다.

> [!NOTE] ExitLinks [는](s-linktrackvars.md) 추가 구성 없이 이 변수를 자동으로 사용합니다.

## 구문

```js
s.useBeacon = true;
```
