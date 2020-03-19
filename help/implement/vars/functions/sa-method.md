---
title: sa
description: 구현 시 언제든지 보고서 세트를 변경합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# sa

이 `sa()` 방법을 사용하면 페이지에서 언제든지 보고서 세트를 동적으로 변경할 수 있습니다. 페이지를 다시 로드하지 않고 데이터를 다른 보고서 세트로 보내려면 이 방법을 사용할 수 있습니다.

## Adobe Experience Platform Launch에서 sa 방법 사용

인터페이스에서 보고서 세트를 변경하는 유연한 방법은 없습니다. Adobe Analytics 확장을 구성할 때 아코디언 아래에 보고서 세트를 설정할 수 [!UICONTROL Library Management] 있습니다. 하지만 규칙을 사용하여 보고서 세트를 변경하거나 업데이트할 수는 없습니다. 보고서 세트 값을 설정한 후 업데이트하려면 AppMeasurement 구문에 따라 사용자 지정 코드 편집기를 사용합니다.

## s.sa() in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.sa()` 메서드를 호출하여 대상 보고서 세트를 변경합니다. 유일한 인수는 보고서 세트 ID가 들어 있는 문자열이거나 쉼표로 구분된 여러 보고서 세트 ID입니다. 보고서 세트 ID 인수가 필요합니다. 문자열 인수에 공백을 사용하지 마십시오.

```js
s.sa("examplersid");
```

## 예

사용자가 사이트에서 특정 작업을 수행하는 경우 보고서 세트를 변경할 수 있습니다.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// If the visitor plays a video, you can add a video report suite
s.sa("examplersid,videorsid");

// Then send an image request
s.t();
```
