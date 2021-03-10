---
title: DFA 통합 - 사용 종료 정보
description: Adobe이 DFA 데이터 커넥터를 사용하지 않는 이유는 무엇이며 어떤 대안이 있습니까?
translation-type: tm+mt
source-git-commit: 6669f678c1327b6af4a5b67c8033a9b7d8c9dbcf
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 1%

---


# DFA 통합 - 사용 종료 정보

Adobe은 최근 3자 데이터(예: ESP, VOC 등)를 통합하기 위한 레거시 도구 세트인 [의 단종 데이터 커넥터 계획을 발표했습니다. ](https://experienceleague.adobe.com/docs/analytics/import/dataconnectors/data-connectors-eol.html) Adobe Analytics과 함께 사용할 수 있습니다.

## 데이터 커넥터가 수명이 종료되는 이유는 무엇입니까?

파트너 통합을 위해 지원되는 플랫폼은 [Adobe Exchange](https://exchange.adobe.com/experiencecloud)입니다. 이 플랫폼은 Adobe Digital Experience 애플리케이션 통합, 제3자 CXM 통합을 용이하게 하고 고객과 파트너 모두의 다양한 데이터 요구 사항을 향후에도 지원하기 위해 고안되었습니다. Data Connectors를 사용하여 통합을 구축한 많은 파트너는 이미 이러한 통합을 Adobe Exchange로 마이그레이션했으며, 이러한 통합을 계획하고 있는 더 많은 파트너가 있습니다.

## DFA 통합이 EOL-OF-Life로 전환되는 이유는 무엇입니까?

[2020년 1월, Google은 Chrome에서 제3자 쿠키를 2022년까지 단계적으로 중단할 것이라고 발표했습니다. ](https://blog.chromium.org/2020/01/building-more-private-web-path-towards.html) Apple 및 Mozilla가 Safari 및 Firefox 브라우저에 맞게 설정한 업계 표준을 따릅니다. DFA 통합은 제3자 쿠키에 크게 의존하므로 3개의 주요 인터넷 브라우저에서 제3자 쿠키가 제거되면 효과적이지 않고 무용지물이 됩니다. Google [은(는) 대체 솔루션을 출시하지 않겠다고 발표함으로써 2021년 3월 이러한 입장을 강화했습니다.](https://blog.google/products/ads-commerce/a-more-privacy-first-web)

안타깝게도 DFA 통합을 소유하고 있는 Google은 Adobe Exchange 플랫폼에서 DFA 통합을 복제할 가능성이 없습니다. 따라서 Data Connectors가 오프라인으로 전환되면 기존 통합이 작동하지 않고 제품 대체 항목이 없을 것으로 가정합니다.

중요한 추가 요인은 DFA 통합의 &quot;뷰스루&quot; 기능입니다. 이 플러그인을 사용하면 사용자가 디스플레이 광고를 보고 클릭하지 않고 나중에 웹 사이트를 방문한 경우를 추적할 수 있습니다. &quot;뷰스루&quot;는 제3자 쿠키를 기반으로 하며, 2021년 이후에도 단계적으로 중단됩니다. 이것은 단지 Adobe 문제가 아니라 시장 전체의 문제이다. 현재로서는 이 데이터를 복제할 대체 요소가 없습니다.

## 여러분에게 어떤 대안이 있습니까?

디스플레이 광고 데이터(&quot;뷰스루&quot; 없이)를 Adobe Analytics에 통합하려는 고객을 위해 현재 다음과 같은 옵션이 있습니다.

* Adobe Advertising Cloud DSP 고객은 [Adobe Analytics](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/introduction-to-the-analytics-for-advertising-cloud-dsp-integration.html?lang=en#integrations)와의 제품 통합 기능을 활용하여 Google에서 Adobe Analytics으로 디스플레이 광고 데이터를 설정할 수 있습니다. 이 통합은 Adobe의 가장 좋은 대안이며 고객에게 권장할 것입니다. Ad Cloud DSP을 사용하면 유료 검색, 디스플레이, 동영상 등을 비롯한 모든 광고 채널에 일관된 경험을 제공할 수 있습니다. [여기](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/introduction/dsp-about.html?lang=en#introduction)에서 추가 정보를 확인하십시오. 그러나 Ad Cloud DSP은 제3자 쿠키 손실에 대해서도 영향을 받습니다.
* 다른 데이터 소스와의 표시 및 통합에 대한 기능을 제공하는 Adobe Experience Platform 및 [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html?lang=en) 고객은 유료 검색 제공자에서 디스플레이 데이터를 다운로드하고 해당 데이터를 Experience Platform에 업로드할 수 있습니다. 그런 다음 데이터를 CJA로 바로 가져와 다른 데이터 세트와 함께 분석합니다.
* Adobe 컨설팅(엔지니어링 설계자)은 디스플레이 광고 지표를 Adobe Analytics에 인제스트하는 맞춤형 솔루션을 구축할 수 있습니다. 이 솔루션은 아직 개발 중이며 베타 프로그램에 참여하려는 모든 고객도 이 프로그램에 참여할 수 있습니다. 기능, 가용성 및 비용에 대한 자세한 내용은 제공되는 대로 제공됩니다.
* Adobe Analytics의 분류뿐만 아니라 Data Sources 기능을 사용하여 자체 디스플레이 광고 통합을 관리할 수 있습니다. 여기에 설명된 대로 데이터 소스 및 분류 [을(를) 사용하여 유료 검색을 가져오고 데이터를 수동으로 표시합니다.](https://experienceleague.adobe.com/docs/analytics/import/use-cases/paid-search-metrics.html?lang=en#use-cases) (참고:이 문서는 유료 검색을 참조하지만 사용 사례 및 개념이 동일하며 표시할 수 있습니다.)

추가 질문 또는 지원을 받으려면 [Adobe 고객 지원](https://helpx.adobe.com/contact/enterprise-support.ec.html)에 문의하십시오.