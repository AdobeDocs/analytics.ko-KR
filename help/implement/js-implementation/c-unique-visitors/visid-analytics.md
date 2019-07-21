---
description: 사용자가 사이트를 방문하면, Adobe 웹 서버에서는 브라우저에 대한 HTTP 응답에 영구적 쿠키를 포함하여 영구적 쿠키를 설정합니다. 이 쿠키는 지정된 데이터 수집 도메인에서 설정됩니다.
keywords: Analytics 구현
seo-description: 사용자가 사이트를 방문하면, Adobe 웹 서버에서는 브라우저에 대한 HTTP 응답에 영구적 쿠키를 포함하여 영구적 쿠키를 설정합니다. 이 쿠키는 지정된 데이터 수집 도메인에서 설정됩니다.
seo-title: Analytics 방문자 ID
solution: Analytics
title: Analytics 방문자 ID
topic: 개발자 및 구현
uuid: FA 7737 CC -0190-4 D 27-AF 1 B -87301 A 715 DF 2
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Analytics 방문자 ID

사용자가 사이트를 방문하면, Adobe 웹 서버에서는 브라우저에 대한 HTTP 응답에 영구적 쿠키를 포함하여 영구적 쿠키를 설정합니다. 이 쿠키는 지정된 데이터 수집 도메인에서 설정됩니다.

Adobe 데이터 수집 서버로 요청이 전송되면 헤더에 방문자 ID 쿠키(`s_vi`)가 있는지 확인이 이루어집니다. 이 쿠키가 요청에 있으면 방문자 식별에 사용됩니다. 쿠키가 요청에 없으면 서버가 고유한 방문자 ID를 생성하고 이것을 HTTP 응답 헤더의 쿠키로 설정하여 다시 요청과 함께 전송합니다. 쿠키는 브라우저에 저장되었다가 다음에 사이트를 방문할 때 데이터 수집 서버로 전송되어 방문 중에 방문자를 식별할 수 있게 합니다.

## 타사 쿠키 및 CNAME 레코드 {#section_61BA46E131004BB2B75929C1E1C93139}

Apple Safari와 같은 일부 브라우저는 현재 웹 사이트의 도메인과 일치하지 않는 도메인의 HTTP 헤더에 설정된 쿠키를 더 이상 보관하지 않습니다(타사 컨텍스트에 사용된 쿠키이거나 타사 쿠키). 예를 들어 `mysite.com`을 방문 중이고 데이터 수집 서버가 `mysite.omtrdc.net`인 경우 브라우저가 `mysite.omtrdc.net`의 HTTP 헤더에서 반환되는 쿠키를 거부할 수 있습니다.

이를 방지하기 위해 많은 고객들이 [자사 쿠키 구현](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/)의 일부로서 데이터 수집 서버에 대한 CNAME 레코드를 구현했습니다. CNAME 레코드가 고객 도메인을 데이터 수집 서버로 호스트 이름을 매핑하도록 구성된 경우(예: `metrics.mysite.com`을 `mysite.omtrdc.net`으로 매핑) 데이터 수집 도메인이 웹 사이트 도메인과 일치하므로 방문자 ID 쿠키가 저장됩니다. 이는 방문자 ID 쿠키가 저장될 가능성을 높이긴 하지만 CNAME 레코드를 구성하고 데이터 수집 서버에 대한 SSL 인증서를 유지해야 하므로 약간의 오버헤드를 유발합니다.

## 모바일 장치의 쿠키 {#section_7D05AE259E024F73A95C48BD1E419851}

쿠키를 사용하여 모바일 장치를 추적하는 경우 몇 가지 설정을 사용하여 측정 방식을 수정할 수 있습니다. 쿠키의 기본 수명은 5년이지만 CL 쿼리 매개 변수(`s.cookieLifetime`)를 사용하여 이 기본값을 바꿀 수 있습니다. cname 구현을 위해 쿠키 위치를 설정하려면 CDP 쿼리 문자열 `s.cookieDomainPeriods`를 사용하십시오. 값이 지정되지 않은 경우 기본값은 2입니다. 기본 위치는 domain.com입니다. CNAME을 사용하지 않는 구현의 경우 방문자 ID 쿠키 위치는 207.net 도메인입니다.
