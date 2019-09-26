---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# s.cookieLifetime

 변수는 쿠키의 수명을 결정할 때 JavaScript와 데이터 수집 서버 모두에서 사용됩니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | cl | 트래픽 &gt; 기술 &gt; 쿠키. 모든 방문자 관련 보고서 | "" |

만약 *`cookieLifetime`* 이 설정되면, 이 값은 아래 설명된 한 가지 예외를 제외하고 JavaScript와 데이터 수집 서버 모두에 대한 다른 쿠키 만료를 무시합니다. The *`cookieLifetime`* variable can have one of three values:

* [!DNL Analytics] 쿠키
* 쿠키
* JavaScript 설정 및 플러그인

## 구문 및 가능한 값

```js
s.cookieLifetime="value"
```

가능한 값은 다음과 같습니다.

* ""
* "NONE"
* "SESSION"
* 만료까지의 시간을 초 단위로 나타낸 정수

## 예

```js
s.cookieLifetime="SESSION"
```

```js
s.cookieLifetime="86400" // one day in seconds
```

## 구성 설정

없음

## 함정, 질문 및 팁

*`cookieLifetime`* 는 [!DNL Analytics] 추적에 영향을 줍니다. If, for example, *`cookieLifetime`* is two days, then monthly, quarterly, and yearly unique visitor reports will be incorrect. 따라서 *`cookieLifetime`*.
