---
title: dynamicAccountMatch
description: dynamicAccountMatch 변수는 동적 계정에서 볼 값을 결정합니다.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# dynamicAccountMatch

> [!IMPORTANT] 동적 계정은 이전 JavaScript 구현(H 코드)을 사용해서만 지원됩니다. 이러한 변수는 현재 AppMeasurement 라이브러리 또는 Adobe Experience Platform Launch에서 지원되지 않습니다.

이 `dynamicAccountMatch` 변수는 값을 보고 `dynamicAccountList` 비교하는 값입니다. 이 `dynamicAccountSelection` 값을 로 설정하지 않으면 `true`이 변수가 무시됩니다.

이 변수가 정의되지 않은 경우 기본값은 `window.location.host`입니다.

## 구문

```js
s.dynamicAccountMatch=[DOM object]
```

## 예

```js
// Look at the URL path to determine report suite
s.dynamicAccountMatch = location.pathname;

// Use a query string
s.dynamicAccountMatch = location.search;

// Use the full URL
s.dynamicAccountMatch = location.href;

// Use concatenated variables
s.dynamicAccountMatch =  location.hostname + location.pathname + location.search;
```

## 추가 참고 사항

* 하드 드라이브에 저장된 페이지에는 몇 개의 `location` 변수가 정의되어 있지 않습니다(예: `location.host` 비어 있음). 기본 보고서 세트가 `s_account` 포함되어 있는지 확인합니다.
* 페이지가 Google과 같은 웹 기반 번역 엔진을 통해 번역되는 경우 다이내믹 계정 선택이 설계된 대로 작동하지 않습니다. For more precise tracking, populate the `s_account` variable server-side.
