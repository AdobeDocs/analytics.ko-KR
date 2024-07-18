---
description: GitHub의 Adobe Analytics Admin API에 대한 링크.
title: Adobe Analytics 1.4 API EOL FAQ
feature: Admin Tools
role: Admin
source-git-commit: da96c049f7cfb73496416c2d8a7f4dcbc8f2303e
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 2%

---

# Adobe Analytics 1.4 API EOL FAQ

## 서비스 종료(EOL) 알림

**중단되는 항목이 무엇입니까?**

* Adobe Analytics 1.4 API

* Adobe Analytics WSSE 인증

**종료되는 시간은 언제입니까?**

이러한 서비스는 2026년 8월 12일에 사용이 중단됩니다. 이 날짜 이후에는 더 이상 액세스할 수 없습니다.

## 1.4 API

**이러한 서비스란 무엇입니까?**

[Adobe Analytics 1.4 API](https://developer.adobe.com/analytics-apis/docs/1.4/)는 보고, 분류, 데이터 피드 및 보고서 세트 구성과 같은 광범위한 작업을 제공하는 API 컬렉션입니다.

**마이그레이션하려면 어떻게 해야 합니까?**

[Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)은(는) 1.4 API 사용자를 위한 마이그레이션 경로를 제공합니다. 현재 1.4 API를 사용하는 고객은 통합을 2.0 API(Adobe Analytics 애플리케이션이 의존하는 동일한 API)로 마이그레이션하고 최신 기능을 활용할 수 있습니다.

2.0 API를 사용하면 세그먼트 및 계산된 지표와 같은 구성 요소 보고 또는 관리와 같이, Analytics 사용자 인터페이스에서 수행할 수 있는 거의 모든 작업을 수행할 수 있습니다.

**2.0 API가 1.4 API와 동일한 기능을 제공합니까?**
1.4 API에서 사용할 수 있는 모든 기능은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)를 사용하여 수행할 수 있습니다. 일부 기능은 1.4 API에서 사용할 수 있는 것과 동일한 기능을 제공하며, 동일한 기능을 사용하면 세그먼트 및 계산된 지표와 같은 구성 요소 보고 또는 관리와 같은 Analytics 사용자 인터페이스에서 수행할 수 있는 거의 모든 작업을 수행할 수 있습니다.

## WSSE 인증

**이러한 서비스란 무엇입니까?**

WSSE 인증은 Analytics 1.4 API에서 지원하는 레거시 인증 프로토콜입니다. [Adobe Developer Console](https://developer.adobe.com/console/home)에 제공된 OAuth 기반 인증 옵션으로 대체되었습니다.

**마이그레이션하려면 어떻게 해야 합니까?**

WSSE 고객은 Adobe Developer Console에서 프로비저닝된 자격 증명을 사용하도록 인증을 업데이트해야 합니다. 이렇게 하려면 [Adobe Developer Console](https://developer.adobe.com/console/home)에 로그인하여 Analytics 2.0 API 통합을 위한 프로젝트를 만드십시오. OAuth 사용자와 OAuth 서버 간 인증 방법 중 하나를 선택합니다.

## 질문

Q: **Analytics API에 대한 기존 Adobe IO 프로젝트에 영향을 줍니까?**

A: Analytics 1.4 API를 사용하는 모든 기존 프로젝트가 영향을 받습니다. 이러한 통합은 EOL 기한 전에 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)(으)로 마이그레이션해야 합니다.

Q: **Analytics API를 사용하는 다른 제품 또는 응용 프로그램과 Adobe 자격 증명을 공유했습니다. 영향을 받습니까?**

A: 해당 제품 또는 애플리케이션이 WSSE 자격 증명을 사용하거나 Analytics 1.4 API를 호출하는 경우 영향을 받으며 EOL 기한 전에 마이그레이션해야 합니다. 마이그레이션 계획 및 일정에 대한 자세한 내용은 제품 또는 애플리케이션 공급자에게 문의하십시오.

Q: **사용 중인 Adobe Analytics API를 잘 모릅니다.**

A: 통합에서 호출되는 주소로 사용 중인 API를 식별할 수 있습니다.

Adobe Analytics 1.4 API는 아래 URL 중 하나를 호출하여 액세스합니다.
* https://api.omniture.com
* https://api3.omniture.com
* https://api4.omniture.com
* https://api5.omniture.com

다음 URL을 호출하여 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)에 액세스합니다.
* https://analytics.adobe.io

api*.omniture.com을 사용하는 경우 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션해야 합니다.

Q: **Adobe Analytics 2.0 API가 1.4 API와 동일합니까? 그렇지 않은 경우 가장 큰 차이점은 무엇입니까?**

A: Adobe Analytics 2.0 API는 1.4 API와 동일하지 않지만 다음과 같은 이점을 포함하여 비슷한 기능을 제공합니다.

* 더 간단하고 효율적인 쿼리 방법으로 응답 시간이 단축되므로 폴링을 수행할 필요가 없습니다.

* 쿼리 및 동적 보고서 업데이트를 위한 프로그래밍 기능

* 더욱 원활한 오류 처리

* Analysis Workspace에서 수행할 수 있는 모든 작업을 수행하는 유연한 기능

* UI 작업에 대한 API 호출의 일관성 및 일치

* Analysis Workspace에서 사용되는 모든 Attribution IQ 모델에 액세스

* Analysis Workspace에서 사용되는 모든 예외 항목 탐지 알고리즘에 액세스

* 다른 Experience Cloud 제품과 통합할 수 있는 기능

* 여러 분류 보고서에 대한 용량 증가

* 최신 Analytics 기능에 액세스

[Adobe Analytics 2.0 API로 마이그레이션](https://developer.adobe.com/analytics-apis/docs/2.0/guides/migration/) 안내서에서 1.4와 2.0 API의 주요 차이점을 설명합니다. 추가 정보는 [Analytics 2.0 API FAQ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/faq/)에서도 확인할 수 있습니다.

Q: **이(가) 데이터 수집에 영향을 줍니까?**

A: Adobe Analytics 1.4 EOL은 태그(이전 Adobe Launch), WebSDK 또는 AppMeasurement.js와 같은 태그 지정 솔루션에 영향을 주지 않습니다. 그러나 1.4 데이터 소스 또는 분류 API를 사용하여 데이터를 수집하거나 향상시키는 경우 이러한 워크플로우를 Adobe Analytics 2.0 API로 마이그레이션해야 합니다. 자세한 내용은 [2.0 API 끝점 안내서](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/)를 참조하십시오.

Q: **데이터 삽입 API에 영향을 미칩니까?**

A: 아니요. 데이터 삽입 API는 Adobe Analytics 1.4 EOL의 영향을 받지 않습니다.

Q: **이 FAQ에서 질문에 대한 답변을 받지 못한 경우 어떻게 해야 합니까?**

A: 질문이 있는 경우 Adobe 계정 담당자에게 문의하십시오.

