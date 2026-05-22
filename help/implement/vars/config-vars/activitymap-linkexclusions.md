---
title: ActivityMap.linkExclusions
description: 링크 이름별로 Activity Map 데이터를 필터링합니다.
role: Admin, Developer
feature: Appmeasurement Implementation
exl-id: 9fc95016-362d-4c21-806e-e23adce9b6f7
TQID: 'https://experienceleague.adobe.com/m4ovqFSZBZ88KFm8lnKRI7z5wbbTNZygEj8koL6HC6E'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 206
ht-degree: 17%

---

# ActivityMap.linkExclusions

`ActivityMap.linkExclusions` 변수를 사용하면 [Activity Map 링크](/help/components/dimensions/activity-map-link.md) 차원의 텍스트를 기반으로 Activity Map 데이터를 선택적으로 필터링하거나 제외할 수 있습니다.

## 웹 SDK 확장의 링크 제외

**[!UICONTROL 클릭 데이터 수집 사용]**&#x200B;이 활성화되면 **[!UICONTROL 필터 클릭 속성]** 콜백 코드 블록을 사용하십시오. 이 코드 블록 내에서 `content.linkName`의 값을 확인하고 값을 변경하거나 링크 추적 데이터 수집을 중단할 수 있습니다.

## 웹 SDK JavaScript 라이브러리에서 링크 제외

[`clickCollectionEnabled`](https://experienceleague.adobe.com/kr/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled)이(가) 활성화되면 `clickCollection` 개체에서 `filterClickDetails` 콜백을 사용합니다. 이 콜백 내에서 `linkName`의 값을 확인하고 값을 변경하거나 링크 추적 데이터 수집을 중단할 수 있습니다.

```js
alloy("configure", {
  clickCollectionEnabled: true,
  clickCollection: {
    filterClickDetails: function(content) {
      // If the link is a clickable telephone number, anonymize it
      if(content.linkUrl.includes("tel:")) {
        content.linkName = content.linkUrl = "Phone number";
      }
      // If the link is an email address, anonymize it
      if(content.linkUrl.includes("mailto:")) {
        content.linkName = content.linkUrl = "Email address";
      }
    }
  }
});
```

## Adobe Analytics 확장을 사용하여 링크 제외

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement을 사용하는 s.ActivityMap.linkExclusions

`s.ActivityMap.linkExclusions` 변수는 Activity Map 추적에서 제외할 구문의 쉼표로 구분된 값이 포함된 문자열입니다. 구문이 [Activity Map 링크](/help/components/dimensions/activity-map-link.md) 차원에 수집된 값과 일치하는 경우 모든 Activity Map 데이터가 히트에서 제거됩니다. 이 변수는 `linkUrl`이(가) 아닌 `linkName`을(를) 봅니다.

```html
<script>
  var s = s_gi("examplersid");
  s.ActivityMap.linkExclusions = "Contact";
</script>

<!-- Clicking this link tracks normally -->
<a href="products.html">View our products</a>

<!-- Activity Map data is not tracked for this link -->
<a href="mailto:user@example.com">Contact this user</a>
```
