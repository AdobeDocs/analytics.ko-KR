---
description: Analysis Workspace의 오류 및 문제 해결에 대해 알아봅니다.
title: Analysis Workspace 문제 해결 도중 오류 발생
feature: Workspace Basics
role: User, Admin
exl-id: e5c6f710-a205-48db-aeee-ee5b83c42795
source-git-commit: 0146d0798571d8589a74fb6d3fbbd574af224631
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 97%

---

# 오류 및 문제 해결

Analysis Workspace와 상호 작용할 때 기능 또는 성능에도 영향을 주는 오류가 발생할 수 있습니다. 다음은 가장 일반적인 오류 유형, 오류 발생 이유 및 적용할 수 있는 최적화의 목록입니다.

## 오류 메시지

Analysis Workspace를 사용할 때 다음과 같은 일반적인 오류 메시지가 표시될 수 있습니다.

| 오류 메시지 | 오류가 발생하는 이유는 무엇입니까? | 최적화 |
| --- | --- | --- |
| [!UICONTROL 데이터 보기에서 비정상적으로 많은 보고가 발생하고 있습니다. 나중에 다시 시도해 주십시오.] | 조직에서 특정 데이터 보기에 대해 너무 많은 동시 요청을 실행하려고 합니다. 이 오류에 기여하는 요소는 API 요청, 예약된 프로젝트, 예약된 보고서, 예약된 경고 및 보고 요청을 수행하는 동시 사용자입니다. | 데이터 보기에 대한 요청과 일정을 하루 전체에 더 고르게 분산시킵니다.<p>관리자는 보고 용량을 소모하는 [요청을 식별 및 취소하는 보고 활동 관리자](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md)를 사용할 수 있습니다.</p> |
| [!UICONTROL 이 보고서는 너무 복잡합니다. Analysis Workspace 보고서 작성을 위한 모범 사례를 검토하십시오.] | 보고 요청이 너무 커서 실행할 수 없습니다. 이 오류에 기여하는 요소는 요청의 복잡성으로 인해 발생하는 시간 초과입니다. | 요청을 단순화합니다. 예를 들어 날짜 범위를 단축하거나, 세그먼트 기준을 단순화하거나, 테이블의 일부 열이나 행을 제거합니다. 테이블을 별도 요청으로 분할할 수도 있습니다. |
| [!UICONTROL 현재 데이터 보기가 보고 용량을 초과하고 있습니다. 요청을 단순화하거나 나중에 다시 시도하십시오.] | 조직에서 특정 데이터 보기에 대해 너무 많은 동시 요청을 실행하려고 합니다. 이 오류에 기여하는 요소는 API 요청, 예약된 프로젝트 및 보고 요청을 수행하는 동시 사용자입니다. | 데이터 보기에 대한 요청과 일정을 하루 전체에 더 고르게 분산시킵니다. |
| [!UICONTROL 시스템 오류가 발생했습니다. **[!UICONTROL 도움말 > 지원 티켓 제출]**&#x200B;에서 고객 지원 요청을 로그하여 오류 코드를 포함하십시오.] | Adobe에서 해결해야 하는 문제가 발생했습니다. | 오류 코드를 고객 지원에 제출합니다. |
| [!UICONTROL 오류 500: 페이지 로드 실패] | 회사 [방화벽 설정](/help/technotes/ip-addresses.md)과 같이 로컬 네트워크에 있는 문제가 이 오류의 발생 요소입니다. Adobe에서 해결해야 하는 문제가 발생할 수도 있습니다. | 몇 분 후에 다시 로그인해 보십시오. 문제가 계속 발생하면 EIM 인스턴스 ID 코드를 고객 지원에 제출합니다. |
| [!UICONTROL 너무 많은 열 또는 사전 구성된 행으로 인해 요청에 실패했습니다.] | 테이블에 자유 형식 셀(행*열)이 너무 많습니다. | 테이블에서 일부 열 또는 행을 제거하거나 테이블을 별도 요청으로 분할해 보십시오. |


## 문제 해결

Analysis Workspace를 사용할 때 아래 정보를 사용하여 몇 가지 일반적인 문제를 해결할 수 있습니다.

| 문제 | 문제 해결 방법 |
|---|---|
| 지표를 드래그하면 *잘못된 데이터*&#x200B;라고 표시됩니다. | 잘못된 데이터는 Adobe가 보고서에 사용된 차원과 지표의 조합을 사용하여 데이터를 반환할 수 없음을 의미합니다. 예를 들어 서로 위에 스택된 두 개의 지표는 이런 식으로 두 개의 지표를 표시할 수 있는 방법이 없으므로 데이터로 반환되지 않습니다. 대신 지표를 나란히 배치합니다. |
| 지표를 드래그하면 실제 데이터가 표시되지 않고, 0만 표시됩니다. | Workspace 보고서를 만들었지만 데이터가 없다면 확인할 수 있는 몇 가지 사항이 있습니다.<ul><li>보고서에서 세그먼트를 적용했다면 세그먼트 기준이 데이터와 일치하지 않을 수 있습니다. 세그먼트를 제거하거나 세그먼트 정의를 조정해 보십시오.</li><li>오른쪽 상단의 날짜 범위를 확인하고 예상한 값으로 설정되어 있는지 확인합니다.</li><li>웹 사이트로 이동하고 [디버거](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html)를 사용하여 데이터가 수집되고 있는지 확인합니다.</li></ul> |



<!--
# Common error messages

You may encounter errors when interacting with Analysis Workspace that will also influence performance. Listed below are the most common error types, why they occur, and optimizations that can be made.

| Error message | Why does this occur? | Optimization |
| --- | --- | --- |
| [!UICONTROL The report suite is experiencing unusually heavy reporting. Please try again later.] | Your organization is trying to run too many concurrent requests against a specific report suite. Contributors to this error are API requests, scheduled projects, and concurrent users making reporting requests. | Spread your requests and schedules for the report suite more evenly throughout the day. <p>Administrators can use the [Reporting Activity Manager to identify and cancel requests](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md) that are consuming reporting capacity. |
| [!UICONTROL The report suite is currently exceeding its reporting capacity. Please simplify the request or try again later.] |  Your organization is trying to run too many concurrent requests against a specific report suite. Contributors to this error are API requests, scheduled projects, scheduled reports, scheduled alerts, and concurrent users making reporting requests. | Spread your requests and schedules for the report suite more evenly throughout the day. |
| [!UICONTROL A system error has occurred. Please log a Customer Care request under Help > Submit Support Ticket and include your error code.] | Adobe is experiencing an issue that needs to be resolved. | Submit the error code to Customer Care. |
| [!UICONTROL An unexpected error has occurred; try refreshing your project again. If the problem persists, please submit this error ID to Adobe Customer Care for further diagnosis.] | Adobe is experiencing an issue that needs to be resolved. | Try refreshing your project and if the problem persists, submit the error code to Customer Care. |
| [!UICONTROL Error 500: Failed to load page] | Issues with your local network, such as company [firewall settings](https://experienceleague.adobe.com/docs/analytics/technotes/ip-addresses.html), are a contributing factor to this error. Additionally, Adobe may be experiencing an issue that needs to be resolved. | Try logging in again after several minutes. If the issue persists, submit the EIM instance ID code to Customer Care. |
| [!UICONTROL One of the segments or the search in this visualization contains a text search that returned too many results.] | Your segment criteria or report filter is too broad. | Narrow your search text criteria and try the request again. |
| [!UICONTROL This dimension does not currently support non-default attribution models.] | Non-default attribution is not supported for the dimension that you are using. | Replace the dimension in your table with one that is compatible with [Attribution](/help/analyze/analysis-workspace/attribution/overview.md). |
| [!UICONTROL Your request failed as a result of too many columns or pre-configured rows.] | Your table has too many freeform cells (row * columns). | Remove columns or rows in your table, or consider splitting the table into separate requests. |
-->