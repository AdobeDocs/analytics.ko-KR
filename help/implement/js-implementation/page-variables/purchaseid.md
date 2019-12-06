---
description: Adobe Analytics에 중복 구매가 표시되지 않도록 하는 purchaseID 변수에 대해 알아봅니다.
keywords: duplicate,purchase,purchaseid,s.purchaseid
solution: Analytics
subtopic: Variables
title: purchaseID
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 3e2f0bccbe7183ea75b12b1ef2b5afdd87837629

---


# purchaseID

The `purchaseID` variable is used to keep an order from being counted multiple times in reporting. Whenever the purchase event is used on your site, Adobe recommends using the `purchaseID` variable.

방문자가 사이트에서 항목을 구매하면 `purchaseID` 일반적으로 "감사합니다" 또는 "주문 확인" 페이지에 채워집니다. 구매 이벤트가 실행되는 동시에 `purchaseID` 변수를 설정합니다. 고유 값으로 `purchaseID` 정의되면 전환 변수 값은 해당 고유 구매 ID를 가진 히트에 대해서만 계산됩니다. 방문자는 `purchaseID` 자신의 목적을 위해 구매 확인 페이지를 자주 책갈피로 지정하므로 값을 정의하는 것이 중요합니다. 구현에서 사용하지 않는 `purchaseID`경우 방문자가 페이지를 새로 고쳐 전환 데이터(예: 매출)가 쉽게 부풀려질 수 있습니다.

구매 데이터 외에 모든 전환 변수 및 이벤트는 동일한 구매 ID의 히트에 대해 여러 번 계산되지 않습니다.

## 구문

이 `purchaseID` 변수에는 영숫자 값을 최대 20바이트로 저장할 수 있습니다. 구매 ID를 20바이트보다 오래 설정하면 값이 잘립니다.

```js
s.purchaseID = "uniqueid";
```
