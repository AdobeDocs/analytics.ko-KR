---
title: pageUrl
description: 사이트에서 자동으로 수집된 페이지 URL을 무시합니다.
feature: Appmeasurement Implementation
exl-id: 411f894d-c31f-4d07-9568-b0b02786735d
role: Admin, Developer
TQID: https://experienceleague.adobe.com/DZM2tZlfVX0g9OYMj6tPFuHInBZdBrboJ4vGz16Lfrs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 310
ht-degree: 84%

---

# pageUrl

AppMeasurement는 각 히트에서 페이지 URL을 자동으로 수집합니다. AppMeasurement에서 자동으로 수집한 페이지 URL을 무시하려면 이 변수를 사용할 수 있습니다. 대부분의 경우 이 변수를 설정할 필요가 없습니다.

>[!NOTE]
>
>이 변수는 Analysis Workspace에서 사용할 수 있는 차원이 아닙니다. 이 변수는 Data Warehouse 및 데이터 피드에서만 사용할 수 있습니다. 또한 Adobe 데이터 수집 서버는 모든 [링크 추적](/help/implement/vars/functions/tl-method.md) 이미지 요청에서 이 차원을 제거합니다. 페이지 URL을 Analysis Workspace에서 차원으로 사용하거나 링크 추적 히트에 이 차원을 사용하려는 경우 모든 히트에서 `pageURL` 변수를 [eVar](evar.md)에 전달하는 것이 좋습니다.

## 웹 SDK을 사용하는 페이지 URL

페이지 URL은 다음 변수에 매핑됩니다.

* [XDM 개체](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webPageDetails.URL`
* [데이터 개체](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.pageURL` 또는 `data.__adobe.analytics.g`

## Adobe Analytics 확장을 사용한 페이지 URL

Adobe Experience Platform 데이터 수집의 Analytics 확장은 페이지 URL을 자동으로 채웁니다. 하지만 Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 페이지 URL 재정의를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3. **[!UICONTROL 규칙]** 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. **[!UICONTROL 작업]**&#x200B;에서 기존 **[!UICONTROL Adobe Analytics - 변수 설정]** 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. **[!UICONTROL 확장 기능]** 드롭다운 목록을 Adobe Analytics로 설정하고 **[!UICONTROL 액션 유형]**&#x200B;을 **[!UICONTROL 변수 설정]**&#x200B;으로 설정합니다.
6. **[!UICONTROL 페이지 URL]** 섹션을 찾습니다.

페이지 URL을 어떤 문자열 값으로든 설정할 수 있습니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.pageURL

`s.pageURL` 변수는 페이지의 URL을 포함하는 문자열입니다. AppMeasurement는 이 변수를 자동으로 수집하지만 원하는 경우 해당 값을 무시할 수 있습니다.

```js
s.pageURL = "https://example.com";
```

보고서에서 페이지 URL을 차원으로 사용하려면 구현에서 다음 내용을 사용하는 것이 좋습니다.

```js
// Set eVar1 to page URL without protocol or query strings
s.eVar1 = window.location.hostname + window.location.pathname;
```

`digitalData` [데이터 레이어](../../prepare/data-layer.md)를 사용하는 경우:

```js
s.pageURL = digitalData.page.pageInfo.destinationURL;
```
