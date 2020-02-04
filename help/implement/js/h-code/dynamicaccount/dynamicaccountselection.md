---
title: dynamicAccountSelection
description: dynamicAccountSelection 변수는 동적 계정 선택을 활성화하거나 비활성화합니다.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# dynamicAccountSelection

> [!IMPORTANT] 동적 계정은 이전 JavaScript 구현(H 코드)을 사용해서만 지원됩니다. 이러한 변수는 현재 AppMeasurement 라이브러리 또는 Adobe Experience Platform Launch에서 지원되지 않습니다.

이 `dynamicAccountSelection` 변수는 동적 계정 선택이 사용되는지 여부를 결정하는 부울입니다.

로 설정된 `true`경우 JavaScript 파일은 및 를 `dynamicAccountMatch` 봅니다 `dynamicAccountList`.

로 `false`설정되거나 이 변수가 정의되지 않은 경우 `dynamicAccountMatch` 및 `dynamicAccountList` 변수가 무시됩니다.

이 변수가 정의되지 않은 경우 기본값은 `false`입니다.

## 구문

```js
s.dynamicAccountSelection = [boolean];
```

## 예

```js
s.dynamicAccountSelection = true;
```
