---
title: purchaseID
description: 고유 구매 식별자를 기반으로 히트를 중복 제거합니다.
feature: Variables
exl-id: 7a4d7f08-65ae-4541-a94e-cc6c445c01db
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 87%

---

# purchaseID

`purchaseID` 변수는 동일한 구매를 포함하는 히트가 보고서를 부풀리지 않도록 하는 데 도움이 됩니다. 예를 들어 방문자가 구매 확인 페이지에 도달하는 경우 일반적으로 트랜잭션에서 생성된 수익 관련 데이터를 Adobe에 보내게 됩니다. 사용자가 이 페이지를 여러 번 새로 고치거나 나중에 방문하기 위해 페이지에 책갈피를 지정하면 해당 히트가 보고서를 부풀릴 수 있습니다. 둘 이상의 히트에 동일한 구매 ID가 있을 때 `purchaseID` 변수는 지표 중복을 제거합니다.

Adobe가 히트를 중복 구매로 인식하면 모든 전환 데이터 (예: eVar 및 이벤트)가 보고에 표시되지 않습니다. 데이터 피드에서 `duplicate_purchase` 열은 `1`로 설정됩니다.

구매 ID는 모든 방문자에게 적용되며 만료되지 않습니다. 한 방문자가 주어진 구매 ID를 설정한 다음, 다른 방문자가 1년 후 동일한 구매 ID를 설정하면 두 번째 구매는 중복 제거됩니다.

## 웹 SDK를 사용한 구매 ID

구매 ID: [Adobe Analytics에 대해 매핑됨](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=ko-KR) XDM 필드 아래 `commerce.order.purchaseID`.

## Adobe Analytics 확장을 사용한 구매 ID

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

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
