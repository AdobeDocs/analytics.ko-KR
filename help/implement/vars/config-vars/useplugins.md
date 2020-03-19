---
title: usePlugins
description: doPlugins() 함수를 활성화하거나 비활성화합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# usePlugins

이 `usePlugins` 옵션이 활성화되면 AppMeasurement가 컴파일되고 Adobe에 히트를 보내기 직전에 [`doPlugins()`](../functions/doplugins.md) 함수가 실행됩니다. 이 `doPlugins()` 함수를 사용하는 경우 이 변수를 활성화합니다.

## Adobe Experience Platform Launch에서 플러그인 사용

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## s.usePlugins in AppMeasurement and Launch custom code editor

이 `s.usePlugins` 변수는 AppMeasurement가 함수를 호출하는지 여부를 결정하는 부울입니다 `doPlugins()` . Its default value is `false`. 구현에서 함수를 사용하는 `true` 경우 이 `doPlugins()` 변수를 설정합니다.

```js
s.usePlugins = true;
```
