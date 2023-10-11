---
description: 보고 활동 관리자를 사용하여 최대 보고 시간 동안 용량 문제를 진단하고 해결하는 방법에 대해 알아봅니다.
title: 활동 관리자 보고
feature: Admin Tools
mini-toc-levels: 3
exl-id: f638c6a9-1c2c-4936-a787-281269f95afc
source-git-commit: 4da5da34518c3fb7350799c185faed789ef5a22b
workflow-type: tm+mt
source-wordcount: '1616'
ht-degree: 19%

---

# 보고 활동 관리자에서 보고 활동 보기

{{release-limited-testing}}

다음 [!UICONTROL 활동 관리자 보고] 최대 보고 시간 동안 보고 용량 문제를 신속하게 진단하고 해결할 수 있습니다.

주요 이점 및 권한 요구 사항을 포함하여 보고 활동 관리자에 대한 자세한 내용은 다음을 참조하십시오. [보고 활동 관리자 개요](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md).

## 모든 보고서 세트에 대한 보고 활동 보기 {#view-all-report-suites}

1. Adobe Analytics에서 **[!UICONTROL 관리자]** > **[!UICONTROL 활동 관리자 보고]**.

   활성화된 기본 보고서 세트 목록이 표시됩니다.

   ![보고서 대기열](/help/admin/admin/assets/reporting-activity1.png)

1. (선택 사항) 보고서 세트 목록을 검색하거나 필터링할 수 있습니다.

   * 검색 필드를 사용하여 특정 보고서 세트를 검색합니다. 보고서 세트 이름 또는 ID와 입력하는 대로 보고서 세트 업데이트 목록을 입력하십시오.

   * 다음 항목 선택 [!UICONTROL **필터**] 아이콘 ![필터 아이콘](assets/filter-icon.png) 필터 옵션 목록을 확장합니다. 다음을 기준으로 필터링할 수 있습니다. [!UICONTROL **즐겨찾기**] 또는 [!UICONTROL **상태**].

     보고서 세트를 즐겨찾기로 표시하려면 보고서 세트 이름 왼쪽에 있는 별 아이콘을 선택합니다.

     <!-- (does this option still exist?) 1. (Optional) Select **[!UICONTROL Refresh]** at the top-right to refresh the data. -->

1. 각 보고서 세트에 대한 사용률 정보를 봅니다. 열 머리글을 선택하여 해당 열을 기준으로 테이블을 정렬할 수 있습니다.

   다음 열을 사용할 수 있습니다.

   | UI 요소 | 설명 |
   | --- | --- |
   | **[!UICONTROL 보고서 세트]** | 기본 보고서 세트 (보고 활동을 모니터링 중인 기본 보고서 세트) |
   | **[!UICONTROL 가상 보고서 세트]** | 이 기본 보고서 세트에 공급되는 모든 가상 보고서 세트를 표시합니다. 가상 보고서 세트는 적용된 필터링 및 세분화의 추가적인 수준으로 인해 보고 요청을 더욱 복잡하게 합니다. 가상 보고서 세트에서 오는 모든 요청은 기본 보고서 세트에 결합됩니다.<p>예를 들어 5개의 가상 보고서 세트에서 10개의 요청이 들어오는 경우 기본 수준 보고서 세트의 요청 수는 50개입니다. 이러한 방식으로 매우 빠르게 용량에 도달할 수 있습니다. |
   | **[!UICONTROL 용량 활용성]** | 실시간으로 사용 중인 보고서 세트의 보고 용량의 비율입니다. <p>**참고** 사용 용량이 100%라고 해서 보고 요청 취소를 바로 시작해야 하는 것은 아닙니다. 평균 대기 시간이 적절하다면 100% 사용 용량은 적절할 수 있습니다. 반면에 100% 사용 용량은 큐에 있는 요청 수가 증가하는 경우에도 문제를 시사할 수 있습니다.</p> |
   | **[!UICONTROL 대기 중인 요청]** | 처리 대기 중인 요청 수입니다. <!-- ??? --> |
   | **[!UICONTROL 대기열 대기 시간]** | 요청 처리를 시작하기 전 평균 대기 시간입니다. <!-- ???? --> |
   | **[!UICONTROL 상태]** | 가능한 상태는 다음과 같습니다. <ul><li>[!UICONTROL **활성**] (파란색): 보고서가 보고서 세트에서 실행되었으며 활동에 대해 모니터링 중입니다.</li><li>[!UICONTROL **비활성**] (회색): 보고서 세트에서 실행된 보고서가 없습니다. 이 상태는 보고서 세트를 처음 만들 때만 표시됩니다.</li></ul> |

   {style="table-layout:auto"}

## 단일 보고서 세트에 대한 보고 활동 보기

1. Adobe Analytics에서 [!UICONTROL **관리자**] > [!UICONTROL **활동 관리자 보고**].

1. 세부 정보를 보려는 보고서 세트의 연결된 제목을 선택합니다.

   선택한 보고서 세트에 대한 보고 활동 데이터가 표시됩니다.

   <!-- Need to update this screenshot: ![report suite](assets/indiv-report-ste.png) -->

1. 사용 가능한 그래프 및 표를 사용하여 보고서 세트의 보고 활동을 이해합니다.

   * [그래프 보기](#view-graphs)

   * [테이블 보기](#view-table)

### 그래프 보기

다음 그래프를 사용하여 보고서 세트에서 발생하는 활동을 더 잘 이해할 수 있습니다.

그래프가 표시되지 않으면 [!UICONTROL **그래프 표시**] 단추를 클릭합니다.

#### 활용률 그래프 {#utilization}

활용률 그래프는 선택한 보고서 세트에 대한 지난 2시간 동안의 보고 활용률을 보여 줍니다.

차트 위로 마우스를 가져가면 해당 분 동안 사용 용량 비율이 가장 높았던 시점을 확인할 수 있습니다.

* **X축**: 지난 2시간 동안의 보고 사용 용량입니다.
* **Y축**: 분 단위 보고 사용 용량 백분율.

  ![활용성 그래프](assets/utilization-graph.png)

#### 고유 사용자 그래프

[고유 사용자] 그래프는 선택한 보고서 세트에 대한 지난 2시간 동안의 보고 활동을 보여 줍니다.

차트 위로 마우스를 가져가면 해당 분 동안 최대 사용자 수가 가장 많았던 시점을 볼 수 있습니다.

* **X축**: 지난 2시간 동안의 보고 활동입니다.
* **Y축**: 보고 요청을 한 사용자의 분당 수입니다.

  ![고유 사용자 그래프](assets/distinct-users-graph.png)

<!--

#### Requests graph

The Requests graph shows the number of processed and completed requests for the selected report suite over the last 2 hours. 

Hover over the chart to view points in time where the maximum number of requests was highest for that minute.

* **X-axis**: The number of processed and completed requests over the last 2-hour time frame.
* **Y-axis**: The number of processed requests (in purple) and completed requests (in green), by minute.

   ![Distinct Users graph](assets/requests-graph.png)

#### Queueing graph

The Queueing graph shows the average queue wait time (in seconds) for reporting requests for the selected report suite over the last 2 hours. 

Hover over the chart to view points in time where the maximum average wait time was highest for that minute.

* **X-axis**: The average queue wait time for reporting requests over the last a 2-hour time frame.
* **Y-axis**: The average wait time (in seconds).

   ![Distinct Users graph](assets/queueing-graph.png)

-->

### 테이블 보기 {#view-table}

데이터 테이블 상단에서 다음 탭 중 하나를 선택하여 데이터를 보도록 선택할 수 있습니다. [!UICONTROL **요청**], [!UICONTROL **사용자**], [!UICONTROL **프로젝트**], 또는 [!UICONTROL **애플리케이션**].

>[!TIP]
>
>다음을 선택할 수 있습니다. [!UICONTROL **그래프 숨기기**] 테이블만 표시합니다.

![표 탭](assets/indiv-report-ste-table-tabs.png)

#### 요청별 데이터 보기

다음을 선택하면 [!UICONTROL **요청**] 탭에서 테이블에서 사용할 수 있는 열은 다음과 같습니다.

| 열 | 설명 |
| --- | --- |
| [!UICONTROL **요청 ID**] | 문제 해결을 위해 사용할 수 있습니다. |
| [!UICONTROL **타임런**] | 요청이 실행된 시간입니다. |
| [!UICONTROL **시작 시간**] | 요청의 처리가 시작된 시기(관리자의 현지 시간 기준). |
| [!UICONTROL **대기 시간**] | 요청이 처리되기 전에 대기한 시간입니다. 이 값은 일반적으로 용량이 충분할 때 &quot;0&quot;입니다. |
| [!UICONTROL **애플리케이션**] | [!UICONTROL 보고 활동 관리자]에서 지원하는 애플리케이션은 다음과 같습니다. <ul><li>Analysis Workspace UI</li><li>Workspace 예약된 프로젝트</li><li>Report Builder</li><li>빌더 UI: 세그먼트, 계산된 지표, 주석, 대상자 등</li><li>1.4 또는 2.0 API의 API 호출</li><li>지능형 경고</li></ul> |
| [!UICONTROL **사용자**] | 요청을 시작한 사용자입니다. <p>**참고:** 이 열의 값이 [!UICONTROL **인식되지 않음**]&#x200B;즉, 사용자가 관리 권한이 없는 로그인 회사에 있습니다.</p> |
| [!UICONTROL **프로젝트**] | 저장된 Workspace 프로젝트 이름, API 보고서 ID 등입니다. (메타데이터는 다양한 애플리케이션에 따라 다를 수 있습니다.) |
| [!UICONTROL **상태**] | 상태 표시기: <ul><li>**실행 중**: 현재 요청을 처리 중입니다.</li><li>**보류 중**: 요청이 처리되기를 대기하고 있습니다.</li></ul> |
| [!UICONTROL **복잡성**] | 모든 요청을 처리하는 데 동일한 시간이 필요한 것은 아닙니다. 요청 복잡성은 요청을 처리하는 데 필요한 시간에 대한 일반적인 아이디어를 제공하는 데 도움이 될 수 있습니다. <p>가능한 값은 다음과 같습니다.</p> <ul><li>[!UICONTROL **낮음**]</li><li>[!UICONTROL **보통**]</li><li>[!UICONTROL **높음**]</li></ul>이 값은 다음 열의 값에 영향을 받습니다.<ul><li>[!UICONTROL **월 경계**]</li><li>[!UICONTROL **열**]</li><li>[!UICONTROL **세그먼트**]</li></ul> |
| [!UICONTROL **월 경계**] | 요청에 포함된 개월 수입니다. 월 경계가 많으면 요청의 복잡성이 증가합니다. |
| [!UICONTROL **열**] | 요청의 지표 및 분류 수입니다. 열이 많으면 요청의 복잡성이 증가합니다. |
| [!UICONTROL **세그먼트**] | 요청에 적용된 세그먼트 수입니다. 세그먼트가 많으면 요청의 복잡성이 증가합니다. |

{style="table-layout:auto"}

#### 사용자별 데이터 보기

다음을 선택하면 [!UICONTROL **사용자**] 탭에서 테이블에서 사용할 수 있는 열은 다음과 같습니다.

| 열 | 설명 |
| --- | --- |
| [!UICONTROL **사용자**] | 요청을 시작한 사용자입니다. 이 열의 값이 [!UICONTROL **인식되지 않음**]&#x200B;즉, 사용자가 관리 권한이 없는 로그인 회사에 있습니다. |
| [!UICONTROL **요청 수**] | 사용자가 시작한 요청 수입니다. |
| [!UICONTROL **프로젝트 수**] | 사용자와 연결된 프로젝트 수입니다. <!-- ??? --> |
| [!UICONTROL **애플리케이션**] | [!UICONTROL 보고 활동 관리자]에서 지원하는 애플리케이션은 다음과 같습니다. <ul><li>Analysis Workspace UI</li><li>Workspace 예약된 프로젝트</li><li>Report Builder</li><li>빌더 UI: 세그먼트, 계산된 지표, 주석, 대상자 등</li><li>1.4 또는 2.0 API의 API 호출</li><li>지능형 경고</li></ul> |
| [!UICONTROL **평균 복잡성**] | 사용자가 시작한 요청의 평균 복잡성입니다. <p>모든 요청을 처리하는 데 동일한 시간이 필요한 것은 아닙니다. 요청 복잡성은 요청을 처리하는 데 필요한 시간에 대한 일반적인 아이디어를 제공하는 데 도움이 될 수 있습니다.</p><p>이 열의 값은 다음 열의 값에 의해 결정되는 점수를 기반으로 합니다.</p><ul><li>[!UICONTROL **평균 월 경계**]</li><li>[!UICONTROL **평균 열**]</li><li>[!UICONTROL **평균 세그먼트**]</li></ul> |
| [!UICONTROL **평균 월 경계**] | 요청에 포함된 평균 개월 수입니다. 월 경계가 많으면 요청의 복잡성이 증가합니다. |
| [!UICONTROL **평균 열**] | 포함된 요청의 평균 지표 및 분류 수입니다. 열이 많으면 요청의 복잡성이 증가합니다. |
| [!UICONTROL **평균 세그먼트**] | 포함된 요청에 적용된 평균 세그먼트 수입니다. 세그먼트가 많으면 요청의 복잡성이 증가합니다. |

{style="table-layout:auto"}

#### 프로젝트별 데이터 보기

다음을 선택하면 [!UICONTROL **프로젝트**] 탭에서 테이블에서 사용할 수 있는 열은 다음과 같습니다.

| 열 | 설명 |
| --- | --- |
| [!UICONTROL **프로젝트**] | 쿼리가 시작된 프로젝트입니다. |
| [!UICONTROL **요청 수**] | 프로젝트와 연계된 요청 수입니다. |
| [!UICONTROL **사용자 수**] | 프로젝트와 연계된 사용자 수입니다. <!-- ??? --> |
| [!UICONTROL **애플리케이션**] | [!UICONTROL 보고 활동 관리자]에서 지원하는 애플리케이션은 다음과 같습니다. <ul><li>Analysis Workspace UI</li><li>Workspace 예약된 프로젝트</li><li>Report Builder</li><li>빌더 UI: 세그먼트, 계산된 지표, 주석, 대상자 등</li><li>1.4 또는 2.0 API의 API 호출</li><li>지능형 경고</li></ul> |
| [!UICONTROL **평균 복잡성**] | 프로젝트에 포함된 요청의 평균 복잡성입니다. <p>모든 요청을 처리하는 데 동일한 시간이 필요한 것은 아닙니다. 요청 복잡성은 요청을 처리하는 데 필요한 시간에 대한 일반적인 아이디어를 제공하는 데 도움이 될 수 있습니다.</p><p>이 열의 값은 다음 열의 값에 의해 결정되는 점수를 기반으로 합니다.</p><ul><li>[!UICONTROL **평균 월 경계**]</li><li>[!UICONTROL **평균 열**]</li><li>[!UICONTROL **평균 세그먼트**]</li></ul> |
| [!UICONTROL **평균 월 경계**] | 요청에 포함된 평균 개월 수입니다. 월 경계가 많으면 요청의 복잡성이 증가합니다. |
| [!UICONTROL **평균 열**] | 포함된 요청의 평균 지표 및 분류 수입니다. 열이 많으면 요청의 복잡성이 증가합니다. |
| [!UICONTROL **평균 세그먼트**] | 포함된 요청에 적용된 평균 세그먼트 수입니다. 세그먼트가 많으면 요청의 복잡성이 증가합니다. |

{style="table-layout:auto"}

#### 애플리케이션별 데이터 보기

다음을 선택하면 [!UICONTROL **애플리케이션**] 탭에서 테이블에서 사용할 수 있는 열은 다음과 같습니다.

| 열 | 설명 |
| --- | --- |
| [!UICONTROL **애플리케이션**] | 쿼리가 시작된 애플리케이션입니다. |
| [!UICONTROL **요청 수**] | 응용 프로그램과 연결된 요청 수입니다. |
| [!UICONTROL **사용자 수**] | 응용 프로그램과 연결된 사용자 수입니다. <!--???--> |
| [!UICONTROL **프로젝트 수**] | 응용 프로그램과 연결된 프로젝트 수입니다. <!--???--> |
| [!UICONTROL **평균 복잡성**] | 애플리케이션과 연결된 요청의 평균 복잡성입니다. <p>모든 요청을 처리하는 데 동일한 시간이 필요한 것은 아닙니다. 요청 복잡성은 요청을 처리하는 데 필요한 시간에 대한 일반적인 아이디어를 제공하는 데 도움이 될 수 있습니다.</p><p>이 열의 값은 다음 열의 값에 의해 결정되는 점수를 기반으로 합니다.</p>이 열의 값은 다음 열의 값에 의해 결정되는 점수를 기반으로 합니다.<ul><li>[!UICONTROL **평균 월 경계**]</li><li>[!UICONTROL **평균 열**]</li><li>[!UICONTROL **평균 세그먼트**]</li></ul> |
| [!UICONTROL **평균 월 경계**] | 요청에 포함된 평균 개월 수입니다. 월 경계가 많으면 요청의 복잡성이 증가합니다. |
| [!UICONTROL **평균 열**] | 포함된 요청의 평균 지표 및 분류 수입니다. 열이 많으면 요청의 복잡성이 증가합니다. |
| [!UICONTROL **평균 세그먼트**] | 포함된 요청에 적용된 평균 세그먼트 수입니다. 세그먼트가 많으면 요청의 복잡성이 증가합니다. |

{style="table-layout:auto"}

<!--

### Filter

You can filter the table by Application (see list in the table below), by User, and by Project.

![filter](/help/admin/admin/assets/filter.png)

### Summary Numbers {#summary}

![filter](/help/admin/admin/assets/summary_numbers.png)

The Summary Numbers show the following information:

| Summary Number | Description |
| --- | --- |
| [!UICONTROL **Users**] | The number of users that are currently sending reporting requests to this report suite. |
| [!UICONTROL **Projects**] | Workspace projects, Report Builder workbooks, etc.  | 
| [!UICONTROL **Queries**] | The number of queries currently running. |
| [!UICONTROL **Average Wait Time**] | The average wait time for all running queries.  |
| [!UICONTROL **Usage Capacity**] | The current usage capacity for this report suite. |

{style="table-layout:auto"}

-->

