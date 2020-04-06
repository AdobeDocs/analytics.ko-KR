---
title: AJAX를 사용하여 구현
description: AJAX를 사용하여 Adobe Analytics를 구현하는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# AJAX를 사용하여 구현

AJAX는 새 페이지를 로드하지 않고 JavaScript 및 HTML을 사용하여 컨텐츠를 지우고 생성하는 방법입니다.

Adobe Analytics는 일반적으로 페이지 재로드를 통해 Analytics 추적 개체를 재설정합니다. 사용자가 다른 URL로 이동할 때마다 모든 Analytics 변수는 재설정되고 다시 정의할 수 있습니다. 사이트에서 AJAX를 사용할 때에는 페이지 새로 고침 부족 문제와 관련하여 구현을 조정함으로써 히트 간에 데이터가 잘못 지속되지 않도록 하십시오.

변수 값을 지우기 위한 적절한 수단이 준비되면 AJAX를 사용하는 사이트에서 Adobe Analytics를 구현하는 것은 대체로 다른 구현 방법과 동일합니다.

## 상호 작용 및 히트 유형 결정

AJAX를 사용하는 페이지는 일반적으로 다시 로드되지 않으므로 사용자가 사이트에서 수행할 수 있는 여러 가지 상호 작용이 있습니다. Adobe Analytics를 구현할 때에는 페이지 보기를 링크 추적 호출과 구분하도록 합니다. 사용자가 사이트에서 수행할 수 있는 각 상호 작용에 대해 다음 질문을 고려하십시오.

*사용자가 내 사이트와 상호 작용할 때 그러한 상호 작용으로 인해 해당 페이지의 컨텐츠가 새 페이지로 분류할 수 있도록 충분히 변경됩니까?*

* 답변이 **예**&#x200B;라면 페이지 보기 추적 호출(`s.t()`)을 사용하는 것이 좋습니다.
* 대답이 **아니요**&#x200B;이면 링크 추적 호출(`s.tl()`)을 사용하여 해당 상호 작용을 추적하는 것이 좋습니다.

>[!NOTE] 모든 상호 작용이나 클릭을 기록할 필요는 없습니다. 추적해야 할 가장 중요한 작업을 신중하게 고려하고 그에 따라 데이터를 Adobe로 보내십시오.

## 각 페이지에서 변수 지우기

페이지가 다시 로드되지 않으므로 변수 값은 AJAX를 사용하여 페이지에서 지속됩니다. 따라서, 변수 값이 히트 간에 잘못 지속되지 않도록 지우려면 특별한 방법이 필요하므로 습니다. Adobe에서는 변수 값을 쉽게 지울 수 있는 [`clearVars`](../vars/functions/clearvars.md) 함수를 제공합니다. 각 히트를 Adobe에 보낸 후 다음 히트에 대한 변수 값을 설정하기 전에 이 함수를 사용해야 합니다.

>[!TIP] `clearVars()` 함수는 H 코드에서는 사용할 수 없습니다. AppMeasurement로 업그레이드하지 않은 경우 각 Analytics 변수 값을 빈 문자열로 설정하십시오.

## 예

다음 예제에서는 간단한 JavaScript를 사용하여 기존 변수 값을 지우고 새 값을 설정한 후 이미지 요청을 Adobe에 보냅니다.

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
