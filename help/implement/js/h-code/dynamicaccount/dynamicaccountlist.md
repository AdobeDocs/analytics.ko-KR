---
title: dynamicAccountList
description: 구현에서 보고서 세트를 결정하는 방법에 대한 논리를 설정합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# s.dynamicAccountList

>[!IMPORTANT] 동적 계정은 이전 JavaScript 구현(H 코드)을 사용해야만 지원됩니다. 이러한 변수는 현재 AppMeasurement 라이브러리 또는 Adobe Experience Platform Launch에서 지원되지 않습니다.

`s.dynamicAccountList` 변수는 `s_account`의 값을 동적으로 결정합니다. `dynamicAccountSelection`을 `true`로 설정하면 `dynamicAccountMatch` 변수가 `dynamicAccountList`와 비교됩니다. 일치하는 항목이 있으면 일치하는 보고서 세트 ID가 사용됩니다.

## 구문

이 변수는 JavaScript 파일에서 자동으로 구문 분석되는 문자열입니다.

```JavaScript
s.dynamicAccountList = "[rsid]=[valuetomatch],[rsid2]=[valuetomatch]";
```

올바른 입력은 세미콜론으로 구분되는 rsid와 값 쌍 목록입니다. 각 목록에는 다음 항목이 포함되어 있습니다.

* 하나 이상의 보고서 세트 ID(쉼표로 구분됨)
* 등호
* 일치시킬 하나 이상의 문자열(쉼표로 구분)

문자열에는 표준 ASCII 문자만 사용해야 합니다. 공백은 포함하지 마십시오.

## 예

다음 모든 예에서 페이지 URL은 `https://example.com/path2/?prod_id=12345`이고, `dynamicAccountSelection` 변수는 `true`로 설정되고, `s_account` 변수는 `examplersid`로 설정됩니다.

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

* 이 변수에 나열된 규칙은 왼쪽에서 오른쪽 순서로 적용됩니다. `dynamicAccountMatch` 변수가 두 개 이상의 규칙과 일치하는 경우, 가장 왼쪽 규칙이 보고서 세트를 결정하는 데 사용됩니다. 따라서 더 일반적인 규칙을 목록의 오른쪽에 배치하십시오.
* 일치하는 규칙이 없을 경우에는 `s_account`의 기본 보고서 세트가 사용됩니다.
* 페이지가 누군가의 하드 드라이브에 저장되거나 웹 기반 번역 엔진을 통해 번역되는 경우(Google의 번역된 페이지)에는, 동적 계정 선택 기능이 작동하지 않을 수 있습니다.
* `dynamicAccountSelection` 규칙은 `dynamicAccountMatch`에 지정된 URL의 섹션에만 적용됩니다.
* [!DNL Adobe Experience Cloud Debugger]를 사용하여 대상 보고서 세트를 테스트하십시오.
