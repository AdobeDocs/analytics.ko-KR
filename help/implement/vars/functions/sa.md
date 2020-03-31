---
title: sa
description: 구현에서 언제든지 보고서 세트를 변경합니다.
translation-type: ht
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# sa

`sa` 메서드를 사용하면 페이지에서 언제든지 보고서 세트를 동적으로 변경할 수 있습니다. 페이지를 다시 로드하지 않고 데이터를 다양한 보고서 세트에 보내려는 경우 이 메서드를 사용할 수 있습니다.

## Adobe Experience Platform Launch에서 sa 메서드 사용

인터페이스에서 보고서 세트를 변경하는 유연한 방법은 없습니다. 보고서 세트는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 라이브러리 관리] 아코디언 아래에서 설정할 수 있습니다. 하지만 규칙을 사용하여 보고서 세트를 변경하거나 업데이트할 수는 없습니다. 보고서 세트 값을 설정한 후 업데이트하려면 AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.sa()

대상 보고서 세트를 변경하려면 `s.sa()` 메서드를 호출하십시오. 이 메서드의 유일한 인수는 하나의 보고서 세트 ID나 쉼표로 구분된 여러 보고서 세트 ID를 포함하는 문자열입니다. 보고서 세트 ID 인수는 필수입니다. 이 문자열 인수에는 공백을 사용하지 마십시오.

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
