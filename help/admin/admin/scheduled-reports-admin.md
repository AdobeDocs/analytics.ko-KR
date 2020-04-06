---
description: 관리자 수준 사용자가 조직 전체에서 예약된 보고서를 보고 관리할 수 있습니다.
title: 예약된 보고서 큐
topic: Reports
uuid: 3fcf92d3-a472-465f-ad7a-c48cd9a8238b
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 예약된 보고서 큐

관리자 수준 사용자가 조직 전체에서 예약된 보고서를 보고 관리할 수 있습니다.

**[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Scheduled Reports]**

예약된 보고서 관리자에는 다음과 같은 관리 수준 기능이 있습니다.

* 조직에서 예약된 [보고서를 모두 표시하는](/help/admin/admin/scheduled-reports-admin.md#section_3F167CAAEEC24140B476CF95B7402690) 옵션.
* [조직 전체의 고급](/help/admin/admin/scheduled-reports-admin.md#section_206A52A85DE84947AAB3AD082FBF6275) 필터링 기능
* 보고 [서버에서](/help/admin/admin/scheduled-reports-admin.md#section_03C866115D354BB182E90BF4D52F1E0B) 실행되도록 큐에 있는 모든 보고서를 나열하는 새 보고서 큐 탭.
* 보고서 [큐](/help/admin/admin/scheduled-reports-admin.md#section_568B70F4228C4229977CB85D2DCD53A1) 인터페이스에서 예약 ID 노출.

## Show all Scheduled Reports {#section_3F167CAAEEC24140B476CF95B7402690}

이 **[!UICONTROL Report List]** 탭에서 개인적으로 예약한 조직 외에 조직에서 **[!UICONTROL Show All Scheduled Reports]** 사용할 수 있습니다.

>[!NOTE] 이 **[!UICONTROL Report Name]** 열에는 예약되는 보고서의 이름이 표시되고, **[!UICONTROL File Name]** 열에는 고급 배달 옵션에서 사용자가 설정한 사용자 지정 파일 이름이 표시됩니다. 따라서 동일한 보고서 유형의 여러 보고서를 예약하고 각각에 대해 사용자 지정된 이름을 지정하는 경우 예약된 보고서 관리자는 같은 보고서 이름과 다른 파일 이름으로 여러 항목을 표시합니다. 이는 예약되는 백엔드 보고서가 동일하기 때문에 보고서 이름 열에는 사용자 지정된 파일 이름(설정된 대로)을 제외한 모든 파일 이름에 대해 동일한 보고서 이름이 표시됩니다.

![](assets/show_all_scheduled_reports.png)

## 고급 필터링 기능 {#section_206A52A85DE84947AAB3AD082FBF6275}

For example, if you wanted to filter on all reports that are scheduled hourly, you would specify **[!UICONTROL Frequency equals Hourly]** in the **[!UICONTROL Advanced]** filter and click **[!UICONTROL Apply]**:

![](assets/advanced_filtering_schedl_reports.png)

## 보고서 큐 {#section_03C866115D354BB182E90BF4D52F1E0B}

이 큐를 사용하면 큐를 &quot;막고 있는&quot; 예약된 보고서를 관리하고 잠재적으로 삭제할 수 있습니다. (일반적으로 보고서는 4시간 후 시간 초과입니다.)

![](assets/scheduled_reports_2.png)

보고서 큐는 &quot;예약된 보고서를 한 번 건너뛰기&quot;도 제공합니다. Just click the blue icon in the **[!UICONTROL Manage]** column.

## 예약 ID {#section_568B70F4228C4229977CB85D2DCD53A1}

Having the **[!UICONTROL Schedule ID]** exposed in the Report Queue interface helps when you need to contact Adobe Client Care for resolution of a scheduled reports issue.

![](assets/schedule_id.png)
