---
description: Adobe Admin Console에서 Analytics 사용자, 그룹 및 제품을 관리합니다.
subtopic: Users and groups
title: 사용자 및 제품 관리
feature: Admin Tools
exl-id: c0fbbb3a-0011-49d2-89a2-70fce11e0fb2
source-git-commit: e735997fed397cf8bb3eb3edcf9af9f841afb9d2
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 100%

---

# 사용자 및 제품 관리(레거시)

Adobe Admin Console에서 Analytics 사용자, 그룹 및 제품을 관리합니다.

>[!IMPORTANT]
>
>사용자 및 제품 관리 기능은 [Adobe Admin Console](https://helpx.adobe.com/kr/enterprise/using/admin-console.html)로 이동되었습니다. Adobe Analytics 사용자에 대한 사용자 권한 관리를 시작하려면 [Adobe Admin Console의 Analytics](/help/admin/admin-console/home.md)를 참조하십시오.

## Adobe Admin Console 관리자에 대한 도움말 리소스 {#section_C13BBB89E4F248F193358BB3A59DD502}

| 작업 또는 리소스 | 설명 |
| --- | --- |
| Analytics 사용자 ID를 Adobe Admin Console로 마이그레이션 | Adobe는 Analytics 관리자가 사용자 ID를 Adobe Admin Console로 마이그레이션하도록 지원합니다. 이러한 지원은 신속하게 이루어질 것입니다. 여러분이 사용자를 마이그레이션해야 하는 경우 Adobe는 이메일로 Analytics 관리자에게 지침을 알려 줍니다. 마이그레이션 도구는 이 작업을 단순화할 수 있는 [Analytics User Management](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=ko-KR) 기능을 제공합니다.<p>**중요**: 이전의 권한 그룹은 사용자의 마이그레이션 당일 자동으로 Adobe Admin Console에 복사됩니다. 더 이상 Analytics 관리 도구에서 새 사용자를 초대하거나 새 그룹을 만들 수 없게 됩니다. 마이그레이션 준비 그리고 그에 영향을 받는 관리 기능에 대한 더 자세한 내용은 FAQ와 Adobe Admin Console로 Analytics 사용자 마이그레이션 도움말에서 확인할 수 있습니다. |
| Adobe Admin Console 시작 | 사용자 계정이 마이그레이션되면 Adobe Admin Console의 모든 솔루션에서 사용자와 제품을 관리할 수 있습니다. `https://adminconsole.adobe.com/enterprise/`로 이동합니다. [Experience Cloud 사용자 및 제품 관리](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html?lang=ko-KR)도 참조할 수 있습니다. |
| Adobe Analytics 제품 프로필, 사용자 그리고 권한을 관리합니다. | [Adobe Admin Console의 Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=ko-KR)를 참조하십시오. |

<!---
## User Management Descriptions {#section_7C19842A3D4249109A9399D4DF18DE75}

The following table describes elements on the [!UICONTROL Users] tab in [!UICONTROL User Management].

<table id="table_6F81D1095EB945D8995FF971B65BA52A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Number of User Logins available</span> </td> 
   <td colname="col2"> The maximum number of user accounts you can create for this company. If necessary, you can contact your Account Representative or Customer Care to increase this number at no charge. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Number of User Logins in use</span> </td> 
   <td colname="col2"> The number of user accounts currently in use for this company. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Number of User Logins Remaining</span> </td> 
   <td colname="col2"> The difference between the user account maximum and the number of existing user accounts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Add New User</span> </td> 
   <td colname="col2"> <p>Lets you add a user account to the company. This link is available only if the Number of User Logins Remaining is greater than 0. </p> <p>See <a href="/help/admin/user-management2/c-user-management/users.md"> Users</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Download Report</span> </td> 
   <td colname="col2">Exports the contents of the <span class="wintitle"> Users</span> table to a tab-delimited file. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Login</span> </td> 
   <td colname="col2"> <p>The user name. You can click the user name to edit the user account properties. </p> <p>See <a href="/help/admin/user-management2/c-user-management/users.md"> Users</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> First Name</span> </td> 
   <td colname="col2"> The user's first (given) name. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Last Name</span> </td> 
   <td colname="col2"> The user's surname (family name). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Title</span> </td> 
   <td colname="col2"> The user's job title. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Admin</span> </td> 
   <td colname="col2"> Specifies if the user account has administrative privileges. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Last Login</span> </td> 
   <td colname="col2"> Displays a timestamp of the last login for this user account. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> Create Time</span> </td> 
   <td colname="col2"> Shows the date and time when the login account was created. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Expires</span> </td> 
   <td colname="col2"> Displays the account expiration account, if applicable. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Manage</span> </td> 
   <td colname="col2"> Provides links for user account management. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Edit</span> </td> 
   <td colname="col2"> <p>Edit user account settings. </p> <p>See <a href="/help/admin/user-management2/c-user-management/users.md"> Users</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Delete</span> </td> 
   <td colname="col2"> Delete the user account. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Transfer</span> </td> 
   <td colname="col2">Assign the privileges (permissions and resource access) of one user account to another. <p>See <a href="/help/admin/user-management2/c-user-management/t-transfer-user-accout-privileges.md"> Transfer user account privileges</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> Login as this user</span> </td> 
   <td colname="col2"> <p>Allows admins to impersonate and log in as a non-admin account. Admin accounts cannot be impersonated. </p> </td> 
  </tr> 
 </tbody> 
</table>
-->