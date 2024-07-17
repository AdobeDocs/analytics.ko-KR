---
title: ActivityMap.regionIDAttribute
description: 영역을 결정하기 위해 Activity Map이 찾는 속성을 변경합니다.
feature: Variables
role: Admin, Developer
source-git-commit: 05010d58ba2a3376473097e9d4543ee4415e83e1
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 10%

---

# ActivityMap.regionIDAttribute

`ActivityMap.regionIDAttribute` 변수를 사용하면 [Activity Map 영역](/help/components/dimensions/activity-map-region.md) 차원을 결정할 때 Activity Map이 찾는 특성을 변경할 수 있습니다. `id` 특성이 Activity Map 영역에 유용하지 않은 방식으로 사이트가 구성된 경우 이 변수를 설정하여 다른 특성을 볼 수 있습니다.

## Web SDK 확장의 지역 ID 속성

**[!UICONTROL 클릭 데이터 수집 사용]**&#x200B;이 활성화되면 **[!UICONTROL 필터 클릭 속성]** 콜백 코드 블록을 사용하십시오. 이 코드 블록 내에서 `content.clickedElement`의 값을 확인하고 값을 변경하거나 링크 추적 데이터 수집을 중단할 수 있습니다.

## 웹 SDK JavaScript 라이브러리의 지역 ID 속성

[`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled)이(가) 활성화되면 `clickCollection` 개체에서 `filterClickDetails` 콜백을 사용합니다. 이 콜백 내에서 `clickedElement`의 값을 확인하고 수집된 영역의 논리를 사용자 지정할 수 있습니다.

```js
alloy("configure", {
  clickCollectionEnabled: true,
  clickCollection: {
    filterClickDetails: function(content) {
      // If the clicked element was in a table, set the region to the contents of the data-custom attribute
      // If the clicked element was not in a table, or if the data-custom attribute doesn't exist, leave region as-is
      content.region = content.clickedElement.closest('table')?.getAttribute('data-custom') || content.region;
    }
  }
});
```

## Adobe Analytics 확장을 사용하는 지역 ID 속성

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement을 사용하는 s.ActivityMap.regionIDAttribute

`s.ActivityMap.regionIDAttribute` 변수는 [Activity Map 영역](/help/components/dimensions/activity-map-region.md) 차원을 결정하는 특성을 나타내는 문자열입니다. 이 변수는 기본적으로 `id`(으)로 설정됩니다. 이 변수를 변경하면 Activity Map은 더 이상 `id` 특성을 찾지 않지만 영역을 결정하는 다른 기준(예: 의미 체계 요소)을 찾습니다.

```html
<script>
  var s = s_gi("examplersid");
  s.ActivityMap.regionIDAttribute = "data-custom";
</script>

<!-- Clicking any of these links populates the region dimension with 'left-nav' -->
<div id="676967617A656C6C65" data-custom="left-nav">
  <a href="index.html">Home</a>
  <a href="products.html">View our products</a>
  <a href="contact.html">Contact us</a>
</div>
```
