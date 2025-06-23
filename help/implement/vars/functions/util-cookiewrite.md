---
title: Util.cookieWrite
description: 쿠키 값을 씁니다.
feature: Appmeasurement Implementation
exl-id: 079dbe50-5568-467b-a67c-f44481a4a20b
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 70%

---

# Util.cookieWrite

쿠키는 동일한 도메인에 있는 페이지 간에 정보를 저장하고 검색할 수 있습니다. 값을 쿠키에 설정하려면 `Util.cookieWrite()` 메서드를 사용하십시오. [`Util.cookieRead()`](util-cookieread.md) 메서드를 사용하면 `Util.cookieWrite()`을 사용하여 설정한 값을 검색할 수 있습니다.

## Adobe Analytics 확장 및 웹 SDK 확장을 사용하여 쿠키를 설정합니다

Adobe Experience Platform 데이터 수집에서는 인터페이스에서 쿠키를 설정하는 기능을 제공하지 않습니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.Util.cookieWrite()

쿠키를 원하는 값으로 설정하려면 `s.Util.cookieWrite()` 메서드를 호출하십시오.

```js
s.Util.cookieWrite("example_cookie","Example cookie value")
```

쿠키가 만료되는 시기를 결정하는 선택적 세 번째 인수를 사용할 수 있습니다. `s.Util.cookieWrite()`을 사용하여 설정된 쿠키는 기본적으로 브라우저 세션이 끝날 때 만료됩니다.

```js
// Set a cookie with an expiration 6 months from now
var cookieDate = new Date();
cookieDate.setMonth(cookieDate.getMonth() + 6);
s.Util.cookieWrite("example_cookie","Example 6-month cookie",cookieDate);
```

## 예

쿠키 쓰기에 성공하면 변수를 인스턴스화할 수 있습니다. 이 변수는 부울입니다.

```js
var success = s.Util.cookieWrite("example_cookie","Example cookie value");
if (success) {
  console.log("Cookie written successfully");
} else {
  console.log("Cookie write failed");
}
```
