---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.cookieDomainPeriods

The  variable determines the domain on which the [!DNL Analytics] cookies `s_cc` and `s_sq` are set by determining the number of periods in the domain of the page URL. 이 변수는 일부 플러그인에서 플러그인의 쿠키를 설정할 올바른 도메인을 결정할 때 사용하기도 합니다.

기본값은 *`cookieDomainPeriods`* "2"입니다. This is the value that is used if *`cookieDomainPeriods`* is omitted. For example, using the domain `www.mysite.com`, *`cookieDomainPeriods`* should be "2". For `www.mysite.co.jp`, *`cookieDomainPeriods`* should be "3".

If *`cookieDomainPeriods`* is set to "2" but the domain contains three periods, the JavaScript file attempts to set cookies on the domain suffix.

For example, if setting *`cookieDomainPeriods`* to "2" on the domain `www.mysite.co.jp`, the `s_cc` and `s_sq` cookies are created on the domain `co.jp`. `co.jp`가 잘못된 도메인이므로 거의 모든 브라우저는 이 쿠키를 거부하게 됩니다. 그 결과, 방문자 클릭 맵 데이터가 유실되고, [!UICONTROL 방문자 프로필] &gt; [!UICONTROL 기술] &gt; [!UICONTROL 쿠키] 보고서는 거의 100%의 방문자가 쿠키를 거부한다고 나타냅니다.

If *`cookieDomainPeriods`* is set to "3" but the domain contains only two periods, the JavaScript file sets the cookies on the subdomain of the site. 예를 들어 도메인에서 *`cookieDomainPeriods`* "3"으로 설정하면 도메인에 `www2.mysite.com``s_cc` 및 `s_sq` 쿠키가 만들어집니다 `www2.mysite.com`. When a visitor goes to another subdomain of your site (such as `www4.mysite.com`), all cookies set with `www2.mysite.com` cannot be read.

>[!NOTE]
>
>Do not include additional subdomains as part of *`cookieDomainPeriods`*. 예를 들어, `store.toys.mysite.com` 여전히 "2"로 *`cookieDomainPeriods`* 설정되어 있습니다. 이 변수 정의는 루트 도메인 [!DNL mysite.com]에 대한 쿠키를 올바로 설정합니다. Setting *`cookieDomainPeriods`* to "3" in this example would set cookies on the domain [!DNL toys.mysite.com], which has the same implications as the prior example.

s.fpCookieDomainPeriods [도 참조하십시오](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-account.html).

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | CDP | 여러 보고서에서 방문자 ID의 저장 및 처리 방식을 제어하는 데 영향을 줍니다. | "2" |

>[!NOTE]
>
>일부 클라우드 컴퓨팅 서비스는 최상위 도메인으로 간주되므로 쿠키를 작성할 수 없습니다. (For example, `compute.amazonaws.com`, `*.herokuapp.com`, `*.googlecode.com`, and so on.) 이러한 서비스에 구현하는 경우 사용자 고유의 도메인이 설정되어 있지 않으면 모든 쿠키를 차단한 사용자를 제거하는 Analytics 개인 정보 보호 설정의 영향을 받을 수 있습니다(예: 구현을 테스트하는 경우). 이 경우 쿠키가 비활성화되었거나, 작동하지 않거나, 액세스할 수 없는 것으로 확인된 히트는 옵트아웃되므로, 보고에서 제외됩니다.

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

* 방문자 클릭 맵 데이터가 없는 것을 발견했거나 [!UICONTROL 트래픽] &gt; [!UICONTROL 기술] &gt; [!UICONTROL 쿠키] 보고서에 대량의 방문자가 쿠키를 거부하는 것으로 표시되면 *`cookieDomainPeriods`* 값이 올바른지 확인하십시오.

* If *`cookieDomainPeriods`* is higher than the number of sections in the domain, cookies will be set with the full domain. 이로 인해 방문자가 하위 도메인 간을 전환하면 데이터 손실이 발생할 수 있습니다.
* The 변수는 방문자 ID 쿠키를 설정하기 전에 더 이상 사용되지 않는 구현에서 *`cookieDomainPeriods`* *`trackingServer`* 사용되었습니다. 오래된 코드에만 존재하지만 이러한 상황에서 올바로 정의하지 *`cookieDomainPeriods`* 않으면 구현 시 데이터 손실이 발생할 수 있습니다.