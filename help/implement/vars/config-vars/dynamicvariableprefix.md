---
title: dynamicVariablePrefix
description: 동적 변수를 식별하는 문자열을 사용자 지정할 수 있습니다.
feature: Variables
exl-id: fe208723-0cf2-4899-be7a-8f23c6501c11
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 70%

---

# dynamicVariablePrefix

동적 변수는 값을 한 변수에서 다른 변수로 복사할 수 있도록 해 주는 축약적인 개념입니다. 이 변수는 이미지 요청의 URL 길이를 줄이는 데 도움이 되므로 긴 변수 값에 유용합니다. 이 개념에 대한 자세한 내용은 [동적 변수](../page-vars/dynamic-variables.md)를 참조하십시오.

기본적으로 동적 변수는 접두사 `D=`를 사용합니다. `dynamicVariablePrefix` 변수는 동적 변수를 식별하는 문자열을 사용자 지정할 수 있도록 해 줍니다. 대/소문자를 구분합니다.

## 웹 SDK를 사용하는 동적 변수 접두사

Web SDK는 동적 변수 형식을 사용하지 않습니다. 대신 데이터 스트림 매핑을 사용하여 단일 Source 필드를 사용하여 여러 대상 필드를 채울 수 있습니다. 자세한 내용은 [Web SDK를 사용하는 동적 변수](../page-vars/dynamic-variables.md#dynamic-variables-using-the-web-sdk)를 참조하십시오.

스키마를 따르지 않고 Adobe Analytics으로 데이터를 직접 전송하는 경우 다음 변수를 사용합니다.

* [데이터 개체](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.dynamicVariablePrefix`

## Adobe Analytics 확장을 사용하는 동적 변수 접두사

동적 변수 접두사는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 전역 변수] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
1. [!UICONTROL 전역 변수] 아코디언을 확장합니다. 그러면 [!UICONTROL 동적 변수 접두사] 필드가 표시됩니다.

이 필드에는 기본적으로 `D=`가 포함됩니다. 다른 동적 변수 접두사를 사용하려는 경우 값을 변경할 수 있습니다. 사이트의 문자 인코딩과 일치하는 한 원하는 값을 사용할 수 있습니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.dynamicVariablePrefix

`s.dynamicVariablePrefix` 변수는 문자 시퀀스를 포함할 수 있는 문자열입니다. 이 변수가 정의되어 있지 않으면 AppMeasurement는 기본적으로 문자열 `D=`를 사용합니다.

```js
// An example that changes the dynamic variable prefix
s.dynamicVariablePrefix="..";

// This eVar uses the above customized dynamic variable prefix to set eVar to page URL
s.eVar1="..g";
```
