---
title: purchaseID
description: 고유 구매 식별자를 기반으로 히트를 중복 제거합니다.
feature: Appmeasurement Implementation
exl-id: 7a4d7f08-65ae-4541-a94e-cc6c445c01db
role: Admin, Developer
TQID: https://experienceleague.adobe.com/A8QIQQbtDhZcQmnokBcQdMqJVAbu1PD7N363QdHcSJc
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 369
ht-degree: 78%

---

# purchaseID

`purchaseID` 변수는 동일한 구매를 포함하는 히트가 보고서를 부풀리지 않도록 하는 데 도움이 됩니다. 예를 들어 방문자가 구매 확인 페이지에 도달하는 경우 일반적으로 트랜잭션에서 생성된 수익 관련 데이터를 Adobe에 보내게 됩니다. 사용자가 이 페이지를 여러 번 새로 고치거나 나중에 방문하기 위해 페이지에 책갈피를 지정하면 해당 히트가 보고서를 부풀릴 수 있습니다. 둘 이상의 히트에 동일한 구매 ID가 있을 때 `purchaseID` 변수는 지표 중복을 제거합니다.

Adobe가 히트를 중복 구매로 인식하면 모든 전환 데이터 (예: eVar 및 이벤트)가 보고에 표시되지 않습니다. 데이터 피드에서 `duplicate_purchase` 열은 `1`로 설정됩니다.

구매 ID는 모든 방문자에게 적용되며 37개월 후에 만료됩니다. 한 방문자가 주어진 구매 ID를 설정한 다음, 다른 방문자가 1년 후 동일한 구매 ID를 설정하면 두 번째 구매는 중복 제거됩니다.

## 웹 SDK을 사용하는 구매 ID

구매 ID는 다음 변수에 매핑됩니다.

* [XDM 개체](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.commerce.order.purchaseID`
* [데이터 개체](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.purchaseID`

## Adobe Analytics 확장을 사용한 구매 ID

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 구매 ID를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장 기능] 드롭다운 목록을 Adobe Analytics로 설정하고 [!UICONTROL 액션 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL 구매 ID] 섹션을 찾습니다.

구매 ID를 값 또는 데이터 요소로 설정할 수 있습니다. 다른 Analytics 변수에서 값을 복사할 수도 있습니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.purchaseID

`s.purchaseID` 변수는 구매에 대한 고유 식별자를 포함하는 문자열입니다. 이 변수는 구매 이벤트와 동일한 히트에 대해 설정됩니다. 이 변수를 채우려면 영숫자만 사용하십시오.

이 변수는 최대 20바이트를 저장할 수 있습니다. 20바이트보다 긴 값은 잘립니다. 이 잘린 값이 이후 잘린 값과 일치하는 경우 그 후속 히트가 중복 제거됩니다.

```js
s.purchaseID = "ABC123";
```

`digitalData` [데이터 레이어](../../prepare/data-layer.md)를 사용하는 경우:

```js
s.purchaseID = digitalData.transaction.transactionID;
```

>[!CAUTION]
>
>구매 ID를 생성하는 데 무작위 지정 함수를 사용하지 마십시오.
