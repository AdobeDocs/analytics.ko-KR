---
description: 이 문서에서는 데이터 주체의 CCPA 액세스 및 삭제 권한을 지원하기 위해 Adobe Analytics에서 수행해야 하는 작업에 대해 설명합니다.
title: Adobe Analytics 및 CCPA
feature: Data Governance
role: Admin
exl-id: 1f37e72b-99e4-4833-a506-98c8ec415757
source-git-commit: 48f1974a0c379a4e619d9a04ae80e43cce9527c1
workflow-type: ht
source-wordcount: '593'
ht-degree: 100%

---

# Adobe Analytics 및 CCPA

이 문서에서는 데이터 주체의 CCPA 액세스 및 삭제 권한을 지원하기 위해 Adobe Analytics에서 수행해야 하는 작업에 대해 설명합니다.

## Adobe 개요

>[!IMPORTANT]
>
>이 문서의 콘텐츠는 법률적인 조언이 아니며, 법률적인 조언을 대체하지 않습니다. CCPA에 대한 자세한 내용은 회사의 법무 부서에 문의하십시오.

2020년 1월 1일부터 CCPA(California Consumer Privacy Act)가 시행됩니다. Adobe의 대응 및 Adobe 고객에게 CCPA가 의미하는 바에 대한 자세한 내용은 [Adobe 개인정보 센터](https://www.adobe.com/kr/privacy.html)를 참조하십시오.

Adobe에서는 기업에 소프트웨어 및 서비스를 제공할 때 서비스 제공의 일부로 고객을 대신하여 수신 및 저장하는 개인 데이터에 대한 데이터 처리자 역할을 합니다. Adobe는 데이터 처리자로서 귀사의 허가 및 지침(예: Adobe와의 계약에 명시된 내용)에 따라 개인 데이터를 처리합니다.

귀하는 데이터 제어자로서 Adobe가 귀하를 대신하여 처리하고 저장하는 개인 데이터를 결정합니다. Adobe Experience Cloud 솔루션을 사용하는 경우 Adobe에서는 사용자가 사용하는 솔루션 및 Adobe Experience Cloud 계정에 전송하기 위해 선택한 정보에 따라 개인 데이터를 호스팅할 수 있습니다. 예제 목록은 [Adobe Experience Cloud 개인정보](https://www.adobe.com/kr/privacy/marketing-cloud.html#collect)를 참조하십시오.

## Adobe에서 CCPA 데이터를 처리하는 방법

Adobe Experience Cloud는 사용자 브랜드의 데이터 거버넌스 인프라와 이 인프라가 소비자 경험을 생성하고 관리하는 데 사용하는 Adobe 도구를 연결하는 통합 솔루션을 제공합니다. Adobe Experience Cloud의 데이터 거버넌스 기능을 사용하면 데이터 거버넌스 정책을 데이터 사용에 직접 연결할 수 있습니다.

개인정보 준비 단계 및 Adobe Experience Cloud 개인정보 서비스 API와 통합하는 방법에 대해 나와 있는 [Adobe Analytics에서 GDPR을 처리하는 방법](https://www.adobe.com/kr/data-analytics-cloud/analytics/general-data-protection-regulation.html)을 숙지하십시오.

## CCPA 준비 및 Adobe Analytics 데이터

사용자가 보고서 세트의 사용자 정의 데이터를 가장 잘 알고 있기 때문에 Adobe는 사용자에게 데이터 거버넌스 설정 및 환경 설정을 정의할 수 있는 기회를 제공하고 있습니다.
이를 위해 Adobe Analytics는 사용자가 데이터 제어자로서 Analytics 보고서 세트와 그러한 보고서 세트의 모든 차원과 지표에 대한 [개인정보 레이블](/help/admin/admin/c-data-governance/data-labeling/gdpr-labels.md#data-governance-labels)을 설정할 수 있는 데이터 거버넌스 사용자 인터페이스를 제공합니다. 사용자는 직접 식별 가능한 데이터 또는 간접적으로 식별 가능한 데이터가 포함된 데이터 세트의 열을 식별할 수 있으므로 액세스 및 삭제 요청을 제출하여 해당 데이터를 처리할 수 있습니다. 각 요청마다 Analytics 데이터 거버넌스 사용자 인터페이스에 정의된 레이블이 해당 요청에 해당하는 특정 식별자에 대해 적용됩니다.

레이블 설정 방법에 대한 자세한 내용은 [보고서 세트 데이터에 레이블 지정](/help/admin/admin/c-data-governance/data-labeling/gdpr-setup-reportsuite.md)을 참조하십시오.

## 사전 요구 사항

* [GDPR 용어](/help/admin/c-data-governance/gdpr-terminology.md)를 숙지합니다.
* Experience Cloud 조직에 로그인 회사를 연결하지 않은 경우 연결합니다. Adobe 고객 지원 센터에 문의하여 [조직 및 계정 연결](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/organizations.html?lang=ko-KR)을 참조하십시오.
* CCPA 삭제 및 액세스 요청을 적용할 수 있도록 각 보고서 세트에 대한 데이터 보존 정책을 설정합니다.

  데이터 보존 기간을 Adobe Analytics에 설정하지 않은 경우 Adobe Analytics에서 Privacy Service API에 대한 요청 처리, 즉 최종 사용자로부터 받은 액세스 또는 삭제 요청 처리를 지원할 수 없습니다. 데이터 보존 기간을 설정하려면 Adobe 계정 팀에 문의하십시오.

* 사용 권한을 확인합니다. Adobe Analytics의 데이터 거버넌스 관리 인터페이스를 사용하려면 Adobe Analytics 관리자여야 합니다.
* [동의 관리 변수](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md)를 구현하여 히트 수준에서 동의 상태를 추적하는 것이 좋습니다.
