---
title: cookieDomainPeriods
description: 도메인의 접미사에 마침표가 있는 경우 쿠키를 저장할 도메인을 AppMeasurement가 이해하도록 도와줍니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# fpCookieDomainPeriods

`fpCookieDomainPeriods` 변수는 AppMeasurement가 도메인 접미사에 불필요한 마침표가 있음을 표시하여 Analytics 쿠키의 설정 위치를 확인하는 데 도움이 됩니다. 이 변수를 사용하면 AppMeasurement가 도메인 접미사의 불필요한 마침표를 수용하고 올바른 위치에 쿠키를 설정할 수 있습니다. 이 변수는 [`cookieDomainPeriods`](cookiedomainperiods.md)의 값을 상속하지만 자사 쿠키 구현을 사용하는 경우에는 설정하는 것이 좋습니다.

* `example.com` 또는 `www.example.com`과 같은 도메인의 경우 이 변수를 설정할 필요가 없습니다. 필요한 경우 이 변수를 `"2"`로 설정할 수 있습니다.
* `example.co.uk` 또는 `www.example.co.jp`와 같은 도메인의 경우에는 이 변수를 `"3"`로 설정하십시오.

>[!IMPORTANT] 이 변수에 대해 하위 도메인을 고려하지는 마십시오. 예를 들어 `fpCookieDomainPeriods`이라는 URL 예에서는 `store.toys.example.com`를 설정하지 마십시오. AppMeasurement는 여러 하위 도메인이 있는 URL에서도 기본적으로 쿠키가 `example.com`에 저장되어야 한다고 인식합니다.

## Adobe Experience Platform Launch의 자사 도메인 마침표

First-party Domain Periods is a field under the [!UICONTROL Cookies] accordion when configuring the Adobe Analytics extension.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. Go to the [!UICONTROL Extensions] tab, then click the [!UICONTROL Configure] button under Adobe Analytics.
4. 필드를 나타내는 [!UICONTROL Cookies] [!UICONTROL First-party Domain Periods] 아코디언을 확장합니다.

접미사에 마침표를 포함하는 도메인에서만 이 필드를 `3`으로 설정하십시오. 다른 경우에는 이 필드를 비워 둘 수 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.fpCookieDomainPeriods

`fpCookieDomainPeriods` 변수는 일반적으로 접미사에 마침표를 포함하는 도메인에서만 `"3"`으로 설정되는 문자열입니다. 기본값은 `"2"`이고, 이렇게 하면 대부분의 도메인이 포함됩니다.

```js
// Manually set fpCookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.fpCookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.fpCookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.fpCookieDomainPeriods = "3" : s.fpCookieDomainPeriods = "2";
```
