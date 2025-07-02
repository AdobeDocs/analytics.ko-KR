---
description: 경고를 관리하는 방법을 알아봅니다.
title: 경고 관리
feature: Alerts
exl-id: 3408c79f-3d85-44b9-8fca-ce956853dfa4
source-git-commit: 24dd47e995523aedba1385ee8882af5e11c7b128
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 22%

---


# 경고 관리


중앙 [!UICONTROL 경고] 관리 인터페이스에서 경고를 필터링, 태그 지정, 삭제, 이름 변경, 복사, 활성화, 비활성화, 갱신 및 내보낼 수 있습니다. 경고를 관리하려면 다음을 수행하십시오.

* 기본 인터페이스에서 **[!UICONTROL 구성 요소]**&#x200B;를 선택한 다음 **[!UICONTROL 경고]**&#x200B;를 선택하십시오.

경고 관리자는 [세그먼트 관리자](/help/components/segmentation/segmentation-workflow/seg-manage.md) 및 [계산된 지표 관리자](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md)와 같이 구성되어 있습니다.


## 경고 관리자

경고 관리자에는 다음과 같은 인터페이스 요소가 있습니다.

![필터 인터페이스](assets/alerts-manager.png)

### 경고 목록

경고 목록 ➊에는 사용자가 소유한 모든 경고, 모든 프로젝트에 범위가 지정된 경고, 사용자와 공유된 경고가 표시됩니다. 목록은 다음과 같습니다.

| 열 | 설명 |
|---|---|
| ![StarOutline](/help/assets/icons/StarOutline.svg) | ![Star](/help/assets/icons/Star.svg)을(를) 선호하거나 ![StarOutline](/help/assets/icons/StarOutline.svg)을(를) 선호하지 않도록 선택하십시오. |
| **[!UICONTROL 제목 및 설명]** | 경고를 편집하려면 제목 링크를 선택하여 [경고 빌더](alert-builder.md#alert-builder)를 엽니다. |
| **[!UICONTROL Type]** | 경고 유형: Adobe Analytics 데이터 경고 또는 서버 호출 사용량 경고. |
| **[!UICONTROL 활성화됨]** | 경고가 활성화되거나 비활성화됩니다. |
| **[!UICONTROL 보고서 세트]** | 이 경고가 적용되는 보고서 세트입니다. |
| **[!UICONTROL 소유자]** | 경고 소유자. 관리자가 아닌 경우 사용자가 소유하거나 사용자와 공유된 경고만 표시됩니다. |
| **[!UICONTROL 태그]** | 이 경고에 대한 태그입니다. |
| **[!UICONTROL 만료 날짜]** | 경고가 만료되도록 설정된 날짜 및 시간입니다. |
| **[!UICONTROL 수정한 날짜]** | 경고를 마지막으로 수정한 날짜 및 시간입니다. |

<!-- 

When "Last used" column is added, add this information as the description: Shows the date when the alert was last used. <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li></ul>

-->

![ColumnSetting](/help/assets/icons/ColumnSetting.svg)을 사용하여 표시할 열을 지정합니다.

### 작업 표시줄

작업 모음 ➋을(를) 사용하여 경고에 대한 작업을 수행할 수 있습니다. 작업 표시줄에는 다음 액션이 포함됩니다.

| 아이콘 | 액션 | 설명 |
|:---:|---|---|
| ![AddCircle](/help/assets/icons/AddCircle.svg) | **[!UICONTROL 추가]** | [경고 빌더](alert-builder.md#alert-builder)를 사용하여 다른 경고를 추가하십시오. |
| ![Search](/help/assets/icons/Search.svg) | [!UICONTROL *제목별 검색*] | 목록에서 경고를 선택하지 않은 경우 이 검색 필드를 사용하여 경고를 검색합니다. |
| ![레이블](/help/assets/icons/Label.svg) | **[!UICONTROL 태그]** | 선택한 경고에 태그를 지정합니다. **[!UICONTROL 태그 경고]** 대화 상자에서 선택한 경고에 대한 태그를 선택하거나 선택 취소합니다. **[!UICONTROL 저장]**&#x200B;을 선택하여 선택한 경고에 대한 태그를 저장합니다. |
| ![삭제](/help/assets/icons/Delete.svg) | **[!UICONTROL 삭제]** | 선택한 경고를 삭제합니다. 확인 메시지가 표시됩니다. |
| ![Edit](/help/assets/icons/Edit.svg) | **[!UICONTROL 이름 바꾸기]** | 선택한 단일 경고의 이름을 변경합니다. 선택하면 경고 이름을 인라인으로 바꿀 수 있습니다. |
| ![복사](/help/assets/icons/Copy.svg) | **[!UICONTROL 복사]** | 선택한 경고를 복사합니다. 같은 이름과 접미사 `(Copy)`을(를) 사용하여 새 경고를 만듭니다. |
| ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg) | **[!UICONTROL 사용]** 또는 **[!UICONTROL 사용 안 함]** | 선택한 경고를 활성화하거나 비활성화합니다. |
| ![새로 고침](/help/assets/icons/Refresh.svg) | **[!UICONTROL 갱신]** | 경고의 만료 날짜를 갱신합니다. 원래 만료 날짜와 상관없이 이 옵션을 선택한 날짜로부터 1년이 만료됩니다. |
| ![FileCSV](/help/assets/icons/FileCSV.svg) | **[!UICONTROL CSV로 내보내기]** | 경고를 `Alerts List.csv` 파일로 내보냅니다. |


### 활성 필터 표시줄

필터 표시줄 ➌은(는) 필터 패널에서 경고 목록에 적용된 활성 필터를 표시합니다. ![CrossSize75](/help/assets/icons/CrossSize75.svg)를 사용하여 필터를 빠르게 제거할 수 있습니다. 두 개 이상의 필터가 지정되면 **[!UICONTROL 모두 제거]**&#x200B;를 사용하여 모든 필터를 제거할 수 있습니다.


### 필터 패널

![필터](/help/assets/icons/Filter.svg) **[!UICONTROL 필터]** 왼쪽 패널 ➍을(를) 사용하여 경고 목록을 필터링할 수 있습니다. 필터 패널에는 필터 유형 및 특정 필터를 적용하는 경고 수가 표시됩니다.


1. ![Filter](/help/assets/icons/Filter.svg)를 선택하여 필터 패널을 엽니다. 알림 목록에 더 많은 공간이 필요한 경우 ![필터](/help/assets/icons/Filter.svg)를 한 번 더 선택하여 패널을 닫을 수 있습니다.
1. 사용 가능한 필터 섹션에서 필터를 선택합니다.


#### 태그 필터 섹션

{{tagfiltersection}}


#### 보고서 세트 필터 섹션

{{reportsuitefiltersection}}


#### 소유자 필터 섹션

{{ownerfiltersection}}


#### 활성화된 상태 필터 섹션

{{enabledstatusfiltersection}}


#### 필터 섹션 입력

{{typefiltersection}}


#### 기타 필터 필터 섹션

{{otherfiltersfiltersection}}



## 경고 편집

경고를 편집할 수 있습니다

* [[!UICONTROL 경고] 목록](#alerts-list)에서 경고의 제목을 선택합니다.

[경고 빌더](alert-builder.md#alert-builder)를 사용하여 경고를 편집합니다.

## 경고 문제 해결

경고와 관련된 문제를 해결할 때 Adobe 지원에 JID(작업 인스턴스 ID) 번호를 입력합니다. JID 번호는 수신하는 경고 이메일 알림 하단에 있습니다.

![경고 이메일](assets/alerts-email.PNG)


<!--

# Manage alerts

You can manage existing alerts in the Alerts manager. You can perform various management tasks on alerts, such as tagging, renaming, deleting, and more.

The Alerts manager is structured very much like the [Segment Manager](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html) and the [Calculated Metric Manager](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html).

 ![](assets/alert-manager.png)

## Create alerts

To create alerts from the Alerts manager:

1. Select **[!UICONTROL Components]** > **[!UICONTROL Alerts]** to access the Alerts manager in Adobe Analytics.

   ![](assets/alert-manager.png)

1. Select [!UICONTROL **Add**] (or [!UICONTROL **Create new alert**] if you don't have any existing alerts).

1. Select the alert type that corresponds to the alert that you want to create:

   * [!UICONTROL **Analytics data alert**]: An alert to notify you when abnormal events occur in your data. 

     If you select this option, continue with [Create alerts](/help/components/c-alerts/alert-builder.md) for more details about creating alerts.

   * [!UICONTROL **Server call usage alert**]: An alert to notify you of the risk or occurrence of an overage in your server call consumption and commitment data. 

     If you select this option, continue with [Server call usage alerts](/help/admin/admin/c-server-call-usage/scu-alerts.md).

     >[!NOTE]
     >
     >You must be an Analytics administrator or a user with the Server call usage permission in order to have access to server call usage. 

## Manage existing alerts

You can perform various actions on existing alerts, such as tagging, renaming, deleting, and so forth.

To manage existing alerts in the Alerts manager:

1. Select **[!UICONTROL Components]** > **[!UICONTROL Alerts]** to access the Alerts manager in Adobe Analytics.

   ![](assets/alert-manager.png)

1. Select one or more alerts that you want to manage.

   ![](assets/alert-manager-tasks.png)

1. In the action bar, select any of the following options:

   | Action | Function | 
   |---------|----------|
   | [!UICONTROL **Tag**] | Apply a tag to an alert. This helps you to organize alerts for ease of use. | 
   | [!UICONTROL **Delete**] | Deletes the alert. | 
   | [!UICONTROL **Rename**] | Renames the alert. |
   | [!UICONTROL **Approve**] | Mark the alert as Approved. |
   | [!UICONTROL **Copy**] | Creates a copy (duplicate) of the alert. |
   | [!UICONTROL **Disable**] | Disables an alert that is currently enabled. |
   | [!UICONTROL **Enable**] | Enables an alert that is currently disabled. |
   | [!UICONTROL **Renew**] | Renews the alert expiration date. This extends the  expiration date to be 1 year from the day you selected this option, regardless of the original expiration date. |
   | [!UICONTROL **Export to CSV**] | Exports the alert to a .CSV file. |

## Edit an alert

To edit an existing alert:

1. Select **[!UICONTROL Components]** > **[!UICONTROL Alerts]** to access the Alerts manager in Adobe Analytics.

   ![](assets/alert-manager.png)

1. Select the alert name in the [!UICONTROL **Title and description**] column.

1. Edit the alert as desired. 

   Following are some of the things you can do when editing an alert:

   * Add alerts to other report suites
   * Add or modify the description
   * Modify the time granularity
   * Modify the recipients 
   * Modify the expiration date
   * Modify the metrics and filters

1. Select [!UICONTROL **Save**].

## Configure columns 

You can configure the information displayed for each alert in the Alerts manager by configuring the columns that are displayed.

To configure the visible columns in the Alerts manager:

1. In Adobe Analytics, select the **[!UICONTROL Components]** tab, then select **[!UICONTROL Alerts]**. 

1. In the Alert manager, select the **Customize columns** icon ![Customize columns icon](assets/customize-columns-icon.png), then select the columns that you want to be displayed in the Alerts manager.

   The following columns are available:

   | Column title  | Description |
   |---|---|
   | Title and description | These values are provided in the Alert builder. To edit the title and description, select the title link to open the Alert builder.  |
   | Favorites  | Displays star icons next to each alert, allowing you to mark alerts as favorites. |
   | Type | Shows whether the alert is an Analytics data alert or a Server call usage alert. |
   | Enabled | Shows whether the alert is currently enabled or disabled. | 
   | Report suite | Indicates in which report suite the alert was last saved.  |
   | Owner | Indicates who owns the alert. As a non-admin, you can see only alerts you own or those that were shared with you.  |
   | Tags | Shows tags that were applied to the alert, either by you or by people who shared the alert with you.  |
   | Expiration date | Shows the date and time when the alert is set to expire. |
   | Date modified | Indicates the date when the alert was last modified.  |

   {style="table-layout:auto"}
   
   
    When "Last used" column is added, add this information as the description: Shows the date when the alert was last used. <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li></ul> 
   
-->

