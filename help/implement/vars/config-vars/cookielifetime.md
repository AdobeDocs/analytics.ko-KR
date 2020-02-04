---
title: cookieLifetime
description: AppMeasurement가 만드는 쿠키의 만료를 무시합니다.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# cookieLifetime

AppMeasurement에서 설정하는 쿠키는 일반적으로 2년 만료입니다. 이 `cookieLifetime` 변수를 사용하여 AppMeasurement에서 설정한 쿠키의 만료 날짜를 재정의합니다.

> [!NOTE] 이 변수는 고유 방문자 수 및 속성에 영향을 줍니다. 이 변수를 설정할 때는 주의하십시오.

## Adobe Experience Platform Launch의 쿠키 라이프타임

쿠키 라이프타임은 Adobe Analytics 확장을 구성할 때 [!UICONTROL 쿠키] 아코디언 아래의 드롭다운입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 확장 [!UICONTROL 탭으로 이동한] 다음 Adobe [!UICONTROL Analytics에서 구성] 단추를 클릭합니다.
4. 쿠키 [!UICONTROL 라이프타임] 드롭다운을 표시하는 쿠키 [!UICONTROL 아코디언을 확장합니다] .

이 드롭다운에는 다음 값이 포함되어 있습니다.

* **기본값**:쿠키는 2년 후 만료됩니다.
* **없음**:AppMeasurement는 쿠키를 설정하지 않습니다.
* **세션**:쿠키는 방문자 세션이 끝날 때 만료됩니다.
* **초**:지정된 시간(초)이 경과하면 쿠키가 만료됩니다. 예를 들어 이 드롭다운을 [!UICONTROL 초로] 설정하고 사용자 정의 필드에 `86400` 배치하면 쿠키가 정확히 24시간 후에 만료됩니다.

## s.cookieLifetime in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.cookieLifetime` 변수는 AppMeasurement에서 설정한 쿠키의 만료 날짜를 결정하는 문자열입니다.

* 로 설정된 `SESSION`경우 AppMeasurement에서 설정한 쿠키는 브라우저 세션이 완료된 후 만료됩니다.
* 로 설정된 `NONE`경우 AppMeasurement가 쿠키를 설정하지 않습니다.
* 정수 문자열로 설정하면 AppMeasurement에서 설정한 쿠키가 지정된 시간(초)이 경과하면 만료됩니다.

```js
// Expire cookies after each session
s.cookieLifetime = "SESSION";

// Expire cookies after exactly 24 hours
s.cookieLifetime = "86400";

