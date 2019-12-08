---
description: 쿠키에 값을 씁니다.
keywords: Analytics Implementation
subtopic: JavaScript AppMeasurement
title: Util.cookieWrite
topic: Developer and implementation
uuid: 8d526e4c-6d7a-4119-9434-d7ce4fbb7577
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

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
| value | (선택 사항) 쿠키에 쓰는 값 |
| expire | (선택 사항) 쿠키의 만료 날짜가 들어 있는 날짜 개체 기본값은 세션 쿠키를 사용하는 것입니다. |

**반환:**

**예:**

```js
//set a cookie with an expiration 6 months from now 
var date = new Date(); 
date.setMonth(date.getMonth() + 6); 
var success = s.Util.cookieWrite("my_cookie", "my_value", date);
```

