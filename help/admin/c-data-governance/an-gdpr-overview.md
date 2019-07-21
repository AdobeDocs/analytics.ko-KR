---
description: 이 문서에서는 데이터 주체의 GDPR 액세스 및 삭제 권한을 지원하기 위해 Adobe Analytics에서 수행해야 하는 작업에 대해 설명합니다.
seo-description: 이 문서에서는 데이터 주체의 GDPR 액세스 및 삭제 권한을 지원하기 위해 Adobe Analytics에서 수행해야 하는 작업에 대해 설명합니다.
seo-title: Adobe Analytics 및 GDPR
title: Adobe Analytics 및 GDPR
uuid: 16 fd 5 af 8-9148-4 e 09-ad 54-9 e 3 cdd 2 b 3 c 6 d
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Adobe Analytics 및 GDPR

이 문서에서는 데이터 주체의 GDPR 액세스 및 삭제 권한을 지원하기 위해 Adobe Analytics에서 수행해야 하는 작업에 대해 설명합니다.

## Adobe 개요 {#section_E582A1D77583410EBB790BB646854A2C}

>[!IMPORTANT]
>
>이 문서의 내용은 법률적인 조언이 아니며, 법률적인 조언을 대체하지 않습니다. GDPR에 대한 자세한 내용은 회사의 법무 부서에 문의하십시오.

2018 년 5 월 25 일, 유럽 연합의 개인 정보 보호 규정 (GDPR) 이 발효되었습니다. Adobe의 대응 및 Adobe 고객에게 GDPR이 의미하는 바에 대한 자세한 내용은 [GDPR 및 비즈니스](https://www.adobe.com/privacy/general-data-protection-regulation.html)를 참조하십시오.

Adobe에서는 기업에 소프트웨어 및 서비스를 제공할 때 서비스 제공의 일부로 고객을 대신하여 수신 및 저장하는 개인 데이터에 대한 데이터 처리자 역할을 합니다. Adobe는 데이터 처리자로서 회사의 사용 권한 및 지침에 따라(예: Adobe와의 계약에 명시된 대로) 개인 데이터를 처리합니다.

데이터 관리자는 Adobe가 귀하를 대신하여 처리하는 개인 데이터를 결정합니다. Adobe Experience Cloud 솔루션을 사용하는 경우 Adobe에서는 사용자가 사용하는 솔루션 및 Adobe Experience Cloud 계정에 전송하기 위해 선택한 정보에 따라 개인 데이터를 호스팅할 수 있습니다. 예제 목록은 [Adobe Experience Cloud 개인 정보](https://www.adobe.com/privacy/marketing-cloud.html#collect)를 참조하십시오.

![](assets/gdpr_ready.png)

## Adobe에서 GDPR 데이터를 처리하는 방법 {#section_A20BCC08A80B410D97601BFB1CAF83F1}

ACP(Adobe Cloud Platform)는 사용자 브랜드의 데이터 거버넌스 인프라와 이 인프라가 소비자 경험을 생성하고 관리하는 데 사용하는 Adobe 도구를 연결하는 통합 솔루션을 제공합니다. Adobe Cloud Platform의 데이터 거버넌스 기능을 사용하면 데이터 거버넌스 정책을 데이터 사용에 직접 연결할 수 있습니다.

GDPR 준비 단계 및 Adobe Experience Cloud GDPR API와 통합하는 방법에 대해 나와 있는 [Adobe Analytics에서 GDPR을 처리하는 방법](https://www.adobe.com/data-analytics-cloud/analytics/general-data-protection-regulation.html)을 숙지하십시오.

## GDPR 준비 및 Adobe Analytics 데이터 {#section_9A47CDCD614C42238F6E05CFF0180195}

사용자가 보고서 세트의 사용자 지정 데이터를 가장 잘 알고 있기 때문에 Adobe는 사용자에게 데이터 거버넌스 설정 및 환경 설정을 정의할 수 있는 기회를 제공하고 있습니다.

이를 위해 Adobe Analytics는 사용자가 데이터 제어자로서 Analytics 보고서 세트와 그러한 보고서 세트의 모든 차원과 지표에 대한 [개인 정보 레이블](../../admin/c-data-governance/gdpr-labels.md#concept_F4061E29353446B5B0A7CF248D54E6F2)을 설정할 수 있는 데이터 거버넌스 사용자 인터페이스를 제공합니다. 사용자는 직접 식별 가능한 데이터 또는 간접적으로 식별 가능한 데이터가 포함된 데이터 세트의 열을 식별할 수 있으므로 액세스 및 삭제 요청을 제출하여 해당 데이터를 처리할 수 있습니다. 각 요청마다 Analytics 데이터 거버넌스 사용자 인터페이스에 정의된 레이블이 해당 요청에 해당하는 특정 식별자에 대해 적용됩니다.

레이블을 설정하는 방법에 대한 자세한 내용은 [보고서 세트 데이터에 레이블 지정](../../admin/c-data-governance/gdpr-setup-reportsuite.md#concept_FAA948AD8CEA4BC38CB482EAF3648731)을 참조하십시오.

## 전제 조건 {#section_3C766371CE0641C0821FE8E750E5AE0C}

* [GDPR 용어](../../admin/c-data-governance/gdpr-terminology.md#concept_83C744A9D077476BAD8F8492DF68EBD7)를 숙지합니다.
* Experience Cloud 조직에 로그인 회사를 연결하지 않은 경우 연결합니다. Adobe 고객 지원 센터에 문의하여 [조직 및 계정 연결](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html)을 참조하십시오.
* 데이터 거버넌스에 대해 설정하려는 모든 Adobe Analytics 보고서 세트를 [Experience Cloud 조직](https://marketing.adobe.com/resources/help/en_US/mcloud/report-suite-mapping.html)에 매핑합니다.
* GDPR 삭제 및 액세스 요청을 적용할 수 있도록 각 보고서 세트에 대한 데이터 보존 정책을 설정합니다.

   >[!NOTE]
   >
   >Adobe Analytics는 Adobe Analytics에 데이터 보유 기간이 설정되어 있지 않은 경우, GDPR API에 대한 처리 요청 (예: 최종 사용자로부터 처리 액세스 또는 삭제 요청 처리) 를 지원할 수 없습니다. 데이터 보존 기간을 설정하려면 Customer Success Manager에 문의하십시오.

* 사용 권한을 확인합니다. Adobe Analytics의 데이터 거버넌스 관리 인터페이스를 사용하려면 Adobe Analytics 관리자여야 합니다.

