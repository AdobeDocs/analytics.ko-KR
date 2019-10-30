---
description: s.tl() 함수를 사용하여 사용자 지정 요소를 추적하고 다이내믹 컨텐츠에 대한 오버레이 렌더링을 구성할 수 있습니다.
seo-description: s.tl() 함수를 사용하여 사용자 지정 요소를 추적하고 다이내믹 컨텐츠에 대한 오버레이 렌더링을 구성할 수 있습니다.
seo-title: s. tl() 함수 사용
solution: Analytics
title: s. tl() 함수 사용
topic: Activity Map
uuid: 59e062af-6a1c-46ff-9c3b-6cf7a0453711
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# s. tl() 함수 사용

s.tl() 함수를 사용하여 사용자 지정 요소를 추적하고 다이내믹 컨텐츠에 대한 오버레이 렌더링을 구성할 수 있습니다.

## Tracking custom elements {#section_5D6688DFFFC241718249A9A0C632E465}

[s.tl() 함수](https://marketing.adobe.com/resources/help/en_US/sc/implement/function_tl.html)를 AppMeasurement 모듈의 일부로 사용하면 클릭한 개체를 추적할 수 있습니다. 앵커 태그나 이미지 요소가 아닌 개체도 추적할 수 있습니다. [!DNL Activity Map] s.tl을 사용하면, 페이지 로드를 발생시키지 않는 모든 사용자 지정 요소를 추적할 수 있습니다.

s.tl 함수에서 현재 종료 링크, 사용자 지정 링크 등을 식별하는 데 사용하는 linkName 매개 변수는 is now also used to identify the Link ID for the [!DNL Activity Map] variable.

```
s.tl(this,linkType, 
<b>linkName</b>,variableOverrides,doneAction)
```

다시 말해, s.tl을 사용하여 사용자 지정 요소를 추적하는 경우, 링크 ID는 s.tl 함수에서 세 번째 매개 변수(linkName)로 전달된 값에서 가져옵니다. It is not pulled from the standard link tracking algorithm that is used for [default tracking](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md) in [!DNL Activity Map].

## Overlay rendering for dynamic content {#section_FD24B61A732149C7B58BA957DD84A5E7}

When the s.tl() function is called directly from the HTML element's on-click event, [!DNL Activity Map] can display an overlay for that element when the web page is loaded. 예:

```
<div onclick="s.tl(this,'o','some link name')">Text to click on</a>
```

초기 페이지 로드 후 웹 페이지 컨텐츠가 페이지에 추가될 때마다 s.tl 함수가 간접적으로 호출되고 Adobe에서는 새 컨텐츠가 명시적으로 활성화되거나 클릭되지 않는 한 해당 새 컨텐츠에 대한 오버레이를 표시할 수 없습니다. Then a new link collection process is triggered from [!DNL Activity Map].

When the s.tl() function is not called directly from the HTML element's on-click event, [!DNL Activity Map] can only display overlay once that element has been clicked by the user. 다음은 s.tl() 함수가 간접적으로 호출되는 예입니다.

```
<div onclick="someFn(event)"></div> 
 <script>function someFn (event) 
 {    
 s.tl(event.srcElement,'o','some link name'); 
 } 
 </script>
```

The best way for [!DNL Activity Map] to overlay dynamic content links is to have a customized ActivityMap.link function set up to call the same function whose return value is passed to s.tl. 예를 들면 다음과 같습니다.

```
var originalLinkFunction = s.ActivityMap.link; 
s.ActivityMap.link = function(element,linkName){ 
    return linkName ||      // if this is a s.tl call, just return string passed 
        makeLinkName(element) || // this is ActivityMap reporting time 
        originalLinkFunction(element,linkName); // our custom function didn't return anything, so just return the default ActivityMap Link 
};
```

```
<button type="button" onclick="s.tl(this,'o',makeLinkName(this)">Add To Cart</button>
```

여기에서는 호출 시 다음 세 가지 중 하나를 수행하도록 ActivityMap.link 함수를 재정의했습니다.

1. linkName이 전달되면, s.tl()이 ActivityMap.link를 호출하므로, s.tl이 linkName으로 전달한 내용을 반환합니다.
1. This is called by [!DNL Activity Map] at reporting time, so a linkName is never passed, and so call makeLinkName() with the link element. This is the crucial step here - the "makeLinkName(element)" call should be the same at the s.tl call's 3rd argument in the `<button>` tag. 이는 s.tl이 호출되면 makeLinkName에 의해 반환된 문자열을 추적한다는 것을 의미합니다. When [!DNL Activity Map] reports on the links on the page, is uses the same call to make a link.
1. 최종 해결 방법은 기본 ActivityMap 링크 함수의 원래 반환 값을 반환하는 것입니다. 기본 사례에서 이 참조를 사용하여 호출하면 makeLinkName에 대한 사용자 지정 코드를 무시하거나 작성하기만 해도 되며, 페이지의 모든 링크에 대해 링크 반환 값을 제공하지 않아도 됩니다.
