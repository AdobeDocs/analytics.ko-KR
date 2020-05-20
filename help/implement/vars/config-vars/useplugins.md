---
title: usePlugins
description: doPlugins() 함수를 활성화하거나 비활성화합니다.
translation-type: ht
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# usePlugins

`usePlugins`가 활성화되면 AppMeasurement가 컴파일되어 히트를 Adobe에 보내기 바로 전에 [`doPlugins()`](../functions/doplugins.md) 함수가 실행됩니다. `doPlugins()` 함수를 사용하는 경우 이 변수를 활성화하십시오.

## Adobe Experience Platform Launch에서 플러그인 사용

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.usePlugins

`s.usePlugins` 변수는 AppMeasurement가 `doPlugins()` 함수를 호출하는지 여부를 결정하는 부울입니다. 기본값은 `false`입니다. 구현에서 `true` 함수를 사용하는 경우 이 변수를 `doPlugins()`로 설정하십시오.

```js
s.usePlugins = true;
```
