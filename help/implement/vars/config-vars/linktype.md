---
title: linkType
description: linkType 변수를 사용하여 히트가 속하는 링크 추적 차원을 결정합니다.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# linkType

링크 추적 히트는 다음 세 가지 차원 중 하나를 채울 수 있습니다.

* 사용자 지정 링크
* 종료 링크
* 다운로드 링크

다음 함수를 실행할 때 채울 차원을 결정하려면 `linkType` 변수를 `tl()` 사용합니다.

## Adobe Experience Platform Launch의 링크 유형

비콘을 전송하도록 규칙을 구성할 때 링크 유형을 설정합니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 규칙 [!UICONTROL 탭으로 이동한] 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. 작업 [!UICONTROL 아래에서]&#39;+&#39; 아이콘을 클릭합니다
5. 확장 [!UICONTROL 프로그램 드롭다운을 Adobe] Analytics로 설정하고 작업 [!UICONTROL 유형을] 비콘 전송으로 설정합니다.
6. 링크 유형 `s.tl()` 드롭다운을 표시하는 [!UICONTROL 라디오 단추를] 클릭합니다.

이 드롭다운을 사용자 지정 링크, 다운로드 [!UICONTROL 링크]또는 [!UICONTROL 종료 링크로]설정할 [!UICONTROL 수]있습니다.

## s.linkType in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.linkType` 변수는 세 개의 단일 문자 값 중 하나를 받는 문자열입니다. `o`또는 `d`를 `e`선택합니다. 링크 유형 없이 함수가 호출되면 기본적으로 사용자 지정 링크로 설정됩니다. `tl()`

* `o` - 사용자 지정 링크
* `d` - 다운로드 링크
* `e` - 종료 링크

> [!TIP] 이 변수는 `tl()` 함수의 두 번째 매개 변수이며, 일반적으로 독립 실행형 변수로 설정할 필요가 없습니다. 그러나 함수에서 값을 인수로 설정하지 않으려면 `linkType` 변수를 사용할 수 `tl()` 있습니다.

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
