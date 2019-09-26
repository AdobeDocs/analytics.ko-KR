---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.dynamicVariablePrefix {#concept_38C1F2452DDB47FCA8F458BE1398E276}

 변수를 사용하면 배포 시 변수에 플래그를 지정하는데 이것은 동적으로 채워집니다.

쿠키, 요청 헤더 및 이미지 쿼리 문자열 매개 변수는 동적으로 채울 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | D= | 임의 | D= |

## 구문 및 가능한 값

```js
s.prop1="D=User-Agent”
```

또는 동적 변수에 대한 사용자 지정 플래그 사용

```js
s.dynamicVariablePrefix=".."
```

## 예

```js
s.prop1="D=User-Agent”
```

또는 동적 변수에 대한 사용자 지정 플래그 사용

```js
s.dynamicVariablePrefix=".."
```

```js
s.prop1="..User-Agent"
```

## 함정, 질문 및 팁

* 동적 변수를 사용하면 값을 다른 변수에 복사하여 URL의 전체 길이를 크게 줄일 수 있습니다.

* 동적 변수는 별도로 데이터 수집에 사용할 수 없는 헤더와 쿠키의 데이터를 모으는 데 사용할 수 있습니다.
