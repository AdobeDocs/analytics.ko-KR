---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.dynamicAccountSelection

 변수를 사용하면 각 페이지의 URL을 기반으로 보고서 세트를 동적으로 선택할 수 있습니다.

>[!NOTE]
>
>`dynamicAccountSelection` 은 사용자 지정 링크 추적 시 작동하지 않습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | False |

>[!NOTE]
>
>Both `dynamicAccountList` and `dynamicAccountMatch` are ignored if the `dynamicAccountSelection` variable is not declared or set to 'false.'

## 구문 및 가능한 값

```js
s.dynamicAccountSelection=[true|false]
```

'true'와 'false'만 *`dynamicAccountSelection`*.

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

* 다이내믹 계정 선택은 [JavaScript용 AppMeasurement](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).

* 각 페이지의 데이터를 받는 보고서 세트를 결정하려면 항상 [!DNL DigitalPulse Debugger]를 사용하십시오.
