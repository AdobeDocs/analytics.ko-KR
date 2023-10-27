---
description: Adobe Analytics에 대한 일반적인 개요 정보입니다. Analytics 인터페이스에 대한 정보와 관리자, 분석가, 사용자 및 개발자를 위한 시작 정보가 포함됩니다.
title: 관리자, 분석가, 최종 사용자 및 개발자용 시작하기
feature: Analytics Basics
exl-id: 11800de5-224a-4bd2-8cb1-a6318925db71
source-git-commit: d64f6687dd6e6f688d332926e6d90fa699cac968
workflow-type: tm+mt
source-wordcount: '1891'
ht-degree: 100%

---

# 관리자, 분석가, 최종 사용자 및 개발자용 시작하기

일반적인 조직에는 4가지 유형의 Adobe Analytics 사용자가 있습니다.

* **관리자:** Adobe Analytics를 구현하고 구성합니다.

* **분석가:** Analysis Workspace를 사용하여 프로젝트를 설정하고 분석을 생성합니다.

* **최종 사용자:** 자체 분석을 생성하거나 분석가와 협력하여 분석을 생성함으로써 고객에 대한 실행 가능한 인사이트를 얻습니다.

* **개발자:** Adobe Analytics 2.0 API를 사용하여 Adobe 서버를 직접 호출함으로써 탐색할 보고서를 작성하거나, 통찰력을 얻거나, 데이터에 대한 중요한 질문에 대해 답변하는 등 사용자 인터페이스에서 수행할 수 있는 거의 모든 작업을 수행합니다.

아래 정보는 이러한 각 사용자가 Adobe Analytics를 시작하는 방법에 대한 간략한 설명을 제공합니다.

## 관리자용 시작하기

Analytics 관리자는 조직에 가장 적합한 구현 방법을 선택합니다.

Adobe Analytics가 구현된 후 관리자는 분석가와 최종 사용자가 Adobe Analytics에서 최대한의 가치를 얻을 수 있도록 다양한 구성 작업을 수행해야 합니다. 또한 관리자는 정기적으로 Analytics 환경을 모니터링하여 시스템이 효율적으로 실행되는지 확인해야 합니다.

### 수집해야 하는 데이터 유형 결정

Adobe Analytics를 사용하면 여러 채널 유형에서 데이터를 수집하고 통합하여 의미 있는 실시간 고객 인사이트를 제공할 수 있습니다.

다음은 데이터를 수집할 수 있도록 지원되는 몇 가지 채널입니다.

* 휴대폰

* 사물 인터넷

* TV

* 음성 지원 디바이스

* 연결된 자동차

* 등 (새 지원 채널이 정기적으로 추가됨)

선택한 [구현 방법](https://experienceleague.adobe.com/docs/analytics/implementation/home.html)에 따라 수집할 수 있는 데이터 유형이 결정됩니다.

### Adobe Analytics 구현

웹 사이트 또는 모바일 앱에서 Adobe Analytics를 구현할 때 다양한 구현 방법을 사용할 수 있습니다.

사용 가능한 각 방법에 대한 자세한 내용은 [Adobe Analytics 구현](https://experienceleague.adobe.com/docs/analytics/implementation/home.html)을 참조하십시오.

| | 구현 방법 |
|---------|---------|
| **웹 사이트** | <ul><li>Web SDK 확장 기능 (권장)</li><li>Web SDK</li><li>Analytics 확장 기능</li><li>기존 JavaScript</li></ul> |
| **모바일 앱** | <ul><li>Mobile SDK 확장 기능 (권장)</li><li>Analytics 확장 기능</li></ul> |

{style="table-layout:auto"}

### Adobe Analytics 구성

Analytics 관리자는 조직의 사용자가 Adobe Analytics를 사용할 수 있도록 설정하기 전에 다음 작업을 완료해야 합니다.

| 작업 | 용도 | 추가 정보 |
|---------|----------|---------|
| 관리자 역할 정의 | Adobe Analytics는 다양한 유형의 관리자를 지원합니다 | [Adobe Analytics의 관리자 역할](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/admin-roles-in-analytics.html?lang=ko) |
| 권한 정의 | Analytics 관리자는 Admin Console에서 Adobe Analytics, 보고서 세트 도구 및 Analytics 도구에 대해 제품 프로필을 할당해야 합니다. | [Admin Console의 Analytics 권한](/help/admin/admin-console/permissions/analytics-tools.md) |
| 보고서 세트 설정 및 회사에 대한 설정 정의 | 보고서 세트는 Adobe Analytics가 보고서를 생성하는 데 사용하는 데이터의 사일로입니다.<p>관리자는 [가상 보고서 세트](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html?lang=ko)를 설정하여 데이터를 더욱 세분화할 수도 있습니다.</p> | <ul><li>[보고서 세트 만들기](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/c-new-report-suite/t-create-a-report-suite.html?lang=ko)</li><li>[회사 설정 개요](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/company-settings/c-company-settings.html?lang=ko)</li></ul> |
| 데이터 가져오기 | Adobe Analytics 데이터 소스를 사용하면 추가적인 온라인 또는 오프라인 데이터를 가져와서 보고에 사용할 수 있습니다. | [데이터 소스 개요](https://experienceleague.adobe.com/docs/analytics/import/data-sources/overview.html?lang=ko) |
| 분류를 사용하여 데이터 분류 | 분류를 사용하면 데이터를 분류하여 변수를 더 잘 활용할 수 있으므로 단일 변수에 더 많은 콘텐츠를 포함할 수 있습니다. | [분류 개요](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=ko) |
| 구성 요소 관리 | 각 구성 요소 유형에 대한 데이터 사전 및 관리 영역을 사용하여 Analytics 구현에서 사용할 수 있는 구성 요소와 조직에 대해 승인된 구성 요소를 정의합니다.<p>이 활동은 구성 요소가 조직에서 효과적으로 사용되고 있는지 확인하기 위해 지속적으로 수행되어야 합니다. </p> | <ul><li>[데이터 사전 개요](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.html?lang=ko)</li><li>[계산된 지표 관리자](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=ko)</li><li>[세그먼트 관리](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=ko)</li><li>[사용자 정의 날짜 범위 만들기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html?lang=ko)</li></ul> |
| 예외 항목 탐지 | 예외 항목 탐지는 이전 데이터에 관해 주어진 지표가 변경되는 방법을 결정하는 통계적 방법을 제공합니다. | [예외 항목 탐지 개요](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html?lang=ko) |
| 기여도 분석 | 기여도 분석은 사용자 데이터 안에서 숨겨진 패턴을 발견하여 통계적 예외 항목을 설명하고 전체 수렴된 대상 세그먼트에서 선택된 지표에 대해 예상치 못한 고객 작업, 범위를 벗어나는 값, 급증 또는 급감 뒤의 상관관계를 식별합니다. | [기여도 분석 개요](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=ko) |
| Analytics 세분화 | 강력한 집중 대상자 세그먼트를 작성하고 관리하고 공유하고 Analytics 기능, Adobe Experience Cloud, Adobe Target 및 기타 통합 Adobe 제품을 사용하여 보고서에 적용할 수 있습니다. | [Analytics 세분화](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html?lang=ko) |
| Audience Manager에 대상자 게시 | Adobe Audience Manager는 자사, 세컨드 파티(파트너) 및 서드파티 데이터 통합에서 고유한 대상자 프로필을 빌드할 수 있도록 지원하는 강력한 데이터 관리 플랫폼입니다. | [Audience Analytics 개요](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=ko) |
| 통합 | Adobe Analytics에서 다른 애플리케이션의 정보를 표시할 수 있습니다. <p>다음은 몇 가지 일반적인 통합입니다.</p><ul><li><a href="https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=ko">Target용 Analytics</a></li><li><a href="https://experienceleague.adobe.com/docs/media-analytics/using/media-overview.html?lang=ko">미디어 분석</a></li> | [Analytics 통합](https://experienceleague.adobe.com/docs/analytics/integration/home.html?lang=ko) |

{style="table-layout:auto"}

### Adobe Analytics 모니터링

Adobe Analytics 환경을 모니터링하는 데 도움이 되는 다양한 기능을 사용할 수 있습니다.

Analytics 관리자는 Analytics 환경의 중요한 측면을 모니터링하는 데 사용할 수 있는 다음 기능을 알고 있어야 합니다.

| 작업 | 용도 | 추가 정보 |
|---------|----------|---------|
| 보고 활동 관리자 | 보고 활동 관리자를 사용하면 조직의 각 보고서 세트에 대한 보고 용량을 확인할 수 있습니다. 보고 사용량에 대해 상세한 가시성을 제공하며, 최대 보고 시간 동안 발생할 수 있는 용량 문제를 쉽게 진단하고 해결할 수 있도록 해 줍니다. | [보고 활동 관리자](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/reporting-activity.html?lang=ko) |
| 서버 호출 사용량 | 서버 호출은 데이터를 처리할 수 있도록 Adobe 서버로 보내는 인스턴스로서, “히트” 또는 “이미지 요청”이라고도 합니다. 서버 호출 사용량 대시보드에서 서버 호출 사용량 데이터를 추적하고, 계약상 한도와 비교할 수 있습니다. 초과분을 방지하도록 경고를 설정할 수 있습니다. | [서버 호출 사용량 개요](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-call-usage/overage-overview.html?lang=ko) |
| 로그 파일 | 사용자가 로그인하는 시점, 사용자의 사용, 액세스, 보고서 세트 및 관리 변경을 확인하는 데 도움이 되는 로그 파일입니다. | [로그](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/logs.html?lang=ko) |

{style="table-layout:auto"}

## 분석가용 시작하기

조직 내 누구나 Adobe Analytics를 사용하여 웹 사이트 및 앱 전체에 걸쳐 고객 행동에 대한 실행 가능한 인사이트를 얻을 수 있지만, Adobe Analytics는 데이터 분석가를 염두에 두고 설계되었습니다.

다음은 분석가가 Adobe Analytics 및 Analysis Workspace의 전체 기능을 활용하기 위해 숙지해야 하는 주요 작업 및 기능입니다.

| 기능 | 용도 | 추가 정보 |
|---------|----------|---------|
| Analysis Workspace에서 프로젝트 빌드 및 공유 | Analysis Workspace는 신속하게 분석을 빌드하고 인사이트를 공유할 수 있는 유연한 브라우저 도구입니다. 드래그하여 놓기 인터페이스를 사용하여 분석을 만들고 시각화를 추가하여 데이터를 생동감 있게 표현하고 데이터 세트를 조정하며 조직 내 누구와도 프로젝트를 공유 및 예약할 수 있습니다.<p>데이터 분석가는 조직 내 사용자를 위해 Analysis Workspace에서 프로젝트를 생성하는 일을 담당합니다.</p><p>프로젝트가 생성된 후 분석가는 데이터를 요청한 조직 내 [최종 사용자](#end-users)(비분석가)와 해당 프로젝트를 공유하고 이를 해석하는 방법을 이해하도록 지원합니다.</p> | <ul><li>[프로젝트 만들기](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md)</li><li>[프로젝트 공유](/help/analyze/analysis-workspace/curate-share/share-projects.md)</li></ul> |
| 속성 | 분석가는 Analysis Workspace에서 다양한 속성 모델 및 전환 확인 창을 사용하여 차원 항목이 성공 이벤트에 대한 크레딧을 받는 방법을 사용자 정의할 수 있습니다.<p>선형 속성 모델은 전환으로 이어지는 모든 접점에 동일한 크레딧을 제공하는 반면, 첫 번째 터치는 첫 번째 접점에 전체 크레딧을 제공합니다. 통계 기법을 사용하여 최적의 크레딧의 최적 할당을 동적으로 결정하는 알고리즘 모델을 포함하여 다른 많은 속성 모델을 사용할 수 있습니다. </p> | [속성 모델 및 전환 확인 기간](/help/analyze/analysis-workspace/attribution/models.md) |
| 예외 항목 탐지 | Analysis Workspace의 통계 모델링은 지표를 분석하고 값의 하한, 상한 및 예상 범위를 분석하여 데이터에서 예상치 않은 범위를 자동으로 파악합니다. 예상치 않은 급등이나 하락이 발생하면 보고서에 경고가 표시됩니다. | [예외 항목 탐지 개요](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) |
| 기여도 분석 | Analysis Workspace를 사용하면 사용자 데이터 안에서 숨겨진 패턴을 발견하여 통계적 예외 항목을 설명하고 대상 세그먼트에서 지표에 대해 예상치 못한 고객 작업, 범위를 벗어나는 값, 급증 또는 급감 뒤의 상관관계를 식별할 수 있습니다. | [기여도 분석 개요](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md) |
| 지능형 경고 | 하나의 경고에서 여러 지표를 캡처하는 데이터 예외 항목 및 “누적된” 경고를 기반으로 경고를 만들고 관리합니다. | [지능형 경고 개요](/help/analyze/analysis-workspace/c-intelligent-alerts/intellligent-alerts.md) |
| 데이터 내보내기 | Data Warehouse 및 데이터 피드를 사용하면 Google Cloud 플랫폼, Azure RBAC, Azure SAS 및 Amazon S3와 같은 다양한 클라우드 대상으로 데이터를 내보낼 수 있습니다. | [Analytics 내보내기 안내서](https://experienceleague.adobe.com/docs/analytics/export/home.html) |
| Activity Map | Activity Map은 시각적 오버레이를 사용하여 링크 활동의 등급을 매기고 실시간 분석 대시보드를 제공하여 웹 페이지에 대한 대상자 참여를 모니터링하도록 설계된 Adobe Analytics 애플리케이션입니다.<p>Activity Map을 사용하면 고객 활동의 가속화를 시각적으로 식별하는 다양한 보기를 설정하고, 마케팅 이니셔티브를 수치화하고 대상의 필요 사항과 행동에 따라 대응할 수 있습니다.</p> | [Activity Map](https://experienceleague.adobe.com/docs/analytics/analyze/activity-map/activity-map.html) |
| Report Builder | Report Builder는 Microsoft Excel용 추가 기능입니다. Report Builder를 사용하면 Excel 워크시트에 삽입되는 Adobe Analytics 데이터에서 사용자 정의 요청을 작성할 수 있습니다. 요청은 워크시트의 셀을 동적으로 참조할 수 있으며, Report Builder의 데이터 표시 방식을 업데이트하고 사용자 정의할 수 있습니다. | [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/home.html) |

{style="table-layout:auto"}

<!-- * Realtime reporting? -->

## 최종 사용자용 시작하기

전문 분석가가 아닌 최종 사용자는 조직의 분석가와 협력하여 Adobe Analytics 및 Analysis Workspace의 전체 기능을 활용하거나 Analysis Workspace의 기본 사항을 학습하여 고객에 대한 실행 가능한 인사이트를 얻을 수 있습니다.

### 분석가와 협력

다양한 사이트에서 고객 행동에 대해 자세히 파악하고자 하는 조직 내 사용자는 일반적으로 전문 분석가가 아닙니다.

가장 좋은 방법은 이들 사용자가 조직 내 [분석가](#analysts)와 협력하여 다음과 같은 작업을 수행하는 것입니다.

1. 고객에 대해 파악하고자 하는 내용을 분석가에게 설명하여 분석 관련 요구 사항을 정의합니다.

1. 해당 분석을 검토하여 목표를 충족하는지 확인합니다.

1. 해당 분석에서 얻은 데이터에 대해 논의합니다.

1. 시간이 지나며 변경되는 필요에 따라 분석을 수정합니다.

### Analysis Workspace에서 분석 만들기

Adobe Analytics에서 실행 가능한 인사이트를 얻기 위해 데이터 분석가가 될 필요는 없습니다.

일부 사용자의 경우 [분석가와 협력](#work-with-analysts)에 설명된 대로 데이터 분석가와 협력하여 Analysis Workspace에서 프로젝트를 설정하고 데이터 해석 방법을 설명하는 것이 도움이 될 수 있습니다. 또는 프로젝트를 구축하고 데이터 자체를 해석하는 것이 편할 수도 있습니다.

Analysis Workspace를 사용하면 신속하게 분석을 빌드하여 인사이트를 수집한 다음 해당 인사이트를 다른 사람과 공유할 수 있습니다. 드래그하여 놓기 브라우저를 사용하여 분석을 만들고, 시각화를 추가하여 데이터를 생동감 있게 표현하고, 데이터 세트를 조정하며, 원하는 누구와도 프로젝트를 공유 및 예약할 수 있습니다.

Analysis Workspace에서 분석을 만드는 방법에 대한 자세한 내용은 [Analysis Workspace 개요](/help/analyze/analysis-workspace/home.md)를 참조하십시오.

## 개발자용 시작하기

[Analytics API를 사용하면 Adobe 서버를 직접 호출하여 사용자 인터페이스에서 수행할 수 있는 작업의 대부분을 수행할 수 있습니다.](https://developer.adobe.com/analytics-apis/docs/2.0/)

데이터에 대해 탐색하고 통찰력을 얻거나 중요한 질문에 답변이 되는 보고서를 생성할 수 있습니다. 세그먼트 생성 또는 계산된 지표와 같은 Adobe Analytics의 구성 요소를 관리할 수도 있습니다.
