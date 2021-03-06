---
title: Activity Map에서 tl() 메서드 사용
description: tl() 메서드를 사용하여 사용자 지정 요소를 추적하고 다이내믹 컨텐츠에 대한 오버레이 렌더링을 구성할 수 있습니다.
feature: Activity Map
role: User, Admin
exl-id: e4e32de7-0e46-413a-abc9-9707e273903d
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 43%

---

# Activity Map에서 `tl()` 메서드 사용

`tl()` 메서드를 사용하여 사용자 지정 요소를 추적하고 다이내믹 컨텐츠에 대한 오버레이 렌더링을 구성할 수 있습니다.

## 사용자 지정 요소 추적

[`tl()` 메서드](/help/implement/vars/functions/tl-method.md)를 Activity Map AppMeasurement 모듈의 일부로 사용하면 클릭한 개체를 추적할 수 있습니다. 앵커 태그나 이미지 요소가 아닌 개체도 추적할 수 있습니다. `tl()` 을 사용하면 페이지 로드를 발생시키지 않는 모든 사용자 지정 요소를 추적할 수 있습니다.

`tl()` 메서드에서 현재 종료 링크, 사용자 지정 링크 등을 식별하는 데 사용하는 `linkName` 매개 변수 지금 Activity Map 변수용 링크 ID를 식별하는 데에도 사용됩니다.

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

즉, `tl()` 을 사용하여 사용자 지정 요소를 추적하는 경우, 링크 ID는 `tl()` 메서드에서 세 번째 매개 변수(링크 이름)로 전달된 값에서 가져옵니다. Activity Map에서 [기본 추적](activitymap-link-tracking-methodology.md)에 사용되는 표준 링크 추적 알고리즘에서는 가져오지 않습니다.

## 다이내믹 컨텐츠를 위한 오버레이 렌더링

`tl()` 메서드가 HTML 요소의 클릭 이벤트에서 바로 호출되면 웹 페이지가 로드될 때 Activity Map이 해당 요소에 대한 오버레이를 표시할 수 있습니다. 예:

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

다이내믹 컨텐츠 링크를 오버레이하는 가장 좋은 방법은 반환 값이 `tl()`에 전달되는 함수와 동일한 함수를 호출하도록 사용자 지정된 `ActivityMap.link` 함수를 설정하는 것입니다. 예를 들어,

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

여기에서 호출될 때 세 가지 작업 중 하나를 수행하기 위해 `ActivityMap.link` 함수를 재정의했습니다.

1. `linkName`이 전달된 경우 `tl()`에 의해 호출되었으므로 `linkName`(으)로 전달된 `tl()`만 반환합니다.
2. 보고 시 Activity Map이 호출하면 `linkName`이 전달되지 않으므로 링크 요소를 사용하여 `makeLinkName()`을 호출하십시오. 이는 중요한 단계입니다. `makeLinkName(element)` 호출은 `<button>` 태그에 있는 `tl()` 호출의 세 번째 인수와 동일해야 합니다. 즉, `tl()`이 호출되면 `makeLinkName()`에서 반환된 문자열을 추적합니다. Activity Map이 페이지의 링크에 대해 보고할 때 동일한 호출을 사용하여 링크를 만듭니다.
3. 최종 해결 방법은 기본 ActivityMap 링크 함수의 원래 반환 값을 반환하는 것입니다. 기본 경우에서 이 참조를 호출 중심으로 유지하면 `makeLinkName()`에 대한 사용자 지정 코드를 무시하거나 작성해야 하며 페이지의 모든 링크에 대한 링크 반환 값을 설정할 필요가 없습니다.
