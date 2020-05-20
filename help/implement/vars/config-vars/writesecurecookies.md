---
title: writeSecureCookies
description: AppMeasurement가 Secure 속성을 사용하여 쿠키를 설정할 수 있도록 허용합니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# writeSecureCookies

`writeSecureCookies` 변수를 사용하면 AppMeasurement가 Analytics에 대한 [보안 쿠키](https://en.wikipedia.org/wiki/Secure_cookie)를 설정할 수 있습니다. 이 설정은 AppMeasurement에서 설정한 방문자 ID 쿠키와 `Util.CookieWrite()` 메서드를 사용하여 설정한 쿠키에 모두 적용됩니다. 이렇게 하려면 AppMeasurement 2.18.0 이상이 필요합니다.

>[!IMPORTANT] `writeSecureCookies` 변수를 활성화하면 사이트의 모든 컨텐츠가 HTTPS에서 안전하게 제공되는지 확인하십시오. 이 변수가 활성화되어 있고 페이지에 안전하지 않은 컨텐츠가 있는 경우 AppMeasurement가 작동하지 않습니다.

## Adobe Experience Platform Launch에서 보안 쿠키 작성

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.writeSecureCookies

`s.writeSecureCookies` 변수는 쿠키를 만들 때 AppMeasurement가 보안 속성을 설정하는지 여부를 결정하는 부울입니다. 기본값은 `false`입니다. 사이트의 모든 컨텐츠가 안전하며 AppMeasurement에서 설정한 쿠키가 보안 속성을 갖도록 하려는 경우 이 변수를 `true`로 설정합니다.

```js
s.writeSecureCookies = true;
```
