---
description: 데이터 주체의 데이터 개인정보 보호 액세스 및 삭제 권한을 지원하기 위해 Adobe Analytics 구현을 활성화하는 절차에 대해 설명합니다.
title: 개인 정보 보호 작업 과정
uuid: f24e8be3-8b5c-409b-ad6b-770198ae2549
translation-type: tm+mt
source-git-commit: b3ea538d0d6e6ebbbbd17871aacaed7527cf3976
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 94%

---


# 개인 정보 보호 작업 과정

이 워크플로우에서는 데이터 주체의 데이터 개인 정보 보호 액세스 및 삭제 권한을 지원하도록 Adobe Analytics를 구현하기 위해 수행해야 하는 단계를 간략하게 설명합니다.

| 작업 설명 | 지침 및 추가 정보에 대한 링크 |
|--- |--- |
| **1단계**: 데이터 개인 정보 보호 관련 데이터가 포함될 수 있는 모든 보고서 세트가 Experience Cloud(또는 IMS) 조직에 매핑되어 있는지 확인합니다.  데이터 개인 정보 보호 요청은 Experience Cloud 조직을 사용하여 제출되며, 해당 조직에서 요구하는 모든 보고서 세트에 적용됩니다. 보고서 세트가 로그인 회사의 일부인 경우에도 해당 조직에 매핑되지 않은 보고서 세트에는 요청이 적용되지 않습니다. | [조직에 보고서 세트 매핑](https://docs.adobe.com/content/help/ko-KR/core-services/interface/about-core-services/report-suite-mapping.html)을 참조하십시오. |
| **2단계**: 데이터 유지 정책을 설정합니다. | Adobe에서 데이터 개인 정보 보호 데이터 액세스/삭제 요청을 처리하려면 데이터 유지 정책이 적용되어 있어야 합니다.  자세한 내용은 이 [Analytics 데이터 유지 FAQ](/help/technotes/data-retention.md)를 참조하십시오. |
| **3단계**: DULE/데이터 개인 정보 보호 레이블, Adobe Analytics ID, 네임스페이스 및 ID 확장에 대해 숙지하십시오. | 다음 설명서 세트에서 이러한 주제를 읽어 보십시오.<ul><li>[Analytics 변수의 데이터 개인 정보 보호 레이블](/help/admin/c-data-governance/gdpr-labels.md)</li><li>[레이블 지정 우수 사례](/help/admin/c-data-governance/gdpr-analytics-ids.md)</li></ul> |
| **4단계**: ID, 민감도 및 데이터 거버넌스 레이블을 보고서 세트의 각 변수에 지정합니다.  참고: 새 보고서 세트를 작성할 때마다 또는 기존 보고서 세트 내에서 새 변수를 활성화하는 경우 레이블 지정을 검토해야 합니다. 또한, 새로운 솔루션 통합이 활성화된 경우 레이블 지정이 필요할 수 있는 새로운 변수를 노출할 수 있으므로 레이블 지정을 검토해야 할 수 있습니다. 모바일 앱 또는 웹 사이트를 재구현하면 기존 변수가 사용되는 방식이 변경될 수 있으며, 이로 인해 레이블 업데이트가 필요할 수도 있습니다. | [보고서 세트 데이터에 레이블 지정](/help/admin/c-data-governance/gdpr-setup-reportsuite.md)의 지침을 따릅니다. |
| **5단계**: Adobe Data Privacy API에 연결하고 액세스 및 삭제 요청을 제출합니다. | Adobe Analytics 고객의 경우 [Adobe Experience Cloud Data Privacy API](https://www.adobe.io/apis/experienceplatform/gdpr.html)를 호출하여 고객 데이터 액세스 및 삭제에 대한 개별 데이터 개인 정보 보호 요청을 제출할 수 있습니다. [레이블 지정 우수 사례](/help/admin/c-data-governance/gdpr-analytics-ids.md) 섹션에 설명된 대로 Analytics 식별자를 해당 네임스페이스 ID(데이터 소스 ID)와 함께 요청에 제출할 수 있습니다. |
| **6단계**: 보고서 세트의 데이터 개인 정보 설정을 보고 관리합니다. | [보고서 세트의 데이터 거버넌스 설정 보기](/help/admin/c-data-governance/gdpr-view-settings.md)의 지침을 따릅니다. |
