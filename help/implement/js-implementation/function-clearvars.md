---
description: 인스턴스 개체에서 다음 값을 지웁니다. 이 함수는 요소를 제거합니다(요소를 "정의되지 않음"으로 설정).
keywords: Analytics Implementation
solution: Analytics
title: s.clearVars() 함수
topic: Developer and implementation
uuid: 43c425bc-15ae-4892-a5a5-e1defcb25ff4
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.clearVars() 함수

인스턴스 개체에서 다음 값을 지웁니다. 이 함수는 요소를 제거합니다(요소를 "정의되지 않음"으로 설정).

* `props`
* `eVars`
* `hier`
* `list`
* `events`
* `eventList`
* `products`
* `productsList`
* `channel`
* `purchaseID`
* `transactionID`
* `state`
* `zip`
* `campaign`

예:

```js
s.clearVars()
```

>[!NOTE]
>
>`clearVars()`는 [JavaScript용 AppMeasurement](/help/implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md)에 포함되어 있지만, H 코드 및 이전 버전에서는 사용할 수 없습니다.

