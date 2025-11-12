---
description: 세그먼트 관리자를 사용하여 세그먼트 공유, 필터링, 태그 지정, 승인, 복사, 삭제 및 즐겨찾기로 세그먼트 표시 등의 세그먼트를 관리하는 방법을 이해합니다.
title: 세그먼트 관리
feature: Segmentation
exl-id: be182a55-23cb-415f-a7d0-3c1efeead1a1
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 63%

---

# 세그먼트 관리


중앙 [!UICONTROL 세그먼트] 관리 인터페이스에서 세그먼트를 [공유](t-seg-share.md), [세그먼트화](t-seg-filter.md), [태그 지정](seg-tag.md), [승인](seg-approve.md), 이름 바꾸기, [복사](seg-copy.md), 삭제, 내보내기하거나 세그먼트를 [즐겨찾기](t-seg-favorite.md)로 표시할 수 있습니다. 세그먼트 방법은 다음과 같습니다.

* 메인 인터페이스에서 **[!UICONTROL 구성 요소]**&#x200B;를 선택한 다음 **[!UICONTROL 세그먼트]**&#x200B;를 선택합니다.


>[!NOTE]
>
>특정 Workspace 프로젝트 내에서 만드는 빠른 세그먼트는 모든 프로젝트에서 사용할 수 있도록 설정하지 않은 한 [!UICONTROL 세그먼트] 관리자에 표시되지 않습니다.
>

## 세그먼트 관리자

세그먼트 관리자에는 다음 인터페이스 요소가 있습니다.

![세그먼트 인터페이스](assets/segments-manager.png)

### 세그먼트 목록

세그먼트 목록 ➊에는 사용자가 소유한 모든 세그먼트, 모든 프로젝트에 범위가 지정된 세그먼트, 사용자와 공유된 세그먼트가 표시됩니다. 목록은 다음과 같습니다.

| 열 | 설명 |
| --- | --- |
| ![StarOutline](/help/assets/icons/StarOutline.svg) | 세그먼트를 ![별](/help/assets/icons/Star.svg) 즐겨찾기에 추가할지 ![StarOutline](/help/assets/icons/StarOutline.svg) 추가하지 않을지 선택합니다. [세그먼트를 즐겨찾기로 표시](t-seg-favorite.md)를 참조하십시오. |
| **[!UICONTROL 제목 및 설명]** | 세그먼트를 편집하려면 제목 링크를 선택하여 [세그먼트 빌더](seg-build.md)를 엽니다. 공유된 세그먼트는 ![공유](/help/assets/icons/ShareAlt.svg)로 표시됩니다. |
| **[!UICONTROL 보고서 세트]** | 이 세그먼트가 적용되는 보고서 세트입니다. |
| **[!UICONTROL 소유자]** | 세그먼트 소유자입니다. 사용자가 소유한 세그먼트 또는 사용자와 공유된 주석만 표시합니다. |
| **[!UICONTROL 태그]** | 이 세그먼트의 태그입니다. |
| **[!UICONTROL 다음 사용자와 공유]** | 세그먼트를 공유한 개인 또는 그룹 수입니다. **[!UICONTROL 구성 요소 공유]** 대화 상자를 열지 선택합니다. 자세한 내용은 [세그먼트 공유](t-seg-share.md)를 참조하십시오. |
| **[!UICONTROL 게시됨]** | [세그먼트가 Experience Cloud에 게시되었는지 여부](seg-publish.md). |
| **[!UICONTROL 수정한 날짜]** | 세그먼트를 마지막으로 수정한 날짜 및 시간입니다. |

![ColumnSetting](/help/assets/icons/ColumnSetting.svg)을 사용하여 표시할 열을 지정합니다.

### 작업 표시줄

작업 모음 ➋을(를) 사용하여 세그먼트에 대해 작업을 수행할 수 있습니다. 작업 표시줄에는 다음 액션이 포함됩니다.

| 액션 | 설명 |
|---|---|
| ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL 추가]** | [세그먼트 빌더](seg-build.md)를 사용하여 다른 세그먼트를 추가하십시오. |
| ![검색](/help/assets/icons/Search.svg) [!UICONTROL *제목별 검색*] | 세그먼트가 목록에서 선택되지 않은 경우 이 검색 필드를 사용하여 세그먼트를 검색합니다. |
| ![레이블](/help/assets/icons/Label.svg) **[!UICONTROL 태그]** | 선택한 세그먼트에 태그를 지정합니다. **[!UICONTROL 세그먼트에 태그 지정]** 대화 상자에서 선택한 세그먼트의 태그를 선택하거나 선택 취소합니다. **[!UICONTROL 저장]**&#x200B;을 선택하여 선택한 세그먼트의 태그를 저장합니다. 자세한 내용은 [세그먼트 태그 지정](seg-tag.md)을 참조하십시오. |
| ![공유](/help/assets/icons/ShareAlt.svg) **[!UICONTROL 공유]** | 선택한 세그먼트를 공유합니다. **[!UICONTROL 세그먼트 공유]** 대화 상자에서 ![검색](/help/assets/icons/Search.svg) *개인 또는 그룹을 검색* 하거나 **[!UICONTROL 조직]** 또는 **[!UICONTROL 그룹]**&#x200B;을 선택할 수 있습니다. **[!UICONTROL 저장]**&#x200B;을 선택하여 선택한 세그먼트에 대한 공유 세부 정보를 저장합니다. 자세한 내용은 [세그먼트 공유](t-seg-share.md)를 참조하십시오. |
| ![삭제](/help/assets/icons/Delete.svg) **[!UICONTROL 삭제]** | 선택한 세그먼트를 삭제합니다. 확인 메시지가 표시됩니다. |
| ![편집](/help/assets/icons/Edit.svg) **[!UICONTROL 이름 바꾸기]** | 선택한 단일 세그먼트 이름을 바꿉니다. 선택한 경우 세그먼트 이름을 인라인으로 바꿀 수 있습니다. |
| ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL 승인]** | 선택한 세그먼트를 승인합니다. 자세한 내용은 [세그먼트 승인](seg-approve.md)을 참조하십시오. |
| ![복사](/help/assets/icons/Copy.svg) **[!UICONTROL 복사]** | 선택한 세그먼트를 복사합니다. 새로운 세그먼트가 동일한 이름에 접미사 `(Copy)`가 추가되어 생성됩니다. |
| ![FileCSV](/help/assets/icons/FileCSV.svg) **[!UICONTROL CSV로 내보내기]** | 세그먼트를 `Segments List.csv` 파일로 내보냅니다. |

### 활성 필터 표시줄

필터 막대 ➌은(는) 필터 패널에서 세그먼트 목록에 적용된 활성 세그먼트를 표시합니다(있는 경우). ![CrossSize75](/help/assets/icons/CrossSize75.svg)를 사용하여 필터를 빠르게 제거할 수 있습니다. 필터를 두 개 이상 지정한 경우 **[!UICONTROL 모두 제거]**&#x200B;를 사용하여 모든 필터를 제거할 수 있습니다.

### 필터 패널

![필터](/help/assets/icons/Filter.svg) **[!UICONTROL 필터]** 왼쪽 패널 ➍을(를) 사용하여 세그먼트 목록을 필터링할 수 있습니다. 필터 패널에는 필터 유형과 특정 필터를 적용하는 세그먼트 수가 표시됩니다. 필터 패널의 표시를 전환하려면 ![필터](/help/assets/icons/Filter.svg)를 선택하십시오.

자세한 내용은 [세그먼트 목록 필터링](t-seg-filter.md)을 참조하십시오.


<!--

The Segment manager offers many ways of curating segments, such as sharing, filtering, tagging, approving, copying, deleting, and marking as favorites.

The Analytics Segment manager shows you all the segments you own and that have been shared with you. Admin-level users can see all segments in the organization. This overview presents the user interface and the capabilities of the Segment manager. 

![Segments manager](assets/segments-manager.png)

## Access the Segment manager

1. In Adobe Analytics, select the **[!UICONTROL Components]** tab, then select **[!UICONTROL Segments]**.

   Or 

   In an existing report, select the Segments icon ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) in the left navigation, then select **[!UICONTROL Manage]**.

## Available actions in the Segment manager

In the Segment manager, you can:

* [Filter segments](/help/components/segmentation/segmentation-workflow/t-seg-filter.md)

* [Mark segments as favorites](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md)

* [Approve segments](/help/components/segmentation/segmentation-workflow/seg-approve.md)

* [Tag segments](/help/components/segmentation/segmentation-workflow/seg-tag.md)

* [Share segments](/help/components/segmentation/segmentation-workflow/t-seg-share.md)

* Export a segment to a CSV file.

* [Copy segments](/help/components/segmentation/segmentation-workflow/seg-copy.md)

* [Delete segments](/help/components/segmentation/segmentation-workflow/seg-delete.md)

## Configure columns

You can configure the information displayed for each segment in the Segment manager by configuring the columns that are displayed.

To configure the visible columns in the Segment manager:

1. In Adobe Analytics, select the **[!UICONTROL Components]** tab, then select **[!UICONTROL Segments]**. 

1. In the Segment manager, select the **Customize columns** icon ![Customize columns icon](assets/customize-columns-icon.png), then select the columns that you want to be displayed in the Segment manager.

   The following columns are available:

   | Column title | Description  |
   |---|---|
   | Title and description | These values are provided in the Segment builder. To edit the title and description, select the title link to open the Segment builder.  |
   | Favorites  | Displays star icons next to each segment, allowing you to mark segments as favorites. For more information, see [Mark segments as favorites](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md). |
   | Report suites  | This column indicates in which report suite the segment was last saved.  |
   | Owner  | Indicates who owns the segment. As a non-Admin, you can see only segments you own or those that were shared with you.  |
   | Tags (not checked in column selector, hence column not appearing)  | Tags that were applied to the segment, either by you or by people who shared the segment with you.  |
   | Shared with  | Lists individuals or groups (Admin only) or All (Admin only) that you shared the segment with. <p>When a segment is being shared by you or with you, a share icon displays next to the segment name.</p>|
   | Date modified  | Shows the date that the segment was last modified.  |
   | Used in | Shows where segments are currently being used, and how many times they are being used in each area. <p>For example, if the segment is being used in 40 projects and 2 alerts, then the value of this column shows as [!UICONTROL **42 components**].</p> <p>Select the value in this column to see the breakdown of where the segments are being used (for example, [!UICONTROL **Projects (40)**], [!UICONTROL **Alerts (2)**]). Furthermore, you can view the list of items where the segments are being used. For example, so see the list of projects where they are being used, select the [!UICONTROL **Projects (40)**] link.</p><p>Each of the following areas shows the number of instances of segments being used in that area:</p>  <ul><li>[!UICONTROL **Projects**]<p>Contains segments that were [created in the segment builder](/help/components/segmentation/segmentation-workflow/seg-build.md) and are available for all projects.</p></li><li>[!UICONTROL **Ad hoc components**]<p>Contains segments that were [created as quick segments](/help/analyze/analysis-workspace/components/segments/quick-segments.md) and are available only within a single project.</p></li><li>[!UICONTROL **Scheduled projects**]</li><li>[!UICONTROL **Mobile Scorecards**]</li><li>[!UICONTROL **Annotations**]</li><li>[!UICONTROL **Alerts**]</li><li>[!UICONTROL **Calculated metrics**]</li><li>[!UICONTROL **Report Builder**]<p>Selecting this option downloads a CSV file, with the following columns of data:</p><ul><li>Report Builder Name</li><li>Last accessed</li><li>Last accessed IMS User ID</li><li>Last accessed user name</li></ul><p>When viewing information for Report Builder, usage information is available starting in September 2024.</p></li></ul><p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information is available only to system administrators.</li><li>The [!UICONTROL **Used in**] column does not display by default. [Configure columns](#configure-columns) to display it.</li><li>If a segment includes another segment in its definition, any use of that segment is not shown in the [!UICONTROL **Used in**] column. If a segment is included in the definition of another type of component (such as a calculated metric), then usage is shown in the [!UICONTROL **Used in**] column.</li><li>This information does not include usage from the API or Data Warehouse.</li><li>If there is no data in this column for a given component but it has a [!UICONTROL **Last used**] date, the component might have been used in an analysis without being saved.</li><li>Usage information is available starting in September 2023.</li></ul><p>You can use the [Data Dictionary](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) along with this information to help you keep track of and better understand how components are being used in your organization.</p>  |
   | Last used | Shows the date when the segment was last used in any of the following component types: <ul><li>Alerts</li><li>Calculated metrics</li><li>Projects</li><li>Scheduled projects</li><li>Segments</li></ul> <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li><li>This information is available only to system administrators.</li></ul><p>You can use the [Data Dictionary](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) along with this information to help you keep track of and better understand how components are being used in your organization. |
   
   {style="table-layout:auto"}

## How-To Video {#section_B3C5DA22DC5248DBA17C56E03DA2D4F2}

This [Adobe Analytics video](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/segmentation/segment-management-and-sharing.html?lang=ko) gives a short overview of how to use the Segment manager.

-->