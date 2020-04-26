---
title: charSet
description: charSet 변수는 Adobe가 이미지 요청을 구문 분석하는 데 사용하는 인코딩을 결정합니다.
translation-type: tm+mt
source-git-commit: f769da139d9890fd736a9b277934b11aa131e166

---


# charSet

charSet 변수는 Adobe에서 수신 데이터를 Analytics의 저장 및 보고를 위해 UTF-8로 변환하는 데 사용합니다. 사이트에서 UTF-8 이외의 charSet을 사용하는 경우 이 변수를 사용하면 Adobe가 데이터를 적절히 인코딩할 수 있습니다. 사이트가 서로 다른 페이지에서 서로 다른 인코딩을 사용하는 경우 이 변수를 페이지별로 설정할 수 있습니다.

## Adobe Experience Platform Launch의 문자 집합

문자 집합은 Adobe Analytics 확장을 구성할 때 [!UICONTROL 일반] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
4. [!UICONTROL 일반] 아코디언을 확장합니다. 그러면 [!UICONTROL 문자 집합] 필드가 표시됩니다.

사전 설정된 문자 집합이나 사용자 지정 문자 집합을 사용할 수 있습니다. 이 값은 사이트의 문자 인코딩과 일치해야 합니다. 대부분의 사이트는 `UTF-8`을 사용합니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.charSet

`charSet` 변수는 문자열입니다. 이 변수를 사이트의 `<meta charset="">` HTML 태그와 동일한 값으로 설정합니다.

```js
s.charSet = "UTF-8";
```
