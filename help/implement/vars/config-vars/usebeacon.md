---
title: useBeacon
description: useBeacon을 사용하면 AppMeasurement에서 브라우저 sendBeacon API를 사용하도록 할 수 있습니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# useBeacon

대부분의 최신 브라우저에는 기본 방법이 포함되어 `navigator.sendBeacon()`있습니다. HTTP를 통해 적은 양의 데이터를 웹 서버로 비동기식으로 전송합니다. AppMeasurement는 `navigator.sendBeacon()` `useBeacon` 변수가 활성화된 경우 이 메서드를 사용할 수 있습니다. 이 기능은 종료 링크 및 페이지를 언로드하기 전에 정보를 전송하려는 기타 상황에 유용합니다.

이 `useBeacon` 활성화되면 Adobe로 전송된 다음 히트는 표준 `navigator.sendBeacon()` 이미지 요청 대신 브라우저의 `GET` 방법을 사용합니다. 이 변수는 [`s.t()`](../functions/t-method.md) 및 [`s.tl()`](../functions/tl-method.md) 이미지 요청 모두에 적용됩니다. AppMeasurement 2.17.0 이상이 필요합니다.

> [!TIP] AppMeasurement는 종료 링크 이미지 요청을 자동으로 `useBeacon` 활성화합니다.

방문자가 지원하지 않는 브라우저를 사용하면 `useBeacon` 변수가 무시됩니다 `navigator.sendBeacon()`. 이 변수를 사용하려면 AppMeasurement 2.16.0 이상이 필요합니다.

## Adobe Experience Platform Launch에서 비콘 사용

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## s.useBeacon in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.useBeacon` 변수는 AppMeasurement가 브라우저의 `navigator.sendBeacon()` 메서드를 사용하는지 여부를 결정하는 부울입니다. Its default value is `false`. 의 비동기 특성을 사용하려는 경우 추적 함수를 호출하기 전에 이 변수를 로 `true` 설정합니다 `navigator.sendBeacon()`.

```js
s.useBeacon = true;
```

> [!NOTE] 추적 호출이 실행된 후 이 변수가 로 재설정됩니다 `false`. 구현에서 동일한 페이지 로드에서 여러 이미지 요청을 전송하는 경우(예: 단일 페이지 애플리케이션) 각 추적 호출 `true` 전에 이 변수를 로 설정합니다.
