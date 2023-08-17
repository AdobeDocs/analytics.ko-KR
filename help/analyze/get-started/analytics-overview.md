---
description: Adobe Analytics에 대한 일반 개요 정보
title: Adobe Analytics 개요
feature: Analytics Basics
hide: true
hidefromtoc: true
source-git-commit: 1c6cc23c9cb6b4b007d2f296ea23e697cc135bd4
workflow-type: tm+mt
source-wordcount: '3101'
ht-degree: 32%

---

# Adobe Analytics 개요

Adobe Analytics을 사용하면 디지털 고객 상호 작용에서 데이터를 수집하고 실행 가능한 통찰력을 얻을 수 있습니다. 심층적인 분석, 다목적 보고 및 예측 인텔리전스를 통해 조직은 고객을 위해 더 나은 경험을 구축하는 데 필요한 통찰력 있는 기반을 확보할 수 있습니다.

## 주요 이점

다음은 조직이 고객에게 더 나은 서비스를 제공하기 위해 중요한 통찰력을 얻을 수 있도록 Adobe Analytics을 지원하는 몇 가지 주요 방법입니다.

Adobe Analytics이 제공하는 이점에 대한 자세한 내용은 다음을 참조하십시오. [Adobe Analytics 제품 페이지](https://business.adobe.com/products/analytics/adobe-analytics.html).

### 웹 분석

Adobe Analytics은 웹 사이트 트래픽을 분석하기 위한 다음과 같은 복잡한 세그멘테이션 및 예측 도구를 제공합니다.

* [Analysis Workspace의 Ad hoc analysis](/help/analyze/analysis-workspace/home.md)

* [흐름 분석](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md)

* [고급 세분화](/https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html)

### 마케팅 분석

Adobe Analytics은 고객이 브랜드와 상호 작용하는 위치, 고객이 선호하는 채널 및 공감하는 경험을 조직에서 이해할 수 있도록 지원합니다.

Adobe Analytics의 다음 주요 기능은 이러한 마케팅 기능을 제공합니다.

* 멀티채널 데이터 수집

* [오프라인 데이터 통합](https://experienceleague.adobe.com/docs/analytics/import/data-sources/overview.html?lang=en)

* [Analysis Workspace의 Ad hoc analysis](/help/analyze/analysis-workspace/home.md)

### 기여도 분석

속성을 통해 조직은 고객 여정 전체에서 다양한 상호 작용이 전환에 미치는 영향을 확인할 수 있습니다. 선형 또는 첫 번째 터치 모델과 같은 보다 전통적인 속성 옵션을 제공하는 것 외에도, Adobe Analytics의 속성 은 머신 러닝 및 고급 통계 모델을 사용하여 모든 터치의 정확한 영향을 파악합니다.

자세한 내용은 [속성 모델 및 전환 확인 기간](/help/analyze/analysis-workspace/attribution/models.md).


### 예측 분석

예측 분석은 머신 러닝 및 고급 통계 모델링을 사용하여 고객 데이터를 분석하고, 패턴을 찾고, 이탈 또는 전환 가능성과 같은 향후 행동을 예측합니다. 이를 통해 데이터 분석가는 낭비될 수 있는 대용량 데이터 세트를 활용할 수 있습니다.

Adobe Analytics의 다음 주요 기능은 이러한 예측 기능을 제공합니다.

* [이상 현상 발견](#anomaly-detection)

* [기여도 분석](#contribution-analysis)

* [지능형 경고](#intelligent-alerts)

## Adobe Analytics 사용을 위한 사전 요구 사항

Adobe Analytics을 사용하려면 먼저 다음을 수행해야 합니다.

* 유효한 Adobe Analytics 라이선스

  Adobe Analytics에는 사이트 라이선스가 필요합니다. 자세한 내용은 Adobe 계정 담당자에게 문의하십시오. <!--is this phrased correctly? Is this important? -->

* 지원되는 브라우저

  Adobe Analytics에 액세스하는 각 사용자는 지원되는 브라우저를 사용해야 합니다. 자세한 내용은 [Adobe Analytics 시스템 요구 사항](https://experienceleague.adobe.com/docs/analytics/analyze/admin-overview/sys-reqs.html?lang=en).

<!-- are there more? -->

## Analytics 인터페이스 이해

Adobe Analytics 인터페이스는 다음 기본 영역으로 구성됩니다.

### 작업 영역 탭

다음 [!UICONTROL 작업 영역] 탭에는 Analysis Workspace 프로젝트 목록이 표시됩니다.

1. Adobe Analytics에서 [!UICONTROL **작업 영역**] 탭.

   ![작업 영역 탭](assets/landing-all2.png)

에서 사용할 수 있는 기능 및 기능에 대한 자세한 내용은 [!UICONTROL 작업 영역] 탭, 참조 [Adobe Analytics 랜딩 페이지](/help/analyze/landing.md).

### 보고서 탭

2023년 12월 31일부로 Adobe는 Reports &amp; Analytics 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다.

대신 [!UICONTROL **보고서**] 왼쪽 레일의 영역 [!UICONTROL **작업 영역**] 탭. 자세한 내용은 *보고서 탭 탐색* 위치: [Adobe Analytics 랜딩 페이지](/help/analyze/landing.md).

### 구성 요소 탭

다음 [!UICONTROL 구성 요소] 탭에는 데이터 분석을 세부적으로 조정하고 강화하는 데 도움이 되는 기능이 포함되어 있습니다.

1. Adobe Analytics에서 [!UICONTROL **구성 요소**] 탭을 선택한 다음 를 선택합니다 [!UICONTROL **모든 구성 요소**].

   ![작업 영역 탭](assets/components-tab.png)

2. 다음 제품 기능 중 하나를 선택하여 구성합니다.


   | 제품 기능 | 함수 | 추가 정보 |
   |---------|----------|----------|
   | 세그먼트 | Adobe Analytics를 사용하여 강력한 집중 대상 세그먼트를 작성하고 관리하고 공유하고 Analytics 기능, Adobe Experience Cloud, Adobe Target 및 기타 통합 Adobe 제품을 통해 보고서에 적용할 수 있습니다. | [Analytics 세그먼테이션](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=ko-KR) |
   | 계산된 지표 | 계산 및 고급 계산(또는 파생) 지표는 기존 지표에서 만들 수 있는 사용자 지정 지표입니다.  이 도구를 사용하는 마케터, 제품 관리자 및 분석가는 Analytics 구현을 변경하지 않아도 데이터에 대해 질문할 수 있습니다. | [계산 및 고급 계산(파생) 지표](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/cm-overview.html?lang=en) |
   | 날짜 범위 | Analysis Workspace에는 사용자가 분석을 작성할 때 사용할 수 있는 기본 날짜 범위 목록이 포함되어 있습니다. 또한 사용자 지정 날짜 범위를 만들어 Analysis Workspace의 사용자가 사용할 수 있도록 할 수 있습니다. | [사용자 정의 날짜 범위 만들기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html?lang=ko) <!-- should create an article in the Components Guide for managing/creating date ranges. This article in the Tools Guide needs updating. --> |
   | 가상 보고서 세트 |  |  |
   | 경고 | 지능형 경고를 사용하면 경고를 더욱 세밀하게 제어할 수 있으며 예외 항목 탐지 기능이 경고 시스템과 통합됩니다. | [지능형 경고](https://experienceleague.adobe.com/docs/analytics/components/alerts/intellligent-alerts.html?lang=en) |
   | 타겟 | 대상을 사용하면 웹 사이트 성능을 측정하고 대상이 되는 목표를 기준으로 진행 상황을 추적할 수 있습니다. 대상을 만들 때 측정하려는 지표 또는 eVar을 선택하거나 선택한 지표에 대해 전체 사이트를 측정하도록 선택할 수 있습니다. <p>대상은 Reports &amp; Analytics의 일부입니다. Reports &amp; Analytics [서비스 종료 공지](https://express.adobe.com/page/6WnF8JK6IRDhf/)에 대해 자세히 알아보십시오.</p> | [타겟](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/targets.html?lang=en) |
   | 달력 이벤트 | 시간 경과에 따른 트렌드 보고서의 경우, 달력 이벤트를 그래픽으로 표시하고 캠페인이나 다른 이벤트가 사이트 트래픽, 매출 또는 기타 지표에 영향을 미치는지 여부를 확인할 수 있습니다. | [달력 이벤트](https://experienceleague.adobe.com/docs/analytics/components/t-calendar-event.html?lang=en) |
   | 주석 | 작업 영역의 주석을 사용하면 상황별 데이터 뉘앙스와 통찰력을 조직에 효과적으로 전달할 수 있습니다. 이를 통해 달력 이벤트를 특정 차원 및 지표에 연결할 수 있습니다. | [주석 관리](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/annotations/manage-annotations.html?lang=en) |
   | 분류 설정 | 분류 세트는 분류 및 규칙을 관리하는 단일 인터페이스를 제공합니다. <p>분류란 Analytics 변수 데이터를 카테고리별로 분류하여 보고서를 생성할 때 여러 다른 방법으로 데이터를 표시하는 방법입니다. 변수 값과 해당 값과 관련된 메타데이터 간의 관계를 설정합니다. 분류는 추적 코드, prop 및 eVar와 같은 대부분의 사용자 지정 차원에 사용할 수 있습니다.</p> | [분류 세트 개요](https://experienceleague.adobe.com/docs/analytics/components/classifications/sets/overview.html?lang=ko) |
   | 위치 | 클라우드 대상에서 Adobe Analytics 분류 데이터를 가져오려면 먼저 분류 데이터를 수집할 위치를 추가하고 구성해야 합니다. 위치를 생성, 편집 또는 삭제할 수 있습니다. | [위치 관리자](https://experienceleague.adobe.com/docs/analytics/components/locations/locations-manager.html?lang=en) |
   | 예약된 프로젝트 | 예약된 프로젝트를 관리할 때, 반복 프로젝트 일정을 편집하고 삭제할 수 있고, 검색 막대에서 또는 왼쪽 레일의 필터 옵션을 사용하여 일정을 검색할 수 있으며, 태그, 승인된 일정, 소유자 등으로 필터링할 수 있습니다. | [예약된 프로젝트](/help/components/scheduled-projects-manager.md) |
   | 책갈피 | 책갈피를 이용하여 가장 많이 사용하는 보고서에 액세스할 수 있습니다. 사용자가 만드는 책갈피는 Experience Cloud에 추가되고 Data Connectors와 같은 통합 기능에서 사용할 수 있습니다. <p>책갈피는 Reports &amp; Analytics의 일부입니다. Reports &amp; Analytics [서비스 종료 공지](https://express.adobe.com/page/6WnF8JK6IRDhf/)에 대해 자세히 알아보십시오. | [북마크 관리자](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/bookmarks.html?lang=en) |
   | 대시보드 | 대시보드는 지표를 시각화하고 데이터를 포함하는 대화형 분석 기능을 제공하기 위해 만들어집니다. 대시보드 내의 항목을 클릭하면 데이터를 빠르고 쉽게 세그먼트화하여 분석에서 정보를 가져올 수 있습니다. <p>대시보드는 Data Workbench의 일부입니다. Data Workbench에 대해 자세히 알아보기 [서비스 종료 공지](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=en). | [대시보드 관리자](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/dashboard-manage.html?lang=en) |
   | 예약된 보고서 | 관리자 수준 사용자는 조직 전체에서 예약된 보고서를 보고 관리할 수 있습니다. | [예약된 보고서 큐](https://experienceleague.adobe.com/docs/analytics/components/scheduled-reports-admin.html?lang=en) |
   | 보고서 설정 | 이러한 설정은 기존 Adobe Analytics 제품을 참조하며, Analysis Workspace 및 관련 구성 요소는 제외됩니다. Analysis Workspace 설정을 조정하려면 구성 요소 > 환경 설정으로 이동하십시오. |  |
   | 환경 설정 | 사용자가 만드는 모든 새 프로젝트 또는 패널에 대한 Analysis Workspace 및 관련 구성 요소의 설정을 관리합니다. 기존 프로젝트 및 패널은 영향을 받지 않습니다. | [기본 설정](/help/analyze/analysis-workspace/user-preferences.md) |

   {style="table-layout:auto"}

### [도구] 탭

도구 탭 ...

1. Adobe Analytics에서 [!UICONTROL **도구**] 탭을 선택한 다음 를 선택합니다 [!UICONTROL **모든 도구**].

   ![작업 영역 탭](assets/tools-tab.png)

2. 다음 제품 기능 중 하나를 선택하여 구성합니다.

   | 제품 기능 | 함수 | 추가 정보 |
   |---------|----------|----------|
   | Data Warehouse | Data Warehouse는 데이터를 필터링하여 실행할 수 있는 스토리지 및 사용자 정의 보고서에 대한 Analytics 데이터 사본을 의미합니다. <p>요청 관리자에서 요청을 보고, 복제하고, 요청의 우선순위를 변경할 수 있습니다.</p> | [Data Warehouse 요청 관리](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-requests-manage.html?lang=en) |
   | Activity Map | Activity Map은 시각적 오버레이를 사용하여 링크 활동의 등급을 매기고 실시간 분석 대시보드를 제공하여 웹 페이지의 대상 참여를 모니터링하도록 설계되었습니다. 고객 활동의 가속화를 시각적으로 식별하고, 마케팅 이니셔티브를 수치화하고, 대상의 요구 사항과 행동에 따라 작동하도록 다양한 보기를 설정할 수 있습니다. | [Activity Map 개요](https://experienceleague.adobe.com/docs/analytics/analyze/activity-map/activity-map.html?lang=ko) |
   | Recommendations Classic |  |  |
   | Search&amp;Promote |  |  |
   | 모바일 서비스 |  |  |
   | Analytics 대시보드 (모바일 앱) |  |  |
   | Report Builder |  |  |

   {style="table-layout:auto"}

### 관리 탭

관리 탭 ...

1. Adobe Analytics에서 [!UICONTROL **관리자**] 탭을 선택한 다음 를 선택합니다 [!UICONTROL **모든 관리자**].

   ![작업 영역 탭](assets/admin-tab.png)

## 관리자, 분석가 및 최종 사용자를 위한 시작하기

일반적인 조직에는 관리자, 분석가 및 최종 사용자의 3가지 유형의 Adobe Analytics 사용자가 있습니다.

관리자는 Adobe Analytics을 구현하고 구성합니다. 분석가는 Analysis Workspace을 사용하여 프로젝트를 설정하고 분석을 만듭니다. 그리고 최종 사용자는 자체 분석을 생성하거나 분석가와 협력하여 고객을 생성함으로써 고객에 대한 실용적인 통찰력을 얻을 수 있습니다.

아래 섹션을 확장하여 이러한 각 사용자가 Adobe Analytics을 시작하는 방법을 알아봅니다.

### 관리자용 시작하기

Analytics 관리자는 조직에 가장 적합한 구현 방법을 선택할 책임이 있습니다.

Adobe Analytics이 구현된 후 관리자는 분석가 및 최종 사용자가 Adobe Analytics에서 모든 가치를 얻을 수 있도록 다양한 구성 작업을 수행해야 합니다.

#### 수집해야 하는 데이터 유형 결정

Adobe Analytics을 사용하면 여러 채널 유형에서 데이터를 수집하고 결합하여 의미 있는 실시간 고객 인사이트를 제공할 수 있습니다.

다음은 데이터를 수집할 수 있는 지원되는 채널 중 일부입니다.

* 휴대폰

* 사물 인터넷

* TV

* 음성 도우미

* 커넥티드 카

* 기타(지원되는 새 채널이 정기적으로 추가됨)

다음 [구현 방법](https://experienceleague.adobe.com/docs/analytics/implementation/home.html) 선택하는 것은 수집할 수 있는 데이터의 유형을 결정합니다.

#### Adobe Analytics 구현

웹 사이트 또는 모바일 앱에서 Adobe Analytics을 구현할 때 다양한 구현 방법을 사용할 수 있습니다.

사용 가능한 각 방법에 대한 자세한 내용은 [Adobe Analytics 구현](https://experienceleague.adobe.com/docs/analytics/implementation/home.html).

| | 구현 방법 |
|---------|---------|
| **웹 사이트** | <ul><li>Web SDK 확장 프로그램 (권장)</li><li>Web SDK</li><li>Analytics 확장</li><li>이전 JavaScript</li></ul> |
| **모바일 앱** | <ul><li>Mobile SDK 확장 프로그램(권장)</li><li>Analytics 확장</li></ul> |

{style="table-layout:auto"}

#### Adobe Analytics 구성

Analytics 관리자는 조직의 사용자가 Adobe Analytics을 사용할 수 있도록 하기 전에 다음 작업을 완료해야 합니다.

| 작업 | 의도한 사용 | 추가 정보 |
|---------|----------|---------|
| 관리자 역할 정의 | Adobe Analytics는 다양한 유형의 관리자를 지원합니다 | [Adobe Analytics의 관리자 역할](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/admin-roles-in-analytics.html?lang=en) |
| 권한 정의 | Analytics 관리자는 Adobe Analytics, 보고서 세트 도구 및 Analytics 도구에 대한 Admin Console에서 제품 프로필을 할당해야 합니다. | [Admin Console의 Analytics 권한](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/summary-tables.html?lang=ko-KR) |
| 보고서 세트 설정 및 회사에 대한 설정 정의 | 보고서 세트는 Adobe Analytics이 보고서를 생성하는 데 사용하는 데이터의 사일로입니다.<p>관리자는 을 설정할 수도 있습니다 [가상 보고서 세트](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=ko-KR) 추가 세그먼트 데이터.</p> | <ul><li>[보고서 세트 만들기](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/c-new-report-suite/t-create-a-report-suite.html?lang=en)</li><li>[회사 설정 개요](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/c-company-settings.html?lang=en)</li></ul> |
| 데이터 가져오기 | Adobe Analytics 데이터 소스를 사용하면 보고를 위해 추가 온라인 또는 오프라인 데이터를 가져올 수 있습니다. | [데이터 소스 개요](https://experienceleague.adobe.com/docs/analytics/import/data-sources/overview.html?lang=en) |
| 분류를 사용하여 데이터 분류 | 분류를 사용하면 변수를 더 잘 활용하도록 데이터를 분류하여 더 많은 콘텐츠를 단일 변수에 포함할 수 있습니다. | |
| 구성 요소 관리 | 각 구성 요소 유형의 데이터 사전 및 관리 영역을 사용하여 Analytics 구현에서 사용할 수 있는 구성 요소와 조직에 대해 승인된 구성 요소를 정의합니다.<p>구성 요소가 조직에서 효과적으로 사용되고 있는지 확인하기 위해 진행 중인 활동이어야 합니다. </p> | <ul><li>[데이터 사전 개요](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.html?lang=ko)</li><li>[계산된 지표 관리자](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=en)</li><li>[세그먼트 관리](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=ko)</li><li>[사용자 지정 날짜 범위 만들기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html?lang=ko)</li></ul> |
| 예외 항목 탐지 및 기여도 분석 | | |
| 고급 세분화 | | |
| Audience Manager에 대상 게시 | | |
| 기여도 분석 | | |
| 보고 활동 관리자 | | |
| 통합 | Adobe Analytics의 다른 응용 프로그램에서 정보를 표시할 수 있습니다. <p>다음은 몇 가지 일반적인 통합입니다.</p><ul><li><a href="https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=en">Target용 Analytics</a></li><li><a href="https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html?lang=ko-KR">미디어 분석</a></li> | |

{style="table-layout:auto"}

### 분석가를 위한 시작하기

조직의 모든 사람이 Adobe Analytics을 사용하여 웹 사이트 및 앱 전반에서 고객 행동에 대한 실용적인 통찰력을 얻을 수 있지만 Adobe Analytics은 데이터 분석가를 염두에 두고 설계되었습니다.

다음은 분석가가 Adobe Analytics 및 Analysis Workspace의 모든 기능을 활용하기 위해 숙지해야 하는 주요 작업 및 기능입니다.

| 기능 | 의도한 사용 | 추가 정보 |
|---------|----------|---------|
| Analysis Workspace에서 프로젝트 빌드 및 공유 | Analysis Workspace는 신속하게 분석을 빌드하고 인사이트를 공유할 수 있는 유연한 브라우저 도구입니다. 드래그하여 놓기 인터페이스를 사용하여 분석을 만들고 시각화를 추가하여 데이터를 생동감 있게 표현하고 데이터 세트를 조정하며 조직 내 누구와도 프로젝트를 공유 및 예약할 수 있습니다.<p>데이터 분석가는 종종 조직 내 사용자를 위해 Analysis Workspace에서 프로젝트를 만들 책임이 있습니다.</p><p>프로젝트가 생성되면 분석가는 해당 프로젝트를 와 공유합니다. [최종 사용자](#end-users)(비분석가) 데이터를 요청하고 해석 방법을 이해하는 데 도움을 주는 조직의 경우.</p> | <ul><li>[프로젝트 만들기](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md)</li><li>[프로젝트 공유](/help/analyze/analysis-workspace/curate-share/share-projects.md)</li></ul> |
| 기여도 분석 | 분석가는 Analysis Workspace에서 다양한 속성 모델과 전환 확인 기간을 사용하여 차원 항목이 성공 이벤트에 대한 크레딧을 받는 방법을 사용자 정의할 수 있습니다.<p>선형 속성 모델은 전환으로 이어지는 모든 터치 포인트에 동일한 크레딧을 제공하는 반면, 첫 번째 터치는 첫 번째 터치 포인트에 전체 크레딧을 제공합니다. 통계적 기법을 사용하여 크레딧의 최적 할당을 동적으로 결정하는 알고리즘 모델을 포함하여 다른 많은 속성 모델을 사용할 수 있습니다. </p> | [속성 모델 및 전환 확인 기간](/help/analyze/analysis-workspace/attribution/models.md) |
| 이상 현상 발견 | Analysis Workspace의 통계 모델링은 지표를 분석하고 값의 하한, 상한 및 예상 범위를 확인하여 데이터에서 예기치 않은 트렌드를 자동으로 찾습니다. 예상치 않은 급등이나 하락이 발생하면 보고서에 경고가 표시됩니다. | [예외 항목 탐지 개요](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) |
| 기여도 분석 | Analysis Workspace을 사용하여 데이터 내에서 숨겨진 패턴을 발견하여 통계적 예외 항목을 설명하고 대상 세그먼트 전반에 걸쳐 지표에 대한 예상치 못한 고객 작업, 범위를 벗어나는 값, 갑작스러운 급증 또는 급감 뒤의 상관 관계를 식별합니다. | [기여도 분석 개요](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md) |
| 지능형 경고 | 데이터 예외 항목 및 하나의 경고에서 여러 지표를 캡처하는 &quot;누적된&quot; 경고를 기반으로 경고를 생성하고 관리합니다. | [지능형 경고 개요](help/analyze/analysis-workspace/c-intelligent-alerts/intellligent-alerts.md) |
| 데이터 내보내기 | Data Warehouse 및 데이터 피드를 사용하면 Google Cloud Platform, Azure RBAC, Azure SAS 및 Amazon S3와 같은 다양한 클라우드 대상으로 데이터를 내보낼 수 있습니다. | [Analytics 내보내기 안내서](https://experienceleague.adobe.com/docs/analytics/export/home.html?lang=ko-KR) |
| Activity Map | Activity Map은 시각적 오버레이를 사용하여 링크 활동의 등급을 매기고 실시간 분석 대시보드를 제공하여 웹 페이지에 대한 대상 참여를 모니터링하도록 설계된 Adobe Analytics 애플리케이션입니다.<p>Activity Map을 사용하면 고객 활동의 가속화를 시각적으로 식별하는 다양한 보기를 설정하고, 마케팅 이니셔티브를 수치화하고 대상의 필요 사항과 행동에 따라 대응할 수 있습니다.</p> | [Activity Map](https://experienceleague.adobe.com/docs/analytics/analyze/activity-map/activity-map.html) |
| Report Builder | Report Builder는 Microsoft Excel용 추가 기능입니다. Report Builder를 사용하면 Excel 워크시트에 삽입되는 Adobe Analytics 데이터에서 사용자 지정 요청을 작성할 수 있습니다. 요청은 워크시트의 셀을 동적으로 참조할 수 있으며, Report Builder의 데이터 표시 방식을 업데이트하고 사용자 지정할 수 있습니다. | [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/home.html) |

{style="table-layout:auto"}

<!-- * Realtime reporting? -->

### 최종 사용자용 시작하기

전문 분석가가 아닌 최종 사용자는 조직의 분석가와 협력하여 Adobe Analytics 및 Analysis Workspace의 모든 기능을 활용하거나, 고객에 대한 실용적인 통찰력을 얻기 위해 Analysis Workspace의 기본 사항을 배울 수 있습니다.

#### 분석가 작업

일반적으로 다양한 사이트에서 고객 행동에 대해 자세히 알고 싶은 조직의 사용자는 전문 분석가가 아닙니다.

이상적으로 이러한 사용자는 [분석가](#analysts) 조직 내에서 다음을 수행합니다.

1. 분석가가 고객에 대해 학습하기를 바라는 사항을 설명하여 분석에 대한 요구 사항을 정의합니다.

1. 분석을 검토하여 목표를 충족하는지 확인합니다.

1. 분석에서 얻은 데이터에 대해 논의합니다.

1. 시간이 지남에 따라 필요에 따라 분석을 수정합니다.

#### Analysis Workspace에서 분석 만들기

Adobe Analytics에서 실행 가능한 통찰력을 얻기 위해 데이터 분석가가 아니어도 됩니다.

일부 사용자는에 설명된 대로 데이터 분석가와 협력하여 Analysis Workspace에서 프로젝트를 설정하고 데이터를 해석하는 방법을 설명하는 것이 도움이 될 수 있습니다. [분석가 작업](#work-with-analysts); 다른 사용자는 프로젝트를 빌드하고 데이터 자체를 해석하는 데 익숙할 수 있습니다.

Analysis Workspace를 사용하면 신속하게 분석을 빌드하여 인사이트를 수집한 다음 해당 인사이트를 다른 사람과 공유할 수 있습니다. 드래그하여 놓기 브라우저를 사용하여 분석을 만들고, 시각화를 추가하여 데이터를 생동감 있게 표현하고, 데이터 세트를 조정하며, 원하는 누구와도 프로젝트를 공유 및 예약할 수 있습니다.

Analysis Workspace에서 분석을 만드는 방법에 대한 자세한 내용은 [Analysis Workspace 개요](/help/analyze/analysis-workspace/home.md).

### 개발자용 시작하기

[Analytics API를 사용하면 Adobe 서버를 직접 호출하여 사용자 인터페이스에서 수행할 수 있는 작업의 대부분을 수행할 수 있습니다.](https://developer.adobe.com/analytics-apis/docs/2.0/)

데이터에 대해 탐색하고 통찰력을 얻거나 중요한 질문에 답변이 되는 보고서를 생성할 수 있습니다. 세그먼트 생성 또는 계산된 지표와 같은 Adobe Analytics의 구성 요소를 관리할 수도 있습니다.

## 비디오 개요

Adobe Analytics 기본 사항에 대해 알아보려면 다음을 확인하십시오 *Adobe Analytics 소개 - Skill Builder 웨비나* 비디오입니다. 이 비디오는 데이터를 캡처하는 방법, 데이터가 Adobe Analytics로 전송되는 방법 및 Adobe Analytics에서 사용할 수 있는 시각화 기능에 대한 기본 사항을 소개합니다. 이 비디오에서는 데이터를 빌드, 배포, 수집 및 해석할 수 있는 기반을 제공하므로 수집된 데이터를 기반으로 실행 가능한 통찰력과 권장 사항을 제공할 수 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/27429/?quality=12)

사용할 도구에 대한 질문은 [어떤 Adobe Analytics 도구를 사용해야 합니까?](https://experienceleague.adobe.com/docs/analytics/analyze/admin-overview/which-analytics-tool.html)를 참조하십시오.

## Customer Journey Analytics 더 보기

Customer Journey Analytics는 Analysis Workspace의 강력한 기능을 Adobe Experience Platform의 데이터에 사용할 수 있는 Adobe의 차세대 Analytics 솔루션입니다. 데이터 분류, 필터링, 쿼리 및 시각화 작업을 할 수 있으며, 모든 종류의 데이터 스키마와 유형을 보유할 수 있는 플랫폼의 기능과 결합되어 있습니다.

다음은 Adobe Analytics에 대한 Customer Journey Analytics의 이점 중 일부입니다.

* **제한 없는 변수 및 이벤트**: eVar, 속성 및 이벤트에 대한 개념이 더 이상 없습니다. 데이터는 주로 차원과 지표에 중점을 둡니다. 데이터 세트의 고유한 차원과 지표 수는 제한이 없습니다.

* **무제한 고유 값**: Adobe Experience Platform은 고유한 제한 사항으로 제한되지 않습니다.

* **이전 데이터 변경**: Adobe Experience Platform을 사용하여 데이터를 제거하거나 수정할 수 있습니다.

* **크로스 보고서 세트 데이터**: 여러 데이터 세트의 기존 구현을 Platform에 결합할 수 있습니다.

자세한 내용은 [Customer Journey Analytics 개요](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=ko).

