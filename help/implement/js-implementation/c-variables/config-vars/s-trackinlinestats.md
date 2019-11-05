---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# s.trackInlineStats

 변수는 ClickMap 데이터가 수집되는지 여부를 결정합니다. 

*`trackInlineStats`*&#x200B;가 'true'이면 클릭한 페이지 및 링크에 대한 데이터가 s_sq라는 쿠키에 저장됩니다. false이면 s_sq에는 "[[B]]"라는 값이 있게 되고, 이것은 null로 간주됩니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | ClickMap | False |

## 구문 및 가능한 값

```
js
s.trackInlineStats=true|false
```

*`trackInlineStats`변수는 'true' 또는 'false'입니다.*

## 예

```js
s.trackInlineStats=true
```

```js
s.trackInlineStats=false
```

## 구성 설정

없음
