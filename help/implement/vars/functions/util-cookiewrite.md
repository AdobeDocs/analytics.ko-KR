---
title: Util.cookieWrite
description: 쿠키에 대한 값을 씁니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Util.cookieWrite

쿠키는 동일한 도메인의 페이지 간에 정보를 저장하고 검색할 수 있습니다. 값을 쿠키로 설정하려면 이 `Util.cookieWrite()` 메서드를 사용합니다. 이 [`Util.cookieRead()`](util-cookieread.md) 방법을 사용하여 값을 검색할 수 `Util.cookieWrite()`있습니다.

## Adobe Experience Platform Launch에서 쿠키 설정

Launch는 인터페이스에서 쿠키를 설정하는 기능을 제공하지 않습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## s.Util.cookieWrite() in AppMeasurement 및 Launch 사용자 지정 코드 편집기

메서드를 `s.Util.cookieWrite()` 호출하여 쿠키를 원하는 값으로 설정합니다.

```js
s.Util.cookieWrite("example_cookie","Example cookie value")
```

쿠키가 만료되는 시기를 결정하는 선택적 세 번째 인수를 사용할 수 있습니다. 기본적으로 브라우저 세션이 끝날 때 `s.Util.cookieWrite()` 만료되도록 설정된 쿠키입니다.

```js
// Set a cookie with an expiration 6 months from now
var cookieDate = new Date();
cookieDate.setMonth(cookieDate.getMonth() + 6);
s.Util.cookieWrite("example_cookie","Example 6-month cookie",cookieDate);
```

## 예

쿠키 작성 성공 시 변수를 인스턴스화할 수 있습니다. 이 변수는 부울입니다.

```js
var success = s.Util.cookieWrite("example_cookie","Example cookie value");
if (success) {
  console.log("Cookie written successfully");
} else {
  console.log("Cookie write failed");
}
```
