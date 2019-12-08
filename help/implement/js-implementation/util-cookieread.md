---
description: 쿠키에 사용할 값을 가져옵니다.
keywords: Analytics Implementation
subtopic: JavaScript AppMeasurement
title: Util.cookieRead
topic: Developer and implementation
uuid: 825a75c6-b804-4bfe-b23a-907113b8bfa6
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

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

