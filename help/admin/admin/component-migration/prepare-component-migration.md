---
description: Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트를 마이그레이션하기 위해 준비하는 데 필요한 준비 사항에 대해 설명합니다.
title: Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트 마이그레이션 준비
feature: Admin Tools
exl-id: a9ff98dc-6568-428d-a8a8-faca5bc76a29
source-git-commit: 03120156e1ba70e50b265da788fa5997fd31c93e
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 14%

---

# Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트 마이그레이션 준비

에 설명된 대로 조직의 누군가가 프로젝트 마이그레이션을 시작하기 전에 [Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트 마이그레이션](/help/admin/admin/component-migration/component-migration.md), 다음 섹션을 완료합니다.

## 사전 요구 사항

프로젝트 및 관련 구성 요소를 마이그레이션할 준비가 되기 전에 먼저 다음을 수행해야 합니다.

* Adobe Analytics 보고서 세트 데이터를 Customer Journey Analytics에서 보려면 다음 방법 중 하나를 사용하여 데이터를 Adobe Experience Platform에 수집합니다.

  >[!NOTE]
  >
  >  WebSDK를 사용하여 데이터를 수집하는 경우 모든 스키마 필드를 수동으로 매핑해야 합니다. 매핑 프로세스에 대한 자세한 내용은 [Adobe Analytics에서 Customer Journey Analytics으로 구성 요소 및 프로젝트 마이그레이션](/help/admin/admin/component-migration/component-migration.md))


   * Adobe Analytics 소스 커넥터를 사용하려면 다음을 수행해야 합니다.

      * [Adobe Experience Platform 및 Customer Journey Analytics에 수집하기 위한 보고서 세트 설정](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html?lang=en#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

      * [데이터 수집 및 사용](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/analytics.html?lang=ko-KR)

   * WebSDK를 사용하려면 다음을 수행해야 합니다.

      * [Adobe Experience Platform 및 Customer Journey Analytics에 수집하기 위한 보고서 세트 설정](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html?lang=en#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

      * [Adobe Experience Platform Web SDK를 통해 데이터 수집](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk.html)

* 만들기 [연결](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html?lang=ko-KR) 및 [데이터 보기](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) 수집한 데이터 포함.

* Customer Journey Analytics의 사용자가 데이터가 매핑되는 데이터 보기에 프로비저닝되었는지 확인합니다.

  자세한 내용은 [Admin Console에서 권한 Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html?lang=en#customer-journey-analytics-permissions-in-admin-console) 위치: [Customer Journey Analytics 액세스 제어](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html).

  권한 탭은 Admin Console 각 제품 프로필의 일부입니다. 특정 제품 프로필에 사용자를 추가할 수 있습니다. 그 다음 특정 데이터 보기에 대한 권한을 할당하고 제품 프로필의 사용자에게 부여할 권한을 지정합니다.

* 구성 요소를 매핑할 방법을 조직으로 결정합니다.

  자세한 내용은 아래 섹션 을 참조하십시오. [구성 요소를 매핑할 방법을 조직으로 결정](#decide-as-an-organization-how-you-will-map-components).

## 마이그레이션에 포함된 내용 이해

다음 표에서는 마이그레이션에 포함된 프로젝트 및 구성 요소의 요소를 간략하게 설명합니다.

### 마이그레이션된 구성 요소

Dimension 및 지표는에 설명된 매핑 프로세스의 일부로 마이그레이션됩니다. [Adobe Analytics 프로젝트를 Customer Journey Analytics으로 마이그레이션](#migrate-adobe-analytics-projects-to-customer-journey-analytics).

Customer Journey Analytics에 아직 존재하지 않는 세그먼트, 날짜 범위 및 계산된 지표는 매핑된 차원 및 지표를 기반으로 세그먼트, 날짜 범위 및 계산된 지표에서 다시 만들어집니다.

|  | [마이그레이션됨] |
|---------|---------|
| **[소유자](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md)** | Dimension 및 지표: 아니요<p>세그먼트 및 날짜 범위: ![확인 표시](assets/Smock_Checkmark_18_N.svg)</p> |
| **[공유](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)** | Dimension 및 지표: 아니요<p>세그먼트 및 날짜 범위: 아니요</p> |
| **[설명](/help/analyze/analysis-workspace/components/add-component-descriptions.md)** | Dimension 및 지표: 아니요<p>세그먼트 및 날짜 범위: ![확인 표시](assets/Smock_Checkmark_18_N.svg)</p> |
| **[태그](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)** | Dimension 및 지표: 아니요<p>세그먼트 및 날짜 범위: 아니요</p> |
| **[속성(차원)](/help/analyze/analysis-workspace/attribution/overview.md)** | Dimension 및 지표: 아니요<p>세그먼트 및 날짜 범위: 아니요</p> |

{style="table-layout:auto"}

### 마이그레이션된 프로젝트 요소

|  | [마이그레이션됨] |
|---------|----------|
| **[날짜 범위](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md)** | ![확인 표시](assets/Smock_Checkmark_18_N.svg) |
| **[세그먼트](/help/components/segmentation/seg-overview.md)** | ![확인 표시](assets/Smock_Checkmark_18_N.svg) |
| **[빠른 세그먼트](/help/analyze/analysis-workspace/components/segments/quick-segments.md)** | ![확인 표시](assets/Smock_Checkmark_18_N.svg) |
| **[차원](/help/components/dimensions/overview.md)** | ![확인 표시](assets/Smock_Checkmark_18_N.svg) 자동 또는 수동으로 매핑됨 |
| **[지표](/help/components/metrics/overview.md)** | ![확인 표시](assets/Smock_Checkmark_18_N.svg) 자동 또는 수동으로 매핑됨 |
| **[패널](/help/analyze/analysis-workspace/c-panels/panels.md)** | ![확인 표시](assets/Smock_Checkmark_18_N.svg) |
| **[시각화](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)** | ![확인 표시](assets/Smock_Checkmark_18_N.svg) |
| **[소유자](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)** | ![확인 표시](assets/Smock_Checkmark_18_N.svg) 마이그레이션을 수행하는 사용자가 정의함 |
| **[큐레이션](/help/analyze/analysis-workspace/curate-share/curate.md)** | 아니요 |
| **[공유](/help/analyze/analysis-workspace/curate-share/share-projects.md)** | 아니요 |
| **[주석](/help/analyze/analysis-workspace/components/annotations/overview.md)** | 아니요 |
| **[폴더 구조](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md)** | 아니요 |
| **[설명](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)** | ![확인 표시](assets/Smock_Checkmark_18_N.svg) |
| **[태그](/help/analyze/landing.md)** | 아니요 |
| **[즐겨찾기](/help/analyze/landing.md)** | 아니요 |
| **[일정](/help/components/scheduled-projects-manager.md)** | 아니요 |
| **[예외 항목 탐지](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md)** | ![확인 표시](assets/Smock_Checkmark_18_N.svg) |

{style="table-layout:auto"}

## 오류를 일으키는 지원되지 않는 요소 이해

다음 시각화 및 패널은 Customer Journey Analytics에서 지원되지 않습니다. 이러한 요소가 마이그레이션 전에 프로젝트에 포함되면 마이그레이션에 실패하거나 프로젝트가 마이그레이션된 후 오류가 발생할 수 있습니다.

프로젝트를 Adobe Analytics으로 마이그레이션하기 전에 Customer Journey Analytics 프로젝트에서 이러한 요소를 제거하십시오. 마이그레이션이 실패하면 마이그레이션을 다시 시도하기 전에 이러한 요소를 제거하십시오.

### 지원되지 않는 시각화

* [맵](/help/analyze/analysis-workspace/visualizations/map-visualization.md)

### 지원되지 않는 패널

* [Analytics for Target (A4T)](/help/analyze/analysis-workspace/c-panels/a4t-panel.md)

* [세그먼트 비교](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

* [미디어 대상 평균 시간](/help/analyze/analysis-workspace/c-panels/average-minute-audience-panel.md)

* [다음 또는 이전 항목](/help/analyze/analysis-workspace/c-panels/next-previous.md)

* [페이지 요약](/help/analyze/analysis-workspace/c-panels/page-summary.md)

* [기여도 분석](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md)

## 구성 요소를 매핑할 방법을 조직으로 결정

>[!IMPORTANT]
>
>마이그레이션 프로세스는 Customer Journey Analytics의 구성 요소에 자동으로 매핑될 수 없는 Adobe Analytics 프로젝트의 구성 요소를 식별하며, 이러한 구성 요소를 수동으로 매핑할 수 있도록 해줍니다.
>
>**한 프로젝트에서 수행된 모든 매핑은 마이그레이션을 수행하는 사용자에 관계없이 전체 조직의 모든 향후 프로젝트에 적용됩니다. 이러한 매핑은 고객 지원 센터에 문의하는 경우를 제외하고는 수정하거나 취소할 수 없습니다.**
>
>따라서 프로젝트가 마이그레이션되기 전에 조직에서 차원과 지표를 매핑하는 방법을 결정하는 것이 중요합니다. 이렇게 하면 개별 관리자가 단일 프로젝트만 고려할 때 사일로에서 결정을 내리는 것을 방지할 수 있습니다.
>
>다음은 프로젝트에 차원 및 지표가 있을 경우 수동으로 매핑해야 하는 목록입니다. 마이그레이션 전에 이 목록을 검토하는 것이 좋습니다. 이러한 구성 요소가 프로젝트에 있는 경우 해당 구성 요소를 매핑할 Customer Journey Analytics 구성 요소를 결정하십시오.


### 수동으로 매핑해야 하는 Dimension

* averagepagetime
* pagetimeseconds
* singlepagevisits
* visitnumber
* timeprior
* timespent
* category
* connectiontype
* customerloyalty
* customlink
* downloadlink
* exitlink
* hitdepth
* hittype
* pathlength
* daysbeforefirstpurchase
* dayssincelastpurchase
* dayssincelastvisit
* identificationstate
* optoutreason
* persistentcookie
* returnfrequency
* searchenginenatural
* searchenginenaturalkeyword
* mobilecarrier
* monitorresolution
* surveybase
* mcaudiences
* tntbase
* targetraw


### 수동으로 매핑해야 하는 지표

* timespentvisit
* timespentvisitor
* 다시 로드
* bounces
* 튀김-
* pageevents
* pageviewspervisit
* orderspervisit
* averagepagedepth
* averagetimespentonsite
* exitlinkinstances
* customlinkinstance
* downloadlinkinstances
* darkvisitors
* singlepagevisits
* singlevaluevisits
* visitorhome
* visitorsmcvisid
* pagesnotfound
* 새 참여 횟수
* time_granularity
* concurrent_viewers_visitors
* concurrent_viewers_occurrences
* 장치
* 예상 사용자
* playback_time_spent_seconds
* playback_time_spent_minutes
* average_minute_audience_time_based
* average_minute_audience_media_time
* average_minute_audience_content_time
* video_length
* targetconversion
* targetimpression
