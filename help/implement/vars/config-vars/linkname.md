---
title: linkName
description: 사용자 지정 링크 히트의 이름을 설정합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkName

Use the `linkName` variable to determine the dimension value of custom links, download links, or exit links when running the next [`tl()`](../functions/tl-method.md) method.

이 변수가 비어 있으면 AppMeasurement는 [`linkURL`](linkurl.md) 변수로 되돌아갑니다.

## Adobe Experience Platform Launch의 링크 이름

비콘을 전송하는 규칙을 구성할 때 링크 이름 필드를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업] 아래에서 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 비콘 보내기로 설정합니다.
6. `s.tl()` 라디오 단추를 클릭합니다. 그러면 [!UICONTROL 링크 이름] 필드가 표시됩니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.linkName

`s.linkName` 변수는 사용자 지정 링크, 다운로드 링크 또는 종료 링크의 차원 값을 결정하는 문자열입니다([`s.linkType`](linktype.md) 값에 따라 다름). 최대 100바이트를 포함할 수 있습니다.

>[!TIP] 이 변수는 `tl()` 메서드의 세 번째 매개 변수이며, 일반적으로 독립 실행형 변수로 설정할 필요가 없습니다. However, you can use the `linkName` variable if you do not want to set values as arguments in the `tl()` method.

```js
s.linkName = "Example custom link";
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
