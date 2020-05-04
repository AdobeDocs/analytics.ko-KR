---
description: 이 섹션에는 Adobe Analytics의 주요 개념, 그 개념에 대한 간단한 설명 및 해당 주제에 대한 추가 설명이 있는 특정 설명서 링크가 포함되어 있습니다.
title: Adobe Analytics - 주요 개념
translation-type: tm+mt
source-git-commit: ad9a7729924636055e456d0fd7ab928be227034d

---


# Adobe Analytics - 주요 개념

이 섹션에는 Adobe Analytics의 주요 개념, 그 개념에 대한 간단한 설명 및 해당 주제에 대한 추가 설명이 있는 특정 설명서 링크가 포함되어 있습니다.

## Analytics 도구 {#concept_833EDD4EB056491DA1BC5A3A45FE285B}

| 제품 | 설명 | 설명서 링크 |
|--- |--- |--- |
| Analysis Workspace | 강력한 사용자 지정 분석 프로젝트를 구축하고 통찰력을 보여주기 위한 브라우저 솔루션입니다. Reports &amp; Analytics보다 더 많은 보고서 유연성을 제공합니다. | [adobe.ly/aaworkspacedocs](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html) |
| Reports &amp; Analytics(이전 SiteCatalyst) | 보고 및 분석을 위한 브라우저 솔루션. Analytics 패키지의 초급자 도구입니다. | [Reports &amp; Analytics 홈](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/reports-analytics/getting-started.html) |
| Report Builder | Adobe Analytics 데이터에서 사용자 지정 요청을 작성하고 Microsoft Excel을 사용하여 이 요청을 시각화할 수 있는 Excel 추가 기능입니다. | [Report Builder 홈](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/report-builder/home.html) |
| Ad Hoc Analysis(이전 Discover) | 고급 디지털 분석용 Java 기반 도구입니다. | [Ad Hoc Analysis 홈](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/ad-hoc-analysis/adhoc-home.html) |
| Data Workbench (이전 Insight) | 여러 채널에서 이루어지는 온라인 및 오프라인 고객 상호 작용 데이터를 수집, 처리, 분석 및 시각화하도록 설계되어 있습니다. | [Data Workbench 클라이언트](https://docs.adobe.com/content/help/en/data-workbench/using/client/t-open-ins.html) |
| Data Warehouse | 데이터를 필터링하여 실행할 수 있는 스토리지 및 사용자 지정 보고서에 대한 처리되지 않은 원시 데이터입니다. 히트 수준은 아닙니다. | [Data Warehouse 홈](https://docs.adobe.com/content/help/ko-KR/analytics/export/data-warehouse/data-warehouse.html) |
| Adobe Mobile Services | Adobe Experience Cloud에서 모바일 애플리케이션을 위한 모바일 마케팅 기능들을 가져와서 사용자의 애플리케이션 참여를 이해하고 개선할 수 있도록 해줍니다. | [Mobile Services 홈](https://docs.adobe.com/content/help/ko-KR/mobile-services/using/home.html) |
| Adobe Exchange Data Connectors(이전 Genesis) | 타사 애플리케이션의 추적 데이터를 Analytics로 가져와서 하나의 중앙 위치에서 종단 간 가시성을 제공합니다. | [Data Connectors 홈](https://marketing.adobe.com/developer/documentation/genesis/c-overview-how-it-works) |
| Dynamic Tag Management (DTM) | 도메인 수에 관계없이 모든 사이트의 분석, 타겟 및 기타 태그를 관리할 수 있도록 도와줍니다. | [DTM 홈](https://docs.adobe.com/content/help/ko-KR/analytics/implementation/implement-analytics-with-dtm/dtm-implementation-overview.html) |
| Adobe Launch | Adobe의 차세대 웹 사이트 태그 및 모바일 SDK 관리 기능. | [Adobe Launch 홈](https://docs.adobe.com/content/help/ko-KR/launch/using/overview.html) |

## 주요 용어 {#concept_E473ACBB8E4A42B4AC005538AC12F154}

Adobe Analytics 용어에 대해 확대된 용어집이 필요하면 [여기](https://docs.adobe.com/content/help/ko-KR/analytics/technotes/terms.html)를 클릭하십시오.

| 용어 | 설명 | 설명서 링크 |
|--- |--- |--- |
| Prop(사용자 지정 트래픽) | 페이지별 사이트 트래픽 활동을 추적하는 데 사용되는 차원. Prop은 페이지 간에 지속되지 않습니다. 트래픽 변수의 주요 응용: <ul><li>특정 값의 &#39;가장 인기 있음&#39;을 찾는 간단한 계산</li><li>사용자가 특정 사이트까지 이동하는 경로 표시 </li></ul><br>트래픽 변수의 예: 페이지 이름, 사이트 섹션, 브라우저</br> | [Prop](https://docs.adobe.com/content/help/ko-KR/analytics/admin/admin-tools/traffic-variables/traffic-var.html) |
| eVar(사용자 지정 전환) | 사용자가 사용자 지정한 기간 동안 지속되는 차원. 만료 옵션은 이벤트 만료, 방문 만료 또는 특정일 만료를 포함하며, 해당 변수에 대해 수행하게 될 분석 유형에 의해 파생되어야 합니다.<br>eVar와 prop 간의 주요 차이점:</br><ul><li>Prop은 지속성이 제거되므로 경로 분석에 자주 사용됩니다.</li><li>eVar는 전환 분석에 자주 사용됩니다.</li></ul><br>전환 변수의 예: 내부 검색어, 내부 프로모션, 외부 캠페인(s.campaign)</br> | [eVar](https://docs.adobe.com/content/help/ko-KR/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html) |
| 이벤트/지표(s.events) | 방문자들이 사이트에서 취하기를 바라는 주요 동작을 측정하는 지표. 카운터, 숫자 및 통화, 이렇게 세 가지 유형의 이벤트가 있습니다. 이벤트는 전환 변수(eVar) 보고서에 추가될 때 가장 유용합니다. eVar에서는 발생한 일에 대한 정성인 정보를 제공하고 이벤트에서는 발생한 일에 대한 정량적 정보를 제공합니다. <br>eVar와 이벤트 간의 주요 차이점:</br><ul><li>eVar는 영향을 받은 사람, 사항 또는 항목에 대해 알려 줍니다.</li><li>이벤트는 전환이 발생하는 방식을 측정합니다.</li></ul><br>전환 이벤트의 예: 주문 수, 애플리케이션 시작, 리드, 매출.</br> | [이벤트](https://docs.adobe.com/content/help/ko-KR/analytics/admin/admin-tools/success-events/success-event.html) |
| 구성 요소 | 프로젝트에 드래그하여 놓을 수 있는 차원, 지표, 세그먼트 및 시간 세부기간(날짜 범위). | [구성 요소](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/components/analysis-workspace-components.html) |
| 차원 | eVar, prop, 분류 및 표준 Adobe에서 수집한 값들의 컬렉션. | [차원](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/dimensions-reports/reports-descriptions.html) |
| 지표 | 구현된 이벤트 및 계산된 지표들의 컬렉션. | [지표](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/components/apply-create-metrics.html) |
| 계산된 지표 | 구현을 통해 캡처된 기존 지표에서 사용자 지정 지표를 파생시키는 기능. | [계산된 지표](https://docs.adobe.com/content/help/ko-KR/analytics/components/calculated-metrics/cm-overview.html) |
| 세그먼트 | 강력하고 집중된 대상 세그먼트를 빌드, 관리, 공유하고 Analytics 보고서에 적용하는 기능입니다. 세그먼트는 Analytics 제품들 간에 공유되고 Experience Cloud에서도 공유할 수 있습니다. | [세그먼테이션](https://docs.adobe.com/content/help/ko-KR/analytics/components/segmentation/seg-home.html) |
| 시간(날짜 범위) | 날짜를 원하는 기간으로 필터링하고 분석에 다시 사용할 수 있는 사용자 지정 날짜 범위를 생성하는 기능. | [데이터 범위](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html) |
| 시각화 | 프로젝트에서 데이터에 생기를 불어넣을 수 있는 풍부한 시각적 요소. | [시각화](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) |
| 큐레이션 | 프로젝트나 가상 보고서 세트에서 액세스할 수 있는 구성 요소를 제한하는 기능. | [VRS 큐레이션](https://docs.adobe.com/content/help/ko-KR/analytics/components/virtual-report-suites/vrs-components.html)<br>[프로젝트 큐레이션](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/curate-share/curate.html)</br><br>[비교](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/curate-share/curate-projects-vrs.html) |

## 주요 보고서

| 보고서 | 설명 | 설명서 링크 |
|--- |--- |--- |
| 전체 차원/보고서 목록 | Adobe Analytics에서 사용 가능한 모든 차원/보고서에 대한 정의입니다. | [차원](https://docs.adobe.com/content/help/en/analytics/components/variables/c-variables.html) |
| Advertising Analytics | Adobe Analytics 내에서 모든 Google 및 Bing 유료 검색 데이터를 나란히 분석합니다. 통합을 통해 생성된 차원에는 광고 플랫폼, 키워드, 일치 유형 등이 포함됩니다. 생성된 지표는 AMO 노출 횟수, AMO 클릭 수, AMO 비용, 평균 위치 및 평균 품질 점수입니다. | [Advertising Analytics](https://docs.adobe.com/help/ko-KR/analytics/integration/advertising-analytics/overview.html) |
| Audience Analytics | AAM에서 사용자 대상 멤버십으로 수신 Analytics 히트를 풍부하게 합니다. 인구 통계학적 정보(예: 성별 또는 수입 수준), 대상 데이터(예: 인구 통계 정보), 사이코그래프 정보(예: 관심사 및 취미), CRM 데이터 및 광고 노출 데이터와 같은 AAM 대상 데이터를 Analytics 워크플로우에 통합할 수 있습니다. 이 통합을 통해 생성된 차원은 대상 ID 및 대상자 이름입니다. | [Audience Analytics](https://docs.adobe.com/content/help/ko-KR/analytics/integration/audience-analytics/mc-audiences-aam.html) |
| 기여도 분석 IQ | 고객 움직임에서 어떻게 의미 있는 참여가 발생하는지를 이해하여 고객을 타겟 결과로 이끄는 변곡점을 지능적으로 식별하며 마케팅 이니셔티브를 효과적으로 최적화할 수 있도록 해줍니다. 모델에는 첫 번째, 마지막, 선형, 기여도, j자형, 역 j자형, u자형, 동일 터치, 사용자 지정 및 시간 감소가 포함됩니다. | [기여도 분석 IQ](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/panels/attribution.html) |
| 예외 항목 탐지 | 이전 데이터에 관해 주어진 지표가 변경되는 방법을 결정하는 통계적 방법. AD(예외 항목 탐지)는 Analysis Workspace의 모든 트렌드 시각화에 대해 기본적으로 켜져 있습니다. | [예외 항목 탐지](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html) |
| 기여도 분석 | 사용자가 액세스하는 모든 개별 지표 및 차원에 대해 자동화된 분석을 실행함으로써 예외 항목이 발생하는 &quot;원인&quot;을 탐구합니다. | [기여도 분석](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| 집단 분석 | 집단은 지정된 기간 동안 공통적인 특성을 공유하는 사람들의 그룹입니다. 집단 분석은 사용자의 유지 및 이탈을 분석하는 데 도움이 됩니다. | [집단 분석](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.html) |
| 고객 움직임 보고서 | 사용자가 사이트 또는 앱을 통해 이동하는 경로에 대한 정보를 표시합니다. Analysis Workspace에서 이 분석을 하는 데 Prop, eVar 및 이벤트를 사용할 수 있습니다. | [Analysis Workspace 폴아웃](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html)[Analysis Workspace 플로우](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/visualizations/flow/flow.html)[Reports &amp; Analytics 경로 지정](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/dimensions-reports/reports-paths.html) |
| 마케팅 채널 | 사용자를 사이트로 유도하는 외부 채널과 전환 유도 시 가장 효과적인 사항을 아는 데 도움이 되는 보고서입니다. 첫 번째 및 마지막 터치 귀인 방식 보기가 제공됩니다. 이것은 유료 채널과 유기 채널 모두를 가장 포괄적으로 볼 수 있는 보기이므로, Adobe Analytics에서 선호되는 외부 트래픽 소스 보고서입니다(캠페인이나 트래픽 소스보다 선호됨). | [마케팅 채널](https://docs.adobe.com/content/help/ko-KR/analytics/components/marketing-channels/c-getting-started-mchannel.html) |
| 모바일 | 모바일 장치나 태블릿에서 액세스한 웹 사이트에 대한 정보를 표시합니다. | [모바일 보고서 | (https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/dimensions-reports/reports-mobile.html) |
| 모바일 앱 | 모바일 앱과 관련된 기본 사용 정보를 표시합니다. 이러한 보고서는 SDK가 구현되고 보고가 설정되어 있으면 사용할 수 있습니다.  또한, Adobe Mobile Services는 보다 포괄적인 앱 데이터를 제공하는 별도의 모바일 앱 인터페이스를 만들어 사용자의 앱 사용을 이해 및 개선할 수 있도록 했습니다.  [여기](https://mobilemarketing.adobe.com)에서 인터페이스에 액세스합니다. | [Adobe Mobile Services](https://docs.adobe.com/content/help/ko-KR/mobile-services/using/home.html) | 제품 | 개별 제품 및 제품 그룹(카테고리)이 매출액 또는 체크아웃 횟수와 같은 다양한 전환 지표에 기여하는 정도를 알 수 있습니다. | [제품 보고서](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/dimensions-reports/reports-products.html) |
| 세그먼트 비교 | 사용자가 액세스하는 모든 개별 지표 및 차원에 대한 자동화된 분석을 통해 세그먼트 간의 통계적으로 가장 유의미한 차이를 알아냅니다. | [세그먼트 비교](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/panels/segment-comparison/segment-comparison.html) |
| 사이트 컨텐츠 보고서 | 가장 방문 횟수가 많은 사이트 페이지 및 영역과 가장 많이 이용하는 서버에 대한 정보를 표시합니다. | [사이트 컨텐츠 보고서](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/dimensions-reports/reports-site-content.html) |
| 사이트 지표 보고서 | 고유 방문자, 주문, 매출 등과 같은 웹 사이트에 대한 정량적 정보를 표시합니다. 각 지표는 항목 기반의 다른 보고서에서 대체될 수 있습니다. | [사이트 지표 보고서](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/dimensions-reports/reports-site-metrics.html) |
| 방문자 프로필 | 국가, 주, ZIP/우편 번호 및 도메인과 같은 다양한 프로필 범주에 속하는 고객의 구매 패턴을 보여주는 보고서입니다. | [방문자 프로필](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/dimensions-reports/reports-visitor-profile.html) |
| 방문자 유지 | 사이트로 돌아오는 방문자의 수와 돌아오는 빈도와 같은, 고객 충성도에 대한 정보를 표시합니다. | [방문자 유지](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/dimensions-reports/reports-visitor-retention.html) |
| 프로젝트 링크, 공유 및 예약 | Analytics 인터페이스에서 작업을 저장하거나 다른 사람과 공유하는 방법입니다. | [파일 보내기 및 예약](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/curate-share/send-schedule-files.html) |

## 주요 지표 {#concept_392819DC275C48688E2CE4ABD4C5EE43}

| 지표 이름 | 정의 | 설명서 링크 |
|---|---|---|
| 전체 지표 목록 | Adobe Analytics에 있는 모든 지표의 정의입니다. | [지표 개요](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/metrics/metrics-overview.html) |
| 고유 방문자 수 | 지정된 기간 동안 복제되지 않는 웹 사이트 방문자의 수입니다. | [고유 방문자 수](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/dimensions-reports/reports-unique-visitors-v15-dsc.html) |
| 방문 횟수 | 중단 없는 일련의 페이지 보기입니다. 방문은 사람이 먼저 사이트에서 페이지를 볼 때 시작되고 활동이 없는 상태로 30분이 경과하면 끝납니다. | [방문 횟수](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/metrics/metrics-visit.html) |
| 페이지 보기 수 | 방문자가 웹 사이트의 페이지를 보면 페이지 보기가 발생합니다. | [페이지 보기 수](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/metrics/metrics-page-view.html) |
| 인스턴스 | 변수가 정의된 횟수입니다. Adobe Analytics에서 변수 내 값을 볼 때마다 해당의 각 보고서에서 인스턴스가 하나씩 증가합니다. | [인스턴스](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/metrics/metrics-instance.html) |
| 발생 횟수 | 변수가 정의되거나 지속된 횟수입니다. | [발생 횟수](https://docs.adobe.com/content/help/ko-KR/analytics/components/variables/metrics/metrics-occurrences.html) |

## 가져오기 옵션 {#concept_7C6DF03B5F9149E2A77F36C739432059}

| 옵션 | 설명 | 설명서 링크 |
|---|---|---|
| 분류 가져오기 | 브라우저나 FTP 업로드를 통해 캡처된 차원을 기준으로 메타데이터를 가져오십시오. 규칙 빌더와 비교되는 수동 방식입니다. | [분류 가져오기](https://docs.adobe.com/content/help/en/analytics/components/classifications/classifications-importer/c-working-with-saint.html) |
| 규칙 빌더 | 사용자 정의된 규칙을 기반으로 차원의 메타데이터 분류를 자동으로 생성합니다. | [분류 규칙 빌더](https://docs.adobe.com/content/help/ko-KR/analytics/components/classifications/classifications-rulebuilder/classification-rule-builder.html) |
| 사용자 특성 | Adobe Analytics 및 Adobe Target에서 사용하기 위해 Experience Cloud에 업로드된 CRM 데이터. | [사용자 특성](https://docs.adobe.com/content/help/ko-KR/core-services/interface/customer-attributes/attributes.html) |
| 데이터 소스 | 오프라인 지표를 차원을 기준으로 하거나 일별로 Analytics에 가져옵니다. | [데이터 소스](https://docs.adobe.com/content/help/ko-KR/analytics/import/data-sources/datasrc-home.html) |
| Adobe Exchange Data Connectors | [Analytics 도구](/help/landing/an-key-concepts.md)를 참조합니다. |  |
| 기본 통합 | Audience Analytics 및 Advertising Analytics. | 주요 보고서 섹션을 참조합니다. |

## 내보내기 옵션 {#concept_C62B688E259141CF92C048E8110464BE}

| 옵션 | 설명 | 설명서 링크 |
|---|---|---|
| UI 다운로드 및 예약 | Analysis Workspace에서 데이터를 CSV 또는 PDF로 내보냅니다. | [PDF 또는 CSV 파일 다운로드](/help/analyze/analysis-workspace/curate-share/download-send.md) |
| Report Builder | Analytics 도구를 참조하십시오. |
| Analytics API | 사용자만의 Analytics 데이터에 대해 사용자 지정된 쿼리를 생성합니다. | <ul><li>[API 2.0](https://www.adobe.io/apis/experiencecloud/analytics/docs.html)</li><li>[API 1.4](https://github.com/AdobeDocs/analytics-1.4-apis)</li></ul> |
| Data Warehouse | Analytics 도구를 참조하십시오. |  |
| Analytics 데이터 피드 | Analytics 외부에서 데이터를 얻는 가장 세분화된 방식입니다. Analytics 외부에서 히트 수준 피드를 설정합니다. | [Analytics 데이터 피드](https://docs.adobe.com/content/help/ko-KR/analytics/export/analytics-data-feed/get-started/data-feed-overview.html) |

## 데이터 수집 및 유효성 검사 {#concept_E07350D4CA5047DAA7D81F762F29606A}

| 방법/리소스 | 설명 | 설명서 링크 |
|--- |--- |--- |
| 개발자 리소스 | 모든 사용 가능한 플랫폼(웹, 모바일 앱, 동영상, 플래시 등)에 걸쳐서 Analytics 데이터를 수집하는 데 사용할 수 있는 라이브러리에 대해 대략적으로 설명하는 설명서입니다. | [개발자 설명서](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) |
| 구현 안내서 | 데이터 수집 변수에 대한 설명과 데이터 수집 코드를 JavaScript로 구현하는 방법에 대한 자세한 설명이 포함되어 있습니다. | [구현 안내서](https://docs.adobe.com/content/help/ko-KR/analytics/implementation/home.html) |
| App Measurement(s_code) | 전역 변수 관리 | [AppMeasurement](https://docs.adobe.com/content/help/ko-KR/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html) |
| 앱 SDK | 사전에 채워진 Apps에 대한 구성 파일 버전을 포함하는 사용자 지정된 패키지입니다. | <ul><li>[iOS](https://docs.adobe.com/content/help/ko-KR/mobile-services/ios/overview.html)</li><li>[Android](https://docs.adobe.com/content/help/ko-KR/mobile-services/android/getting-started-android/requirements.html)</li></ul> |
| DTM 및 Adobe Launch | Analytics 도구를 참조하십시오. |  |
| VISTA | 수집된 데이터를 변경하거나 세그먼트화하는 서버측 로직을 적용할 수 있습니다. | [VISTA 규칙](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/processing-rule-order.html) |
| 처리 규칙 | Analytics UI에서 변수를 설정, 수정 및 복사하여 수집된 데이터를 변경하는 기능. | [처리 규칙](https://docs.adobe.com/content/help/ko-KR/analytics/admin/admin-tools/processing-rules/processing-rules.html) |
| 디버거 옵션 | Adobe Experience Cloud 디버거를 비롯하여 구현의 유효성을 확인하는 데 도움이 될 수 있는 디버거 및 패킷 스니퍼에는 몇 가지가 있습니다. | [Adobe Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=en) |
| 데이터 삽입 API | 데이터 삽입 API는 서버측 데이터 수집과 Experience Cloud 서버에 데이터를 제출하기 위한 메커니즘을 제공합니다. 서버측 데이터 수집에서는 각 웹 페이지에서 JavaScript 비콘을 사용하여 방문자 데이터를 Experience Cloud 서버에 전송하는 대신 웹 브라우저 요청과 웹 서버 응답만 기준으로 해서 데이터를 수집합니다. | [POST를 사용하여 Adobe Analytics 데이터 삽입 API를 구현하는 절차](https://helpx.adobe.com/kr/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) |
