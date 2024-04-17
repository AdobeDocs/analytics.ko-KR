---
description: Adobe Analytics에서 수집하는 데이터와 기타 개인정보 보호 고려 사항 개요.
keywords: 개인정보 보호
title: 개인정보 보호 개요
feature: Privacy
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: 43c39b99cbae3e714b7f017dec14dd02fa350790
workflow-type: ht
source-wordcount: '978'
ht-degree: 100%

---

# 개인정보 보호 개요

Adobe는 귀하의 조직이 해당 법률 및 규정을 준수할 수 있도록 지원하고자 합니다. 자세한 내용은 [Adobe Experience Cloud 개인정보 보호](https://www.adobe.com/kr/privacy/experience-cloud.html){target=_blank}를 참조하십시오. Adobe Analytics와 귀하의 조직 사이에서 Adobe는 “데이터 처리자” 역할을 하며 귀하는 “데이터 컨트롤러” 역할(또는 관련 개인정보 보호 및 데이터 보호법에 따라 이에 상응하는 역할)을 합니다. 조직에서 Adobe의 솔루션 구현 방법을 독점적으로 제어하기 때문에 Adobe 제품 및 서비스의 사용 방법은 조직의 판단에 따라 공개합니다. Adobe Analytics를 사용하는 동안 귀하의 조직은 자체 개인정보 처리방침, Adobe와의 서비스 계약 및 모든 관련 법률을 준수할 책임이 있습니다.

Adobe는 다음과 같은 중요한 개념을 준수할 것을 강력히 권장합니다.

* **개인 데이터를 수집하는 경우 개인정보 보호 법률 및 규정을 준수하는지 확인합니다.** 사용자 정의 변수를 사용하면 액세스 가능한 거의 모든 것을 수집할 수 있습니다. 단, 조직의 개인정보 처리방침과 해당 법률도 고려해야 합니다.
* **조직의 개인정보 보호 정보를 찾기 쉽고 이해하기 쉽게 고객에게 제공합니다.** 유용한 정보에는 옵트아웃 링크, 찾아보기 데이터가 사용되는 방식, Adobe 서비스 사용 방법 또는 사용 계획 등이 포함됩니다.
* **적용되는 현지 법률과 국제 법률을 모두 숙지합니다.** 조직이 글로벌 규모로 운영되는 경우 일부 국제 법률이 적용될 수 있습니다.

## 데이터 수집 분류

Adobe는 Adobe로 데이터를 전송하는 데 도움이 되는 여러 데이터 수집 라이브러리를 제공합니다. 주요 예는 다음과 같습니다.

* **AppMeasurement**: 데이터를 Adobe Analytics로 직접 전송하도록 설계된 라이브러리입니다.
* **Web SDK**: Adobe Experience Platform Edge Network로 데이터를 전송하고, 여기에서 해당 데이터를 Adobe Analytics로 전달하도록 설계된 라이브러리입니다.
* **태그**: 초기 태그 구현 이후 웹 사이트나 앱의 소스 코드에 액세스하지 않고도 구현을 구성할 수 있는 웹 기반 UI입니다. AppMeasurement와 Web SDK 모두에 확장 기능을 사용할 수 있습니다.

Adobe Analytics는 다음 유형의 데이터를 수집할 수 있습니다.

| 데이터 유형 | 세부 사항 | 이 데이터를 포함하는 예시 변수 |
| --- | --- | --- |
| 사이트에 있는 웹 페이지의 페이지 이름 또는 URL | Adobe Analytics가 작동하려면 이 데이터가 필요합니다. 모든 히트에는 URL 또는 페이지 이름이 필요합니다. | [페이지](../components/dimensions/page.md), [페이지 URL](../components/dimensions/page-url.md) |
| 시간 기반 데이터 | Adobe Analytics가 작동하려면 이 데이터가 필요합니다. 데이터 수집에는 타임스탬프가 필요하며, 시간 기반 데이터는 타임스탬프에서 파생됩니다. | [페이지에서 보낸 시간](../components/dimensions/time-spent-on-page.md), [시간(일 기준)](../components/dimensions/hour-of-day.md), [오전/오후](../components/dimensions/am-pm.md), [평일/주말](../components/dimensions/weekday-weekend.md), [요일](../components/dimensions/day-of-week.md), [월(연 기준)](../components/dimensions/month-of-year.md) |
| 레퍼러 데이터 | 데이터 수집 라이브러리는 방문자가 웹 사이트에 도착할 때 기본적으로 참조 URL을 수집합니다. 레퍼러의 쿼리 문자열 내에서 데이터를 수집하도록 구현을 사용자 정의할 수 있습니다. 이 방법은 캠페인 및 광고 성과 추적에 일반적입니다. | [레퍼러](../components/dimensions/referrer.md), [참조 도메인](../components/dimensions/referring-domain.md) |
| 익명화된 방문자 ID | 데이터 수집 라이브러리는 사이트를 방문하는 각 브라우저에 대한 방문자 ID를 생성하고 참조합니다. 이 ID는 쿠키에 저장됩니다. 데이터 수집 라이브러리가 쿠키 식별자를 설정할 수 없는 경우 라이브러리는 익명 방문자 식별이라는 대체 방법을 사용합니다. 이 방법에는 방문자의 IP 주소와 사용자 에이전트 문자열을 사용하여 관련 히트를 동일한 방문에 연결하는 작업이 포함됩니다. 조직에서 IP 난독화가 활성화된 경우 이 설정이 적용됩니다. 자세한 내용은 [Adobe Analytics 및 브라우저 쿠키](cookies/cookies.md)를 참조하십시오. | [고유 방문자 수](../components/metrics/unique-visitors.md) |
| 식별 가능한 방문자 ID | Adobe는 사용자 정의 방문자 ID를 자동으로 수집하지 않습니다. 그러나 이 데이터를 수집하도록 구현을 사용자 정의할 수 있습니다. | [`visitorID`](../implement/vars/config-vars/visitorid.md) |
| 외부 검색어 | 외부 검색 데이터에는 검색 엔진에서 발생한 키워드가 포함됩니다. 데이터 수집 라이브러리는 참조 URL을 기반으로 이 데이터를 찾습니다. 그러나 대다수의 최신 검색 엔진에 더 이상 이 정보가 포함되지 않습니다. | [검색 키워드](../components/dimensions/search-keyword.md) |
| 내부 검색어 | 내부 검색 데이터에는 웹 사이트나 앱의 검색 기능 내에서 발생한 키워드가 포함됩니다. Adobe는 내부 검색 데이터를 자동으로 수집하지 않습니다. 그러나 이 데이터를 수집하도록 구현을 사용자 정의할 수 있습니다. 이 방법은 Adobe Analytics를 사용하는 조직에서 일반적입니다. | [eVar](../components/dimensions/evar.md) |
| 컴퓨터 및 브라우저 사양 | 데이터 수집 라이브러리는 브라우저 유형, 운영 체제 유형, 디바이스가 데스크탑인지 모바일인지 여부 등 낮은 엔트로피 브라우저 힌트를 자동으로 수집합니다. 브라우저의 특정 버전/빌드, 디바이스 모델 또는 운영 체제 버전과 같은 높은 엔트로피 힌트를 수집하려면 사용자 정의 구성이 필요합니다. 자세한 내용은 [클라이언트 힌트 개요](client-hints.md)를 참조하십시오. | [브라우저](../components/dimensions/browser.md), [운영 체제](../components/dimensions/operating-systems.md), [모바일 차원](../components/dimensions/mobile-dimensions.md), [모니터 해상도](../components/dimensions/monitor-resolution.md) |
| 지리적 위치 정보 | Adobe는 IP 주소의 마지막 옥텟을 0으로 설정하여 자세한 지리적 위치를 방지하는 기능을 제공합니다. 이 기능은 지리적 정보의 정확성을 낮추는 역할을 하며, [보고서 세트 설정](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/general-acct-settings-admin.html)에서 설정할 수 있습니다. | [도시](../components/dimensions/cities.md), [지역](../components/dimensions/regions.md), [국가](../components/dimensions/countries.md) |
| IP 주소 | Adobe는 이 데이터를 저장할 때 방문자의 IP 주소를 난독화(해시)하거나 완전히 제거하는 기능을 제공합니다. EMEA 고객은 일반적으로 IP 주소 설정이 기본적으로 난독화되어 있습니다. 난독화 설정에 관계없이 IP 주소는 Analysis Workspace에서 차원으로 사용할 수 없으며 [데이터 피드](../export/analytics-data-feed/data-feed-overview.md)에만 포함됩니다. 사용 가능한 난독화 설정에 대한 자세한 내용은 관리 안내서의 [일반 계정 설정](../admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md)을 참조하십시오. | 없음 |
| 사이트에 제공된 양식 정보 | 이 데이터를 수집하려면 모든 구현 유형에 구성이 필요합니다. 이 데이터를 사용자 정의 변수에 포함할 수 있습니다. | [eVar](../components/dimensions/evar.md) |
| 사이트에서 클릭된 광고 또는 링크 | [`trackExternalLinks`](../implement/vars/config-vars/trackexternallinks.md) 또는 [`trackDownloadLinks`](../implement/vars/config-vars/trackdownloadlinks.md)가 활성화된 경우 수집됩니다. 클릭 위치와 같은 추가 정보는 Activity Map을 활성화하면 확인할 수 있습니다. | [Activity Map](../analyze/activity-map/activity-map.md), [종료 링크](../components/dimensions/exit-link.md), [다운로드 링크](../components/dimensions/download-link.md) |
| 사이트에서 구매한 제품 | 이 데이터를 수집하려면 모든 구현 유형에 구성이 필요합니다. Adobe는 이 정보를 수집하기 위해 여러 가지 기본 변수를 제공합니다. | [제품](../components/dimensions/product.md), [주문](../components/metrics/orders.md), [매출](../components/metrics/revenue.md) |

{style="table-layout:auto"}

Adobe가 잠재적으로 데이터를 수집할 수 있는 더 많은 변수는 [차원 개요](../components/dimensions/overview.md) 및 [지표 개요](../components/metrics/overview.md) 아래의 탐색 메뉴를 참조하십시오.

## 데이터 처리 위치

Adobe는 Adobe Analytics에 대해 세 가지 데이터 처리 위치를 유지 관리합니다. 이러한 사이트는 원시 데이터를 수신하여 이를 데이터 저장 및 보고 검색에 최적화된 보고서 세트로 처리합니다. 이러한 데이터 처리 위치는 현재 미국(오리건), 영국(런던) 및 싱가포르에 있습니다. 자세한 내용은 [Adobe Analytics 보안 개요](https://www.adobe.com/kr/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adb-analytics-security-wp.pdf){target=_blank}를 참조하십시오.
