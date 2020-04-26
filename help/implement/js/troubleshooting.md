---
title: JavaScript 구현 문제 해결
description: JavaScript 구현 문제 해결을 위한 일반적인 문제 및 우수 사례에 대해 알아봅니다.
translation-type: tm+mt
source-git-commit: 8aa6932dcbb6dad88c27ba1cd4f5aad3bafcfc52

---


# JavaScript 구현 문제 해결

다음은 조직에서 데이터를 Adobe Analytics에 올바로 보내는 데 문제가 발생할 수 있는 몇 가지 원인입니다.

## 따옴표 사용

Adobe에 전송되는 대부분의 변수는 문자열입니다. JavaScript에서는 작은 따옴표나 큰 따옴표를 사용할 수 있습니다.

### 인용 부호를 혼합하여 변수 정의

사용하는 따옴표 유형에 일치하는지 확인하는 것이 좋습니다. 작은 따옴표가 문자열의 시작을 지정하는 경우 작은 따옴표를 사용하여 문자열을 닫아야 합니다.

예를 들어, `s.eVar1 = 'Value'`와 `s.eVar1 = "Value"`는 모두 유효합니다. `s.eVar1 = 'Value"`는 유효하지 않습니다.

### 문자열에 작은 따옴표 또는 큰 따옴표 포함

경우에 따라 문자열에 작은 따옴표나 큰 따옴표를 포함하는 것이 좋습니다. 예를 들어 값 `Alex's sale` 또는 `John the "Hunter"`를 보고서에 포함하려는 경우가 있을 수 있습니다. 이 값을 포함하는 방법에는 다음 두 가지가 있습니다.

* **다른 따옴표 유형 사용**: 예를 들어, `s.eVar1 = "Alex's sale"`과 `s.eVar1 = 'John the "Hunter"'`는 모두 유효합니다.
* **따옴표 이스케이프 처리**: 백슬래시를 사용하여 따옴표를 이스케이프 처리합니다. 예를 들어, `s.eVar1 = 'Alex\'s sale'`과 `s.eVar1 = "John the \"Hunter\""`는 모두 유효합니다.

### 둥근 따옴표 사용 방지

일부 프로그램은 중립 따옴표(`"..."`와 `'...'`)를 둥근 따옴표(`“...”`와 `‘...’`)로 자동으로 변환합니다. 문서 편집기(예: Microsoft Word)를 사용하거나 이메일을 통해 코드 조각을 전송하지 마십시오. JavaScript에서는 둥근 따옴표를 사용할 수 없습니다.

## Analytics 개체 참조

Adobe에 전송되는 모든 변수는 Analytics 개체를 사용합니다. 대부분의 구현에서는 `s` 개체를 사용합니다. 변수를 참조할 때에는 반드시 Analytics 개체를 참조에 포함하도록 하십시오.

예를 들어, `s.eVar1 = 'Value'`는 유효하지만 `eVar1 = 'Value'`는 유효하지 않습니다.

## 각 변수를 한 번 정의

추적 함수(`s.t()`)가 실행되면 AppMeasurement는 정의된 모든 변수를 가져와 이미지 요청으로 컴파일합니다. 구현에서 변수를 두 번 이상 정의하는 경우에는 최신 값만 사용됩니다. 추적 함수가 실행될 때 모든 변수 값에 올바른 값을 포함하는지 확인하십시오.

## 올바른 변수 대문자

일부 변수는 대문자를 사용합니다. JavaScript 변수는 대/소문자를 구분합니다. 변수를 정의할 때 반드시 올바른 대/소문자를 사용하십시오. 예를 들어, `s.eVar1 = 'Value'`는 유효하지만 `s.evar1 = 'Value'`는 유효하지 않습니다.

## 플러그인

일부 조직에서는 플러그인을 사용하여 Adobe Analytics의 구현을 개선합니다. AppMeasurement 버전을 업그레이드할 때 설치된 플러그인을 다시 포함하는 것을 잊지 마십시오. [!UICONTROL 코드 관리자]에서 만든 코드에는 플러그인 코드가 없습니다. 이전 버전의 AppMeasurement로 되돌려야 하는 경우에 대비하여 기존 코드의 사본을 만드십시오.

## 변수 값의 공백

HTML에는 공백을 만드는 문자가 몇 개 있습니다. 이런 문자에는 공백, 탭 및 캐리지 리턴(또는 줄 바꿈)이 있습니다. 다음 예를 생각해 보십시오.

```html
<head>
  <title>
    Home Page
  </title>
</head>
<body>
<script language="javascript">
  s.pageName = document.title;
</script>
</body>
```

이 경우 `document.title`은 `s.pageName`을 채우며, 이 변수는 &quot;홈 페이지&quot; 값을 받습니다. 그러나 일부 브라우저는 공백을 다르게 해석할 수 있습니다. 결과는 다음 두 가지 예 중 하나일 수 있습니다.

```js
s.pageName = "Home Page";
```

```js
s.pageName = "        Home Page";
```

이 두 변수 값은 Adobe Analytics에서 별개로 간주됩니다. 하지만 이 공백은 표시를 위해 자동으로 제거됩니다. 그 결과, 겉보기에 동일한 두 개의 &quot;홈 페이지&quot; 라인 항목을 표시하는 보고서가 생깁니다. 변수 값에 원하는 값의 앞 또는 뒤로 공백이 없는지 확인하십시오.
