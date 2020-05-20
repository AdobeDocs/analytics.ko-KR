---
title: cookieDomain
description: cookieDomain 변수는 쿠키를 설정할 도메인을 결정하는 데 도움이 됩니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# cookieDomain

>[!IMPORTANT] 이 변수는 사용이 중단되었습니다. 대신 [`trackingServer`](trackingserver.md)를 사용하십시오.

`cookieDomain` 변수는 AppMeasurement가 쿠키를 설정하는 도메인을 결정합니다. 이 변수를 사용하면 [`cookieDomainPeriods`](cookiedomainperiods.md) 변수를 사용하는 대신 쿠키 도메인을 명시적으로 설정할 수 있습니다.

이 변수는 다음 조건을 **모두** 충족할 때만 사용해야 합니다.

* 구현에서 자사 쿠키를 사용하는 경우. 이 변수는 `sc.omtrdc.net`을 포함하는 [`trackingServer`](trackingserver.md) 값을 사용하는 구현에는 필요하지 않습니다.
* 도메인 접미사에 마침표가 있는 경우. 예를 들어, `example.co.uk`가 `cookieDomain` 변수를 사용하여 쿠키 도메인이 `co.uk`가 아니고 `example.co.uk`라고 명시할 수 있습니다.

적은 수의 구현만 `cookieDomain` 변수를 사용할 수 있으며, 그러한 때에도 [`cookieDomainPeriods`](cookiedomainperiods.md)같은 대체 변수를 대신 사용할 수 있습니다.

## Adobe Experience Platform Launch의 쿠키 도메인

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.cookieDomain

`cookieDomain` 변수는 문자열이며, 쿠키를 저장할 도메인으로 설정됩니다.

```js
s.cookieDomain = "stats.example.com";
```
