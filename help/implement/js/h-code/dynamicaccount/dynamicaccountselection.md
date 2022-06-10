---
title: dynamicAccountSelection
description: dynamicAccountSelection 변수는 동적 계정 선택을 활성화하거나 비활성화합니다.
feature: Implementation Basics
exl-id: ccb530f9-b128-4d2d-9b5d-9b305272f0a4
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '86'
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
