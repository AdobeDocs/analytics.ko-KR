---
title: cookieLifetime
description: AppMeasurement가 만드는 쿠키의 만료를 무시합니다.
exl-id: 2cd64301-9f12-4e77-abae-af431e4b499d
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 85%

---

# cookieLifetime

AppMeasurement에서 설정하는 쿠키는 일반적으로 만료 기한이 2년입니다. AppMeasurement에서 설정한 쿠키의 만료 날짜를 무시하려면 `cookieLifetime` 변수를 사용하십시오.

>[!NOTE]
>
>이 변수는 고유 방문자 수 및 기여도 분석에 영향을 줍니다. 따라서 이 변수를 설정할 때에는 주의하십시오.

## Adobe Experience Platform 태그의 쿠키 수명

쿠키 라이프타임은 Adobe Analytics 확장을 구성할 때 [!UICONTROL 쿠키] 아코디언 아래의 드롭다운입니다.

1. `experience.adobe.com` 로 이동한 후 메시지가 표시되면 로그인합니다.
1. [!UICONTROL 시작 / 데이터 수집]을 선택합니다.
1. [!UICONTROL Launch / Data Collection으로 이동]을 클릭한 다음 [!UICONTROL 태그]를 선택합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
1. [!UICONTROL 쿠키] 아코디언을 확장합니다. 그러면 [!UICONTROL 쿠키 라이프타임] 드롭다운이 표시됩니다.

이 드롭다운에는 다음 값이 포함되어 있습니다.

* **기본값**: 쿠키가 2년 후 만료됩니다.
* **없음**: AppMeasurement가 쿠키를 설정하지 않습니다.
* **세션**: 쿠키가 방문자 세션이 끝날 때 만료됩니다.
* **초**: 지정된 초 수가 경과하면 쿠키가 만료됩니다. 예를 들어 이 드롭다운을 [!UICONTROL 초]로 설정하고 `86400`을 사용자 지정 필드에 배치하면 쿠키가 정확히 24시간 후에 만료됩니다.

## AppMeasurement 및 데이터 수집 사용자 지정 코드 편집기의 s.cookieLifetime

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
