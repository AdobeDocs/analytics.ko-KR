---
title: cookieDomainPeriods
description: 도메인의 접미사에 마침표가 있는 경우 쿠키를 저장할 도메인을 AppMeasurement가 이해하도록 도와줍니다.
feature: Variables
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
role: Admin, Developer
source-git-commit: 43c39b99cbae3e714b7f017dec14dd02fa350790
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 43%

---


# cookieDomainPeriods

AppMeasurement는 도메인과 도메인 접미사를 확인하여 쿠키 위치를 결정합니다. `example.com`과 같은 도메인의 경우 AppMeasurement는 쿠키를 올바른 위치에 설정합니다. 하지만, `example.co.uk`와 같은 다른 도메인의 경우 AppMeasurement가 실수로 쿠키를 `co.uk`에 설정할 수 있습니다. 대부분의 브라우저는 이 잘못된 도메인에 설정된 쿠키를 거부하여 방문자 식별에 문제가 발생합니다.

`cookieDomainPeriods` 변수는 AppMeasurement가 도메인 접미사에 불필요한 마침표가 있음을 표시하여 Analytics 쿠키의 설정 위치를 확인하는 데 도움이 됩니다. 이 변수를 사용하면 AppMeasurement가 도메인 접미사의 불필요한 마침표를 수용하고 올바른 위치에 쿠키를 설정할 수 있습니다.

* `example.com` 또는 `www.example.com`과 같은 도메인의 경우 이 변수를 설정할 필요가 없습니다. 필요한 경우 이 변수를 `"2"`로 설정할 수 있습니다.
* `example.co.uk` 또는 `www.example.co.jp`와 같은 도메인의 경우에는 이 변수를 `"3"`로 설정하십시오.


>[!IMPORTANT]
>
>이 변수에 대해 하위 도메인을 고려하지는 마십시오. 예를 들어 `cookieDomainPeriods`이라는 URL 예에서는 `store.toys.example.com`를 설정하지 마십시오. AppMeasurement는 여러 하위 도메인이 있는 URL에서도 기본적으로 쿠키가 `example.com`에 저장되어야 한다고 인식합니다.


## 쿠키 도메인 기간, 타사 쿠키 및 기존 방문자 식별

권장 Experience Cloud ID 서비스 대신 기존 Adobe Analytics 방문자 ID를 사용하는 경우에만 의 암시적 또는 명시적 구성 `cookieDomainPeriods` 은 서드파티 쿠키의 차단 여부에 따라 방문자가 식별되는 방식에 영향을 줄 수 있습니다.

다음 표는 네 가지 가능한 시나리오를 보여 줍니다.

| 시나리오 | `cookieDomainPeriods` 구성은 입니다... | 서드파티 쿠키가 차단되었습니까? | 기존 Adobe Analytics 방문자 식별 서비스를 사용할 때의 결과 |
|:---:|---|---|---|
| 1 | <span style="color:green">정답</span> | 아니요 | 방문자는 다음으로 식별됨 `s_vi` 쿠키, 서버측을 설정합니다. |
| 2 | <span style="color:green">정답</span> | 예 | 방문자는 대체 항목으로 식별됩니다. `s_fid` 쿠키, 클라이언트측(자사 페이지 도메인)을 설정합니다. |
| 3 | <span style="color:red">잘못됨</span> | 아니요 | 방문자는 사용자 에이전트와 IP 주소의 조합을 기반으로 하는 대체 식별자로 식별됩니다. <br/>AppMeasurement은 쿠키를 타사 쿠키로 설정해야 합니다.<br/> 다음 `s_vi` 쿠키는 다음과 같은 경우에 설정됩니다. `cookieDomainPeriods` 가 제대로 전송되지 않습니다. |
| 4 | <span style="color:red">잘못됨</span> | 예 | 방문자는 사용자 에이전트와 IP 주소의 조합을 기반으로 하는 대체 식별자로 식별됩니다.<br/>AppMeasurement은 쿠키를 차단된 서드파티 쿠키로 설정해야 하므로 쿠키가 설정되지 않습니다. |

>[!CAUTION]
>
>실수로 구성되었을 수 있습니다. `cookieDomainPeriods` <span style="color:red">부정확해</span> (기본값: `"2"`)과 같은 도메인을 사용하는 동안 `example.co.uk`. 이렇게 하면 시나리오 3 또는 4에 따라 방문자를 식별하는 결과가 부정확해집니다.
>
>AppMeasurement 릴리스 2.26.x 이상 `cookieDomainPeriods` 은 시나리오 1 또는 2만 가능하도록 올바른 값을 사용하여 자동으로 수행됩니다. 현재 방문자를 잘못 식별하는(시나리오 3 또는 4) 동안 AppMeasurement 릴리스 2.26.x 이상으로 업데이트하는 경우, 업데이트에 중요한 의미가 있습니다.
>
>* 방문자 식별자가 재설정되고 방문자는 새 방문자로 표시됩니다. 새 활동을 이전 방문자 식별자에 연결할 수 있는 방법이 없습니다.
>* 쿠키가 설정됩니다 (예: 링크 추적 또는 Activity Map용).`s_sq` cookie), 보고에서 갑작스런 차이 발생.
>
>올바르게 구성하는 동안 `cookieDomainPeriods` 는 AppMeasurement 및 Analytics 기능을 향상시키므로 AppMeasurement 라이브러리 업그레이드로 인한 변경 사항의 영향을 받는지 평가하는 것이 좋습니다.
>
> 다음을 참조하십시오 [Analytics 쿠키](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=ko-KR) AppMeasurement이 사용하는 쿠키에 대한 자세한 정보.

## 웹 SDK를 사용한 쿠키 도메인 마침표

Web SDK는 이 변수 없이 올바른 쿠키 스토리지 도메인을 결정할 수 있습니다.

## Adobe Analytics 확장을 사용한 쿠키 도메인 마침표

도메인 기간은 Adobe Analytics 확장을 구성할 때 [!UICONTROL 쿠키] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
1. [!UICONTROL 쿠키] 아코디언을 확장합니다. 그러면 [!UICONTROL 도메인 마침표] 필드가 표시됩니다.

접미사에 마침표를 포함하는 도메인에서만 이 필드를 `3`으로 설정하십시오. 다른 경우에는 이 필드를 비워 둘 수 있습니다.

## 코드 AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 쿠키 도메인 마침표

다음을 설정할 수 있습니다. `cookieDomainPeriods` AppMeasurement 변수를 채우는 방법에 따라 페이지를 순서대로 표시합니다.

`cookieDomainPeriods` 변수는 일반적으로 접미사에 마침표를 포함하는 도메인에서만 `"3"`으로 설정되는 문자열입니다. 기본값은 `"2"`이고, 이렇게 하면 대부분의 도메인이 포함됩니다.

```js
// Manually set cookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.cookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.cookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```
