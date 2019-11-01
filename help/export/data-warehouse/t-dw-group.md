---
description: 관리자가 사용자 그룹에 대한 Data Warehouse 보고 액세스 권한을 활성화할 수 있는 방법을 설명하는 단계입니다.
seo-description: 관리자가 사용자 그룹에 대한 Data Warehouse 보고 액세스 권한을 활성화할 수 있는 방법을 설명하는 단계입니다.
seo-title: Data Warehouse 사용자 그룹 추가
solution: Analytics
title: Data Warehouse 사용자 그룹 추가
topic: Data Warehouse
uuid: d89294db-caa3-4044-b70d-65b512b0dc1c
translation-type: tm+mt
source-git-commit: ed22e0520bf1c7427ead039fb1d0391f2f1e567f

---


# Data Warehouse 사용자 그룹 추가

관리자가 사용자 그룹에 대한 Data Warehouse 보고 액세스 권한을 활성화할 수 있는 방법을 설명하는 단계입니다.

1. Click **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL User Management]**.
1. Click **[!UICONTROL Edit Groups]**.
1. Click **[!UICONTROL Add New User Group]**.
1. In the **[!UICONTROL Define User Group]** section, type a name in the Group Name field. 다음 그룹 정보를 입력하십시오. 

   예, `Data Warehouse Access`.
1. Type a description in the **[!UICONTROL Group Description]** field.
1. In the **[!UICONTROL Report Suite Access]** section, select the report suites that you want group members to be able to access.
1. Under [!UICONTROL Tools], enable **[!UICONTROL All Tools]**.

   Alternatively, click **[!UICONTROL Customize]**, then enable **[!UICONTROL Custom Data Warehouse Report]**.

1. [!UICONTROL 사용자 로그인 지정]에서 원하는 사용자 로그인을 추가합니다.
1. Click **[!UICONTROL Save Group]**.

   다음번에 이 그룹에 추가된 사용자가 로그인하면 해당 사용자는 [!UICONTROL Reports &amp; Analytics] 메뉴에 추가된 Data Warehouse 옵션을 볼 수 있습니다.

   >[!NOTE]
   >
   >권한이 충돌하는 경우(두 그룹에 할당된 사용자 중 한 그룹은 기능에 대한 액세스를 거부하고 다른 그룹은 동일한 액세스를 부여하는 경우) 시스템에서 권한을 제한합니다. Data Warehouse 액세스를 거부하는 그룹에 속하는 사용자는 해당 그룹에서 제거해야 할 수 있습니다.

>[!MORELIKETHIS]
>
>* [그룹 ](/help/admin/user-management2/c-user-groups/groups.md)

