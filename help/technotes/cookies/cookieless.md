---
title: 브라우저 쿠키 제안의 영향을 경감하기 위한 옵션
description: 브라우저 쿠키 제안의 영향을 경감하여 Adobe Analytics에 대한 데이터 수집을 개선하는 방법을 알아보십시오.
source-git-commit: 6c354a343648162ce2951c52a70a688970e1304d
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 51%

---


# 브라우저 쿠키 제안의 영향을 경감하기 위한 옵션

이 문서에서는 주요 브라우저가 쿠키에 대한 추적 방지 조치를 구현하므로 속성 및 솔루션에서 지속적인 방문자 식별을 유지하기 위한 옵션에 대해 설명합니다.

Adobe Analytics는 자사 쿠키를 기반으로 방문자의 현장 활동을 기록합니다. Analytics는 또한 제3자 쿠키를 기반으로 소유 중인 다른 도메인에서 이루어지는 활동 같이 방문자의 현장 활동을 기록합니다. 제3자 쿠키는 많은 브라우저에서 차단되며, 출시 예정인 Chrome의 지원 제거에서는 대개 사용할 수 없습니다(현재 2022년 에정). 자사 쿠키가 모든 브라우저에서 허용되는 것은 아니지만, 사용할 수 있는 것은 Apple의 [ITP 추적 방지](https://webkit.org/tracking-prevention) 조치에 따라 Safari 및 다른 브라우저에 대한 만료가 제한되어 있습니다. 브라우저 쿠키의 현재 제한 사항에 대한 자세한 내용은 [Adobe Analytics 및 브라우저 쿠키](cookies.md)를 참조하십시오.

이러한 브라우저 제한은 익명으로 제3자 추적하는 경향에서 사용자와 사용자가 신뢰하는 브랜드가 정보를 명시적으로 공유하는 경향으로 폭넓게 이동하는 것을 반영합니다. 이러한 변화를 지원하기 위해, Adobe는 자사와 관계를 통해 수집된 오래 지속되는 식별자를 포함하여 고객이 전통적인 쿠키를 보완하는 방법을 제공합니다.

## Customer Journey Analytics 및 Cross Device Analytics

[Adobe 고객 여정 ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=ko-KR) Analytics 및  [교차 장치 ](/help/components/cda/overview.md) Analytics에서는 쿠키 외에 해시된 로그인과 같은 내구성이 있는 식별자를 포함합니다. 이를 통해 여러 장치 및 Customer Journey Analytics의 경우 온라인 및 오프라인 채널에서 고객 여정을 이해할 수 있습니다.

* **고객 여정** 분석은 Adobe Experience Platform을 기반으로 구축되었으며 일반적인 고객 ID를 기반으로 Analysis Workspace에서 온라인 및 오프라인 데이터를 결합할 수 있는 유연성을 제공합니다. 주어진 분석에 사용할 ID를 지정하고 Analysis Workspace에서 데이터를 탐색할 수 있습니다. Analytics Select, Prime 및 Ultimate 고객은 이 제품을 추가 기능 제품으로 구입할 수 있습니다.

* **교차 장치 분석** 은 고객이 방문자에게 대체 식별자를 사용할 수 있도록 하는 기존 Adobe Analytics의 개선 사항입니다. 이 기능을 사용하면 장치 중심 보기에서 사람 중심 보기로 이동할 수 있습니다. Analytics Ultimate 고객은 교차 장치 분석을 사용할 수 있습니다.

## 서버측 데이터 수집

서버측 수집에서는 유연성을 제공하여 자신의 쿠키 설정을 위한 브라우저 메커니즘에 의존하기 보다는 식별자를 제공합니다.

[데이터 삽입 API](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/data-insertion-api/index.md) 또는 [대량 데이터 삽입 API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)를 사용하여 Analytics 서버측에 데이터를 제출할 수 있습니다. 새로운 서버측 구현에는 벌크 데이터 삽입 API가 권장됩니다. 두 API를 비교하려면, &quot;[어느 Adobe Analytics 도구를 사용해야 하는가](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/which-analytics-tool.html?lang=ko-KR)&quot;를 참조하십시오.

## 추가 정보

서드파티 쿠키에서 전환하기 위해 비즈니스에 취할 수 있는 실용적인 단계는 [Adobe](https://business.adobe.com/solutions/cookieless.html) 및 심층적인 [타사 쿠키를 넘어 생각하면서 쿠키를 사용하지 않는 환경에 고객 확보 및 유지 를 참조하십시오.타사 쿠키](https://business.adobe.com/content/dam/www/us/en/pdfs/Adobe_Thinking_Beyond_the_Third_Party_Cookie.pdf) 가 없는 세계에 대한 완전한 안내서입니다.&quot;

>[!MORELIKETHIS]
[Adobe Analytics 및 브라우저 쿠키](cookies.md)>
>
