---
title: pt
description: 변수 목록에서 함수를 실행합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:pt

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `pt` 플러그인은 Analytics 변수 목록에서 함수나 메서드를 실행합니다. 예를 들어, 매번 수동으로 메서드를 호출하지 않고 여러 변수에서 [`clearVars`](../functions/clearvars.md) 메서드를 선택적으로 실행할 수 있습니다. 이 코드에 따라 다른 여러 플러그인이 올바르게 실행됩니다. 한 번에 두 개 이상의 Analytics 변수에서 특정 함수를 실행할 필요가 없거나 종속 플러그인을 사용하지 않는 경우에는 이 플러그인이 필요하지 않습니다.

## Adobe Experience Platform Launch 익스텐션을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있는 확장 기능을 제공합니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. 원하는 속성을 클릭합니다.
1. 탭으로 이동한 다음 [!UICONTROL Extensions] [!UICONTROL Catalog] 단추를 클릭합니다.
1. 확장 [!UICONTROL Common Analytics Plugins] 프로그램 설치 및 게시
1. 아직 설정하지 않은 경우, &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 다음 구성으로 만듭니다.
   * 조건:없음
   * 이벤트:코어 - 라이브러리가 로드됨(페이지 상단)
1. 다음 구성으로 위 규칙에 작업을 추가합니다.
   * 확장:공통 Analytics 플러그인
   * 작업 유형:pt 초기화
1. 변경 내용을 저장하고 규칙에 게시합니다.

## Launch 사용자 정의 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려면 사용자 정의 코드 편집기를 사용할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. 원하는 속성을 클릭합니다.
1. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 확장 프로그램 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
1. 단추를 표시하는 [!UICONTROL Configure tracking using custom code] 아코디언을 [!UICONTROL Open Editor] 확장합니다.
1. 사용자 정의 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여 넣습니다.
1. Analytics 확장 프로그램에 변경 사항을 저장하고 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣습니다(사용 [`s_gi`](../functions/s-gi.md)). 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: pt v2.01 */
 s.pt=function(l,de,cf,fa){if(l&&this[cf]){l=l.split(de||",");de=l.length;for(var e,c=0;c<de;c++)if(e=this[cf](l[c],fa))return e}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `pt` 메서드는 다음 인수를 사용합니다.

* **`l`** (필수, 문자열):인수에 포함된 함수가 실행할 수 있는 변수의 `cf` 목록입니다.
* **`de`** (선택 사항, 문자열):인수의 변수 목록을 구분하는 구분 `l` 기호입니다. 기본값은 쉼표(`,`)입니다.
* **`cf`** (필수, 문자열):인수에 포함된 각 변수에 대해 호출할 AppMeasurement 개체에 포함된 콜백 함수의 이름입니다. `l`
* **`fa`** (선택 사항, 문자열):인수의 함수가 실행될 때 추가 인수를 호출하는 경우 여기에 포함시키십시오. `cf` 기본값은 `undefined`입니다.

이 메서드를 호출하면 인수에서 콜백 함수가 값을 반환하면 값이 반환됩니다. `cf`

## 호출 예

### 예 #1

다음 코드는 getQueryParam 플러그인의 일부입니다.  URL의 쿼리 문자열(fullQueryString)에 들어 있는 각 키-값 쌍에 대해 getParameterValue 도우미 함수를 실행합니다.  다른 방법으로 각 키-값 쌍을 추출하려면 fullQueryString을 앰퍼샌드 &quot;&amp;&quot; 문자로 구분하여 구분해야 합니다. parameterKey는 플러그인이 특히 쿼리 문자열에서 추출하려고 하는 쿼리 문자열 매개 변수를 참조합니다

```javascript
returnValue = s.pt(fullQueryString, "&", "getParameterValue", parameterKey)
```

위의 줄은 다음과 유사한 코드를 실행하는 단축키입니다.

```js
var returnValue = "",
  parameters = fullQueryString.split("&"),
  parametersLength = parameters.length;
for(var i = 0; i < parametersLength; i++)
{
  returnValue = s.getParameterValue(parameters[i], parameterKey);
  if(returnValue !== "") break;
}
```

## 버전 내역

### 2.01(2019년 9월 24일)

* 전체 크기를 줄이기 위해 작은 코드 변경

### 2.0(2018년 4월 17일)

* 포인트 릴리스(다시 컴파일되고 더 작은 코드 크기).
* H-code 및 AppMeasurement 모두에 대한 지원을 추가했습니다.

### 1.0(2013년 9월 23일)

* 초기 릴리스.
