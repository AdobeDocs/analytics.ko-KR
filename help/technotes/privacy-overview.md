---
description: Adobe Analytics에서 수집하는 데이터와 기타 개인정보 보호 고려 사항 개요.
keywords: 개인정보 보호
title: 개인정보 보호 개요
feature: Privacy
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: ee0bf5beeac3c9780eb0c8420845114f7e840aec
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 12%

---

# 개인정보 보호 개요

방문자는 Adobe [개인정보 보호 센터](https://www.adobe.com/kr/privacy.html)에서 Adobe가 수집하는 정보를 일반적으로 사용하는 방법에 대해 자세히 알아볼 수 있습니다. 조직에서 Adobe의 서비스 구현 방법을 독점적으로 제어하기 때문에 Adobe 제품 및 서비스의 사용 방법은 조직의 판단에 따라 공개합니다. 조직은 자체 개인정보 처리방침, Adobe과의 서비스 계약 및 모든 적용 가능한 법률을 준수할 책임이 있습니다.

Adobe은 다음과 같은 중요한 개념을 준수할 것을 강력히 권장합니다.

* **Adobe Analytics에서 개인 식별 정보를 수집하지 마십시오.** 사용자 지정 변수를 사용하면 액세스할 수 있는 거의 모든 항목을 수집할 수 있습니다. 그러나 조직의 개인정보 처리방침 및 적용 가능한 법도 고려해야 합니다.
* **방문자에게 옵트아웃 정보와 관련하여 찾기 쉽고 이해하기 쉬운 정보를 제공합니다.** 엄격히 필요하지 않은 모든 항목을 옵트아웃하도록 허용합니다. 대다수 유럽 연합 국가는 분석 쿠키가 필수적이라고 간주하지 않습니다.

## 데이터 수집 분류

Adobe Analytics은 다음 유형의 데이터를 자동으로 수집하거나 잠재적으로 수집할 수 있습니다.

| 데이터 유형 | 세부 사항 | 이 데이터를 포함하는 예제 변수 |
| --- | --- | --- |
| 사이트에 있는 웹 페이지의 페이지 이름 또는 URL | 항상 수집됩니다. 모든 히트에 URL 또는 페이지 이름이 필요합니다. | [페이지](../components/dimensions/page.md), [페이지 URL](../components/dimensions/page-url.md) |
| 시간 기반 데이터 | 항상 수집됩니다. 데이터 수집에는 타임스탬프가 필요하며 시간 기반 데이터는 타임스탬프에서 파생됩니다. | [페이지에서 보낸 시간](../components/dimensions/time-spent-on-page.md), [시간(일 기준)](../components/dimensions/hour-of-day.md), [오전/오후](../components/dimensions/am-pm.md), [평일/주말](../components/dimensions/weekday-weekend.md), [요일](../components/dimensions/day-of-week.md), [월(연 기준)](../components/dimensions/month-of-year.md) |
| 다른 사이트의 웹 페이지 데이터 | Adobe은 웹 사이트의 소스 코드를 변경할 수 없는 제휴되지 않은 사이트에서 데이터를 수집할 수 없습니다. AppMeasurement은 방문자가 웹 사이트에 도달하면 참조 URL을 자동으로 수집합니다. 구현을 사용자 정의하여 사이트에 도착한 후 쿼리 문자열 내에서 데이터를 수집할 수 있습니다. | [레퍼러](../components/dimensions/referrer.md), [참조 도메인](../components/dimensions/referring-domain.md) |
| 익명으로 처리된 방문자 ID | AppMeasurement은 사이트를 방문하는 각 브라우저에 대해 방문자 ID를 자동으로 생성하고 참조합니다. 이 ID는 쿠키에 저장됩니다. 특정 구현에 쿠키를 사용할 수 없는 경우, Adobe Analytics은 IP 주소 및 사용자 에이전트 문자열을 사용하여 방문자 식별을 위한 대체 방법을 사용합니다. 다음을 참조하십시오 [Adobe Analytics 및 브라우저 쿠키](cookies/cookies.md) 추가 정보. | [고유 방문자 수](../components/metrics/unique-visitors.md) |
| 식별 가능한 방문자 ID | Adobe은 사용자 지정 방문자 ID를 자동으로 수집하지 않습니다. 그러나 구현을 사용자 지정하여 이 데이터를 수집할 수 있습니다. | [`visitorID`](../implement/vars/config-vars/visitorid.md) |
| 외부 검색어 | AppMeasurement은 참조 URL을 기반으로 이 데이터를 자동으로 수집하려고 합니다. 그러나 많은 최신 검색 엔진은 더 이상 이 정보를 포함하지 않습니다. | [검색 키워드](../components/dimensions/search-keyword.md) |
| 내부 검색어 | Adobe은 내부 검색 데이터를 자동으로 수집하지 않습니다. 그러나 구현을 사용자 정의하여 이 데이터를 수집할 수 있으며 Adobe Analytics을 사용하는 조직의 일반적인 방법입니다. | [eVar](../components/dimensions/evar.md) |
| 컴퓨터 및 브라우저 사양 | AppMeasurement은 브라우저 유형, 운영 체제 유형 및 디바이스가 데스크톱이나 모바일인 경우와 같은 낮은 엔트로피 브라우저 힌트를 자동으로 수집합니다. 브라우저의 특정 버전/빌드, 디바이스 모델 또는 운영 체제 버전과 같은 높은 엔트로피 힌트를 수집하려면 구성이 필요합니다. 다음을 참조하십시오 [클라이언트 힌트 개요](client-hints.md) 추가 정보. | [브라우저](../components/dimensions/browser.md), [운영 체제](../components/dimensions/operating-systems.md), [모바일 차원](../components/dimensions/mobile-dimensions.md), [모니터 해상도](../components/dimensions/monitor-resolution.md) |
| 지리적 위치 정보 | Adobe은 (보고서 세트 수준에서) 각 웹 사이트 또는 앱에 대한 지리적 위치 데이터 수집을 활성화하거나 비활성화하는 기능을 제공합니다. AppMeasurement을 포함한 많은 구현 유형에서 이 데이터를 자동으로 수집합니다. | [도시](../components/dimensions/cities.md), [지역](../components/dimensions/regions.md), [국가](../components/dimensions/countries.md) |
| IP 주소 | Adobe은 이 데이터를 저장할 때 마지막 옥텟을 가리는 기능 또는 방문자의 IP 주소를 완전히 가리는 기능을 제공합니다. EMEA 고객은 일반적으로 IP 주소를 기본적으로 완전히 숨깁니다. IP 주소는 Adobe Analytics에서 차원으로 사용할 수 없으며, 원시 데이터에만 포함됩니다([데이터 피드](../export/analytics-data-feed/data-feed-overview.md)). | 없음 |
| 사이트에 제공된 양식 정보 | 이 데이터를 수집하려면 모든 구현 유형을 구성해야 합니다. 이 데이터를 사용자 지정 변수에 포함할 수 있습니다. | [eVar](../components/dimensions/evar.md) |
| 사이트에 있을 때 클릭한 광고 또는 링크 | AppMeasurement을 사용하는 경우 자동으로 수집됩니다. 클릭 위치와 같은 추가 정보는 Activity Map이 활성화된 상태에서 사용할 수 있습니다. | [Activity Map](../analyze/activity-map/activity-map.md), [종료 링크](../components/dimensions/exit-link.md), [다운로드 링크](../components/dimensions/download-link.md) |
| 사이트에서 구매한 제품 | 이 데이터를 수집하려면 모든 구현 유형을 구성해야 합니다. Adobe은 이 정보를 저장할 몇 가지 기본 변수를 제공합니다. | [제품](../components/dimensions/product.md), [주문 수](../components/metrics/orders.md), [매출](../components/metrics/revenue.md) |

{style="table-layout:auto"}

아래의 탐색 메뉴를 참조하십시오. [Dimension 개요](../components/dimensions/overview.md) 및 [지표 개요](../components/metrics/overview.md) Adobe이 잠재적으로 아래의 데이터를 수집할 수 있는 추가 변수의 경우.
