---
title: dynamicVariablePrefix
description: 동적 변수를 식별하는 문자열을 사용자 지정할 수 있습니다.
translation-type: tm+mt
source-git-commit: 03a4c0d5e080219a7fd96dff33ce122669351ac3

---


# dynamicVariablePrefix

동적 변수는 한 변수에서 다른 변수로 값을 복사할 수 있는 축약적인 개념입니다. 이미지 요청의 URL 길이를 줄이는 데 도움이 되므로 긴 변수 값에 유용합니다. 이 [개념에 대한 자세한 내용은 동적 변수를](../page-vars/dynamic-variables.md) 참조하십시오.

기본적으로 동적 변수는 접두사를 `D=`사용합니다. 이 `dynamicVariablePrefix` 변수를 사용하면 동적 변수를 식별하는 문자열을 사용자 지정할 수 있습니다. 대소문자를 구분합니다.

## Adobe Experience Platform Launch의 동적 변수 접두사

동적 변수 접두사는 Adobe Analytics 확장을 구성할 [!UICONTROL 때] 전역 변수 아코디언 아래의 필드입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 확장 [!UICONTROL 탭으로 이동한] 다음 Adobe [!UICONTROL Analytics에서 구성] 단추를 클릭합니다.
4. 동적 변수 [!UICONTROL 접두사] 필드를 표시하는 전역 변수 [!UICONTROL 아코디언을 확장합니다] .

이 필드에는 `D=` 기본적으로 포함되어 있습니다. 다른 동적 변수 접두사를 사용하려면 값을 변경할 수 있습니다. 사이트에서 문자 인코딩과 일치하는 경우 원하는 값을 사용할 수 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.dynamicVariablePrefix

이 `s.dynamicVariablePrefix` 변수는 문자 시퀀스를 포함할 수 있는 문자열입니다. 이 변수가 정의되지 않은 경우 AppMeasurement는 `D=` 기본적으로 문자열을 사용합니다.

```js
// An example that changes the dynamic variable prefix
s.dynamicVariablePrefix="..";

// This eVar uses the above customized dynamic variable prefix to set eVar to page URL
s.eVar1="..g";
```
