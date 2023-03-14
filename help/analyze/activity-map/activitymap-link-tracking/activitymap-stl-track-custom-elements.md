---
title: Activity Map과 함께 tl() 메서드 사용
description: tl () 메서드를 사용하여 사용자 지정 요소를 추적하고 다이내믹 컨텐츠에 대한 오버레이 렌더링을 구성할 수 있습니다.
feature: Activity Map
role: User, Admin
exl-id: e4e32de7-0e46-413a-abc9-9707e273903d
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 43%

---

# 사용 `tl()` Activity Map이 있는 메서드

`tl()` 메서드를 사용하여 사용자 지정 요소를 추적하고 다이내믹 컨텐츠에 대한 오버레이 렌더링을 구성할 수 있습니다.

## 사용자 지정 요소 추적

[`tl()` 메서드](/help/implement/vars/functions/tl-method.md)를 Activity Map AppMeasurement 모듈의 일부로 사용하면 클릭한 개체를 추적할 수 있습니다. 앵커 태그나 이미지 요소가 아닌 개체도 추적할 수 있습니다. 사용 `tl()`로 설정되지 않은 모든 사용자 지정 요소를 추적할 수 있습니다.

`tl()` 메서드에서 현재 종료 링크, 사용자 지정 링크 등을 식별하는 데 사용하는 `linkName` 매개 변수 지금 Activity Map 변수용 링크 ID를 식별하는 데에도 사용됩니다.

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

즉, `tl()` 사용자 지정 요소를 추적하기 위해 링크 ID는에서 세 번째 매개 변수(링크 이름)로 전달된 값에서 가져옵니다. `tl()` 메서드를 사용합니다. Activity Map에서 [기본 추적](activitymap-link-tracking-methodology.md)에 사용되는 표준 링크 추적 알고리즘에서는 가져오지 않습니다.

## 다이내믹 컨텐츠를 위한 오버레이 렌더링

다음의 경우 `tl()` 메서드는 HTML 요소의 클릭 이벤트에서 직접 호출되며, 웹 페이지가 로드될 때 Activity Map에서 해당 요소에 대한 오버레이를 표시할 수 있습니다. 예:

```html
<a href="javascript:" onclick="s.tl(this,'o','Example custom link');">Example link text</a>
```

초기 페이지 로드 후 웹 페이지 컨텐츠가 페이지에 추가될 때마다 `tl()` 메서드가 간접적으로 호출되고 Adobe에서는 새 컨텐츠가 명시적으로 활성화되거나 클릭되지 않는 한 해당 새 컨텐츠에 대한 오버레이를 표시할 수 없습니다. 그런 다음 새 링크 컬렉션 프로세스가 Activity Map에서 트리거됩니다.

`tl()` 메서드가 HTML 요소의 클릭 이벤트에서 바로 호출되지 않으면 사용자가 해당 요소를 클릭한 후에만 Acitivity Map에서 오버레이를 표시할 수 있습니다. 다음은 `tl()` 메서드가 간접적으로 호출되는 예입니다.

```html
<a href="javascript:" onclick="someFn(event);">Example link text</a>
<script>function someFn (event)
{
  s.tl(event.srcElement,'o','Example custom link');
}
</script>
```

Activity Map이 다이내믹 콘텐츠 링크를 오버레이하는 가장 좋은 방법은 를 사용자 지정하는 것입니다 `ActivityMap.link` 반환 값이에 전달되는 함수와 동일한 함수를 호출하도록 설정된 함수 `tl()`. 예:

```js
var originalLinkFunction = s.ActivityMap.link;
s.ActivityMap.link = function(element,linkName)
{
    // if this is a s.tl call, just return string passed
    return linkName ||      
    // this is ActivityMap reporting time
    makeLinkName(element) ||
    // our custom function didn't return anything, so just return the default ActivityMap Link
    originalLinkFunction(element,linkName);
};
```

```html
<button type="button" onclick="s.tl(this,'o',makeLinkName(this)">Add To Cart</button>
```

여기에서는 을(를) 재정의했습니다. `ActivityMap.link` 함수를 호출하면 다음 세 가지 중 하나를 수행합니다.

1. If `linkName` 가 전달된 후 이 호출자: `tl()`, 그러니까 그냥 `tl()` 다음으로 전달됨 `linkName`.
2. 보고 시 Activity Map에서 호출하는 경우 `linkName` 은(는) 전달되지 않으므로 을 호출하십시오. `makeLinkName()` 와 함께 사용할 수 있습니다. 이것은 여기서 중요한 단계입니다 - `makeLinkName(element)` 호출은 와 동일해야 합니다. `tl()` 에서 호출의 세 번째 인수 `<button>` 태그에 가깝게 배치하십시오. 이는 다음과 같은 경우를 의미합니다. `tl()` 가 호출되면 가 반환하는 문자열을 추적합니다. `makeLinkName()`. Activity Map이 페이지의 링크에 대해 보고할 경우 동일한 호출을 사용하여 링크를 만듭니다.
3. 최종 해결 방법은 기본 ActivityMap 링크 함수의 원래 반환 값을 반환하는 것입니다. 이 참조를 주위에 유지하여 기본 사례에서 를 호출하면 의 사용자 지정 코드만 재정의하거나 작성하면 됩니다. `makeLinkName()` 또한 페이지의 모든 링크에 대한 링크 반환 값을 제안할 필요가 없습니다.
