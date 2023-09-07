---
description: Adobe Analytics에서 수집하는 데이터와 기타 개인정보 보호 고려 사항 개요.
keywords: 개인정보 보호
title: 개인정보 보호 개요
feature: Privacy
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: 04f8602ccfa7fd2d1d2f3c56f477aeee3739c563
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 3%

---

# 개인정보 보호 개요

Adobe은 귀하가 해당 개인 정보 보호 법률 및 규정을 준수할 수 있도록 귀하의 조직을 활성화하고자 합니다. 다음을 참조하십시오 [Adobe Experience Cloud 개인 정보 보호](https://www.adobe.com/kr/privacy/experience-cloud.html) 추가 정보. Adobe Analytics과 관련하여 Adobe은 &quot;데이터 프로세서&quot; 역할을 하며 귀하는 &quot;데이터 컨트롤러&quot;(또는 해당 개인정보 보호 및 데이터 보호 법률에 따라 동등)입니다. 조직에서 Adobe의 솔루션 구현 방법을 독점적으로 제어하기 때문에 Adobe의 제품 및 서비스의 사용 방법은 조직의 판단에 따라 공개합니다. 조직은 자체 개인정보 처리방침, Adobe과의 서비스 계약 및 모든 적용 가능한 법률을 준수할 책임이 있습니다.

Adobe은 다음과 같은 중요한 개념을 준수할 것을 강력히 권장합니다.

* **개인 데이터를 수집하는 경우 개인 정보 보호 법률 및 규정을 준수하는지 확인하십시오.** 사용자 지정 변수를 사용하면 액세스할 수 있는 거의 모든 항목을 수집할 수 있습니다. 그러나 조직의 개인정보 처리방침 및 적용 가능한 법도 고려해야 합니다.
* **고객에게 찾기 쉽고 이해하기 쉬운 조직 개인정보 보호 정보를 제공합니다.** 유용한 정보에는 옵트아웃 링크, 탐색 데이터의 사용 방법, Adobe의 서비스를 사용하거나 사용할 계획이 있습니다.
* **본인에게 적용되는 국내법과 국제법을 모두 숙지하십시오.** 조직이 전세계적인 규모로 운영되는 경우 일부 국제법을 적용할 수 있습니다.

## 데이터 수집 분류

Adobe은 Adobe에 데이터를 전송하는 데 도움이 되도록 여러 데이터 수집 라이브러리를 제공합니다. 주목할 만한 예는 다음과 같습니다.

* **AppMeasurement**: Adobe Analytics으로 직접 데이터를 전송하도록 디자인된 라이브러리입니다.
* **웹 SDK**: Adobe Experience Platform Edge 네트워크로 데이터를 보낸 다음 해당 데이터를 Adobe Analytics으로 전달하도록 디자인된 라이브러리입니다.
* **태그**: 초기 태그 구현 외에 웹 사이트 또는 앱의 소스 코드에 액세스하지 않고도 구현을 구성할 수 있는 웹 기반 UI입니다. 확장은 AppMeasurement 및 Web SDK 모두에서 사용할 수 있습니다.

Adobe Analytics은 다음 유형의 데이터를 수집할 수 있습니다.

| 데이터 유형 | 세부 사항 | 이 데이터를 포함하는 예제 변수 |
| --- | --- | --- |
| 사이트에 있는 웹 페이지의 페이지 이름 또는 URL | Adobe Analytics이 작동하도록 항상 수집됩니다. 모든 히트에 URL 또는 페이지 이름이 필요합니다. | [페이지](../components/dimensions/page.md), [페이지 URL](../components/dimensions/page-url.md) |
| 시간 기반 데이터 | Adobe Analytics이 작동하도록 항상 수집됩니다. 데이터 수집에는 타임스탬프가 필요하며, 시간 기반 데이터는 타임스탬프에서 파생됩니다. | [페이지에서 보낸 시간](../components/dimensions/time-spent-on-page.md), [시간(일 기준)](../components/dimensions/hour-of-day.md), [오전/오후](../components/dimensions/am-pm.md), [평일/주말](../components/dimensions/weekday-weekend.md), [요일](../components/dimensions/day-of-week.md), [월(연 기준)](../components/dimensions/month-of-year.md) |
| 다른 사이트의 웹 페이지 데이터 | Adobe은 웹 사이트 또는 앱의 소스 코드를 변경할 수 없는 제휴 해제된 사이트에서 데이터를 수집할 수 없습니다. 데이터 수집 라이브러리는 방문자가 웹 사이트에 도달하면 기본적으로 참조 URL을 수집합니다. 웹 사이트 또는 앱 방문자가 도착한 후 쿼리 문자열 내에서 데이터를 수집하도록 구현을 사용자 지정할 수 있습니다. | [레퍼러](../components/dimensions/referrer.md), [참조 도메인](../components/dimensions/referring-domain.md) |
| 익명으로 처리된 방문자 ID | 데이터 수집 라이브러리는 사이트를 방문하는 각 브라우저에 대한 방문자 ID를 생성하고 참조합니다. 이 ID는 쿠키에 저장됩니다. 데이터 수집 라이브러리가 어떤 이유로든 쿠키를 설정할 수 없는 경우, 라이브러리는 IP 주소 및 사용자 에이전트 문자열을 사용하는 방문자 식별 대비책을 사용합니다. 다음을 참조하십시오 [Adobe Analytics 및 브라우저 쿠키](cookies/cookies.md) 추가 정보. | [고유 방문자 수](../components/metrics/unique-visitors.md) |
| 식별 가능한 방문자 ID | Adobe은 사용자 지정 방문자 ID를 자동으로 수집하지 않습니다. 그러나 구현을 사용자 지정하여 이 데이터를 수집할 수 있습니다. | [`visitorID`](../implement/vars/config-vars/visitorid.md) |
| 외부 검색어 | 외부 검색 데이터에는 검색 엔진에서 생성된 키워드가 포함됩니다. 데이터 수집 라이브러리는 참조 URL을 기반으로 이 데이터를 찾습니다. 그러나 많은 최신 검색 엔진은 더 이상 이 정보를 포함하지 않습니다. | [검색 키워드](../components/dimensions/search-keyword.md) |
| 내부 검색어 | 내부 검색 데이터에는 웹 사이트 또는 앱의 검색 기능 내에서 생성된 키워드가 포함됩니다. Adobe은 내부 검색 데이터를 자동으로 수집하지 않습니다. 그러나 구현을 사용자 지정하여 이 데이터를 수집할 수 있습니다. 이 방법은 Adobe Analytics을 사용하는 조직에 일반적입니다. | [eVar](../components/dimensions/evar.md) |
| 컴퓨터 및 브라우저 사양 | AppMeasurement은 브라우저 유형, 운영 체제 유형 및 디바이스가 데스크톱이나 모바일인 경우와 같은 낮은 엔트로피 브라우저 힌트를 자동으로 수집합니다. 브라우저의 특정 버전/빌드, 디바이스 모델 또는 운영 체제 버전과 같은 높은 엔트로피 힌트를 수집하려면 사용자 지정 구성이 필요합니다. 다음을 참조하십시오 [클라이언트 힌트 개요](client-hints.md) 추가 정보. | [브라우저](../components/dimensions/browser.md), [운영 체제](../components/dimensions/operating-systems.md), [모바일 차원](../components/dimensions/mobile-dimensions.md), [모니터 해상도](../components/dimensions/monitor-resolution.md) |
| 지리적 위치 정보 | Adobe은 (보고서 세트 수준에서) 각 웹 사이트 또는 앱에 대한 지리적 위치 데이터 수집을 활성화하거나 비활성화하는 기능을 제공합니다. 지리적 위치 데이터 수집은 기본적으로 활성화되어 있습니다. 활성화된 경우 데이터 수집 라이브러리에는 지리적 위치가 포함됩니다. | [도시](../components/dimensions/cities.md), [지역](../components/dimensions/regions.md), [국가](../components/dimensions/countries.md) |
| IP 주소 | Adobe은 이 데이터를 저장할 때 마지막 옥텟을 난독화하거나 방문자의 IP 주소를 완전히 난독화하는 기능을 제공합니다. EMEA 고객은 일반적으로 기본적으로 IP 주소 설정을 완전히 난독화했습니다. IP 주소는 난독화 설정에 관계없이 Adobe Analytics에서 차원으로 사용할 수 없으며 에만 포함됩니다. [데이터 피드](../export/analytics-data-feed/data-feed-overview.md). | 없음 |
| 사이트에 제공된 양식 정보 | 이 데이터를 수집하려면 모든 구현 유형을 구성해야 합니다. 이 데이터를 사용자 지정 변수에 포함할 수 있습니다. | [eVar](../components/dimensions/evar.md) |
| 사이트에서 광고 또는 링크를 클릭함 | 데이터 수집 라이브러리를 사용하는 경우 기본적으로 수집됩니다. Activity Map을 활성화하면 클릭 위치와 같은 추가 정보를 사용할 수 있습니다. | [Activity Map](../analyze/activity-map/activity-map.md), [종료 링크](../components/dimensions/exit-link.md), [다운로드 링크](../components/dimensions/download-link.md) |
| 사이트에서 구매한 제품 | 이 데이터를 수집하려면 모든 구현 유형을 구성해야 합니다. Adobe은 이 정보를 수집하기 위한 몇 가지 기본 변수를 제공합니다. | [제품](../components/dimensions/product.md), [주문 수](../components/metrics/orders.md), [매출](../components/metrics/revenue.md) |

{style="table-layout:auto"}

아래의 탐색 메뉴를 참조하십시오. [Dimension 개요](../components/dimensions/overview.md) 및 [지표 개요](../components/metrics/overview.md) Adobe이 잠재적으로 아래의 데이터를 수집할 수 있는 추가 변수의 경우.

## 데이터 처리 위치

Adobe은 Adobe Analytics에 대해 세 개의 데이터 처리 위치를 유지 관리합니다. 이러한 사이트는 원시 데이터를 수신하여 보고서 세트로 처리하며, 이 보고서 세트는 데이터 저장 및 보고 검색에 최적화됩니다. 이러한 데이터 처리 위치는 다음 위치에 있습니다. **오레곤**, **런던**, 및 **싱가포르**. 다음을 참조하십시오 [Adobe Analytics 보안 개요](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adb-analytics-security-wp.pdf) 추가 정보.
