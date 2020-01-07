---
title: useBeacon
description: useBeacon을 사용하면 AppMeasurement에서 브라우저 sendBeacon API를 사용하도록 할 수 있습니다.
keywords: Analytics Implementation
translation-type: ht
source-git-commit: 6c57780d0ecf65669c1a5306dde267f6e48f1cc4

---


# s.useBeacon

이 `s.useBeacon` 변수는 그 다음 요청에서 브라우저의 [sendBeacon API](https://developer.mozilla.org/ko-KR/docs/Web/API/Navigator/sendBeacon)를 사용하도록 강제합니다. `s.sendBeacon`을 사용하면 HTTP 요청을 페이지의 컨텍스트 외부로 보낼 수 있습니다. 페이지를 언로드하기 전에 정보를 전송하려는 종료 링크 및 기타 상황에 유용합니다.

이 값을 설정하면 AppMeasurement가 실행되는 그 다음 요청에만 적용됩니다. 요청이 실행되면, `s.useBeacon`이 false로 재설정됩니다. 이 변수는 `s.t()` 및 `s.tl()` 이미지 요청 모두에 적용됩니다.

`s.useBeacon` 변수를 사용하려면 AppMeasurement 2.17.0 이상이 필요합니다.

> [!NOTE] [종료 링크](s-linktrackvars.md)는 추가적인 구성 없이 이 변수를 자동으로 사용합니다.

## 구문

```js
s.useBeacon = true;
```
