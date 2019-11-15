---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics Implementation
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.cookieDomainPeriods

이 변수는 페이지 URL의 도메인에서 점의 수를 파악하여 [!DNL Analytics] 쿠키 `s_cc` 및 `s_sq`가 설정되는 도메인을 결정합니다. 이 변수는 일부 플러그인에서 플러그인의 쿠키를 설정할 올바른 도메인을 결정할 때 사용하기도 합니다.

*`cookieDomainPeriods`* 기본값은 "2"입니다. 이 값은 *`cookieDomainPeriods`*&#x200B;가 생략된 경우 사용됩니다. 예를 들어 `www.mysite.com` 도메인을 사용하는 경우 *`cookieDomainPeriods`*&#x200B;는 "2"여야 합니다. `www.mysite.co.jp`에서 *`cookieDomainPeriods`*&#x200B;는 "3"이어야 합니다.

*`cookieDomainPeriods`*&#x200B;가 "2"로 설정되어 있지만 도메인에 세 개의 점이 포함되어 있는 경우 JavaScript 파일은 도메인 접미사에 대한 쿠키 설정을 시도하게 됩니다.

예를 들어 `www.mysite.co.jp` 도메인에서 *`cookieDomainPeriods`*&#x200B;를 "2"로 설정하면 `co.jp` 도메인에 `s_cc` 및 `s_sq` 쿠키가 만들어집니다. `co.jp`가 잘못된 도메인이므로 거의 모든 브라우저는 이 쿠키를 거부하게 됩니다. 그 결과, 방문자 클릭 맵 데이터가 유실되고, [!UICONTROL 방문자 프로필] &gt; [!UICONTROL 기술] &gt; [!UICONTROL 쿠키] 보고서는 거의 100%의 방문자가 쿠키를 거부한다고 나타냅니다.

*`cookieDomainPeriods`*&#x200B;가 "3"으로 설정되어 있지만 도메인에 두 개의 점만 포함되어 있는 경우에는 JavaScript 파일이 사이트의 하위 도메인에 대한 쿠키를 설정합니다. 예를 들어 `www2.mysite.com` 도메인에서 *`cookieDomainPeriods`*&#x200B;를 "3"으로 설정하면 `www2.mysite.com` 도메인에 `s_cc` 및 `s_sq` 쿠키가 만들어집니다. 방문자가 사이트의 다른 하위 도메인(`www4.mysite.com` 등)으로 이동하면 `www2.mysite.com`과 관련하여 설정된 모든 쿠키를 읽을 수 없게 됩니다.

> [!NOTE] 의 일부로 추가 하위 도메인을 포함하지 *`cookieDomainPeriods`*&#x200B;마십시오. 예를 들어 `store.toys.mysite.com`에 여전히 *`cookieDomainPeriods`*&#x200B;가 "2"로 설정되어 있습니다. 이 변수 정의는 루트 도메인 [!DNL mysite.com]에 대한 쿠키를 올바로 설정합니다. 이 예에서 *`cookieDomainPeriods`*&#x200B;를 "3"으로 설정하면 [!DNL toys.mysite.com] 도메인에 대한 쿠키가 설정되고, 이 쿠키는 이전 예와 같은 의미를 갖습니다.

[s.fpCookieDomainPeriods](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html)도 참조하십시오.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | CDP | 여러 보고서에서 방문자 ID의 저장 및 처리 방식을 제어하는 데 영향을 줍니다. | "2" |

>[!NOTE]
>
>일부 클라우드 컴퓨팅 서비스는 쿠키를 작성할 수 없는 최상위 도메인으로 간주됩니다. 예: `compute.amazonaws.com`, `*.herokuapp.com`, `*.googlecode.com` 등. 이러한 서비스에 구현하는 경우 사용자 고유의 도메인이 설정되어 있지 않으면 모든 쿠키를 차단한 사용자를 제거하는 Analytics 개인 정보 보호 설정의 영향을 받을 수 있습니다(예: 구현을 테스트하는 경우). 이 경우 쿠키가 비활성화되었거나, 작동하지 않거나, 액세스할 수 없는 것으로 확인된 히트는 옵트아웃되므로, 보고에서 제외됩니다.

## 예

수동 변수 설정:

```js
s.cookieDomainPeriods = "3";
```

코어 Javascript 파일이 두 유형을 모두 호스팅하는 경우 이 변수를 동적으로 설정하는 몇 가지 예:

```js
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```

```js
s.cookieDomainPeriods = "2"; 
var d=window.location.hostname; 
if(d.indexOf(".co.uk") > 0 || d.indexOf(".com.au") > 0) 
    {s.cookieDomainPeriods = "3";}
```

```js
s.cookieDomainPeriods = "2"; 
if(window.location.indexOf(".co.jp") > 0 || window.location.indexOf(".com.au") > 0) 
    {s.cookieDomainPeriods = "3";}
```

## 함정, 질문 및 팁

* 방문자 클릭 맵 데이터가 없거나 [!UICONTROL 트래픽] &gt; [!UICONTROL 기술] &gt; [!UICONTROL 쿠키] 보고서에 많은 방문자가 쿠키를 거부하는 것으로 표시되면 *`cookieDomainPeriods`* 값이 올바른지 확인합니다.

* *`cookieDomainPeriods`*&#x200B;가 도메인의 섹션 수보다 큰 경우에는 쿠키가 전체 도메인에 설정됩니다. 이로 인해 방문자가 하위 도메인 간을 전환하면 데이터 손실이 발생할 수 있습니다.
* The *`cookieDomainPeriods`* 변수는 *`trackingServer`*&#x200B;가 방문자 ID 쿠키로 설정되기 전에 지원되지 않는 구현에 사용되었습니다. 오래된 코드에만 표시되지만 이 환경에서 *`cookieDomainPeriods`*&#x200B;를 올바르게 정의하지 않으면 구현 시 데이터가 손실됩니다.
