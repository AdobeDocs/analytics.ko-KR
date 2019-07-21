---
description: s.tl() 함수를 사용하여 사용자 지정 요소를 추적하고 다이내믹 컨텐츠에 대한 오버레이 렌더링을 구성할 수 있습니다.
seo-description: s.tl() 함수를 사용하여 사용자 지정 요소를 추적하고 다이내믹 컨텐츠에 대한 오버레이 렌더링을 구성할 수 있습니다.
seo-title: s. tl () 함수 사용
solution: Analytics
title: s. tl () 함수 사용
topic: Activity Map
uuid: 59 e 062 af -6 a 1 c -46 ff -9 c 3 b -6 cf 7 a 0453711
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# s. tl () 함수 사용

s.tl() 함수를 사용하여 사용자 지정 요소를 추적하고 다이내믹 컨텐츠에 대한 오버레이 렌더링을 구성할 수 있습니다.

## Tracking custom elements {#section_5D6688DFFFC241718249A9A0C632E465}

[s.tl() 함수](https://marketing.adobe.com/resources/help/en_US/sc/implement/function_tl.html)를 Activity Map AppMeasurement 모듈의 일부로 사용하면 클릭한 개체를 추적할 수 있습니다. 앵커 태그나 이미지 요소가 아닌 개체도 추적할 수 있습니다. s.tl을 사용하면, 페이지 로드를 발생시키지 않는 모든 사용자 지정 요소를 추적할 수 있습니다.

s.tl 함수에서 현재 종료 링크, 사용자 지정 링크 등을 식별하는 데 사용하는 linkName 매개 변수는 지금 Activity Map 변수용 링크 ID를 식별하는 데에도 사용됩니다.

```
s.tl(this,linkType, 
<b>linkName</b>,variableOverrides,doneAction)
```

다시 말해, s.tl을 사용하여 사용자 지정 요소를 추적하는 경우, 링크 ID는 s.tl 함수에서 세 번째 매개 변수(linkName)로 전달된 값에서 가져옵니다. Activity Map에서 [기본 추적](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md)에 사용되는 표준 링크 추적 알고리즘에서는 가져오지 않습니다.

## Overlay rendering for dynamic content {#section_FD24B61A732149C7B58BA957DD84A5E7}

s.tl() 함수가 HTML 요소의 클릭 이벤트에서 바로 호출되면 웹 페이지가 로드될 때 해당 요소에 대한 오버레이가 Activity Map에 표시될 수 있습니다. 예:

```
<div onclick="s.tl(this,'o','some link name')">Text to click on</a>
```

초기 페이지 로드 후 웹 페이지 컨텐츠가 페이지에 추가될 때마다 s.tl 함수가 간접적으로 호출되고 Adobe에서는 새 컨텐츠가 명시적으로 활성화되거나 클릭되지 않는 한 해당 새 컨텐츠에 대한 오버레이를 표시할 수 없습니다. 그런 다음 새 링크 컬렉션 프로세스가 Activity Map에서 트리거됩니다.

s.tl() 함수가 HTML 요소의 클릭 이벤트에서 바로 호출되지 않으면 사용자가 해당 요소를 클릭한 후에만 Activity Map에서 오버레이를 표시할 수 있습니다. 다음은 s.tl() 함수가 간접적으로 호출되는 예입니다.

```
<div onclick="someFn(event)"></div> 
 <script>function someFn (event) 
 {    
 s.tl(event.srcElement,'o','some link name'); 
 } 
 </script>
```

Activity Map이 다이내믹 컨텐츠 링크를 오버레이하는 가장 좋은 방법은 반환 값이 s.tl로 전달되는 함수와 동일한 함수를 호출하도록 사용자 지정된 ActivityMap.link 함수를 설정하는 것입니다. 다음은 그 예입니다.

```
var originalLinkFunction = s.ActivityMap.link; 
s.ActivityMap.link = function(element,linkName){ 
    return linkName ||      // if this is a s.tl call, just return string passed 
        makeLinkName(element) || // this is ActivityMap reporting time 
        originalLinkFunction(element,linkName); // our custom function didn't return anything, so just return the default ActivityMap Link 
};
```

```
<button type=”button” onclick=”s.tl(this,’o’,makeLinkName(this)”>Add To Cart</button>
```

여기에서는 호출 시 다음 세 가지 중 하나를 수행하도록 ActivityMap.link 함수를 재정의했습니다.

1. linkName이 전달되면, s.tl()이 ActivityMap.link를 호출하므로, s.tl이 linkName으로 전달한 내용을 반환합니다.
1. 보고 시 Activity Map에 의해 호출되므로 linkName은 전달되지 않습니다. 따라서 링크 요소로 makeLinkName()을 호출합니다. This is the crucial step here - the “makeLinkName(element)” call should be the same at the s.tl call’s 3rd argument in the `<button>` tag. 이는 s.tl이 호출되면 makeLinkName에 의해 반환된 문자열을 추적한다는 것을 의미합니다. Activity Map은 페이지의 링크에 대해 보고할 때 동일한 호출을 사용하여 링크를 만듭니다.
1. 최종 해결 방법은 기본 ActivityMap 링크 함수의 원래 반환 값을 반환하는 것입니다. 기본 사례에서 이 참조를 사용하여 호출하면 makeLinkName에 대한 사용자 지정 코드를 무시하거나 작성하기만 해도 되며, 페이지의 모든 링크에 대해 링크 반환 값을 제공하지 않아도 됩니다.
