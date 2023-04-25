---
title: cookieLifetime
description: AppMeasurement가 만드는 쿠키의 만료를 무시합니다.
feature: Variables
exl-id: 2cd64301-9f12-4e77-abae-af431e4b499d
source-git-commit: 78cfb1f3c4d45fc983982a8da11b66f2b2c9ecbc
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 64%

---

# cookieLifetime

AppMeasurement에서 설정하는 쿠키는 일반적으로 만료 기한이 2년입니다. AppMeasurement에서 설정한 쿠키의 만료 날짜를 무시하려면 `cookieLifetime` 변수를 사용하십시오.

>[!NOTE]
>
>이 변수는 고유 방문자 수 및 기여도 분석에 영향을 줍니다. 이 변수를 설정할 때에는 주의하십시오.

## 웹 SDK를 사용한 쿠키 라이프타임

웹 SDK는 아직 설정하는 쿠키 수명 동안 사용자 지정을 제공하지 않습니다.

## Adobe Analytics 확장을 사용한 쿠키 라이프타임

쿠키 라이프타임은 [!UICONTROL 쿠키] 아코디언을 사용하여 Adobe Analytics 확장을 구성할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1.  [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
1. 를 확장합니다. [!UICONTROL 쿠키] 아코디언을 표시합니다. [!UICONTROL 쿠키 수명] 드롭다운 목록.

이 드롭다운 목록에는 다음 값이 포함되어 있습니다.

* **기본값**: 쿠키가 2년 후 만료됩니다.
* **없음**: AppMeasurement가 쿠키를 설정하지 않습니다.
* **세션**: 쿠키가 방문자 세션이 끝날 때 만료됩니다.
* **초**: 지정된 초 수가 경과하면 쿠키가 만료됩니다. 예를 들어 이 드롭다운 목록을 로 설정합니다. [!UICONTROL 초] 및 배치 `86400` 을 사용자 지정 필드에 삽입하면 쿠키가 정확히 24시간 후에 만료됩니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.cookieLifetime

`s.cookieLifetime` 변수는 AppMeasurement에서 설정한 쿠키의 만료 날짜를 결정하는 문자열입니다.

* `SESSION`으로 설정하면 AppMeasurement에서 설정한 쿠키가 브라우저 세션이 완료된 후 만료됩니다.
* `NONE`으로 설정하면 AppMeasurement가 쿠키를 설정하지 않습니다.
* 정수 문자열로 설정하면 AppMeasurement에서 설정한 쿠키가 지정된 초 수가 경과하면 만료됩니다.

```js
// Expire cookies after each session
s.cookieLifetime = "SESSION";

// Expire cookies after exactly 24 hours
s.cookieLifetime = "86400";
```
