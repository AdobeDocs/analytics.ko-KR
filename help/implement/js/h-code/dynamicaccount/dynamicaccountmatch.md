---
title: dynamicAccountMatch
description: dynamicAccountMatch 변수는 동적 계정에서 볼 값을 결정합니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# dynamicAccountMatch

>[!IMPORTANT] 동적 계정은 이전 JavaScript 구현(H 코드)을 사용해야만 지원됩니다. 이러한 변수는 현재 AppMeasurement 라이브러리 또는 Adobe Experience Platform Launch에서 지원되지 않습니다.

`dynamicAccountMatch` 변수는 `dynamicAccountList`에서 보고 그 값을 비교하는 값입니다. `dynamicAccountSelection`이 `true`로 설정되지 않으면 이 변수는 무시됩니다.

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

* 하드 드라이브에 저장된 페이지에 몇 개의 `location` 변수가 정의되어 있지 않습니다(예: `location.host`가 비어 있음). `s_account`에 기본 보고서 세트가 포함되어 있는지 확인하십시오.
* 페이지가 Google과 같은 웹 기반 번역 엔진을 통해 번역되는 경우, 동적 계정 선택 기능이 설계대로 작동하지 않습니다. 더 정밀한 추적을 수행하려면, `s_account` 변수 서버측을 채우십시오.
