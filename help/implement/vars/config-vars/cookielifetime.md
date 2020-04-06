---
title: cookieLifetime
description: AppMeasurement가 만드는 쿠키의 만료를 무시합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# cookieLifetime

AppMeasurement에서 설정하는 쿠키는 일반적으로 만료 기한이 2년입니다. AppMeasurement에서 설정한 쿠키의 만료 날짜를 무시하려면 `cookieLifetime` 변수를 사용하십시오.

>[!NOTE] 이 변수는 고유 방문자 수 및 기여도 분석에 영향을 줍니다. 따라서 이 변수를 설정할 때에는 주의하십시오.

## Adobe Experience Platform Launch의 쿠키 라이프타임

Cookie Lifetime is a dropdown under the [!UICONTROL Cookies] accordion when configuring the Adobe Analytics extension.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. Go to the [!UICONTROL Extensions] tab, then click the [!UICONTROL Configure] button under Adobe Analytics.
4. 드롭다운을 표시하는 [!UICONTROL Cookies] 아코디언을 [!UICONTROL Cookie Lifetime] 확장합니다.

이 드롭다운에는 다음 값이 포함되어 있습니다.

* **기본값**: 쿠키가 2년 후 만료됩니다.
* **없음**: AppMeasurement가 쿠키를 설정하지 않습니다.
* **세션**: 쿠키가 방문자 세션이 끝날 때 만료됩니다.
* **초**: 지정된 초 수가 경과하면 쿠키가 만료됩니다. For example, setting this dropdown to [!UICONTROL Seconds] and placing `86400` into the custom field forces cookies to expire after exactly 24 hours.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.cookieLifetime

`s.cookieLifetime` 변수는 AppMeasurement에서 설정한 쿠키의 만료 날짜를 결정하는 문자열입니다.

* `SESSION`으로 설정하면 AppMeasurement에서 설정한 쿠키가 브라우저 세션이 완료된 후 만료됩니다.
* `NONE`으로 설정하면 AppMeasurement가 쿠키를 설정하지 않습니다.
* 정수 문자열로 설정하면 AppMeasurement에서 설정한 쿠키가 지정된 초 수가 경과하면 만료됩니다.

```js
// Expire cookies after each session
s.cookieLifetime = "SESSION";

// Expire cookies after exactly 24 hours
s.cookieLifetime = "86400";

