---
title: dynamicAccountMatch
description: dynamicAccountMatch 변수는 동적 계정에서 볼 값을 결정합니다.
feature: Implementation Basics
exl-id: 3b68f2e6-1bd9-4b16-9d03-a87c9217e1b7
role: Developer
TQID: https://experienceleague.adobe.com/Ag4YQOjHPMRsktGSbzpErM55lVCydDHXfNiS4HJofIU
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: df312454-73c4-43f6-a90e-18f5043f074cid: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 100%

---

# dynamicAccountMatch

>[!IMPORTANT]
>
>동적 계정은 이전 JavaScript 구현(H 코드)을 사용해야만 지원됩니다. 이러한 변수는 현재 AppMeasurement 라이브러리 또는 Adobe Experience Platform의 태그에서 지원되지 않습니다.

`dynamicAccountMatch` 변수는 `dynamicAccountList`에서 보고 그 값을 비교하는 값입니다. `dynamicAccountSelection`이 `true`로 설정되지 않으면 이 변수는 무시됩니다.

이 변수가 정의되지 않은 경우 기본값은 `window.location.host`입니다.

## 구문

```js
s.dynamicAccountMatch=[DOM object]
```

## 예

```js
// Look at the URL path to determine report suite
s.dynamicAccountMatch = location.pathname;

// Use a query string
s.dynamicAccountMatch = location.search;

// Use the full URL
s.dynamicAccountMatch = location.href;

// Use concatenated variables
s.dynamicAccountMatch =  location.hostname + location.pathname + location.search;
```

## 추가 참고 사항

* 하드 드라이브에 저장된 페이지에 몇 개의 `location` 변수가 정의되어 있지 않습니다(예: `location.host`가 비어 있음). `s_account`에 기본 보고서 세트가 포함되어 있는지 확인하십시오.
* 페이지가 Google과 같은 웹 기반 번역 엔진을 통해 번역되는 경우, 동적 계정 선택 기능이 설계대로 작동하지 않습니다. 더 정밀한 추적을 수행하려면 `s_account` 변수 서버측을 채우십시오.
