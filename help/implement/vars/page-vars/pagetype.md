---
title: pageType
description: 현재 페이지가 404 오류인지 판단합니다.
feature: Appmeasurement Implementation
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/SD-hwWJmZby-y99FIZHrnevSBsVqD6T5gwovn5tJfxo'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 75%

---

# pageType

`pageType` 변수는 404 오류와 같이 사이트에서 오류 페이지를 지정하는 데 사용되는 플래그입니다. 이 변수에 문자열 `errorPage`가 포함되어 있으면 “페이지를 찾을 수 없음” [차원](/help/components/dimensions/pages-not-found.md) 및 [지표](/help/components/metrics/pages-not-found.md)가 채워집니다.

>[!IMPORTANT]
>
>오류가 아닌 페이지에서 이 변수를 설정하지 마십시오.

## Web SDK를 사용하는 페이지 유형

채널은 다음 변수에 매핑됩니다.

* [XDM 개체](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webPageDetails.isErrorPage` - 이 XDM 필드는 부울입니다. 오류 페이지로 플래그를 지정하려면 `true`(으)로 설정하고, 오류 페이지가 아닌 경우 `false`(으)로 설정하십시오.
* [데이터 개체](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.pageType` - 이 데이터 개체 필드는 문자열입니다. `"errorPage"`(으)로 설정하여 플래그를 지정하십시오.

## Adobe Analytics 확장을 사용하는 페이지 유형

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 정의 코드 편집기의 s.pageType

`s.pageType` 변수는 값 `errorPage`가 유일하게 유효한 값인 문자열입니다. 이 변수는 404 페이지처럼 사이트의 어떤 오류 페이지에서든 이 값으로 설정하십시오.

```js
s.pageType = "errorPage";
```

>[!TIP]
>
>방문자가 사이트에서 당면하는 특정 오류에 대한 자세한 정보를 사용자가 알 수 있도록 오류 코드를 수집하려면 eVar를 사용하십시오.
