---
title: dynamicAccountSelection
description: dynamicAccountSelection 변수는 동적 계정 선택을 활성화하거나 비활성화합니다.
feature: Implementation Basics
exl-id: ccb530f9-b128-4d2d-9b5d-9b305272f0a4
role: Developer
TQID: https://experienceleague.adobe.com/tne4K1ppeYbWGckTmuJy0f8Bjdw9WvGbjrOSKs4RXlk
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 82%

---

# dynamicAccountSelection

>[!IMPORTANT]
>
>동적 계정은 이전 JavaScript 구현(H 코드)을 사용해야만 지원됩니다. 이러한 변수는 현재 AppMeasurement 라이브러리 또는 Adobe Experience Platform 데이터 수집에서 지원되지 않습니다.

`dynamicAccountSelection` 변수는 동적 계정 선택이 사용되는지 여부를 결정하는 부울입니다.

`true`로 설정되면 JavaScript 파일이 `dynamicAccountMatch` 및 `dynamicAccountList`를 봅니다.

`false`로 설정되거나 이 변수가 정의되지 않으면 `dynamicAccountMatch` 및 `dynamicAccountList` 변수가 무시됩니다.

이 변수가 정의되지 않으면 기본값은 `false`입니다.

## 구문

```js
s.dynamicAccountSelection = [boolean];
```

## 예

```js
s.dynamicAccountSelection = true;
```
