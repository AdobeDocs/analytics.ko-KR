---
title: linkTrackVars
description: 링크 추적 이미지 요청에 포함할 변수를 지정합니다.
feature: Variables
exl-id: b884f6e9-45d9-49f0-ac74-ea6f4f01020a
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 61%

---

# linkTrackVars

일부 구현에서는 모든 링크 추적 이미지 요청에 모든 변수를 포함할 필요가 없습니다. [`tl()`](../functions/tl-method.md) 호출에 차원 및 지표를 선택적으로 포함하려면 `linkTrackVars` 및 [`linkTrackEvents`](linktrackevents.md) 변수를 사용하십시오.

이 변수는 페이지 보기 호출 ([`t()`](../functions/t-method.md) 메서드)에 사용되지 않습니다.

## 웹 SDK를 사용하여 XDM 이벤트에 포함할 변수를 결정합니다

웹 SDK는 링크 추적 호출에 대한 특정 필드를 제외하지 않습니다. 그러나 를 사용할 수 있습니다 `onBeforeEventSend` Adobe으로 데이터를 보내기 전에 원하는 필드를 지우거나 설정하려면 콜백하십시오. 자세한 내용은 [이벤트 전역 수정](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) 를 참조하십시오.

## Adobe Analytics 확장을 사용한 링크 추적 호출의 변수

이 변수는 인터페이스에 설정된 변수를 기반으로 백엔드에서 자동으로 채워지므로 Adobe Analytics 확장을 사용하여 구현에서 항상 설정됩니다.

>[!IMPORTANT]
>
>사용자 지정 코드 편집기를 사용하여 변수를 설정하는 경우 변수를 `linkTrackVars` 사용자 지정 코드도 사용합니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.linkTrackVars

`s.linkTrackVars` 변수는 링크 추적 이미지 요청 (`tl()` 메서드)에 포함할 쉼표로 구분된 변수 목록이 포함된 문자열입니다. 링크 추적 히트에 차원을 포함하려면 다음 두 기준을 모두 충족해야 합니다.

* 원하는 변수 값을 설정합니다. (예: `s.eVar1 = "Example value";`)
* `linkTrackVars` 변수에서 원하는 변수를 설정합니다. (예: `s.linkTrackVars = "eVar1";`)

```js
s.linkTrackVars = "eVar1,eVar2,events,channel,products";
```

이 변수의 기본값은 빈 문자열입니다. 그러나 Adobe는 이 변수가 `"None"`으로 설정된 코드 관리자에서 AppMeasurement 코드를 제공했습니다. 유효한 값은 차원을 채우는 모든 페이지 수준 변수입니다.

* 이 변수가 정의되지 않거나 빈 문자열로 설정되면 *모든* 변수가 링크 추적 이미지 요청에 포함됩니다.
* 이 변수가 `"None"`으로 설정되면 어떠한 변수도 링크 추적 이미지 요청에 포함되어 *않습니다*.

>[!TIP]
>
>이 변수에서 변수를 지정할 때 Analytics 개체 식별자 (`s.`)를 사용하지 마십시오. 예를 들어 `s.linkTrackVars = "eVar1";`은 올바르지만 `s.linkTrackVars = "s.eVar1";`은 틀립니다.

## 예

다음 링크 추적 함수에는 Adobe에 전송된 이미지 요청에서 `eVar1`만 (`eVar2`는 아님) 포함됩니다.

```js
s.eVar1 = "Example value 1";
s.eVar2 = "Example value 2";
s.linkTrackVars = "eVar1";
s.tl(this,"o","Example Custom Link");
```
