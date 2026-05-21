---
title: 레퍼러
description: 히트에 대해 자동으로 수집된 레퍼러를 무시합니다.
feature: Appmeasurement Implementation
exl-id: 09a76de9-0689-424a-aead-3fdff1709fd9
role: Admin, Developer
TQID: https://experienceleague.adobe.com/YsYfgjFNDiJoQbvPU-XoB6bQt2IAriP1qmkOqc2lFDk
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: c069c44e-5426-4c1a-accc-8028662f2fdeid: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 85%

---

# 레퍼러

`referrer` 변수는 보고서에서 자동으로 수집된 레퍼러를 무시합니다. 이 변수는 리디렉션하거나 방문자를 일시적으로 결제 프로세서에 전달하는 동안 등 레퍼러가 손실될 수 있는 상황에서 유용하며, &#39;레퍼러&#39; 및 &#39;참조 도메인&#39; 차원을 채우는 데에도 도움이 됩니다.

## 웹 SDK을 사용하는 레퍼러

레퍼러는 다음 변수에 매핑됩니다.

* [XDM 개체](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webReferrer.URL`
* [데이터 개체](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.referrer`

사용 가능한 경우 웹 SDK은 보낸 모든 이벤트에 `web.webReferrer.URL`을(를) 자동으로 포함합니다.

## Adobe Analytics 확장을 사용한 레퍼러

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 레퍼러를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장 기능] 드롭다운 목록을 Adobe Analytics로 설정하고 [!UICONTROL 액션 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL 레퍼러] 섹션을 찾습니다.

레퍼러를, 데이터 요소를 포함한 어떤 문자열 값으로든 설정할 수 있습니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.referrer

`s.referrer` 변수는 이전 페이지의 URL을 포함하는 문자열입니다. 이 변수는 최대 255바이트를 저장할 수 있습니다. 255바이트보다 큰 값은 잘립니다. AppMeasurement는 이 변수를 자동으로 `document.referrer`로 설정합니다. 자동으로 수집된 값을 무시하려면 이 변수를 설정할 필요가 없습니다.

```js
s.referrer = "https://example.com";
```

`digitalData` [데이터 레이어](../../prepare/data-layer.md)를 사용하는 경우:

```js
s.referrer = digitalData.page.pageInfo.referringURL;
```

>[!CAUTION]
>
>이 변수를 URL이 아닌 값으로 설정하지 마십시오. URL의 프로토콜을 제거하지 마십시오.

## 예

많은 조직은 리디렉션에 따라 구현을 처리합니다. 사이트가 레퍼러를 포함하는 경우 [`Util.getQueryParam()`](../functions/util-getqueryparam.md) 유틸리티를 사용하여 URL에서 레퍼러를 얻을 수 있습니다. URL이 쿼리 문자열에 포함된 모든 값을 인코딩하는지 확인하십시오.

```js
// Example if the URL is https://example.com?r=https%3A%2F%2Fexample.org
s.referrer = s.Util.getQueryParam("r");
```
