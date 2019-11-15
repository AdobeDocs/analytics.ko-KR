---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics Implementation
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.dynamicAccountSelection

 변수를 사용하면 각 페이지의 URL을 기반으로 보고서 세트를 동적으로 선택할 수 있습니다.

> [!NOTE] `dynamicAccountSelection` 은 사용자 지정 링크 추적 시 작동하지 않습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | False |

> [!NOTE]`dynamicAccountList` 변수가 선언되지 않았거나 'false'로 설정된 경우 `dynamicAccountMatch`와 `dynamicAccountSelection`가 모두 무시됩니다.

## 구문 및 가능한 값

```js
s.dynamicAccountSelection=[true|false]
```

'true'와 'false'만 *`dynamicAccountSelection`* 값으로 사용할 수 있습니다.

## 예

```js
s.dynamicAccountSelection=true
```

```js
s.dynamicAccountSelection=false
```

## 구성 설정

없음

## 함정, 질문 및 팁

* [JavaScript용 AppMeasurement](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html)에서는 동적 계정 선택을 지원하지 않습니다.

* 각 페이지의 데이터를 받는 보고서 세트를 결정하려면 항상 [!DNL DigitalPulse Debugger]를 사용하십시오.
