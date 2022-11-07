---
title: Adobe Analytics 및 브라우저 쿠키
description: 추적 방지 조치가 Adobe Analytics에서 설정한 서드파티 및 자사 쿠키에 어떤 영향을 미치는지 알아보십시오.
feature: Data Configuration and Collection
exl-id: c4a4751e-49fc-40c3-aa39-f0f0b20bda1b
source-git-commit: ac9e4934cee0178fb00e4201cc3444d333a74052
workflow-type: tm+mt
source-wordcount: '1981'
ht-degree: 99%

---

# Adobe Analytics 및 브라우저 쿠키

이 문서에서는 주요 브라우저의 추적 방지 조치가 Adobe Analytics에서 설정한 서드파티 및 자사 쿠키에 미치는 영향을 설명합니다. 여기에는 Apple의 ITP(Intelligent Tracking Prevention) 프로그램에 대한 정보와 SameSite 속성을 통한 서드파티 쿠키에 대한 Chrome의 제한 사항이 포함됩니다.

## 브라우저는 쿠키 사용을 어떻게 제한했습니까?

>[!NOTE]
>[Cross-Device Analytics](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html#cda) 및 [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html#comparing-cja-to-traditional-adobe-analytics)는 해시된 로그인 id와 같은 사용자 ID를 사용하여 쿠키 간에 연결할 수 있습니다.

### 서드파티 쿠키 제한

서드파티 컨텍스트에서 사용되는 쿠키는 광범위하게 더 이상 사용되지 않고 있습니다. Firefox와 Safari는 각각 2019년과 2020년부터 기본적으로 서드파티 쿠키를 차단하기 시작했습니다. Chrome은 2023년에 서드파티 쿠키 지원을 중단할 계획을 발표했습니다. 그럴 경우 서드파티 쿠키는 사실상 사용할 수 없게 됩니다.

또한 Chrome은 현재 “SameSite” 속성이 없음으로 설정되어 있고 보안 레이블로 지정되어 있는 경우(HTTPS를 통해서만 사용할 수 있음을 의미함)에만 서드파티 컨텍스트에서 작동하도록 허용합니다. 자세한 내용은 “[SameSite 쿠키 속성이란 무엇이며 Analytics에 어떤 영향을 줍니까?](#samesite-effect)” 섹션에서 확인할 수 있습니다.

#### 영향을 받는 Adobe 서드파티 쿠키는 무엇입니까?

방문자 ID 서비스는 &quot;[demdex.net](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html?lang=ko-KR)&quot; 쿠키를 사용하여 다양한 고객 도메인의 방문자에 대한 영구 식별자를 제공합니다. 기존 Analytics ID 서비스인 &quot;s_vi&quot; 쿠키는 사용자 지정 CNAME 수집 도메인을 사용하지 않는 구현을 위한 서드파티 쿠키로 설정됩니다.

서드파티 쿠키가 차단된 브라우저에서는 도메인 간 추적을 사용할 수 없습니다.

### 자사 쿠키 제한 {#limitations-first-party-cookies}

자사 쿠키는 모든 주요 브라우저에서 허용됩니다. 그러나 Apple은 ITP(Intelligent Tracking Prevention)를 통해 Adobe에서 설정한 자사 쿠키의 수명을 제한합니다. 이는 iOS 및 iPadOS의 모든 브라우저뿐만 아니라 Safari에도 영향을 미칩니다.

Adobe의 자사 쿠키는 Apple에서 추적기에서 발생한다고 판단하는 클릭스루 7일 만료로 제한됩니다. 7일 만료인 경우 사용자가 사이트를 방문한 후 7일 안에 다시 방문하면 쿠키 만료일은 7일 더 연장됩니다. 하지만 사용자가 사이트를 방문한 후 8일째 다시 방문하면 두 번째 방문할 때는 새로운 사용자로 취급됩니다.

현재, 방문자 ID 서비스를 사용하거나 레거시 Analytics ID(&quot;s_vi&quot; cookie)를 사용하고 있는 경,우 ITP 정책이 Adobe가 설정한 모든 자사 쿠키에 적용됩니다. 한때는 이 정책이 클라이언트측 설정 쿠키에만 적용되었으며, CNAME 구현을 통해 서버측 설정 쿠키에는 적용되지 않았습니다. 하지만 2020년 11월에 ITP가 업데이트되어 CNAME 구현에도 적용되었습니다.

#### ITP 정책에 대한 주요 변경 사항의 시간표 {#ITP-timeline}

* 2019년 2월, [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/): 클라이언트측 쿠키는 7일 만료로 제한됨
* 2019년 4월, [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/): 참조 도메인이 a) 교차 사이트 추적 및 b) 조각 식별자에 포함된 쿼리 스트링 및/또는 최종 URL에 포함된 경우에는 클라이언트측 쿠키는 광고 클릭에 대해 24시간으로 제한됩니다.
* 2020년 11월, [CNAME 클로킹 및 바운스 추적 디펜스](https://webkit.org/blog/11338/cname-cloaking-and-bounce-tracking-defense/): ITP 제한이 CNAME 구현으로 확장되었습니다.

ITP 정책은 자주 발전하고 있습니다. 최신 정책은 Apple의 [Webkit의 Tracking Prevention](https://webkit.org/tracking-prevention)을 참조하십시오.

#### 영향을 받는 Adobe 자사 쿠키는 어떤 것입니까?

Adobe가 설정한 모든 자사 쿠키 및 관련 JavaScript 라이브러리는 ITP 정책의 영향을 받습니다.

* Adobe Experience Cloud 방문자 ID(ECID) 서비스 라이브러리가 설정한 [&quot;AMCV&quot; 쿠키](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html)
* Analytics 레거시 [&quot;s_vi&quot; 쿠키](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html?lang=ko-KR), CNAME를 사용하는 자사 데이터 콜렉션으로 구성된 경우
* Analytics 레거시 [&quot;s_fid&quot; 쿠키](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html), &quot;s_vi&quot;를 설정할 수 없는 경우에 사용되는 폴백 쿠키

#### ITP는 Analytics의 Safari에 어떤 영향이 있습니까?

ITP 제한의 영향은 사용자의 동작에 따라 크게 달라집니다. ITP의 영향을 받은 브라우저(예: Safari)를 사용하고 7일 부재 후에 다시 방문하는 사용자만 영향을 받습니다. ITP 브라우저를 사용하지 않거나 7일 안에 돌아오는 경우에는 방문자는 영향을 받지 않습니다. 중요한 점은 Analytics에서 자신의 데이터를 살펴보고 이러한 제한이 주는 영향의 정도를 이해하는 것입니다. 사이트에 대한 영향을 측정하는 방법에 대한 팀은 &quot;[Safari 변화가 비즈니스에 어떤 영향을 주는가?](#measure-itp-effect)&quot;를 참조하십시오.

이러한 제한이 데이터에 영향을 주는 경우는 다음과 같습니다.

1. 재방문자의 쿠키가 만료되어 신규 방문자로 처리되었기 때문에 방문자 수가 늘어났습니다. (방문자당 판매 같은) 방문자 지표를 기준으로 하는 지표도 영향을 받습니다.
2. 속성에 대한 변경 사항. 속성은 변환 이벤트를 동일한 방문자의 이전 활동과 연결하는 것을 기반으로 합니다. 쿠키가 만료되면 후속 이벤트가 새 방문자와 연결됩니다. 새 방문자의 활동은 이전 방문자의 활동과 연결될 수 없습니다.

>[!NOTE]
>
>현재 모바일 앱에 임베드된 브라우저에는 ITP 기술이 적용되지 않습니다.

## 서드파티 쿠키와 자사 쿠키의 차이점은 무엇입니까?

### 서드파티 쿠키

서드파티 쿠키는 사용자가 방문하는 웹 사이트에서 생성되지 않습니다.

브라우저는 현재 모든 서드파티 쿠키를 동일하게 취급하고 저장하지만, 서드파티 쿠키는 다른 방식으로 작동할 수 있습니다. 고객의 Analytics 서드파티 쿠키를 구현하면 브라우저는 Adobe [demdex.net](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=ko-KR) ID를 서드파티 쿠키로 저장하지만, 고객은 Adobe에 대해서만 호출을 하고 알 수 없거나 의심스러운 서드파티 도메인에 대해서는 호출을 하지 않습니다. 이 쿠키는 도메인 간에 영구 식별자를 제공하며 보안(HTTPS) 콘텐츠를 허용합니다. 자세한 내용은 [쿠키 및 Experience Platform ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html)를 참조하십시오.

서드파티 쿠키는 Analytics이 구현되는 범위 내에서 도메인 간 추적 및 대상 변경 광고를 포함한 사용 사례에 사용됩니다. 서드파티 쿠키를 사용하면 자신이 소유하는 다른 도메인을 방문하거나 자신이 소유하지 않는 사이트에 광고를 표시하는 방문자를 식별할 수 있습니다.<!--  Without these cookies, you cannot identify visitors as they visit different domains that you own or as they are shown ads on sites that you do not own unless your implementation can stitch other types of cookies and   -->

### 자사 쿠키

자사 쿠키는 도메인에 고유하며, 고객 웹 사이트에 의해 만들어지고 사용자가 웹 사이트를 방문할 때 고객 브라우저에 저장됩니다. [Safari가 일정한 유형의 자사 쿠키에 대한 만료를 제한하지만](#limitations-first-party-cookies), 모든 브라우저에서는 일반적으로 자사 쿠키를 수락합니다.

자사 쿠키는 Analytics이 구현되는 범위 내에서 사이트에 있는 사용자를 식별하므로 사용자 활동에 대한 모든 분석을 지원하는 데 사용됩니다. 서드파티 쿠키가 현장 활동을 이해할 필요는 없습니다.

자세한 내용은 [자사 쿠키 정보](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=ko-KR)를 참조하십시오.

![쿠키 비교](/help/technotes/assets/cookies2.png)

## SameSite 쿠키 속성이란 무엇이며 Analytics에 어떤 영향을 줍니까? {#samesite-effect}

2020년 2월에 Chrome 80 브라우저가 출시되고 Firefox 및 Edge 브라우저의 후속 버전이 출시됨에 따라 SameSite 쿠키 속성은 서드파티 컨텍스트에서 쿠키를 사용할 수 있는지 여부를 결정하는 세 가지 다른 값에 대한 사양을 적용합니다.

* `None`: 이 설정을 사용하면 사이트 간 액세스가 가능하고 쿠키를 서드파티 컨텍스트에서 전달할 수 있습니다. 이 속성을 지정하려면 `Secure`도 지정해야 하며 모든 브라우저 요청이 HTTPS를 따라야 합니다. 예를 들어 쿠키를 설정할 때 속성 값을 다음과 같이 쌍으로 묶습니다. `Set-Cookie: example_session=test12; SameSite=None; Secure`. 레이블이 제대로 지정되지 않은 경우, 쿠키는 최신 브라우저에서 사용할 수 없으며 거부됩니다.

* `Lax`: *안전한*(읽기 전용, 예: `GET`) HTTP 메서드를 사용하는 최상위 수준 탐색에 대해서만 SameSite 쿠키를 사용하여 사이트 간 요청을 보낼 수 있습니다.

* `Strict`: 서드파티 웹 사이트 요청에 대해 동일한 사이트 쿠키가 전송되지 않습니다. 쿠키에 대한 사이트가 URL 표시줄의 사이트와 일치하는 경우에만 쿠키가 전송됩니다.

이러한 브라우저 버전의 기본 동작은 지정된 `SameSite` 속성이 없는 쿠키를 `SameSite=Lax`와 동일하게 처리하는 것입니다.

### Analytics는 SameSite 쿠키 속성을 어떻게 관리합니까?

방문자 ID 서비스를 사용하는 고객의 경우 쿠키에는 기본적으로 `SameSite=None` 및 `secure` 속성이 설정되어 있으며, 이를 통해 서드파티 사용 사례를 지원할 수 있습니다.

Analytics 레거시 식별자(&quot;s_vi&quot; 및 &quot;s_buk&quot; 쿠키)를 사용하는 고객의 경우 adobedc.net, 2o7.net 및 omtrdc.net 등 표준 수집 도메인에서 서드파티 사용 사례도 사용하도록 쿠키가 설정되어 있습니다. CNAME 구현을 사용하는 고객의 경우 Analytics는 `SameSite=Lax`를 설정합니다.

>[!NOTE]
>
>여러 도메인을 소유하고 있고, 모든 도메인에서 동일한 CNAME을 사용하여 데이터 수집하는 경우 쿠키가 다른 도메인에 있는 서드파티 쿠키로 취급됩니다. 기존 Analytics 식별자를 사용하는 경우 사이트 간에 쿠키를 공유할 수 있도록 설정을 `SameSite=None`로 업데이트할 수 있습니다. 자세한 내용은 다음 섹션의 &quot;[여러 도메인에 대해 하나의 CNAME을 사용할 때 SameSite 값 변경](#samesite-one-cname)&quot;을 참조하십시오.

`SameSite`가 `None`로 설정되면 Google에서 잘못 처리된 쿠키로 식별하는 브라우저의 경우에는 대신에 `SameSite`가 설정되지 않습니다.

다음의 표에서는 Analytics 쿠키에 대한 SameSite 쿠키을 요약합니다.

![쿠키 테이블](/help/technotes/assets/cookies1.png)

### 내 사이트에서는 SameSite 속성을 어떻게 해결할 수 있습니까?

#### HTTPS로 모든 사이트 페이지 제공

JavaScript 구성이 Adobe 서비스에 대한 모든 호출에 HTTPS를 사용하는지 확인합니다.

사이트에서 Experience Cloud 방문자 ID 서비스를 사용하는 경우에는 서비스가 서드파티 HTTP 호출을 HTTPS 끝점으로 리디렉션하며, 이로 인해 지연 시간이 늘어날 수 있지만 구성을 변경해야 하는 것은 아닙니다.

#### 여러 개의 도메인에 대해 CNAME를 사용하는 경우에 SameSite 값 변경 {#samesite-one-cname}

>[!NOTE]
>
>다음 정보는 Experience Cloud 방문자 ID 서비스를 사용하지 않는 사이트에 만 적용됩니다.

CNAME 구현이 자신의 웹 사이트와 동일한 도메인에 설정되어 있는 경우에는 쿠키가 자사 컨텍스트에 생성되며 변경할 필요가 없습니다.

그러나 여러 도메인을 소유하고 있고 모든 도메인에서 동일한 CNAME을 사용하여 데이터 수집하는 경우에는 쿠키가 다른 도메인에 있는 다른 쿠키로 취급됩니다. Chrome 80 이상에서는 더 이상 다른 도메인에서 보이지 않습니다. Analytics에서는 모든 브라우저에서 더 유사하게 동작하도록 명시적으로 이 쿠키의 `SameSite` 값을 `Lax`로 설정했습니다. 친숙한 제3 컨텍스트에서 이 쿠키를 사용하는 경우, `SameSite=None` 값을 사용하여 쿠키를 설정하기 때문에 항상 HTTPS를 사용해야 합니다. 아직 그렇게 하지 않은 경우, Adobe 고객 지원 센터에 문의하여 보안 CNAME에 대해 SameSite 값을 변경하십시오.

## Safari 변화가 비즈니스에 영향을 주는지 어떻게 판단할 수 있습니까? {#measure-itp-effect}

고객은 데이터 수집을 변경하기 전에 자신의 회사 내에서 어떤 영향이 있는지 측정하는 것이 좋습니다. Analysis Workspace를 사용하여 ITP 추적이 개인 비즈니스에 어떤 영향을 주는지 측정할 수 있습니다.

* ITP 적용 브라우저에서 트래픽의 비율을 측정합니다.

   1. 세그먼트를 만들어 ITP 플랫폼을 사용하는 방문자의 수를 확인합니다.

      >[!NOTE]
      >
      >ITP의 영향을 받는 특정 브라우저는 사용자가 CNAME 구현을 사용했는지 여부에 따라 달라집니다. 자세한 내용은 &quot;[ITP 정책의 주요 변경 타임라인](#ITP-timeline)&quot;을 참조하십시오.

      ![ITP 방문자에 대한 세그먼트](/help/technotes/assets/itp-visitor-segment.png)

   2. 세그먼트를 방문자의 수에 적용하여 사용자 기반에서 Safari의 상대적인 사용을 이해합니다. 이렇게 하면 다음과 같이 표를 만들 수 있습니다.

      ![ITP 방문자별 방문 비율](/help/technotes/assets/visits-vs-safari-visits.png)

* 7일 안에 돌아오지 않는 비Safari 방문자를 사용하여 방문자의 비율을 측정합니다. 비Safari 방문자가 7일 안에 반복해서 돌아오는 경우에는 Safari 트래픽이 크게 영향을 받지 않을 수 있습니다.

   1. 비Safari 트래픽에 대해 다음과 같이 세그먼트를 만듭니다.

      ![7일 후에 돌아오는 방문자에 대한 세그먼트](/help/technotes/assets/visits-after-seven-days.png)

   2. 세그먼트를 방문자의 수에 적용하여 사용자 기반에서 Safari의 상대적인 사용을 이해합니다. 이렇게 하면 다음과 같이 표를 만들 수 있습니다.

      ![7일 후에 돌아오는 방문자의 비율에](/help/technotes/assets/percent-visits-after-seven-days.png)

### 보고하는 동안 데이터를 조정하는 방법

비즈니스가 ITP 추적 방지의 영향을 받는 경우, 다음과 같은 조치를 취하여 보고하는 동안 데이터를 조정할 수 있습니다.

* 세그먼트를 만들어 ITP 사용자를 필터링합니다.

   ![비ITP 방문자에 대한 세그먼트](/help/technotes/assets/non-itp-visitor-segment.png)

* 계산된 지표를 만들어 알려진 방문자 인플레이션을 조정합니다.

   ![알려진 방문자 인플레이션을 조정하기 위한 계산된 지표](/help/technotes/assets/estimated-itp-visitors-metric.png)

>[!MORELIKETHIS]
>
>[브라우저 쿠키 제안의 영향을 경감하기 위한 옵션](cookieless.md)
>[Apple의 Adobe Analytics에 대한 New App Tracking Transparency Framework](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-impact-of-apple-s-new-app-tracking-transparency-framework-on/td-p/401833)
