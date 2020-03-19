---
title: cookieDomainPeriods
description: 도메인에 마침표가 있을 경우 AppMeasurement가 쿠키를 저장할 도메인을 파악합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# fpCookieDomainPeriods

이 `fpCookieDomainPeriods` 변수는 AppMeasurement가 도메인 접미사에 추가 기간이 있음을 호출하여 Analytics 쿠키의 설정 위치를 확인하는 데 도움이 됩니다. 이 변수를 사용하면 AppMeasurement가 도메인 접미사의 추가 기간을 수용하고 올바른 위치에 쿠키를 설정할 수 있습니다. 퍼스트 파티 쿠키 구현을 사용하는 경우 [`cookieDomainPeriods`](cookiedomainperiods.md)은 의 값을 상속하지만 설정하는 것이 좋습니다.

* 또는 같은 도메인의 경우 `example.com` 이 변수를 설정할 `www.example.com`필요가 없습니다. 필요한 경우 이 변수를 로 설정할 수 `"2"`있습니다.
* 또는 같은 도메인의 경우 `example.co.uk` 이 `www.example.co.jp`변수를 로 설정합니다 `"3"`.

> [!IMPORTANT] 이 변수에 대해 하위 도메인을 고려하지 마십시오. 예를 들어 예제 URL `fpCookieDomainPeriods` 에 설정하지 마십시오 `store.toys.example.com`. AppMeasurement는 기본적으로 쿠키가 여러 하위 도메인이 있는 URL에서도 `example.com`저장되어야 함을 인식합니다.

## Adobe Experience Platform Launch의 자사 도메인 기간

퍼스트 파티 도메인 기간은 Adobe Analytics 확장을 구성할 때 아코디언 아래에 있는 [!UICONTROL Cookies] 필드입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
4. 필드를 나타내는 [!UICONTROL Cookies] [!UICONTROL First-party Domain Periods] 아코디언을 확장합니다.

접미어로 마침표를 포함하는 도메인에서만 이 필드를 `3` 설정합니다. 그렇지 않으면 이 필드를 비워 둘 수 있습니다.

## s.fpCookieDomainPeriods in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `fpCookieDomainPeriods` 변수는 일반적으로 `"3"`마침표가 포함된 도메인에서만 설정된 문자열입니다. 기본값은 `"2"`대부분의 도메인을 수용하는 것입니다.

```js
// Manually set fpCookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.fpCookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.fpCookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.fpCookieDomainPeriods = "3" : s.fpCookieDomainPeriods = "2";
```
