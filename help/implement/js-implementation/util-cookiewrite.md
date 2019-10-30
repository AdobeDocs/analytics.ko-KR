---
description: 쿠키에 값을 씁니다.
keywords: Analytics 구현
seo-description: 쿠키에 값을 씁니다.
seo-title: Util.cookieWrite
solution: Analytics
subtopic: JavaScript AppMeasurement
title: Util.cookieWrite
topic: 개발자 및 구현
uuid: 8d526e4c-6d7a-4119-9434-d7ce4fbb7577
translation-type: ht
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Util.cookieWrite

쿠키에 값을 씁니다.

**구문:**

```
s.Util.cookieWrite(key, value [,expire])
```

**매개 변수:**

| 매개 변수 | 설명 |
|---|---|
| key | (필수) 쿠키에서 값을 쓰는 키 |
| 값 | (선택 사항) 쿠키에 쓰는 값 |
| expire | (선택 사항) 쿠키의 만료 날짜가 들어 있는 날짜 개체 기본값은 세션 쿠키를 사용하는 것입니다. |

**반환:**

**예:**

```js
//set a cookie with an expiration 6 months from now 
var date = new Date(); 
date.setMonth(date.getMonth() + 6); 
var success = s.Util.cookieWrite("my_cookie", "my_value", date);
```

