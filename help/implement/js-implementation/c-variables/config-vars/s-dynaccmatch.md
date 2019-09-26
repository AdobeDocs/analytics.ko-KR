---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.dynamicAccountMatch

이 변수는 DOM 개체를 사용하여 의 모든 규칙이 적용되는 URL의 섹션을 검색합니다.

This variable is only valid when *`dynamicAccountSelection`* is set to 'True.' 기본값이 [!DNL window.location.host]이므로, 이 값은 [!UICONTROL 동적 계정 선택] 기능이 작동하는 데 필요하지 않습니다. For additional information, see [dynamicAccountList](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).

에 있는 규칙은 의 값에 `dynamicAccountList` 적용됩니다 `dynamicAccountMatch`. 에 `dynamicAccountMatch` (기본값)만 [!DNL window.location.host] 포함된 경우 의 규칙은 페이지의 도메인에만 `dynamicAccountList` 적용됩니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | window.location.host |

## 구문 및 가능한 값

The `dynamicAccountMatch`변수는 보통 JavaScript용 AppMeasurement 파일을 제공하는 Adobe 컨설턴트가 채웁니다. 하지만 아래 목록의 값들은 언제든지 적용할 수 있습니다.

```js
s.dynamicAccountMatch=[DOM object]
```

| 설명 | 값 |
|---|---|
| 도메인(기본값) | window.location.host |
| 경로 | window.location.pathname |
| 쿼리 문자열 | (window.location.search?window.location.search:"?") |
| 도메인 및 경로 | window.location.host+window.location.pathname |
| 경로 및 쿼리 문자열 | window.location.pathname+(window.location.search?window.location.search:"?") |
| 전체 URL | window.location.href |

## 예

```js
s.dynamicAccountMatch=window.location.pathname
```

```js
s.dynamicAccountMatch=window.location.host+window.location.pathname
```

## 구성 설정

없음

## 함정, 질문 및 팁

* 다이내믹 계정 선택은 [JavaScript용 AppMeasurement](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).

* When pages are saved to a hard drive, [!DNL window.location.host] is empty, causing those page views to be sent to the default report suite (in `s_account`).

* 페이지가 Google과 같은 웹 기반 번역 엔진을 통해 번역되는 경우, [!UICONTROL 동적 계정 선택] 기능이 설계대로 작동하지 않습니다. 더 정밀한 추적을 수행하려면, [!UICONTROL s_account ]변수 서버측을 채우십시오.
