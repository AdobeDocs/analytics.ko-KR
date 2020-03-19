---
title: linkType
description: linkType 변수를 사용하여 히트가 속하는 링크 추적 차원을 결정합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkType

링크 추적 히트는 다음 세 가지 차원 중 하나를 채울 수 있습니다.

* 사용자 지정 링크
* 종료 링크
* 다운로드 링크

다음 함수를 실행할 때 채울 차원을 결정하려면 `linkType` 변수를 [`tl()`](../functions/tl-method.md) 사용합니다.

## Adobe Experience Platform Launch의 링크 유형

비콘을 전송하도록 규칙을 구성할 때 링크 유형을 설정합니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다. [!UICONTROL Rules]
4. 아래에서 [!UICONTROL Actions]&#39;+&#39; 아이콘을 클릭합니다.
5. 드롭다운을 Adobe [!UICONTROL Extension] Analytics로 설정하고 비콘 전송으로 [!UICONTROL Action Type] 설정합니다.
6. 드롭다운을 표시하는 `s.tl()` 라디오 단추를 [!UICONTROL Link Type] 클릭합니다.

이 드롭다운을 [!UICONTROL Custom Link], [!UICONTROL Download Link]또는 [!UICONTROL Exit Link]으로 설정할 수 있습니다.

## s.linkType in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.linkType` 변수는 세 개의 단일 문자 값 중 하나를 받는 문자열입니다. `o`또는 `d`를 `e`선택합니다. 링크 유형 없이 메서드를 호출하면 기본적으로 사용자 지정 링크가 사용됩니다. `tl()`

* `o` - 사용자 지정 링크
* `d` - 다운로드 링크
* `e` - 종료 링크

> [!TIP] 이 변수는 `tl()` 메서드의 두 번째 매개 변수이며, 일반적으로 독립 실행형 변수로 설정할 필요가 없습니다. 하지만, `linkType` `tl()` 메서드에서 값을 인수로 설정하지 않으려면 변수를 사용할 수 있습니다.

```js
s.linkType = "e";
```

## 예

다음 두 가지 예제 링크 추적 호출은 기능적으로 동일합니다. 동일한 링크 추적 히트를 수행하는 방법은 다릅니다.

```js
// Set link tracking arguments as individual variables
s.linkType = "d";
s.linkName = "Example download link";
s.tl();

// Set link tracking arguments directly in the tl() function
s.tl(this,"d","Example download link");
```
