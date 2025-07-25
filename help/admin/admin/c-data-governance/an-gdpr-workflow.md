---
description: 데이터 주체의 데이터 개인정보 보호 액세스 및 삭제 권한을 지원하기 위해 Adobe Analytics 구현을 활성화하는 절차에 대해 설명합니다.
title: 개인정보 보호 워크플로
feature: Data Governance
role: Admin
exl-id: c364b364-6d77-4b2c-88ab-65daf812f242
source-git-commit: 1281bdc569c9ebc5d8daa151b19dc21710633eab
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 100%

---

# 개인정보 보호 워크플로

이 워크플로에서는 데이터 주체의 데이터 개인정보 보호 액세스 및 삭제 권한을 지원하도록 Adobe Analytics를 구현하기 위해 수행해야 하는 단계를 간략하게 설명합니다.

1. Adobe Experience Platform의 [Privacy Service 개요](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ko-KR) 페이지에서 시작하여 Analytics 데이터에 레이블을 지정하기 전에 필요한 질문에 대해 알아보십시오.
1. **데이터 보존 정책을 설정합니다.** Adobe가 데이터 개인정보 보호 데이터 액세스/삭제 요청을 처리하려면 데이터 보존 정책이 필요합니다.  자세한 내용은 [데이터 보존 FAQ](/help/technotes/data-retention.md)를 참조하십시오. Privacy Service API를 사용하려면 Adobe Analytics 내에 데이터 보존 기간이 설정되어 있는지 확인해야 합니다.
1. **데이터 개인정보 보호 레이블, Adobe Analytics ID 및 네임스페이스에 대해 숙지하십시오.** [Analytics 변수의 데이터 개인정보 보호 레이블](/help/admin/admin/c-data-governance/data-labeling/gdpr-labels.md) 및 [레이블 지정 모범 사례](/help/admin/admin/c-data-governance/data-labeling/gdpr-analytics-ids.md)를 참조하십시오.
1. **ID, 민감도 및 데이터 거버넌스 레이블을 보고서 세트의 각 변수에 지정합니다.** 새 보고서 세트가 작성되거나 기존 보고서 세트 내에서 새 변수가 활성화될 때마다 레이블 지정을 검토해야 합니다. 또한 새로운 솔루션 통합이 활성화된 경우 레이블 지정이 필요할 수 있는 새로운 변수를 노출할 수 있으므로 레이블 지정을 검토해야 합니다. 모바일 앱 또는 웹 사이트를 재구현하면 기존 변수가 사용되는 방식이 변경될 수 있으며, 이로 인해 레이블 업데이트가 필요할 수도 있습니다. [보고서 세트 데이터에 레이블 지정](/help/admin/admin/c-data-governance/data-labeling/gdpr-namespaces.md)을 참조하십시오.
1. **Adobe 데이터 개인정보 보호 API에 연결하고 액세스 및 삭제 요청을 제출합니다.** Adobe Analytics 고객은 [Adobe Experience Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=ko-KR)를 호출하여 고객 데이터 액세스 및 삭제에 대한 개별 데이터 개인정보 보호 요청을 제출할 수 있습니다. [레이블 지정 모범 사례](/help/admin/admin/c-data-governance/data-labeling/gdpr-analytics-ids.md) 섹션에 설명된 대로 Analytics 식별자를 해당 네임스페이스 ID(데이터 소스 ID)와 함께 요청에 제출할 수 있습니다.
1. **보고서 세트의 데이터 개인정보 보호 설정을 보고 관리합니다.** [보고서 세트의 데이터 거버넌스 설정 보기](/help/admin/admin/c-data-governance/data-labeling/gdpr-view-settings.md)를 참조하십시오.
