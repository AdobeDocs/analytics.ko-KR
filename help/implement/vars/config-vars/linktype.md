---
title: linkType
description: linkType 변수를 사용하여 히트가 속하는 링크 추적 차원을 결정합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkType

링크 추적 히트는 다음 세 가지 차원 중 하나를 채울 수 있습니다.

* 사용자 지정 링크
* 종료 링크 
* 다운로드 링크

다음 [`tl()`](../functions/tl-method.md) 함수를 실행할 때 채울 차원을 결정하려면 `linkType` 변수를 사용하십시오.

## Adobe Experience Platform Launch의 링크 유형

비콘을 전송하는 규칙을 구성할 때 링크 유형을 설정하십시오.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. Go to the [!UICONTROL Rules] tab, then click the desired rule (or create a rule).
4. Under [!UICONTROL Actions], click the &#39;+&#39; icon
5. Set the [!UICONTROL Extension] dropdown to Adobe Analytics, and the [!UICONTROL Action Type] to Send Beacon.
6. Click the `s.tl()` radio button which reveals the [!UICONTROL Link Type] dropdown.

이 드롭다운을 [!UICONTROL Custom Link], [!UICONTROL Download Link]또는 [!UICONTROL Exit Link]으로 설정할 수 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.linkType

`s.linkType` 변수는 `o`, `d` 또는 `e`, 이렇게 세 개의 단일 문자 값 중 하나를 받는 문자열입니다. If a `tl()` method is called without a link type, it defaults to Custom link.

* `o` - 사용자 지정 링크
* `d` - 다운로드 링크
* `e` - 종료 링크

>[!TIP] 이 변수는 `tl()` 메서드의 두 번째 매개 변수이며, 일반적으로 독립 실행형 변수로 설정할 필요가 없습니다. However, you can use the `linkType` variable if you do not want to set values as arguments in the `tl()` method.

```js
s.linkType = "e";
```

## 예

다음 두 가지 링크 추적 호출 예는 기능적으로 동일하지만, 동일한 링크 추적 히트를 수행하는 방법은 다릅니다.

```js
// Set link tracking arguments as individual variables
s.linkType = "d";
s.linkName = "Example download link";
s.tl();

// Set link tracking arguments directly in the tl() function
s.tl(this,"d","Example download link");
```
