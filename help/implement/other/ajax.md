---
title: AJAX를 사용하여 구현
description: AJAX를 사용하여 사이트에서 Adobe Analytics를 구현하는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: 0439440e10dddf8a5d64e4ea8f9868b521e5ca20

---


# AJAX를 사용하여 구현

AJAX 파섹

Adobe Analytics는 일반적으로 페이지를 다시 로드하여 Analytics 추적 개체를 재설정합니다. 다른 URL로 이동할 때마다 모든 Analytics 변수가 재설정되고 다시 정의할 수 있습니다. 사이트에서 AJAX를 사용하는 경우 페이지 새로 고침 부족 문제를 중심으로 구현을 조정하여 히트 간에 데이터가 잘못 지속되지 않도록 하십시오.

변수 값을 지우기 위한 측정값이 있는 경우 AJAX를 사용하는 사이트에서 Adobe Analytics를 구현하는 것은 대부분 다른 구현 방법과 동일합니다.

## 상호 작용 및 히트 유형 결정

AJAX를 사용하는 페이지는 일반적으로 다시 로드되지 않으므로 사용자가 사이트에서 수행할 수 있는 여러 가지 상호 작용이 있습니다. Adobe Analytics를 구현할 때는 페이지 보기를 링크 추적 호출과 구분해야 합니다. 사용자가 사이트에서 취할 수 있는 각 상호 작용에 대해 다음 질문을 고려하십시오.

*사용자가 내 사이트와 상호 작용할 때 이 상호 작용은 새 페이지로 분류할 수 있도록 페이지의 컨텐츠가 충분히 변경됩니까?*

* 답변이 **예인**&#x200B;경우 페이지 보기 추적 호출(`s.t()`)을 사용하는 것이 좋습니다.
* 대답이 **없는**&#x200B;경우 링크 추적 호출(`s.tl()`)을 사용하여 해당 상호 작용을 추적하는 것이 좋습니다.

> [!NOTE] 모든 상호 작용 또는 클릭을 기록할 필요는 없습니다. 추적해야 할 가장 중요한 작업을 신중하게 고려하고 그에 따라 데이터를 Adobe로 보냅니다.

## 각 페이지에서 변수 지우기

페이지가 다시 로드되지 않으므로 AJAX를 사용하여 페이지에서 변수 값이 유지됩니다. 따라서, 변수 값을 지우려면 특별한 숙박이 필요하므로 히트 간에 잘못 지속되지 않습니다. Adobe는 변수 값을 쉽게 지울 수 있는 [`clearVars`](../vars/functions/clearvars.md) 기능을 제공합니다. 각 히트를 Adobe로 보낸 후 다음 히트에 대한 변수 값을 설정하기 전에 이 함수를 사용해야 합니다.

> [!TIP] 이 `clearVars()` 함수는 H 코드에서 사용할 수 없습니다. AppMeasurement로 업그레이드하지 않은 경우 각 Analytics 변수 값을 빈 문자열로 설정합니다.

## 예

다음 예제에서는 간단한 JavaScript를 사용하여 기존 변수 값을 지우고 새 값을 설정한 다음 이미지 요청을 Adobe에 보냅니다.

```js
s.clearVars();
s.pageName = "Example AJAX page";
s.eVar1="Example value";
void(s.t());
```

다음 예제는 JQuery `done` 함수의 `.ajax` 콜백에서 추적 호출을 보여줍니다.

```js
$.ajax({
  url: "example.html",
  dataType: "html"
})
  .done(function( response ) {
    $( "#content" ).html( response );
  s.clearVars();
  s.pageName = $( "h1:first" ).text();
  s.t();
  });
```
