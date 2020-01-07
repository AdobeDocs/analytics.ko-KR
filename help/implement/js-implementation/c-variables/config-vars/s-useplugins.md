---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics Implementation
solution: null
title: 다이내믹 변수
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.usePlugins

이 함수를 사용할 수 있고 이 함수에 유용한 코드가 들어 있는 경우 [!UICONTROL s_usePlugins]를 'true'로 설정해야 합니다.

[!UICONTROL usePlugins]가 'true'이면 각 이미지 요청 전에 *`s_doPlugins`* 함수가 호출됩니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 해당 없음 | 해당 없음 | 해당 없음 | True |

## 구문 및 가능한 값

```js
s.usePlugins=true|false
```

[!UICONTROL usePlugins] 변수는 'true' 또는 'false'입니다.

## 예

```js
s.usePlugins=true
```

```js
s.usePlugins=false
```

JavaScript 파일에 *`s_doPlugins`* 함수가 선언되지 않은 경우에만 [!UICONTROL usePlugins] 변수가 false(또는 선언되지 않음)여야 합니다.

## 구성 설정

없음
