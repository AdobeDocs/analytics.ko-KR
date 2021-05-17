---
title: 브라우저 쿠키 제한의 효과를 완화시키는 옵션
description: Adobe Analytics에 대한 데이터 수집을 개선하기 위해 브라우저 쿠키 제한의 효과를 완화하는 방법을 알아봅니다.
source-git-commit: 6c354a343648162ce2951c52a70a688970e1304d
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 5%

---


# 브라우저 쿠키 제한의 효과를 완화시키는 옵션

이 문서에서는 주요 브라우저가 쿠키 추적 방지 조치를 구현하므로 속성 및 솔루션에서 방문자 식별이 지속되도록 하는 옵션에 대해 설명합니다.

Adobe Analytics은 자사 쿠키를 사용하여 방문자의 사이트 내 활동을 기록합니다. 또한 Analytics는 타사 쿠키를 사용하여 소유한 다른 도메인의 활동과 같이 방문자의 외부 활동을 파악합니다. 제3자 쿠키는 많은 브라우저에서 차단되며 Chrome의 향후 지원 제거(현재 2022년 예정)에서는 거의 사용할 수 없습니다. 자사 쿠키는 모든 브라우저에서 사용할 수 있지만 Apple의 [ITP 추적 방지 정책](https://webkit.org/tracking-prevention) 측정에서 Safari 및 기타 브라우저에서 제한된 만료가 발생합니다. 브라우저 쿠키의 현재 제한 사항에 대한 자세한 내용은 [Adobe Analytics 및 브라우저 쿠키](cookies.md)를 참조하십시오.

이러한 브라우저 제한 사항은 익명의 제3자 추적에서 벗어나 사용자가 신뢰하는 사용자와 브랜드 간의 정보를 명시적 공유하는 것으로 확대된 전환을 제공합니다. 이러한 전환을 지원하기 위해 Adobe은 퍼스트 파티 관계를 통해 수집한 내구성 식별자를 포함하여 고객이 기존 쿠키를 보완하는 방법을 제공합니다.

## Customer Journey Analytics 및 크로스 디바이스 분석

[Adobe 고객 여정 ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) 분석 및  [장치 간 ](/help/components/cda/overview.md) Analytics 사용자가 쿠키 외에 해시된 로그인 같은 내구성이 좋은 식별자를 포함하도록 합니다. 이를 통해 다양한 디바이스와 Customer Journey Analytics의 경우 온라인 및 오프라인 채널에서 고객 여정을 파악할 수 있습니다.

* **Adobe Experience Platform 기반의 고객 여정** Analytics를 사용하면 일반적인 고객 ID를 기반으로 온라인 데이터와 오프라인 데이터를 Analysis Workspace에서 유연하게 결합할 수 있습니다. 특정 분석에 사용할 ID를 지정하고 Analysis Workspace에서 데이터를 탐색할 수 있습니다. Analytics Select, Prime 및 Ultimate 고객은 이 제품을 추가 제품으로 구매할 수 있습니다.

* **크로스 디바이스 분석** 은 고객이 방문자에게 대체 식별자를 사용할 수 있도록 기존의 Adobe Analytics에 대한 향상된 기능입니다. 이 기능을 사용하면 디바이스 중심의 뷰에서 개인 중심의 보기로 이동할 수 있습니다. Analytics Ultimate 고객은 크로스 디바이스 분석을 이용할 수 있습니다.

## 서버측 데이터 수집

서버측 컬렉션은 쿠키를 설정하는 브라우저 메커니즘에 의존하지 않고 자체 식별자를 제공할 수 있는 유연성을 제공합니다.

[데이터 삽입 API](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/data-insertion-api/index.md) 또는 [벌크 데이터 삽입 API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)를 사용하여 Analytics 서버측에 데이터를 제출할 수 있습니다. 새로운 서버측 구현에는 벌크 데이터 삽입 API가 권장됩니다. 두 API를 비교하려면 &quot;[어떤 Adobe Analytics 도구를 사용해야 합니까](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/which-analytics-tool.html)&quot;를 참조하십시오.

## 추가 정보

제3자 쿠키로부터 전환하기 위해 기업에서 취할 수 있는 실용적인 단계를 보려면 [Adobe](https://business.adobe.com/solutions/cookieless.html) 및 제3자 쿠키를 넘어 생각의 심층적인 [를 참조하십시오.제3자 쿠키 없이 완벽한 가이드](https://business.adobe.com/content/dam/www/us/en/pdfs/Adobe_Thinking_Beyond_the_Third_Party_Cookie.pdf)&quot;

>[!MORELIKETHIS]
[Adobe Analytics 및 브라우저 쿠키](cookies.md)>
>
