---
title: 브라우저 쿠키 제안의 영향을 경감하기 위한 옵션
description: 브라우저 쿠키 제안의 영향을 경감하여 Adobe Analytics에 대한 데이터 수집을 개선하는 방법을 알아보십시오.
source-git-commit: 6c354a343648162ce2951c52a70a688970e1304d
workflow-type: ht
source-wordcount: '516'
ht-degree: 100%

---


# 브라우저 쿠키 제안의 영향을 경감하기 위한 옵션

이 문서에서는 주요 브라우저가 쿠키에 대한 추적 방지 디바이스를 구현할 때 여러 속성과 솔루션에서 지속적인 방문자 식별을 유지하는 방법에 대해 다룹니다.

Adobe Analytics는 자사 쿠키를 기반으로 방문자의 현장 활동을 기록합니다. Analytics는 또한 서드파티 쿠키를 기반으로 소유 중인 다른 도메인에서 이루어지는 활동 같이 방문자의 현장 활동을 기록합니다. 서드파티 쿠키는 많은 브라우저에서 차단되며, 출시 예정인 Chrome의 지원 제거에서는 대개 사용할 수 없습니다(현재 2022년 에정). 자사 쿠키가 모든 브라우저에서 허용되는 것은 아니지만, 사용할 수 있는 것은 Apple의 [ITP 추적 방지](https://webkit.org/tracking-prevention) 조치에 따라 Safari 및 다른 브라우저에 대한 만료가 제한되어 있습니다. 브라우저 쿠키에 대한 현재의 제한과 관련된 자세한 내용은 [Adobe Analytics 및 브라우저 쿠키](cookies.md)를 참조하십시오.

이러한 브라우저 제한은 익명으로 서드파티를 추적하는 경향에서 사용자와 사용자가 신뢰하는 브랜드가 정보를 명시적으로 공유하는 경향으로 폭넓게 이동하는 것을 반영합니다. 이러한 변화를 지원하기 위해, Adobe는 자사와 관계를 통해 수집된 오래 지속되는 식별자를 포함하여 고객이 전통적인 쿠키를 보완하는 방법을 제공합니다.

## Customer Journey Analytics 및 Cross Device Analytics

[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=ko) 및 [Cross-Device Analytics](/help/components/cda/overview.md)를 통해 사용자는 쿠키 외에 해시된 로그인과 같은 지속적인 식별자를 포함할 수 있습니다. 이렇게 하면 여러 디바이스의 고객 여정을 확인할 수 있으며, Customer Journey Analytics의 경우 온라인 및 오프라인 채널에서도 가능합니다.

* **Customer Journey Analytics**&#x200B;는 Adobe Experience Platform을 기반으로 구축되었으며 공통 고객 ID를 기반으로 Analysis Workspace의 온라인 및 오프라인 데이터를 유연하게 결합할 수 있습니다. 분석에 사용할 ID를 지정하고 Analysis Workspace에서 데이터를 탐색할 수 있습니다. Analytics Select, Prime 및 Ultimate 고객은 이 추가 기능 제품을 구매할 수 있습니다.

* **Cross-Device Analytics**&#x200B;는 고객이 방문자에게 대체 식별자를 사용할 수 있도록 하는 기존 Adobe Analytics의 향상된 기능입니다. 이 기능을 사용하면 디바이스 중심 보기에서 사용자 중심 보기로 이동할 수 있습니다. Cross-Device Analytics는 Analytics Ultimate 고객에게 제공됩니다.

## 서버측 데이터 수집

서버측 수집에서는 유연성을 제공하여 자신의 쿠키 설정을 위한 브라우저 메커니즘에 의존하기 보다는 식별자를 제공합니다.

[Data Insertion API](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/data-insertion-api/index.md) 또는 [Bulk Data Insertion API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)를 사용하여 Analytics 서버측에 데이터를 제출할 수 있습니다. 새로운 서버측 구현에는 Bulk Data Insertion API를 사용하는 것이 좋습니다. 두 API를 비교하려면 &quot;[어느 Adobe Analytics 도구를 사용해야 하는가](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/which-analytics-tool.html?lang=ko)&quot;를 참조하십시오.

## 추가 정보

사용자의 비즈니스가 서드파티 쿠키에서 전환하기 위해 취할 수 있는 조치는 [Adobe를 통해 쿠키 없는 세상에서 고객 확보 및 유지](https://business.adobe.com/solutions/cookieless.html) 및 자세한 [서드파티 쿠키를 넘어선 사고: 서드파티 쿠키가 없는 세상을 위한 완벽한 안내서](https://business.adobe.com/content/dam/www/us/en/pdfs/Adobe_Thinking_Beyond_the_Third_Party_Cookie.pdf)를 참조하십시오.

>[!MORELIKETHIS]
>
>[Adobe Analytics 및 브라우저 쿠키](cookies.md)>

