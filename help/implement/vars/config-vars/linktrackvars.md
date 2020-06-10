---
title: linkTrackVars
description: 링크 추적 이미지 요청에 포함할 변수를 지정합니다.
translation-type: tm+mt
source-git-commit: a28a05047e95d12343fd94f7b11e5cabf7fac070
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 100%

---


# linkTrackVars

일부 구현에서는 모든 링크 추적 이미지 요청에 모든 변수를 포함할 필요가 없습니다. [`tl()`](../functions/tl-method.md) 호출에 차원 및 지표를 선택적으로 포함하려면 `linkTrackVars` 및 [`linkTrackEvents`](linktrackevents.md) 변수를 사용하십시오.

이 변수는 페이지 보기 호출([`t()`](../functions/t-method.md) 메서드)에 사용되지 않습니다.

## Adobe Experience Platform Launch를 사용한 링크 추적 호출의 변수

Launch는 인터페이스에 설정된 변수를 기반으로 백엔드에서 이 변수를 자동으로 채우며, 따라서 Launch를 사용하여 구현에서 항상 설정됩니다.

>[!IMPORTANT] 사용자 지정 코드 편집기를 사용하여 Launch에서 변수를 설정하는 경우 사용자 지정 코드도 사용하여 `linkTrackVars`에서 변수를 포함해야 합니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.linkTrackVars

`s.linkTrackVars` 변수는 링크 추적 이미지 요청(`tl()` 메서드)에 포함할 쉼표로 구분된 변수 목록이 포함된 문자열입니다. 링크 추적 히트에 차원을 포함하려면 다음 두 기준을 모두 충족해야 합니다.

* 원하는 변수 값을 설정합니다. (예: `s.eVar1 = "Example value";`)
* `linkTrackVars` 변수에서 원하는 변수를 설정합니다. (예: `s.linkTrackVars = "eVar1";`)

```js
s.linkTrackVars = "eVar1,eVar2,events,channel,products";
```

이 변수의 기본값은 빈 문자열입니다. 그러나 Adobe는 이 변수가 `"None"`으로 설정된 코드 관리자에서 AppMeasurement 코드를 제공했습니다. 유효한 값은 차원을 채우는 모든 페이지 수준 변수입니다.

* 이 변수가 정의되지 않거나 빈 문자열로 설정되면 *모든* 변수가 링크 추적 이미지 요청에 포함됩니다.
* 이 변수가 `"None"`으로 설정되면 어떠한 변수도 링크 추적 이미지 요청에 포함되어 *않습니다*.

>[!TIP] 이 변수에서 변수를 지정할 때 Analytics 개체 식별자(`s.`)를 사용하지 마십시오. 예를 들어, `s.linkTrackVars = "eVar1";`은 올바르지만 `s.linkTrackVars = "s.eVar1";`은 틀립니다.

## 예

다음 링크 추적 함수에는 Adobe에 전송된 이미지 요청에서 `eVar1`만(`eVar2`는 아님) 포함됩니다.

```js
s.eVar1 = "Example value 1";
s.eVar2 = "Example value 2";
s.linkTrackVars = "eVar1";
s.tl(this,"o","Example Custom Link");
```
