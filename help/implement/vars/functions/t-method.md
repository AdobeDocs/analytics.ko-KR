---
title: t
description: Adobe에 페이지 보기 추적 호출을 보냅니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# t()

이 `t()` 메서드는 Adobe Analytics의 중요한 핵심 구성 요소입니다. 페이지에 정의된 모든 Analytics 변수를 가져와 이미지 요청으로 컴파일한 다음 해당 데이터를 Adobe 데이터 수집 서버로 보냅니다.

예를 들어 다음 JavaScript 코드를 고려해 보십시오.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// Define config variables and page variables
s.trackingServerSecure = "data.example.com";
s.eVar1 = "Example dimension value";

// Compile the variables on the page into an image request to Adobe
s.t();
```

이 `t()` 메서드를 실행하면 정의된 모든 Analytics 변수가 사용되고 해당 변수를 기반으로 URL이 생성됩니다. 일부 Analytics 변수는 이미지의 URL을 결정하지만 다른 변수는 쿼리 문자열 매개 변수 값을 결정합니다.

```text
https://data.example.com/b/ss/examplersid/1/?v1=Example%20dimension%20value
```

Adobe는 이미지 요청을 받은 다음 요청 헤더, URL 및 쿼리 문자열 매개 변수를 구문 분석합니다. 그런 다음 데이터 수집 서버는 투명 1x1 픽셀 이미지를 반환하고 사이트에 보이지 않게 표시됩니다.

## Adobe Experience Platform Launch의 페이지 보기 추적 호출

Launch에는 페이지 보기 추적 호출을 설정하는 전용 위치가 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다. [!UICONTROL Rules]
4. 아래에서 [!UICONTROL Actions]&#39;+&#39; 아이콘을 클릭합니다.
5. 드롭다운을 Adobe [!UICONTROL Extension] Analytics로 설정하고 비콘 전송으로 [!UICONTROL Action Type] 설정합니다.
6. Click the `s.t()` radio button.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.t() 메서드

Adobe에 추적 호출을 전송하려면 이 `s.t()` 메서드를 호출합니다.

```js
s.t();
```

필요에 따라 개체를 인수로 사용하여 변수 값을 재정의할 수 있습니다. 자세한 내용은 [변수 대체를](../../js/overrides.md) 참조하십시오.

```js
var y = new Object();
y.eVar1 = "Override value";
s.t(y);
```

> [!NOTE] 이전 버전의 AppMeasurement에서는 이 함수를 호출하기 위해 여러 줄의 코드를 사용했습니다. 지금까지 다른 브라우저에 대한 해결 방법을 추가로 제공했습니다. 최신 브라우저의 표준화와 우수 사례는 더 이상 이 코드 블록을 필요로 하지 않습니다. 이제 메서드 호출만 `s.t()` 필요합니다.
