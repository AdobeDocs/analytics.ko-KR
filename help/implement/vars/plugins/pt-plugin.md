---
title: pt
description: 변수 목록에 대해 함수를 실행합니다.
feature: Variables
exl-id: 2ab24a8e-ced3-43ea-bdb5-7c39810e4102
source-git-commit: 7c7a7d8add9edb1538df12b440bc0a15f09efe5e
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 97%

---

# Adobe 플러그인: pt

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`pt` 플러그인은 Analytics 변수 목록에서 함수나 메서드를 실행합니다. 예를 들어 매번 수동으로 함수를 호출하지 않고 몇 개의 변수에서 [`clearVars`](../functions/clearvars.md) 함수를 선택적으로 실행할 수 있습니다. 몇 가지 다른 플러그인은 이 코드를 사용하여 올바로 실행됩니다. 한 번에 두 개 이상의 Analytics 변수에서 특정 함수를 실행할 필요가 없거나 종속 플러그인을 사용하지 않는 경우에는 이 플러그인이 필요하지 않습니다.

<!--## Install the plug-in using the Web SDK or the Adobe Analytics extension

Adobe offers an extension that allows you to use most commonly-used plug-ins.

1. Log in to [Adobe Experience Platform Data Collection](https://experience.adobe.com/data-collection) using your AdobeID credentials.
1. Click the desired tag property.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. Install and publish the [!UICONTROL Common Analytics Plugins] extension
1. If you haven't already, create a rule labeled "Initialize Plug-ins" with the following configuration:
    * Condition: None
    * Event: Core – Library Loaded (Page Top)
1. Add an action to the above rule with the following configuration:
    * Extension: Common Analytics Plugins
    * Action Type: Initialize pt
1. Save and publish the changes to the rule.-->

## 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
1. [!UICONTROL 사용자 지정 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 버튼이 표시됩니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화 ([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: pt v3.0 */
function pt(l,de,cf,fa){var b=l,d=de,f=cf,g=fa;if("-v"===b)return{plugin:"pt",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var c;a<window.s_c_il.length;a++)if(c=window.s_c_il[a],c._c&&"s_c"===c._c){a=c;break a}}a=void 0}if("undefined"!==typeof a&&(a.contextData.pt="3.0",b&&a[f])){b=b.split(d||",");d=b.length;for(var e=0;e<d;e++)if(c=a[f](b[e],g))return c}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`pt` 함수에서는 다음 인수를 사용합니다.

* **`l`** (필수, 문자열): 인수에 `cf` 포함된 함수가 실행할 수 있는 변수의 목록입니다.
* **`de`** (선택 사항, 문자열): `l` 인수의 변수 목록을 구분하는 구분 기호입니다. 기본값은 쉼표(`,`)입니다.
* **`cf`** (필수, 문자열): `l` 인수에 포함된 각 변수에 대해 호출할 AppMeasurement 개체에 포함된 콜백 함수의 이름입니다.
* **`fa`** (선택 사항, 문자열): `cf` 인수의 함수가 실행될 때 이 함수가 추가적인 인수를 호출하는 경우 해당 인수를 여기에 포함하십시오. 기본값은 `undefined`입니다.

이 함수를 호출하면 `cf` 인수에서 콜백 함수가 값을 반환하는 경우 값이 반환됩니다.

## 호출 예

### 예 #1

다음 코드는 getQueryParam 플러그인의 일부입니다.  이 코드는 URL의 쿼리 문자열(fullQueryString)에 들어 있는 각 키-값 쌍에 대해 getParameterValue 도우미 함수를 실행합니다.  각 키-값 쌍을 추출하려면 fullQueryString을 앰퍼샌드 &quot;&amp;&quot; 문자로 구분하여 분리해야 합니다. parameterKey는 플러그인이 쿼리 문자열에서 특별히 추출하려고 하는 쿼리 문자열 매개 변수를 참조합니다.

```js
returnValue = pt(fullQueryString, "&", "getParameterValue", parameterKey)
```

위의 줄은 다음과 유사한 코드를 실행하는 간단한 방법입니다.

```js
var returnValue = "",
  parameters = fullQueryString.split("&"),
  parametersLength = parameters.length;
for(var i = 0; i < parametersLength; i++)
{
  returnValue = getParameterValue(parameters[i], parameterKey);
  if(returnValue !== "") break;
}
```

## 버전 내역

### 3.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 2.01 (2019년 9월 24일)

* 전체 크기를 줄이기 위한 작은 코드 변경

### 2.0 (2018년 4월 17일)

* 포인트 릴리스 (다시 컴파일됨, 더 작은 코드 크기).
* H-코드 및 AppMeasurement 모두에 대한 지원을 추가했습니다.

### 1.0 (2013년 9월 23일)

* 초기 릴리스.
