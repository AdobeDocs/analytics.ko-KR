---
title: 동적 계정 개요
description: H 코드를 사용하여 보고서 세트를 동적으로 선택하는 방법에 대한 워크플로우에 대해 알아봅니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 동적 계정 개요

>[!IMPORTANT] 동적 계정은 이전 JavaScript 구현(H 코드)을 사용해야만 지원됩니다. 이러한 변수는 현재 AppMeasurement 라이브러리 또는 Adobe Experience Platform Launch에서 지원되지 않습니다.

동적 계정은 사용자가 정의한 기준에 따라 사용할 보고서 세트를 결정할 수 있도록 해주는 구현 기능입니다. 조직에서 두 개 이상의 보고서 세트를 필요로 하지만 사이트 간에 동일한 구현을 사용하고자 하는 경우 동적 계정을 사용하는 것이 좋습니다.

>[!TIP] 데이터를 단일 보고서 세트에 보낸 다음, 필요한 경우 가상 보고서 세트를 사용하여 데이터를 구분하는 것이 좋습니다. 자세한 내용은 [글로벌 보고서 세트 고려 사항](../../../prepare/global-rs.md)을 참조하십시오.

보고서 세트를 동적으로 선택하는 데에는 3개의 변수가 사용됩니다.

* [`dynamicAccountSelection`](dynamicaccountselection.md): 동적 계정 선택을 활성화하거나 비활성화합니다.
* [`dynamicAccountMatch`](dynamicaccountmatch.md): URL이나 쿼리 문자열과 같은 관찰할 값을 결정합니다.
* [`dynamicAccountList`](dynamicaccountlist.md): 값을 `dynamicAccountMatch`와 비교하고, 일치하는 값이 발견되면 `account` 변수를 채웁니다.

`dynamicAccountSelection = true`인 경우, `dynamicAccountMatch` 내의 값은 `dynamicAccountList`와 비교됩니다. `dynamicAccountList`의 값이 일치하면 보고서 세트 ID가 `account` 변수에 포함됩니다.

## 기본 보고서 세트

`account` 변수는 맨 먼저 설정할 수 있고, 지정된 문자열을 찾을 수 없는 경우 기본값으로 작동합니다. 예:

```javascript
s_account = "examplersiddefault";
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersiddev=dev.example.com;examplersidprod=example.com";
```

`location.hostname`이 `dev.example.com`과 `example.com` 중 어느 것도 아니면 히트가 `examplersiddefault`에 전송됩니다.

## 다중 세트 태그 지정

다중 세트 태깅은 동적 계정 선택과 함께 사용할 수 있습니다. 예:

```js
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersid1,examplersid2=example.com";
```

`location.hostname`에 `example.com`이 포함되어 있으면 히트가 `examplersid1`과 `examplersid2` 모두에 전송됩니다.
