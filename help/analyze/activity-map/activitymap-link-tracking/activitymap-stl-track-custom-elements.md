---
description: s.tl() 메서드를 사용하여 사용자 지정 요소를 추적하고 동적 내용에 대한 오버레이 렌더링을 구성할 수 있습니다.
title: s.tl() 메서드 사용
topic: Activity map
uuid: 59e062af-6a1c-46ff-9c3b-6cf7a0453711
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# 메서드 `tl()` 사용

You can use the `tl()` method to track custom elements and to configure overlay rendering for dynamic content.

## 사용자 지정 요소 추적 {#section_5D6688DFFFC241718249A9A0C632E465}

Using the [`tl()` method](/help/implement/vars/functions/tl-method.md) as part of the Activity Map AppMeasurement module lets you track any object that is clicked on, even objects that are not anchor tags or image elements. s.tl을 사용하면, 페이지 로드를 발생시키지 않는 모든 사용자 지정 요소를 추적할 수 있습니다.

In the `tl()` method, the `linkName` parameter that is currently used to identify the exit links, custom links, etc. 지금 Activity Map 변수용 링크 ID를 식별하는 데에도 사용됩니다.

```js
s.tl(this,linkType,linkName,variableOverrides)
```

In other words, if you use `s.tl()` to track your custom elements, the link ID is pulled from the value passed as the third parameter (linkName) in the `s.tl()` method. Activity Map에서 [기본 추적](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md)에 사용되는 표준 링크 추적 알고리즘에서는 가져오지 않습니다.

## 다이내믹 컨텐츠를 위한 오버레이 렌더링 {#section_FD24B61A732149C7B58BA957DD84A5E7}

s.tl() 함수가 HTML 요소의 클릭 이벤트에서 바로 호출되면 웹 페이지가 로드될 때 해당 요소에 대한 오버레이가 Activity Map에 표시될 수 있습니다. 예:

```html
<div onclick="s.tl(this,'o','Example custom link')">Example link text</a>
```

Whenever any web page content is added to the page after the initial page load, the `tl()` method is called indirectly and we cannot display overlays for that new content unless it is expressly activated/clicked. 그런 다음 새 링크 컬렉션 프로세스가 Activity Map에서 트리거됩니다.

When the `tl()` method is not called directly from the HTML element&#39;s on-click event, Activity Map can only display overlay once that element has been clicked by the user. Here is an example where the `tl()` method is called indirectly:

```html
<div onclick="someFn(event)"></div>
<script>function someFn (event)
{
  s.tl(event.srcElement,'o','Example custom link');
}
</script>
```

The best way for Activity Map to overlay dynamic content links is to have a customized ActivityMap.link function set up to call the same function whose return value is passed to `s.tl`. 예:

```js
var originalLinkFunction = s.ActivityMap.link;
s.ActivityMap.link = function(element,linkName) {
    return linkName ||      // if this is a s.tl call, just return string passed
        makeLinkName(element) || // this is ActivityMap reporting time
        originalLinkFunction(element,linkName); // our custom function didn't return anything, so just return the default ActivityMap Link
};
```

```html
<button type="button" onclick="s.tl(this,'o',makeLinkName(this)">Add To Cart</button>
```

여기에서는 호출 시 다음 세 가지 중 하나를 수행하도록 ActivityMap.link 함수를 재정의했습니다.

1. linkName이 전달되면, s.tl()이 ActivityMap.link를 호출하므로, s.tl이 linkName으로 전달한 내용을 반환합니다.
2. 보고 시 Activity Map에 의해 호출되므로 linkName은 전달되지 않습니다. 따라서 링크 요소로 makeLinkName()을 호출합니다. 이는 중요한 단계입니다. 다시 말해 &#39;makeLinkName(element)&#39; 호출은 `<button>` 태그에 있는 s.tl 호출의 세 번째 인수에서 동일해야 합니다. 이는 s.tl이 호출되면 makeLinkName에 의해 반환된 문자열을 추적한다는 것을 의미합니다. Activity Map은 페이지의 링크에 대해 보고할 때 동일한 호출을 사용하여 링크를 만듭니다.
3. 최종 해결 방법은 기본 ActivityMap 링크 함수의 원래 반환 값을 반환하는 것입니다. 기본 사례에서 이 참조를 사용하여 호출하면 makeLinkName에 대한 사용자 지정 코드를 무시하거나 작성하기만 해도 되며, 페이지의 모든 링크에 대해 링크 반환 값을 제공하지 않아도 됩니다.
