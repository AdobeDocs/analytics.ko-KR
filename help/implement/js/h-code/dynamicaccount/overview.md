---
title: 동적 계정 개요
description: H 코드를 사용하여 보고서 세트를 동적으로 선택하는 방법에 대한 워크플로우에 대해 알아봅니다.
translation-type: tm+mt
source-git-commit: f313fd0c9ffda054a18ad1d457a74602b08e51fa

---


# 동적 계정 개요

> [!IMPORTANT] 동적 계정은 이전 JavaScript 구현(H 코드)을 사용해서만 지원됩니다. 이러한 변수는 현재 AppMeasurement 라이브러리 또는 Adobe Experience Platform Launch에서 지원되지 않습니다.

동적 계정은 정의한 기준에 따라 사용할 보고서 세트를 결정할 수 있는 구현 기능입니다. 조직에서 두 개 이상의 보고서 세트를 필요로 하지만 사이트 간에 동일한 구현을 사용하고자 하는 경우 동적 계정이 좋은 솔루션입니다.

> [!TIP] Adobe에서는 데이터를 단일 보고서 세트로 보낸 다음, 필요한 경우 가상 보고서 세트를 사용하여 데이터를 구분하는 것이 좋습니다. 자세한 [내용은 글로벌 보고서 세트 고려 사항을](../../../prepare/global-rs.md) 참조하십시오.

보고서 세트를 동적으로 선택하는 데 3개의 변수가 사용됩니다.

* [`dynamicAccountSelection`](dynamicaccountselection.md):동적 계정 선택을 활성화하거나 비활성화합니다.
* [`dynamicAccountMatch`](dynamicaccountmatch.md):관찰할 값을 결정합니다. 예: URL 또는 쿼리 문자열.
* [`dynamicAccountList`](dynamicaccountlist.md):값을 로 `dynamicAccountMatch`비교하고, 일치하는 항목이 발견되면 `account` 변수가 채워집니다.

이 `dynamicAccountSelection = true`경우, 해당 값이 와 `dynamicAccountMatch` 비교됩니다 `dynamicAccountList`. 일치하는 값이 `dynamicAccountList` 있으면 보고서 세트 ID가 `account` 변수에 포함됩니다.

## 기본 보고서 세트

`account` 변수는 맨 먼저 설정할 수 있고, 지정된 문자열을 찾을 수 없는 경우 기본값으로 작동합니다. 예:

```javascript
s_account = "examplersiddefault";
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersiddev=dev.example.com;examplersidprod=example.com";
```

둘 `location.hostname` 중 어느 `dev.example.com` 것도 아니면 히트가 로 전송됩니다 `example.com``examplersiddefault`.

## 다중 세트 태그 지정

다중 세트 태깅은 다이내믹 계정 선택과 함께 사용할 수 있습니다. 예:

```js
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersid1,examplersid2=example.com";
```

가 `location.hostname` 포함되어 `example.com`있으면 히트가 및 `examplersid1` `examplersid2`으로 전송됩니다.
