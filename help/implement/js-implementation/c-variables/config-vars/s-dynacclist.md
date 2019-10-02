---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 5d6ff87bd49140a974fcaaeed714d0f0b7d1e58b

---


# s.dynamicAccountList

> [!NOTE] The `s.dynamicAccountList` variable is not supported in [Current AppMeasurement libraries](../../c-appmeasurement-js/appmeasure-mjs.md). H 코드와 같이 레거시 AppMeasurement에서만 사용됩니다.

이 `s.dynamicAccountList` 변수는 데이터를 보낼 보고서 세트를 동적으로 결정하는 데 사용됩니다. It is used in conjunction with the  and  variables. `dynamicAccountSelection``dynamicAccountMatch` 의 규칙은 로 설정된 `dynamicAccountList` 경우 `dynamicAccountSelection` 적용되며, `true`에 지정된 URL의 섹션에 적용됩니다 `dynamicAccountMatch`.

## 구문 및 가능한 값

```JavaScript
s.dynamicAccountList="rs1[,rs2]=domain1.com[,domain2.com/path][;...]";
```

유효한 입력은 세미콜론으로 구분된 이름=값 쌍(규칙) 목록입니다. 각 목록에는 다음 항목이 포함되어 있습니다.

* 하나 이상의 보고서 세트 ID(쉼표로 구분)
* 등호
* 하나 이상의 URL 필터(쉼표로 구분)

문자열에는 공백 없이 표준 ASCII 문자만 사용해야 합니다.

## 예

다음 모든 예에서 페이지 URL은 `https://example.com/path2/?prod_id=12345`으로, `dynamicAccountSelection` 변수는 `true`로, `s_account` 변수는 로 `examplersid`설정됩니다.

```js
// In this example, the report suite that receives data is examplersid1.
s.dynamicAccountMatch = "window.location.hostname";
s.dynamicAccountList = "examplersid2=www2.example.com;examplersid1=example.com";

// In this example, the report suite that receives data is examplersid2.
s.dynamicAccountMatch = "window.location.pathname";
s.dynamicAccountList = "examplersid2=path2;examplersid3=path3";

// In this example, no rules match so it resorts to the default rsid in s_account, examplersid.
s.dynamicAccountMatch = "window.location.pathname";
s.dynamicAccountList = "examplersid4=path4;examplersid5=path5";
```

## 함정, 질문 및 팁

* The 이 변수에 나열된 규칙은 왼쪽에서 오른쪽 순서로 적용됩니다. If the `dynamicAccountMatch` variable matches more than one rule, the left-most rule is used to determine the report suite. 따라서 목록 오른쪽에 더 많은 일반 규칙을 배치합니다.
* If no rules match, the default report suite in `s_account` is used.
* If your page is saved to someone's hard drive or translated via a web-based translation engine (such as Google's translated pages), the dynamic account selection likely won't work.
* The `dynamicAccountSelection` rules apply only to the section of the URL specified in `dynamicAccountMatch`.
* 대상 보고서 세트를 [!DNL Adobe Experience Cloud Debugger] 테스트하려면 을 사용합니다.
