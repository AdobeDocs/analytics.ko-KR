---
description: 값을 변수에 입력할 때 따라야 할 몇 가지 우수 사례가 있습니다.
keywords: Analytics 구현
seo-description: 값을 변수에 입력할 때 따라야 할 몇 가지 우수 사례가 있습니다.
seo-title: 따옴표 사용
solution: Analytics
subtopic: 문제 해결
title: 따옴표 사용
topic: 개발자 및 구현
uuid: 9 F 09 C 48 B -7 AE 5-441 E -8635-FD 6 BDC 2 E 94 C 7
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 따옴표 사용

값을 변수에 입력할 때 따라야 할 몇 가지 우수 사례가 있습니다.

작은 따옴표나 큰 따옴표를 사용할 수 있습니다. 반드시 일관되게 사용하십시오. 작은 따옴표를 사용하면 항상 작은 따옴표를 사용하고, 큰 따옴표를 사용하면 항상 큰 따옴표를 사용하십시오. 아래 두 예 모두 맞습니다.

```js
s.prop2='test' (single quotes)
```

```js
s.prop2="test" (double quotes)
```

둥근 따옴표를 껐는지 확인하십시오. 작은 따옴표를 사용하고, 변수 값에 아포스트로피가 있으면, JavaScript가 아포스트로피를 작은 따옴표로 해석합니다. 이것은 문자열의 끝임을 의미합니다. 다음 예를 생각해 보십시오.

```js
s.pageName='John's Home Page'
```

이 경우, JavaScript는 "John's"의 아포스트로피(작은 따옴표이기도 함)를 문자열의 끝으로 해석합니다. ''s Home Page"는 JavaScript에서 아무 의미를 가지지 않기 때문에 이미지 요청이 발생하지 않게 하는 오류가 발생합니다. 다음 중 한 예는 작동합니다.

```js
s.pageName='John\'s Home Page'
```

```js
s.pageName="John's Home Page"
```

첫 번째 예에서는, 아포스트로피를 escape하기 직전에 백슬래시(\)를 삽입하여 escape할 수 있습니다. 이것은 JavaScript에게 아포스트로피가 문자열이 끝났음을 표시하기 위해 있는 것이 아니라 문자열의 일부임을 알려 줍니다. 그러면 문자열은 의도한 대로 닫는 작은 따옴표에서 끝납니다. 두 번째 예에서는 전체 문자열 주변에 큰 따옴표를 사용합니다. 이 경우, 작은 따옴표 하나는 문자열의 끝을 나타낼 수 없습니다. 큰 따옴표 하나가 문자열의 일부일 경우에도 마찬가지입니다. 문자열을 둘러싸는 큰 따옴표는 물론 문자열 내의 큰 따옴표 사용으로 인해 s.pageName="Team Says "We Win!""라는 값은 올바르지 않게 됩니다. 이것은 s.pageName="Team Says \"We Win!\""으로 입력할 경우에만 올바르게 됩니다.
