---
title: t
description: Adobe에 페이지 보기 추적 호출을 보냅니다.
translation-type: ht
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# t

`t` 메서드는 Adobe Analytics의 중요한 핵심 구성 요소입니다. 이 메서드는 페이지에 정의된 모든 Analytics 변수를 가져와 이미지 요청에 컴파일한 다음, 해당 데이터를 Adobe 데이터 수집 서버에 보냅니다.

예를 들어 다음 JavaScript 코드를 생각해 보십시오.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// Define config variables and page variables
s.trackingServerSecure = "data.example.com";
s.eVar1 = "Example dimension value";

// Compile the variables on the page into an image request to Adobe
s.t();
```

`t` 메서드 실행에서는 정의된 모든 Analytics 변수를 사용하고 해당 변수를 기반으로 URL을 생성합니다. 일부 Analytics 변수는 이미지의 URL을 결정하고, 또 다른 변수는 쿼리 문자열 매개 변수 값을 결정합니다.

```text
https://data.example.com/b/ss/examplersid/1/?v1=Example%20dimension%20value
```

Adobe는 이미지 요청을 받은 다음, 요청 헤더, URL 및 쿼리 문자열 매개 변수를 구문 분석합니다. 그러면 데이터 수집 서버가 사이트에는 보이지 않게 표시되는 투명한 1x1 픽셀 이미지를 반환합니다.

## Adobe Experience Platform Launch의 페이지 보기 추적 호출

Launch에는 페이지 보기 추적 호출을 설정하는 전용 위치가 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업] 아래에서 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 비콘 보내기로 설정합니다.
6. `s.t()` 라디오 단추를 클릭합니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.t() 메서드

추적 호출을 Adobe에 보내려면 `s.t()` 메서드를 호출하십시오.

```js
s.t();
```

원할 경우 개체를 인수로 사용하여 변수 값을 무시할 수 있습니다. 자세한 내용은 [변수 무시](../../js/overrides.md)를 참조하십시오.

```js
var y = new Object();
y.eVar1 = "Override value";
s.t(y);
```

> [!NOTE] 이전 버전의 AppMeasurement에서는 이 함수를 호출하기 위해 여러 줄의 코드를 사용했습니다. 지금까지는 추가적인 코드가 다양한 브라우저에 대한 해결 방법을 제공했습니다. 최신 브라우저의 표준화와 우수 사례를 통해 더 이상 이 코드 블록이 필요하지 않게 되었습니다. 이제 메서드 호출 `s.t()`만 있으면 됩니다.
