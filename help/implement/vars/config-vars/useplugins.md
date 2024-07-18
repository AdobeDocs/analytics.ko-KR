---
title: usePlugins
description: doPlugins () 함수를 활성화하거나 비활성화합니다.
feature: Variables
exl-id: e8499acf-d8b9-490c-9f67-ad9a8f6ca7df
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 34%

---

# usePlugins

`usePlugins`가 활성화되면 AppMeasurement가 컴파일되어 히트를 Adobe에 보내기 바로 전에 [`doPlugins()`](../functions/doplugins.md) 함수가 실행됩니다. `doPlugins()` 함수를 사용하는 경우 이 변수를 활성화하십시오.

## 웹 SDK를 사용하여 `onBeforeEventSend` 콜백 사용

Web SDK에는 데이터가 Adobe으로 전송되기 전에 추가 논리 실행을 처리하는 부울이 없지만 `onBeforeEventSend` 콜백을 등록하여 데이터를 수정할 수 있습니다. 자세한 내용은 웹 SDK 설명서의 [전역 이벤트 수정](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally)을 참조하십시오.

## Adobe Analytics 확장을 사용하여 플러그인 사용

Adobe은 대부분의 [플러그인](../plugins/impl-plugins.md)을 호출할 수 있는 &#39;일반 Analytics 플러그인&#39; 확장 프로그램을 제공합니다. 확장을 설치하고 규칙 내에서 원하는 플러그인을 호출합니다.

원하는 플러그인이 Adobe 확장에 포함되지 않은 경우 AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.usePlugins

`s.usePlugins` 변수는 AppMeasurement가 `doPlugins()` 함수를 호출하는지 여부를 결정하는 부울입니다. 기본값은 `false`입니다. 구현에서 `true` 함수를 사용하는 경우 이 변수를 `doPlugins()`로 설정하십시오.

```js
s.usePlugins = true;
```
