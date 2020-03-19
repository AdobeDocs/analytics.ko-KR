---
title: linkTrackVars
description: 링크 추적 이미지 요청에 포함할 변수를 지정합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkTrackVars

일부 구현에서는 모든 링크 추적 이미지 요청에 모든 변수를 포함하기를 원하지 않습니다. 및 `linkTrackVars` 변수를 사용하여 [`linkTrackEvents`](linktrackevents.md) [`tl()`](../functions/tl-method.md) 호출에 차원 및 지표를 선택적으로 포함할 수 있습니다.

이 변수는 페이지 보기 호출(`t()` 메서드)에 사용되지 않습니다.

## Adobe Experience Platform Launch를 사용한 링크 추적 호출의 변수

Launch는 인터페이스에 설정된 변수를 기반으로 백 엔드에서 이 변수를 자동으로 채우므로 Launch를 사용하여 구현에서 항상 설정됩니다.

> [!IMPORTANT] 사용자 지정 코드 편집기를 사용하여 Launch에서 변수를 설정하는 경우 사용자 지정 코드도 `linkTrackVars` 사용할 때 변수를 포함해야 합니다.

## s.linkTrackVars in AppMeasurement and Launch 사용자 지정 코드 편집기

이 `s.linkTrackVars` 변수는 링크 추적 이미지 요청(`tl()` 메서드)에 포함할 쉼표로 구분된 변수 목록이 포함된 문자열입니다. 링크 추적 히트에 차원을 포함하려면 다음 기준을 모두 충족해야 합니다.

* 원하는 변수 값을 설정합니다. (예: `s.eVar1 = "Example value";`)
* 변수에서 원하는 변수를 `linkTrackVars` 설정합니다. (예: `s.linkTrackEvents = "eVar1";`)

```js
s.linkTrackVars = "eVar1,eVar2,events,channel,products";
```

이 변수의 기본값은 빈 문자열입니다. 그러나 Adobe는 이 변수가 설정된 코드 관리자에서 AppMeasurement 코드를 `"None"`제공했습니다. 유효한 값은 차원을 채우는 모든 페이지 수준 변수입니다.

* 이 변수가 정의되지 않았거나 빈 문자열로 설정된 경우 *모든* 변수가 링크 추적 이미지 요청에 포함됩니다.
* 이 변수가 로 설정된 `"None"`경우 링크 추적 이미지 요청에 변수가 *포함되지* 않습니다.

> [!TIP] 이 변수에서 변수를 지정할 때 Analytics 개체 식별자(`s.`)를 사용하지 마십시오. 예를 들어, `s.linkTrackVars = "eVar1";` 는 올바르지만 `s.linkTrackVars = "s.eVar1";` 틀립니다.

## 예

다음 링크 추적 함수에는 Adobe로 전송된 이미지 요청에만 `eVar1` ( `eVar2`아님)이 포함됩니다.

```js
s.eVar1 = "Example value 1";
s.eVar2 = "Example value 2";
s.linkTrackVars = "eVar1";
s.tl(this,"o","Example Custom Link");
```
