---
description: 조직 전체에서 예약된 보고서를 보고 관리합니다.
title: 예약된 프로젝트 관리자
feature: Admin Tools
exl-id: 8bc8d983-f680-48fa-8483-694c87a9ae4c
source-git-commit: d4d0eeac4f1f29e4c68e80b6fa0fe987a1fb32b9
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 42%

---

# 예약된 프로젝트

예약된 Analysis Workspace 프로젝트는 **[!UICONTROL 구성 요소]** > **[!UICONTROL 예약된 프로젝트]**&#x200B;를 사용하여 Adobe Analytics에서 관리할 수 있습니다.

**[!UICONTROL 예약된 프로젝트]**&#x200B;에서 반복되는 프로젝트 일정을 편집하고 삭제할 수 있습니다.  [예약된 프로젝트 목록](#scheduled-project-list)에 특정 사용자가 만든 항목이 표시됩니다. 애플리케이션에서 사용자 계정이 비활성화된 경우 모든 예약된 배달이 중지됩니다.

![예약된 프로젝트 인터페이스](assets/scheduled-projects.png)

## 예약된 프로젝트 목록

예약된 프로젝트 목록 ➊에는 다음에 대한 열이 표시됩니다.

| 열 | 설명 |
| --- | --- |
| ![SelectBox](/help/assets/icons/SelectBox.svg) | 하나 이상의 예약된 프로젝트를 선택하면 예약된 프로젝트 인터페이스 하단에 파란색 작업 표시줄이 나타납니다. 자세한 내용은 [액션](#actions)을 참조하십시오. |
| ![Star](/help/assets/icons/Star.svg) | 예약된 프로젝트에 대해 ![별](/help/assets/icons/Star.svg)을(를) 선호하거나 ![StarOutline](/help/assets/icons/StarOutline.svg)을(를) 선호하지 않도록 선택하십시오. |
| **[!UICONTROL 예약 ID]** | 주로 디버깅을 위해 사용되는 ID입니다. |
| **[!UICONTROL 이름]** | 이 프로젝트의 이름.<br/>예약된 프로젝트에 대한 자세한 내용을 보려면 ![InfoOutline](/help/assets/icons/InfoOutline.svg)을(를) 선택하십시오.<br/>컨텍스트 메뉴를 열려면 ![자세히](/help/assets/icons/More.svg)를 선택하십시오. 이 메뉴에서 다음 작업을 수행할 수 있습니다.<ul><li>예약된 프로젝트 ![삭제](/help/assets/icons/Delete.svg) **[!UICONTROL 삭제]**</li><li>예약된 프로젝트에 대해 ![레이블](/help/assets/icons/Labels.svg) **[!UICONTROL 태그]**.</li><li>예약된 프로젝트에 대해 ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL 승인]**.</li><li>![FileCSV](/help/assets/icons/FileCSV.svg) **[!UICONTROL CSV 내보내기]**: 예약된 프로젝트를 CSV 파일로 내보냅니다.</li></ul> |
| **[!UICONTROL 소유자]** | 프로젝트를 만들고 소유하고 있는 사람입니다. |
| **[!UICONTROL 태그]** | (선택 사항) 태그 지정은 프로젝트를 구성하는 좋은 방법입니다. 모든 사용자는 태그를 만든 후 하나의 프로젝트에 하나 이상의 태그를 적용할 수 있습니다. 그렇지만 본인이 소유하거나 본인과 공유된 프로젝트에 대한 태그만 볼 수 있습니다. |
| **[!UICONTROL 다음으로 배달됨]** | 이 예약된 프로젝트의 수신자입니다. |
| **[!UICONTROL 만료 날짜]** | 일정 빈도에 관계없이 만료일은 최대 1년까지 설정할 수 있습니다. |
| **[!UICONTROL 빈도]** | 이 일정 프로젝트를 한 명 이상의 수신자에게 보낼 빈도. |
| **[!UICONTROL 실행 시간]** | 이 예약된 프로젝트를 보내고자 하는 하루 중의 시간 |
| **[!UICONTROL 쿼리 개수]** | 이 프로젝트에 대한 쿼리 개수 |
| **[!UICONTROL 가장 긴 날짜 범위]** | 예약된 프로젝트에 대해 정의된 가장 긴 날짜 범위입니다. 이 값은 성능 문제를 조사하는 데 적절할 수 있습니다. 자세한 내용은 [보고 활동 관리자](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md)를 참조하십시오. |
| **[!UICONTROL 쿼리 개수]** | 예약된 프로젝트에 대해 실행된 쿼리 수입니다. 이 값은 성능 문제를 조사하는 데 적절할 수 있습니다. 자세한 내용은 [보고 활동 관리자](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md)를 참조하십시오. |


![ColumnSetting](/help/assets/icons/ColumnSetting.svg)을(를) 사용하여 표시할 열을 구성할 수 있습니다.

![검색](/help/assets/icons/Search.svg)을 사용하여 예약된 프로젝트를 검색합니다. 필터 패널에서 필터가 적용되어 있는지 확인할 수도 있습니다. 필터를 제거하려면 필터에 대해 ![CrossSize75](/help/assets/icons/CrossSize75.svg)을(를) 선택하십시오. 모든 필터를 제거하려면 **[!UICONTROL 모두 지우기]**&#x200B;를 선택하십시오.

예약된 프로젝트를 편집하려면 예약된 프로젝트의 제목을 선택합니다. **[!UICONTROL 예약된 프로젝트 편집]** 대화 상자를 사용하여 일정 세부 정보를 업데이트합니다. 자세한 내용은 [다른 사용자에게 파일 보내기](../analyze/analysis-workspace/curate-share/t-schedule-report.md)를 참조하십시오.

![예약된 프로젝트 편집](assets/edit-scheduled-project.png)

**[!UICONTROL 업데이트]**&#x200B;를 선택하여 일정을 업데이트합니다.




## 액션

다음은 예약된 프로젝트 관리자의 일반적인 액션입니다. 하나 이상의 예약된 프로젝트를 선택할 때 컨텍스트 메뉴 또는 파란색 작업 표시줄에서 작업을 선택할 수 있습니다.

| 아이콘 | 액션 | 설명 |
|:---:|---|---|
| ![닫기](/help/assets/icons/Close.svg) | **[!UICONTROL *x *선택됨]** | 선택한 예약된 프로젝트를 선택 취소하려면 선택합니다. |
| ![삭제](/help/assets/icons/Delete.svg) | **[!UICONTROL 삭제]** | 프로젝트에 대해 선택한 예약된 프로젝트를 삭제합니다. 프로젝트는 삭제되지 않습니다. |
| ![레이블](/help/assets/icons/Labels.svg) | **[!UICONTROL 태그]** | 선택한 예약된 프로젝트에 태그를 지정합니다. **[!UICONTROL 예약된 프로젝트에 태그 지정]**&#x200B;에서 태그를 선택하고 **[!UICONTROL 저장]**&#x200B;을 선택하여 저장합니다. |
| ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg) | **[!UICONTROL 승인]** | 선택한 예약된 프로젝트를 승인합니다. |
| ![FileCSV](/help/assets/icons/FileCSV.svg) | **[!UICONTROL CSV로 내보내기]** | 선택한 예약된 프로젝트를 `Export Scheduled Projects List.csv`(이)라는 파일로 내보냅니다. |


## 필터

➌ 필터 패널을 사용하여 예약된 프로젝트 [예약된 프로젝트 목록](#scheduled-project-list)을(를) 필터링할 수 있습니다. 필터 패널을 표시하거나 숨기려면 ![필터](/help/assets/icons/Filter.svg)를 사용합니다.

필터 패널은 다음 섹션으로 구성되어 있습니다.

### 태그

| 태그 | 설명 |
|---|---|
| ![태그](/help/components/assets/scheduledprojects-filter-tags.png){width="300"} | **[!UICONTROL 태그]** 섹션에서는 태그를 필터링할 수 있습니다. <ul><li>![검색](/help/assets/icons/Search.svg) **[!UICONTROL 태그 검색]**&#x200B;을 사용하면 필터링할 태그를 검색할 수 있습니다.</li><li>둘 이상의 태그를 선택할 수 있습니다. 사용할 수 있는 태그는 필터 패널의 다른 섹션에서 선택한 내용에 따라 달라집니다.</li><li>숫자는 다음을 나타냅니다.<ul><li>⃣7︎: 특정 태그와 연결된 예약된 프로젝트 수입니다.</li></ul></li></ul> |


### 소유자

| 소유자 | 설명 |
|---|---|
| ![소유자](/help/components/assets/scheduledprojects-filter-owners.png){width="300"} | **[!UICONTROL 소유자]** 섹션에서는 소유자를 필터링할 수 있습니다. <ul><li>![검색](/help/assets/icons/Search.svg) *소유자 검색*&#x200B;을 사용하여 필터링할 소유자를 검색합니다.</li><li>둘 이상의 소유자를 선택할 수 있습니다. 사용할 수 있는 소유자는 필터 패널의 다른 섹션에서 선택한 내용에 따라 달라집니다.</li><li>숫자는 다음을 나타냅니다.<ul><li>⃣4︎: 특정 소유자와 연결된 예약된 프로젝트 수입니다.</li></ul></li></ul> |


### 기타 필터

| 기타 필터 | 설명 |
|---|---|
| ![기타 필터](/help/components/assets/scheduledprojects-filter-otherfilters.png){width="300"} | **[!UICONTROL 기타 필터]** 섹션에서는 미리 정의된 다른 필터를 필터링할 수 있습니다.<ul><li>다음 옵션 중 하나 이상을 선택할 수 있습니다.<ul><li> **[!UICONTROL 만료됨]**: 만료된 예약된 프로젝트를 필터링합니다.</li><li>**[!UICONTROL 실패]**: 예약에 실패한 예약된 프로젝트를 필터링합니다.</li></ul>선택할 수 있는 내용은 역할과 권한에 따라 달라집니다.</li><li>둘 이상의 기타 필터를 선택할 수 있습니다. 사용할 수 있는 기타 필터는 필터 패널의 다른 섹션에서 선택한 내용에 따라 달라집니다.</li><li>숫자는 다음을 나타냅니다.<ul><li>⃣4︎: 특정 다른 필터와 연결된 예약된 프로젝트 수입니다.</li></ul></li></ul> |


<!--
# Scheduled projects

Scheduled Analysis Workspace projects can be managed under **Analytics > Components > Scheduled Projects**.

When you manage scheduled projects, you can edit and delete recurring project schedules:

*  Change the file type (.csv or PDF)
*  Update the project description
*  Add or remove recipients
*  Change the frequency

To modify a scheduled project

1.  Select **Analytics > Components > Scheduled Projects**.
1.  Search for a schedule in the search bar or by using the filter options in the left rail. You can filter by [!UICONTROL Tags], [!UICONTROL Owners], [!UICONTROL Favorites], and more.

![Screenshot showing the scheduled projects list with the column displaying title, owner, tags, delivered to, and other columns described in the Available columns section.](assets/scheduled-project-manager2.png)

## Available columns

| Field | Description |
| --- | --- |
| [!UICONTROL Favorites] | Selecting the star icon makes this schedule a favorite. |
| [!UICONTROL Schedule ID] | This ID is used mainly for debugging purposes. |
| [!UICONTROL Title and description] | Title and description of this project. |
| [!UICONTROL Owner] | The person who created and owns the project. |
| [!UICONTROL Tags] | (optional) Tagging is a good way to organize projects. All users can create tags and apply one or more tags to a project. However, you can see tags only for those projects that you own or that have been shared with you.  |
| [!UICONTROL Delivered to] | The recipient(s) of this scheduled project. |
| [!UICONTROL Expiration date] | For any scheduled project frequency, you can set the expiration date for up to one year in the future. |
| [!UICONTROL Frequency] | How often you want to have this schedule project sent to the recipient(s). |
| [!UICONTROL Execution time] | At what time of day this scheduled project gets sent. |
| [!UICONTROL Number of queries] | The number of queries against this project. | 

## Common actions

The following are common actions in the Scheduled Projects manager:

|Action|Description|
|---|---|
|**[!UICONTROL Edit]**|Select the title of the schedule to update its delivery settings.|
|**[!UICONTROL Delete]**|Select the scheduled project in the list and then click Delete from the menu. This will delete the selected schedule for the project; the project itself will not be deleted.|
|**[!UICONTROL Tag]**|Select the scheduled project in the list and then choose "Tag" or "Approve" to organize your schedules and make them easier to search for.|
|**[!UICONTROL View failed schedules]**|Navigate to the left rail > Other filters > Failed to see schedules that have failed.|
|**[!UICONTROL View expired schedules]**|Navigate to the left rail > Other filters > Expired to see schedules that have expired. Click the title of the schedule to setup a new delivery schedule.|
|**[!UICONTROL View schedule ID]**|Navigate to column options in the top right and add the Schedule ID column to the table. The scheduled ID is often useful for debugging.|

The Scheduled Projects manager shows the items that a specific user created. If the user account is disabled in the application, all scheduled deliveries stop. Scheduled project ownership can be transferred to a new user under **Admin** > **Analytics Users & Assets** > **Transfer Assets**.
-->