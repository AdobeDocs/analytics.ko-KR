---
title: Util.getQueryParam
description: 쿼리 문자열 매개 변수의 값을 반환합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Util.getQueryParam

브라우저 URL의 쿼리 문자열 매개 변수에는 Analytics에 대한 중요한 데이터가 자주 포함됩니다. 이 `Util.getQueryParam()` 메서드를 사용하여 쿼리 문자열에서 데이터를 검색합니다.

## Adobe Experience Platform Launch에서 쿼리 문자열 매개 변수 데이터 가져오기

데이터 요소의 값을 설정하여 쿼리 문자열 매개 변수 데이터를 가져올 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 다음 원하는 데이터 요소를 클릭합니다(또는 데이터 요소 만들기). [!UICONTROL Data Elements]
4. 드롭다운을 [!UICONTROL Extension] 설정하고 [!UICONTROL Core]을 [!UICONTROL Data Element Type] [!UICONTROL Query String Parameter]설정합니다.
5. 텍스트 필드에 쿼리 문자열 매개 변수를 입력합니다.

쿼리 문자열 매개 변수 값은 데이터 요소에 저장됩니다. 그런 다음 규칙의 데이터 요소를 참조하여 Analytics 변수를 할당할 수 있습니다.

## s.Util.getQueryParam(), AppMeasurement 및 Launch 사용자 지정 코드 편집기

브라우저 URL에서 쿼리 문자열 값을 검색하려면 `s.Util.getQueryParam()` 메서드를 호출합니다. 쿼리 문자열 매개 변수를 포함하는 문자열 인수가 필요합니다. 이 메서드는 Analytics 변수에 할당할 수 있는 문자열을 반환합니다.

```js
s.eVar1 = s.Util.getQueryParam("cid");
```

두 번째 선택적 인수를 사용하면 쿼리 문자열 매개 변수를 확인할 문자열을 지정할 수 있습니다. 기본적으로 유틸리티는 브라우저 URL을 확인합니다.

```js
// Search a custom string for query string parameter
var customString = "https://example.com?q=search";

// eVar1 is set to "search"
s.eVar1 = s.Util.getQueryParam("q",customString);
```

세 번째 선택적 인수를 사용하면 쿼리 문자열 구분 기호를 사용자 지정할 수 있습니다. Its default value is `&`. 쿼리 문자열에서 다른 구분 기호를 사용하는 경우 이 값을 변경할 수 있습니다.

```js
var customString = "https://example.com?q1=value1;q2=value2;q3=value3";

// eVar1 is set to "value2"
s.eVar1 = s.Util.getQueryParam("q2",customString,";");
```

> [!TIP] 이름이 같은 유사한 플러그인을 [`s.getQueryParam`](../plugins/getqueryparam.md) 사용할 수 있습니다. 이 플러그인에는 더 많은 고급 기능이 포함되어 있지만, 기본적으로 AppMeasurement에 포함되지 않고 보다 복잡합니다.
