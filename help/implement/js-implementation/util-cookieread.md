---
description: 쿠키에 사용할 값을 가져옵니다.
keywords: Analytics 구현
seo-description: 쿠키에 사용할 값을 가져옵니다.
seo-title: Util.cookieRead
solution: Analytics
subtopic: JavaScript AppMeasurement
title: Util.cookieRead
topic: 개발자 및 구현
uuid: 825a75c6-b804-4bfe-b23a-907113b8bfa6
translation-type: ht
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Util.cookieRead

쿠키에 사용할 값을 가져옵니다.

**구문:**

```
s.Util.cookieRead(key)
```

**매개 변수:**

| 매개 변수 | 설명 |
|---|---|
| key | (필수) 쿠키에서 값을 쓰는 키 |

**반환:**

쿠키 값 또는 빈 문자열(쿠키가 없을 경우)

**예:**

```js
var myCookie = s.Util.cookieRead("my_cookie");
```

