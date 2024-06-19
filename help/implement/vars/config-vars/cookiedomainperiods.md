---
title: cookieDomainPeriods
description: (사용 안 함) 웹 사이트의 최상위 도메인에 마침표가 포함되어 있을 때 도움말 AppMeasurement이 쿠키를 저장할 위치를 결정합니다.
feature: Variables
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
role: Admin, Developer
source-git-commit: 75ae77c1da1b578639609888e794e13d965ef669
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 19%

---


# cookieDomainPeriods

>[!IMPORTANT]
>이 변수는 더 이상 사용되지 않습니다. AppMeasurement v2.26.x 이상 또는 Adobe Analytics 확장 v1.9.4 이상을 사용하는 경우 라이브러리는 쿠키를 설정할 도메인을 자동으로 감지합니다.

다음 `cookieDomainPeriods` 변수는 AppMeasurement이 최상위 도메인에 추가 기간이 있음을 표시하여 Analytics 쿠키를 설정할 위치를 결정하는 데 도움이 되었습니다. 이 변수를 사용하면 AppMeasurement이 최상위 도메인의 추가 기간을 수용하고 올바른 위치에 쿠키를 설정할 수 있습니다. 웹 사이트의 최상위 도메인에 추가 기간이 포함되지 않은 경우 이 변수는 필요하지 않습니다.

* `example.co.uk` 또는 `www.example.co.jp`와 같은 도메인의 경우에는 이 변수를 `"3"`로 설정하십시오.
* 과 같은 도메인의 경우 `example.nsw.gov.au`, 이 변수를 다음으로 설정 `"4"`.
* 과 같은 도메인의 경우 `example.com` 또는 `products.example.org`, 이 변수 설정을 생략하거나 다음으로 설정 `"2"`.

>[!TIP]
>
>이 변수에 대해 하위 도메인을 고려하지는 마십시오. 예를 들어 `cookieDomainPeriods`이라는 URL 예에서는 `store.toys.example.com`를 설정하지 마십시오. AppMeasurement은 쿠키가에 저장되어 있음을 인식합니다. `example.com`하위 도메인이 많은 URL에서도 가능합니다.

AppMeasurement v2.26.x 이상에서 구현의 경우 [`s_ac`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) 쿠키는 올바른 쿠키 도메인을 자동으로 판별하는 데 사용됩니다. 라이브러리는 먼저 두 개의 도메인 마침표를 포함하는 쿠키를 작성하려고 합니다. 이 쿠키를 설정하지 못하면 성공할 때까지 더 많은 도메인 기간을 포함하여 다시 시도합니다. 이 쿠키는 설정되면 즉시 삭제됩니다.

## 웹 SDK를 사용한 쿠키 도메인 마침표

Web SDK는 쿠키를 설정할 올바른 도메인을 자동으로 결정합니다.

## Adobe Analytics 확장을 사용한 쿠키 도메인 마침표

**[!UICONTROL 도메인 마침표]** 은(는) 아래 필드입니다. [!UICONTROL 쿠키] Adobe Analytics 확장을 구성할 때 아코디언

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
1. [!UICONTROL 쿠키] 아코디언을 확장합니다. 그러면 [!UICONTROL 도메인 마침표] 필드가 표시됩니다.

이 필드를 다음으로 설정 `3` 마침표를 포함하는 최상위 도메인에서만 가능합니다. 그렇지 않으면 이 필드를 비워 둘 수 있습니다.

## AppMeasurement 및 Analytics 확장 사용자 정의 코드 편집기의 쿠키 도메인 마침표

다음 `cookieDomainPeriods` 변수는 일반적으로 로 설정된 문자열입니다. `"3"`를 조정할 때 반드시 필요합니다. 기본값은 입니다 `"2"`와 같은 대부분의 최상위 도메인을 포함합니다. `.com` 및 `.org`.

```js
// Manually set cookieDomainPeriods for domains with a period in the top-level domain, such as www.example.co.uk
s.cookieDomainPeriods = "3";
```
