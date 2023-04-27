---
title: usePlugins
description: doPlugins () 함수를 활성화하거나 비활성화합니다.
feature: Variables
exl-id: e8499acf-d8b9-490c-9f67-ad9a8f6ca7df
source-git-commit: 41154580c272514e504c5478215bb67795488de3
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# usePlugins

`usePlugins`가 활성화되면 AppMeasurement가 컴파일되어 히트를 Adobe에 보내기 바로 전에 [`doPlugins()`](../functions/doplugins.md) 함수가 실행됩니다. `doPlugins()` 함수를 사용하는 경우 이 변수를 활성화하십시오.

## 를 사용하십시오 `onBeforeEventSend` 웹 SDK를 사용한 콜백

웹 SDK에는 데이터가 Adobe으로 전송되기 전에 추가 로직 실행을 처리할 부울이 없지만 `onBeforeEventSend` 콜백으로 데이터를 수정할 수 있습니다. 자세한 내용은 [이벤트 전역 수정](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) 를 참조하십시오.

## Adobe Analytics 확장을 사용하여 플러그인 사용

Adobe은 가장 많이 호출할 수 있는 &#39;일반 Analytics 플러그인&#39;이라는 확장을 제공합니다 [플러그인](../plugins/impl-plugins.md). 확장을 설치하고 규칙 내에서 원하는 플러그인을 호출합니다.

원하는 플러그인이 Adobe 확장에 포함되지 않은 경우 AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.usePlugins

`s.usePlugins` 변수는 AppMeasurement가 `doPlugins()` 함수를 호출하는지 여부를 결정하는 부울입니다. 기본값은 `false`입니다. 구현에서 `true` 함수를 사용하는 경우 이 변수를 `doPlugins()`로 설정하십시오.

```js
s.usePlugins = true;
```
