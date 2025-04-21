---
description: Adobe Analytics 1.4 API 서비스 종료 공지에 대한 세부 사항입니다.
title: Adobe Analytics 1.4 API EOL FAQ
feature: Admin Tools
role: Admin
exl-id: 88769032-a7cd-4ca8-958f-3300a4bfe71f
source-git-commit: 73c0210ac931f3e7f823e033a3bffdc22e159ddb
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 4%

---

# Adobe Analytics 1.4 API EOL FAQ

Adobe은 **2026년 8월 12일**&#x200B;에 Adobe Analytics 1.4 API를 중단할 예정입니다. 이 날짜 이후에는 더 이상 액세스할 수 없습니다. 이 발표는 다음 사항에 직접적인 영향을 줍니다.

* Adobe Analytics 1.4 API, 데이터 삽입 API 제외
* Adobe Analytics WSSE 인증

## 1.4 API

[Adobe Analytics 1.4 API](https://developer.adobe.com/analytics-apis/docs/1.4/)는 보고, 분류, 데이터 피드 및 보고서 세트 구성과 같은 광범위한 작업을 제공합니다. [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)를 위해 만료됩니다. 2.0 API를 사용하면 세그먼트 및 계산된 지표와 같은 구성 요소 보고 또는 관리와 같이, Analytics 사용자 인터페이스에서 수행할 수 있는 거의 모든 작업을 수행할 수 있습니다.

Adobe은 1.4 API 사용자를 위한 [마이그레이션 경로](https://developer.adobe.com/analytics-apis/docs/2.0/guides/migration/)를 제공합니다. 통합을 2.0 API(Adobe Analytics 애플리케이션이 의존하는 동일한 API)로 마이그레이션하고 최신 기능을 활용할 수 있습니다. 1.4 API에서 사용할 수 있는 모든 기능은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)를 사용하여 수행할 수 있습니다.

## WSSE 인증

WSSE 인증은 Analytics 1.4 API에서 지원하는 레거시 인증 프로토콜입니다. [Adobe Developer Console](https://developer.adobe.com/console/home)에 제공된 OAuth 기반 인증 옵션으로 대체되었습니다. WSSE 인증을 사용하는 프로젝트는 Adobe Developer Console에서 프로비저닝된 것으로 자격 증명을 업데이트해야 합니다. 이렇게 하려면 [Adobe Developer Console](https://developer.adobe.com/console/home)에 로그인하여 Analytics 2.0 API 통합을 위한 프로젝트를 만드십시오. OAuth 사용자 또는 OAuth 서버 간 인증 방법을 선택합니다.

## FAQ

+++**Analytics API에 대한 기존 Adobe IO 프로젝트에 영향을 줍니까?**

Analytics 1.4 API를 사용하는 모든 기존 프로젝트가 영향을 받습니다. 이러한 통합은 EOL 기한 전에 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)&#x200B;(으)로 마이그레이션해야 합니다.

+++

+++**Analytics API를 사용하는 다른 제품 또는 응용 프로그램과 Adobe 자격 증명을 공유했습니다. 영향을 받습니까?**

해당 제품 또는 애플리케이션이 WSSE 자격 증명을 사용하거나 Analytics 1.4 API를 호출하는 경우 영향을 받으며 EOL 기한 전에 마이그레이션해야 합니다. 마이그레이션 계획 및 타임라인에 대한 자세한 내용은 제품 또는 애플리케이션 공급자에게 문의하십시오.

+++

+++**내 프로젝트에서 사용하는 API를 확인하려면 어떻게 해야 합니까?**

API가 호출하는 기본 URL은 프로젝트에서 사용하는 API 버전을 결정합니다. Adobe Analytics 1.4 API는 다음 URL을 사용합니다.
* `https://api.omniture.com`
* `https://api3.omniture.com`
* `https://api4.omniture.com`
* `https://api5.omniture.com`

[Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)에서는 다음 URL을 사용합니다.

* `https://analytics.adobe.io`

API 프로젝트에서 `api*.omniture.com`을(를) 사용하는 경우 Adobe Analytics 1.4 API를 사용하며 2.0 API로 마이그레이션해야 합니다.

+++

+++**이 서비스 종료가 데이터 수집에 영향을 줍니까?**

Adobe Analytics 1.4 EOL은 태그(이전의 Adobe Launch), Web SDK 또는 AppMeasurement과 같은 태그 지정 솔루션에 영향을 주지 않습니다. 그러나 1.4 데이터 소스 또는 분류 API를 사용하여 데이터를 향상시키는 경우 이러한 워크플로우를 Adobe Analytics 2.0 API로 마이그레이션해야 합니다.

Data Insertion API는 이 서비스 종료 공지의 영향을 받지 않습니다. AdobeAdobe 는 데이터 삽입 API에 대한 지원을 계속할 계획이지만 대신 [대량 데이터 삽입 API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/)를 사용하는 것이 좋습니다.

+++

이 페이지에서 답변되지 않은 서비스 종료 공지에 대한 추가 질문이 있는 경우 Adobe 계정 팀에 문의하십시오.
