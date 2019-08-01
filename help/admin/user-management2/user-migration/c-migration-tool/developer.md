---
description: 'null'
seo-description: 'null'
seo-title: 마이그레이션의 영향을 받는 API
title: 마이그레이션의 영향을 받는 API
uuid: 9 A 5 D 43 BE-E 146-476 B -961 E -49 EA 0 A 30 B 500
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 2fcd72e6c61f8004268e583b934e9cf474e5e44f

---


# 마이그레이션의 영향을 받는 API{#apis-affected-by-the-migration}

## 마이그레이션의 영향을 받는 API {#topic-8d34296a67d74b1081c3f7e8f650f3ce}

Adobe는 [!DNL my.omniture.com] 및 Adobe Experience Cloud를 통한 인증 방식으로 모든 Analytics 로그인 기업을 마이그레이션하고 있습니다. 기업에서 마이그레이션을 시작하면 Analytics 관련 권한 및 Analytics Admin API의 v1.3 및 v1.4에서 사용할 수 있는 `GetLoginKey` 메서드를 통한 프로그래밍 방식의 사용자 생성 및 관리가 더 이상 지원되지 않습니다. 이제 이러한 작업은 이제 [!DNL adobe.io]를 통해 Experience Cloud에서 사용할 수 있습니다.

## 영향을 받는 API 메서드 {#section-d19051ac26cc49aeb124f767c4760254}

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

## 수행할 수 있는 작업 {#section-8b0b89a862614f729ebdbe092ce99027}

현재 기업에서 이러한 메서드를 사용하는 경우, 2018년 3월 31일부터 시작되는 사전 마이그레이션 알림을 확인하십시오. 기업이 Experience Cloud 인증으로 마이그레이션을 시작하기 최소 30일 전에 알림이 전송되며, 해당 시점에는 이러한 메서드가 지원되지 않습니다.

기업에서 이러한 메서드를 사용하지 않는 경우 이러한 메소드를 사용하지 않는 것 외에는 다른 조치가 필요하지 않습니다.

추가 정보:

* [일반 사용자 관리 정보](https://helpx.adobe.com/enterprise/help/users.html)
* [adobe.io를 통한 사용자 관리 API](https://www.adobe.io/apis/cloudplatform/usermanagement/docs/gettingstarted.html)
* [사용자 관리 API 포럼](https://forums.adobe.com/community/umapi/overview)
* [Experience Cloud로 Analytics 사용자 액세스 및 관리 마이그레이션](https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/)

