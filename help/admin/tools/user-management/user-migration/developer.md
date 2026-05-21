---
description: 사용자 마이그레이션의 영향을 받는 API를 나열합니다.
title: 사용자 마이그레이션의 영향을 받는 API
feature: Admin Tools
exl-id: 82d0a1cd-1e25-4157-9bb9-bba1049fdc48
role: Admin, Developer
TQID: https://experienceleague.adobe.com/vrfYIoa98hEoUVW17cwOLWTPk-3MIRS2wwLPB-ZB5DA
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: fd307ce7-56f5-4ee3-af68-a7833ff6e85eid: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 9e2c89f4188c723b4623a6e7859b74ede15e155b
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 31%

---

# 사용자 마이그레이션의 영향을 받는 API{#apis-affected-by-the-migration}

Adobe은 모든 Analytics 로그인 회사를 [!DNL my.omniture.com]에서 Adobe CX Enterprise를 통한 인증으로 마이그레이션하고 있습니다. 기업에서 마이그레이션을 시작하면 Analytics 관련 권한 및 Analytics Admin API v1.3 및 v1.4에서 사용할 수 있는 `GetLoginKey` 메서드를 통한 프로그래밍 방식의 사용자 생성 및 관리가 더 이상 지원되지 않습니다. 이러한 작업은 이제 `adobe.io`을(를) 통해 CX Enterprise에서 사용할 수 있습니다.

## 영향을 받는 API 메서드 {#methods}

사용자 마이그레이션을 시작하면 관리 API v1.3 및 v1.4의 다음 API 메서드가 더 이상 지원되지 않습니다.

* Company.GetLoginKey
* Permissions.Addlogin
* Permissions.Authentication
* Permissions.DeleteGroup
* Permissions.DeleteLogin
* Permissions.GetGroup
* Permissions.GetGroups
* Permissions.GetLogin
* Permissions.GetLogins
* 권한.GetReportSuiteGroups
* Permissions.RemoveLoginSegment
* Permissions.SaveGroup
* Permissions.SaveLog
* Permissions.GetLoginSegment

## 수행할 수 있는 작업 {#actions}

회사에서 현재 이러한 방법을 사용하는 경우 2018년 3월 31일부터 마이그레이션 전 알림을 찾으십시오. 회사에서 CX 엔터프라이즈 인증으로 마이그레이션을 시작하기 최소 30일 전에 알림이 전송되며 이 때 이러한 방법은 지원되지 않습니다.

회사에서 이러한 방법을 사용하지 않는 경우 이러한 방법을 사용하지 않도록 보장하는 것 외에는 다른 조치가 필요하지 않습니다.

추가 정보:

* [일반 사용자 관리 정보](https://helpx.adobe.com/kr/enterprise/help/users.html)
* [사용자 관리 API 포럼](https://community.adobe.com/t5/enterprise-teams/bd-p/enterprise-and-teams)
* [Analytics 사용자 액세스 및 관리를 CX Enterprise로 마이그레이션](/help/admin/tools/user-management/user-migration/c-migration-tool.md)
