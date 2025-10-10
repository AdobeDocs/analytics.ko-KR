---
title: cookieDomainPeriods
description: (사용 중지) 웹 사이트의 최상위 도메인에 마침표가 포함되어 있을 때 AppMeasurement이 쿠키를 저장할 위치를 결정하는 데 도움이 됩니다.
feature: Appmeasurement Implementation
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 18%

---

# cookieDomainPeriods

>[!IMPORTANT]
>이 변수는 더 이상 사용되지 않습니다. 다음 중 하나를 사용하는 경우
>
>* AppMeasurement v2.26.x 이상
>* Adobe Analytics 확장 v1.9.4 이상
>* Adobe Experience Cloud ID 서비스
>
>해당 라이브러리는 쿠키를 설정할 도메인을 자동으로 감지하므로 이 변수는 아무 작업도 하지 않습니다.

`cookieDomainPeriods` 변수는 AppMeasurement이 최상위 도메인에 추가 기간이 있음을 표시하여 Analytics 쿠키를 설정할 위치를 결정하는 데 도움이 되었습니다. 이 변수를 사용하면 AppMeasurement이 최상위 도메인의 추가 기간을 수용하고 올바른 위치에 쿠키를 설정할 수 있습니다. 웹 사이트의 최상위 도메인에 추가 기간이 포함되지 않은 경우 이 변수는 필요하지 않습니다.

* `example.co.uk` 또는 `www.example.co.jp`와 같은 도메인의 경우에는 이 변수를 `"3"`로 설정하십시오.
* `example.nsw.gov.au`과(와) 같은 도메인의 경우 이 변수를 `"4"`(으)로 설정하십시오.
* `example.com` 또는 `products.example.org`과(와) 같은 도메인의 경우 이 변수 설정을 생략하거나 `"2"`(으)로 설정하십시오.

>[!TIP]
>
>이 변수에 대해 하위 도메인을 고려하지는 마십시오. 예를 들어 `cookieDomainPeriods`이라는 URL 예에서는 `store.toys.example.com`를 설정하지 마십시오. AppMeasurement은 쿠키가 여러 하위 도메인이 있는 URL에서도 `example.com`에 저장되어 있음을 인식합니다.

AppMeasurement v2.26.x 이상 버전의 구현의 경우 [`s_ac`](https://experienceleague.adobe.com/ko/docs/core-services/interface/data-collection/cookies/analytics) 쿠키를 사용하여 자동으로 올바른 쿠키 도메인을 결정합니다. 라이브러리는 먼저 두 개의 도메인 마침표를 포함하는 쿠키를 작성하려고 합니다. 이 쿠키를 설정하지 못하면 성공할 때까지 더 많은 도메인 기간을 포함하여 다시 시도합니다. 이 쿠키는 설정되면 즉시 삭제됩니다.

## 웹 SDK을 사용한 쿠키 도메인 마침표

웹 SDK은 쿠키를 설정할 올바른 도메인을 자동으로 결정합니다.

## Adobe Analytics 확장을 사용한 쿠키 도메인 마침표

**[!UICONTROL 도메인 마침표]**&#x200B;는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 쿠키] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
1. [!UICONTROL 쿠키] 아코디언을 확장합니다. 그러면 [!UICONTROL 도메인 마침표] 필드가 표시됩니다.

기간이 포함된 최상위 도메인에서만 이 필드를 `3`(으)로 설정하십시오. 그렇지 않으면 이 필드를 비워 둘 수 있습니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 쿠키 도메인 마침표

`cookieDomainPeriods` 변수는 일반적으로 마침표를 포함하는 최상위 도메인에서만 `"3"`(으)로 설정된 문자열입니다. 기본값은 `"2"`이며, 이 값은 `.com` 및 `.org`과(와) 같은 대부분의 최상위 도메인을 포함합니다.

```js
// Manually set cookieDomainPeriods for domains with a period in the top-level domain, such as www.example.co.uk
s.cookieDomainPeriods = "3";
```
