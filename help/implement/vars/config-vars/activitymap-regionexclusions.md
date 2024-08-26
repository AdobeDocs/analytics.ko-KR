---
title: ActivityMap.regionExclusions
description: 영역별로 Activity Map 데이터를 필터링합니다.
role: Admin, Developer
feature: Variables
exl-id: 353282aa-860c-45dc-a6b0-8d9f1fa09f13
source-git-commit: bcab98e453247c74b7d96497d34e6aea9ca32bc7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 13%

---

# ActivityMap.regionExclusions

`ActivityMap.regionExclusions` 변수를 사용하면 [Activity Map 영역](/help/components/dimensions/activity-map-region.md) 차원에서 수집된 차원 항목을 기반으로 Activity Map 데이터를 선택적으로 필터링하거나 제외할 수 있습니다.

## 웹 SDK 확장의 영역 제외

**[!UICONTROL 클릭 데이터 수집 사용]**&#x200B;이 활성화되면 **[!UICONTROL 필터 클릭 속성]** 콜백 코드 블록을 사용하십시오. 이 코드 블록 내에서 `content.linkRegion`의 값을 확인하고 값을 변경하거나 링크 추적 데이터 수집을 중단할 수 있습니다.

## 웹 SDK JavaScript 라이브러리의 영역 제외

[`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled)이(가) 활성화되면 `clickCollection` 개체에서 `filterClickDetails` 콜백을 사용합니다. 이 콜백 내에서 `linkRegion`의 값을 확인하고 값을 변경하거나 링크 추적 데이터 수집을 중단할 수 있습니다.

```js
alloy("configure", {
  clickCollectionEnabled: true,
  clickCollection: {
    filterClickDetails: function(content) {
      // If the clicked region has personal links in it, don't send click data
      if(content.linkRegion.includes("personal")) {
        return false;
      }
    }
  }
});
```

## Adobe Analytics 확장을 사용한 영역 제외

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement을 사용하는 s.ActivityMap.regionExclusions

`s.ActivityMap.regionExclusions` 변수는 Activity Map 추적에서 제외할 쉼표로 구분된 구문을 포함하는 문자열입니다. 구문이 [Activity Map 영역](/help/components/dimensions/activity-map-region.md) 차원에서 수집된 값과 일치하는 경우 모든 Activity Map 데이터가 히트에서 제거됩니다.

```html
<script>
  var s = s_gi("examplersid");
  s.ActivityMap.regionExclusions = "contact";
</script>

<!-- Clicking any of these links tracks normally. -->
<!-- While "contact" is present, it is not tracked in region. The region is "nav" -->
<nav>
  <a href="index.html">Home</a>
  <a href="products.html">View our products</a>
  <a href="contact.html">Contact us</a>
</nav>

<!-- Activity Map data is not tracked for any of these links. -->
<!-- All these links belong to the region "Personal contact information" -->
<div id="personal-contact-information">
 <a href="mailto:user@example.com">Example user</a>
 <a href="mailto:user2@example.com">Example user 2</a>
 <a href="mailto:user3@example.com">Example user 3</a>
</div>
```
