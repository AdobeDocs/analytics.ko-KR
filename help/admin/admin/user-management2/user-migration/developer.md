---
description: 사용자 마이그레이션의 영향을 받는 API를 나열합니다.
title: 사용자 마이그레이션의 영향을 받는 API
feature: Admin Tools
exl-id: 82d0a1cd-1e25-4157-9bb9-bba1049fdc48
role: Admin, Developer
source-git-commit: 4c4e68afcf9a7e2c5cd00ef109fbbf44578a3d1a
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 99%

---

# 사용자 마이그레이션의 영향을 받는 API{#apis-affected-by-the-migration}

Adobe는 모든 Analytics 로그인 기업을 [!DNL my.omniture.com]에서 Adobe Experience Cloud를 통한 인증 방식으로 마이그레이션하고 있습니다. 기업에서 마이그레이션을 시작하면 Analytics 관련 권한 및 Analytics Admin API v1.3 및 v1.4에서 사용할 수 있는 `GetLoginKey` 메서드를 통한 프로그래밍 방식의 사용자 생성 및 관리가 더 이상 지원되지 않습니다. 이제 이러한 작업은 이제 [!DNL adobe.io]를 통해 Experience Cloud에서 사용할 수 있습니다.

## 영향을 받는 API 메서드 {#methods}

사용자 마이그레이션을 시작하면 Admin API의 v1.3 및 v1.4에 있는 다음 API 메서드가 더 이상 지원되지 않습니다.

* Company.GetLoginKey
* Permissions.AddLogin
* Permissions.Authenticate
* Permissions.DeleteGroup
* Permissions.DeleteLogin
* Permissions.GetGroup
* Permissions.GetGroups
* Permissions.GetLogin
* Permissions.GetLogins
* Permissions.GetReportSuiteGroups
* Permissions.RemoveLoginSegment
* Permissions.SaveGroup
* Permissions.SaveLogin
* Permissions.GetLoginSegment

## 수행할 수 있는 작업 {#actions}

현재 기업에서 이러한 메서드를 사용하는 경우, 2018년 3월 31일부터 시작되는 사전 마이그레이션 알림을 확인하십시오. 기업이 Experience Cloud 인증으로 마이그레이션을 시작하기 최소 30일 전에 알림이 전송되며, 해당 시점에는 이러한 메서드가 지원되지 않습니다.

기업에서 이러한 메서드를 사용하지 않는 경우 이러한 메소드를 사용하지 않는 것 외에는 다른 조치가 필요하지 않습니다.

추가 정보:

* [일반 사용자 관리 정보](https://helpx.adobe.com/kr/enterprise/help/users.html)
* [adobe.io를 통한 사용자 관리 API](https://developer.adobe.com/umapi)
* [사용자 관리 API 포럼](https://community.adobe.com/t5/enterprise-teams/bd-p/enterprise-and-teams)
* [Experience Cloud로 Analytics 사용자 액세스 및 관리 마이그레이션](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=ko-KR)
