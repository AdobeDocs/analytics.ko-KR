---
title: Adobe Analytics 및 브라우저 쿠키
description: 방지 추적 조치가 Adobe Analytics에서 설정한 제3자 및 제1자 쿠키에 미치는 영향을 알아봅니다.
translation-type: tm+mt
source-git-commit: 07c76cea1f6fd64957fd4fd20bc5187976f3c14c
workflow-type: tm+mt
source-wordcount: '1887'
ht-degree: 7%

---


# Adobe Analytics 및 브라우저 쿠키

이 문서에서는 주요 브라우저의 추적 방지 조치가 Adobe Analytics이 설정하는 제3자 및 자사 쿠키에 어떤 영향을 미치는지 설명합니다. 여기에는 Apple의 ITP(Intelligent Tracking Prevention) 프로그램에 대한 정보와 SameSite 속성을 통해 제3자 쿠키에 대한 Chrome의 제한 사항이 포함됩니다.

## 브라우저가 쿠키 사용을 제한한 이유는 무엇입니까?

### 타사 쿠키 제한

제3자 컨텍스트에 사용된 쿠키는 더 이상 사용되지 않습니다. Firefox 및 Safari는 2019년과 2020년에 각각 기본적으로 제3자 쿠키를 차단했습니다. Chrome은 2022년쯤에 제3자 쿠키 지원을 중단할 계획이라고 발표했습니다. 이렇게 하면 제3자 쿠키는 사실상 사용할 수 없게 됩니다.

또한, Chrome에서는 현재 &quot;SameSite&quot; 속성이 [없음]으로 설정되어 있고, &quot;SameSite&quot; 속성이 &quot;secure&quot;로 레이블이 지정되는 경우에만 제3자 컨텍스트에서 쿠키가 작동할 수 있도록 허용합니다. 이것은 쿠키를 HTTPS를 통해서만 사용할 수 있음을 의미합니다. 자세한 내용은 &quot;[SameSite 쿠키 속성은 무엇이며 Analytics에 어떤 영향을 미칩니까?](#samesite-effect)&quot; 섹션에 있습니다.

#### 영향을 받는 Adobe 제3자 쿠키는 무엇입니까?

방문자 ID 서비스는 [`demdex.net`](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html) 쿠키를 사용하여 다른 고객 도메인에서 방문자에 대한 영구 식별자를 제공합니다. 타사 쿠키가 차단된 브라우저에서는 도메인 간 추적을 사용할 수 없습니다.

### 자사 쿠키 제한 사항 {#limitations-first-party-cookies}

자사 쿠키는 모든 주요 브라우저에서 허용됩니다. 하지만, Apple은 ITP(Intelligent Tracking Program)를 통해 Adobe이 설정하는 자사 쿠키의 수명을 제한합니다. 여기에는 MacOS의 Safari와 iOS 및 iPadOS의 모든 브라우저가 포함됩니다.

Adobe의 자사 쿠키는 Apple이 판단하기에 추적기에서 나오는 클릭스루 횟수에 대한 7일 만료 또는 24시간 만료로 제한됩니다. 7일 만료의 경우, 사용자가 사이트를 방문하고 7일 이내에 돌아오면, 쿠키의 만료 날짜는 다른 7일까지 연장됩니다. 그러나 사용자가 사이트를 방문하고 8일 후에 돌아오면 두 번째 방문에서 새 사용자로 처리됩니다.

현재, ITP 정책은 방문자 ID 서비스 또는 이전 Analytics ID(&quot;s_vi&quot; 쿠키)를 사용하든 Adobe이 설정한 모든 자사 쿠키에 적용됩니다. 한 시점에서, 이러한 정책은 CNAME 구현을 통해 서버측을 설정하는 쿠키와 달리 클라이언트측을 설정하는 쿠키에만 적용됩니다. 그러나 2020년 11월에 ITP가 업데이트되어 CNAME 구현에도 적용되었습니다.

#### ITP 정책에 대한 주요 변경 사항 타임라인

* [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) 포함: 2019년 2월클라이언트측 쿠키는 7일 만료로 제한됩니다.
* [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) 포함:참조 도메인이 a) 사이트 간 추적과 관련이 있고 b) 최종 URL에 쿼리 문자열 및/또는 조각 식별자가 포함된 경우 클라이언트측 쿠키는 광고 클릭에 대해 24시간으로 제한되었습니다.
* [CNAME 종료 및 바운스 추적 방어가 포함된 2020년 11월](https://webkit.org/blog/11338/cname-cloaking-and-bounce-tracking-defense/):ITP 제한이 CNAME 구현으로 확장되었습니다.

ITP 정책은 자주 진화하고 있습니다. 최신 정책은 Webkit](https://webkit.org/tracking-prevention)의 추적 방지를 참조하십시오.[

#### 영향을 받는 Adobe 퍼스트 파티 쿠키는 무엇입니까?

Adobe에 의해 설정된 모든 자사 쿠키 및 관련 JavaScript 라이브러리는 ITP 정책의 영향을 받습니다.

* [`AMCV` Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html) 방문자 ID(ECID) 서비스 라이브러리에서 설정한 쿠키
* CNAME을 사용하여 퍼스트 파티 데이터 수집으로 구성된 경우 Analytics 이전 [`s_vi` 쿠키](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html)
* `s_vi`을(를) 설정할 수 없을 때 사용되는 폴백 쿠키인 Analytics 이전 [`s_fid` 쿠키](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html)

#### Analytics용 Safari에 ITP가 미치는 영향은 무엇입니까?

ITP 제한 사항의 영향은 사용자의 행동에 따라 상당히 달라집니다. ITP로 인해 영향을 받는 브라우저(Safari)를 사용하고 7일간의 부재 후 돌아오는 방문자만 영향을 받습니다. 방문자가 ITP 브라우저를 사용하지 않거나 7일 이내에 재방문하면 영향을 받지 않습니다. Analytics에서 자신의 데이터를 검토하여 이 제한이 미치는 영향을 이해해야 합니다. 사이트에 미치는 영향을 측정하는 방법에 대한 팁은 &quot;[Safari 변경 사항이 비즈니스에 영향을 미치는지 어떻게 확인할 수 있습니까?](#measure-itp-effect)&quot;를 참조하십시오.

이러한 제한이 데이터에 영향을 주는 경우 다음을 볼 수 있습니다.

1. 쿠키가 만료되었기 때문에 재방문자로 카운트되는 증가된 방문자는 새 방문자로 처리됩니다. 방문자 지표를 기반으로 하는 모든 지표(예: 방문자당 판매)도 영향을 받습니다.
2. 속성 변경 사항. 전환 이벤트는 같은 방문자의 이전 활동과 연결되어 있습니다. 쿠키가 만료되면 향후 이벤트는 새 방문자와 연결되며 전환은 원래 방문자에게 다시 연결될 수 없습니다.

>[!NOTE]
>
>현재 ITP 기술은 모바일 앱의 임베디드 브라우저에 적용되지 않습니다.

## 서드파티 쿠키와 자사 쿠키의 차이점은 무엇입니까?

### 서드파티 쿠키

제3자 쿠키는 사용자가 방문하는 웹사이트에 의해 만들어지지 않습니다.

브라우저가 현재 모든 제3자 쿠키를 동일하게 처리하고 그에 따라 저장하지만, 제3자 쿠키는 다른 방식으로 작동할 수 있습니다. 고객의 Analytics 제3자 쿠키 구현을 사용하는 브라우저는 Adobe [demdex.net](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html) ID를 제3자 쿠키로 저장하지만 클라이언트는 Adobe에만 호출하고 알 수 없거나 의심스러운 제3자 도메인에는 호출하지 않습니다. 이 쿠키는 도메인 간에 영구 식별자를 제공하며 보안(HTTPS) 콘텐츠를 허용합니다. 자세한 내용은 [쿠키 및 Experience Platform ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html)를 참조하십시오.

Analytics 구현 내에서 제3자 쿠키는 도메인 간 추적과 광고 재타깃팅 광고를 포함한 광고 사용 사례에 사용됩니다. 제3자 쿠키를 사용하면 사용자가 소유하는 다른 도메인을 방문하거나 소유하지 않은 사이트에 광고를 표시할 때 방문자를 식별할 수 있습니다.<!--  Without these cookies, you cannot identify visitors as they visit different domains that you own or as they are shown ads on sites that you do not own unless your implementation can stitch other types of cookies and   -->

### 자사 쿠키 (First-party cookies)

자사 쿠키는 도메인별로 다르며, 고객 웹 사이트에서 만들고 사용자가 웹 사이트를 방문할 때 클라이언트 브라우저에 저장됩니다. 모든 브라우저는 일반적으로 퍼스트 파티 쿠키를 승인하지만, [Safari는 일부 유형의 자사 쿠키](#limitations-first-party-cookies)의 사용을 제한합니다.

Analytics 구현 내에서 자사 쿠키는 사용자가 사이트에 있을 때 사용자를 식별하기 위해 사용되므로 사용자 활동에 대한 모든 분석을 지원합니다. 온사이트 활동을 이해하려면 타사 쿠키가 필요하지 않습니다.

자세한 내용은 [자사 쿠키 정보](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html)를 참조하십시오.

![쿠키 비교](/help/technotes/assets/cookies2.png)

## SameSite 쿠키 속성은 무엇이며 Analytics 쿠키에 어떤 영향을 줍니까?{#samesite-effect}

2020년 2월에 Chrome 80 브라우저가 릴리스되고 Firefox 및 Edge 브라우저의 후속 버전이 있을 경우, SameSite 쿠키 속성은 사이트 간 요청 동작을 제어하기 위해 3개의 다른 값에 대한 사양을 적용합니다.

* `None`: 이 설정을 사용하면 사이트 간 액세스가 가능하고 쿠키를 타사 컨텍스트에서 전달할 수 있습니다. 이 속성을 지정하려면 `Secure`도 지정해야 하며 모든 브라우저 요청이 HTTPS를 따라야 합니다. 예를 들어 쿠키를 설정할 때 속성 값을 다음과 같이 쌍으로 묶습니다. `Set-Cookie: example_session=test12; SameSite=None; Secure`. 제대로 레이블이 지정되지 않으면 쿠키는 최신 브라우저에서 사용할 수 없고 거부됩니다.

* `Lax`:사이트 간 요청이 동일한 사이트 쿠키와 함께 전송되도록 허용하며,  *안전* (예: 읽기 전용) HTTP 메서드를 사용하는 최상위 수준의 탐색에만  `GET`사용됩니다.

* `Strict`: 타사 웹 사이트 요청에 대해 동일한 사이트 쿠키가 전송되지 않습니다. 쿠키에 대한 사이트가 URL 표시줄의 사이트와 일치하는 경우에만 쿠키가 전송됩니다.

이러한 브라우저 버전의 기본 동작은 지정된 `SameSite` 속성이 없는 쿠키를 `SameSite=Lax`와 동일하게 처리하는 것입니다.

### Analytics는 SameSite 쿠키 속성을 어떻게 관리합니까?

모든 Adobe 쿠키 업데이트는 Adobe 서버를 통해 처리되며 Adobe Edge Server는 적절한 쿠키 특성을 설정합니다. 모든 제3자 쿠키는 적절한 속성을 사용하여 서버 측에서 업데이트되었습니다. 사이트에 JavaScript 업데이트가 필요하지 않습니다.

Adobe Edge Server에 의한 이 업그레이드는 사용자가 쿠키가 사용된 모든 웹 사이트를 방문할 때 자동으로 수행됩니다. 대부분의 Adobe 제품의 경우 Chrome 80이 2020년에 릴리스될 때 쿠키에 적절한 플래그가 적용되었습니다. 예외 사항은 제3자 데이터 수집을 사용하고 Experience Cloud 방문자 ID 서비스를 사용하지 않는 Adobe Analytics 구현입니다. 이러한 유형의 구현에 대해서는 고객 지원 센터에 플래그를 변경하도록 요청해야 합니다.자세한 내용은 다음 섹션의 &quot;[여러 도메인에 대해 하나의 CNAME을 사용할 때 동일한 사이트 값 변경](#samesite-one-cname)&quot;을 참조하십시오. 플래그가 변경될 때까지 이러한 고객은 새로운 방문자가 일시적으로 증가하거나 재방문자로 태그를 지정할 수 있습니다.

`SameSite`이(가) `None`(으)로 설정된 경우 Google에서 잘못 처리한 쿠키로 식별한 브라우저의 경우 `SameSite`이(가) 대신 설정되지 않은 상태로 유지됩니다.

다음 표에 Analytics 쿠키에 대한 SameSite 속성이 요약되어 있습니다.

![쿠키 테이블](/help/technotes/assets/cookies1.png)

### 내 사이트에서 SameSite 속성에 대한 요구 사항을 어떻게 해결할 수 있습니까?

#### HTTPS를 사용하여 모든 사이트 페이지 제공

JavaScript 구성에서 Adobe 서비스에 대한 모든 호출에 대해 HTTPS를 사용하는지 확인합니다.

사이트에서 Experience Cloud 방문자 ID 서비스를 사용하는 경우 서비스는 제3자 HTTP 호출을 HTTPS 끝점으로 리디렉션하여 지연을 높일 수 있지만 구성을 변경할 필요가 없음을 의미합니다.

#### 여러 도메인 {#samesite-one-cname}에 대해 하나의 CNAME을 사용할 때 SameSite 값을 변경합니다.

>[!NOTE]
>
>다음 정보는 Experience Cloud 방문자 ID 서비스를 사용하지 않는 사이트에만 해당됩니다.

웹 사이트와 동일한 도메인에 설정된 CNAME 구현이 있는 경우 퍼스트 파티 컨텍스트에서 쿠키가 생성되므로 변경할 필요가 없습니다.

하지만 여러 도메인을 소유하고 있고 모든 도메인에서 데이터 수집에 동일한 CNAME을 사용하는 경우 쿠키는 다른 도메인에서 제3자 쿠키로 처리됩니다. Chrome 80 이상의 경우 이러한 다른 도메인에서 더 이상 볼 수 없습니다. 모든 브라우저에서 비헤이비어가 보다 유사하도록 Analytics는 이 쿠키의 `SameSite` 값을 `Lax`으로 명시적으로 설정했습니다. 친숙한 타사 컨텍스트에서 이 쿠키를 사용하는 경우, `SameSite=None` 값으로 설정된 쿠키가 있어야 합니다. 즉, 항상 HTTPS를 사용해야 합니다. 아직 그렇게 하지 않은 경우 Adobe 고객 지원 센터에 문의하여 보안 CNAME에 대해 동일한 사이트 값을 변경하십시오.

## Safari 변경 사항이 비즈니스에 영향을 미치는지 어떻게 확인할 수 있습니까?{#measure-itp-effect}

Adobe은 고객이 데이터 수집을 변경하기 전에 회사 내의 영향을 측정할 것을 권장합니다. Analysis Workspace을 사용하여 개인 비즈니스에 대한 ITP 추적 방지 효과를 측정할 수 있습니다.

* ITP 관리 브라우저에서 트래픽의 비율을 측정합니다.

   1. 세그먼트를 만들어 ITP 플랫폼을 사용하는 방문자 수를 확인합니다.

      ![ITP 방문자용 세그먼트](/help/technotes/assets/itp-visitor-segment.png)

   2. 방문 횟수에 세그먼트를 적용하여 사용자 기반에서 Safari의 상대적 사용량을 파악합니다. 다음과 같은 테이블을 만들 수 있습니다.

      ![ITP 방문자별 방문 비율](/help/technotes/assets/visits-vs-safari-visits.png)

* 7일 이내에 돌아오지 않는 비 Safari 브라우저를 사용하는 방문자의 비율을 측정합니다. Safari가 아닌 방문자가 7일 이내에 반복적으로 돌아오는 경우 Safari 트래픽에 큰 영향을 주지 않을 수 있습니다.

   1. Safari가 아닌 트래픽에 대해 다음과 같은 세그먼트를 만듭니다.

      ![7일 후 돌아오는 방문자를 위한 세그먼트](/help/technotes/assets/visits-after-seven-days.png)

   2. 방문 횟수에 세그먼트를 적용하여 사용자 기반에서 Safari의 상대적 사용량을 파악합니다. 다음과 같은 테이블을 만들 수 있습니다.

      ![7일 후 돌아오는 방문자의 비율](/help/technotes/assets/percent-visits-after-seven-days.png)

### 보고 중에 데이터를 조정하는 방법

ITP 추적 방지 기능이 비즈니스에 영향을 미치는 경우 보고 중에 데이터를 조정하기 위해 다음 조치를 고려할 수 있습니다.

* ITP 사용자를 필터링하는 세그먼트를 만듭니다.

   ![ITP가 아닌 방문자에 대한 세그먼트](/help/technotes/assets/non-itp-visitor-segment.png)

* 알려진 방문자 인플레이션에 맞게 조정할 계산된 지표를 만듭니다.

   ![방문자 인플레이션에 맞게 조정할 계산된 지표](/help/technotes/assets/estimated-itp-visitors-metric.png)

>[!MORELIKETHIS]
>
>[브라우저 쿠키 제한의 효과를 완화시키는 옵션](cookieless.md)
>[Apple의 새로운 앱 추적 투명도 프레임워크가 Adobe Analytics](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-impact-of-apple-s-new-app-tracking-transparency-framework-on/td-p/401833)에 미치는 영향
