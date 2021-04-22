---
title: charSet
description: charSet 변수는 Adobe가 이미지 요청을 구문 분석하는 데 사용하는 인코딩을 결정합니다.
exl-id: 2a2660c6-809d-4b33-a846-01e49dd99c7f
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '196'
ht-degree: 100%

---

# charSet

charSet 변수는 Adobe에서 수신 데이터를 Analytics의 저장 및 보고를 위해 UTF-8로 변환하는 데 사용합니다. 대부분의 사이트는 이 변수를 설정할 필요가 없습니다.

보고서에 잘못된 값 ([글자 깨짐](https://en.wikipedia.org/wiki/Mojibake))이 표시되는 경우에만 이 변수를 설정하십시오. 사이트가 서로 다른 페이지에서 다른 인코딩을 사용하는 경우 이 변수를 페이지별로 설정할 수 있습니다.

## Adobe Experience Platform Launch의 문자 집합

문자 집합은 Adobe Analytics 확장을 구성할 때 [!UICONTROL 일반] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
4. [!UICONTROL 일반] 아코디언을 확장합니다. 그러면 [!UICONTROL 문자 집합] 필드가 표시됩니다.

사전 설정된 문자 집합이나 사용자 지정 문자 집합을 사용할 수 있습니다. 보고서에 잘못된 값이 표시되지 않는 한 `UTF-8`에서 값을 변경하지 마십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.charSet

`charSet` 변수는 문자열입니다. Adobe Analytics에 잘못된 값이 있는 경우 이 변수를 사이트의 `<meta charset="">` HTML 태그와 동일한 값으로 설정하십시오.

```js
s.charSet = "UTF-8";
```
