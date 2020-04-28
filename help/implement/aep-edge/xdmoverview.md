---
title: Analytics에서 XDM 데이터 사용
description: 'Adobe Analytics에서 경험 플랫폼의 XDM 데이터 사용 개요 '
translation-type: tm+mt
source-git-commit: 31efa43043120b68de90e817a7980addbe2ded39

---




# Adobe Experience Platform Edge 데이터를 Analytics와 함께 사용

>[!IMPORTANT]
>
>Adobe Experience Edge Web SDK는 제공되지 않으며 초대받은 고객 간의 베타 테스트에만 사용할 수 있습니다. 이 설명서는 베타 사용자만을 대상으로 하며 기능의 전체 동작을 나타내지는 않습니다. 이 기능의 베타 사용자가 되고자 하는 경우 Adobe [고객 지원팀](https://helpx.adobe.com/kr/contact/enterprise-support.ec.html)에 문의하십시오.


Adobe Experience Platform( [AEP) 웹 SDK를 사용하여](https://docs.adobe.com/content/help/ko-KR/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html) 데이터를 Adobe Analytics로 전송할 수 있습니다. XDM( [경험 데이터 모델)](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html) 을 Analytics에서 사용하는 형식으로 변환하는 방식으로 작동합니다.

Analytics는 다음 두 가지 방법을 통해 XDM 데이터를 수집합니다.

* XDM 스키마에서 자동 매핑

* 컨텍스트 데이터에 대한 수동 매핑

## 자동 매핑

자동 매핑은 XDM의 기본 [스키마에](https://docs.adobe.com/content/help/en/experience-platform/xdm/schema/composition.html) 의존하여 일반적인 Analytics 데이터 수집에 포함된 JSON 개체를 자동으로 채웁니다. XDM [에서 구성된 보고서 세트에 자동으로 매핑되는](https://git.corp.adobe.com/analytics-data-collection/anedge/blob/master/XDM_Translator.md) Analytics 변수는 통합할 개발자 지원이 필요하지 않습니다.

## 수동 매핑

XDM 데이터를 Analytics에 수동으로 매핑하려면 Analytics 컨텍스트 [데이터](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/contextdata.html) 변수가 필요합니다. 이러한 변수는 적용 가능한 스키마에 해당하는 JSON 개체에 배치됩니다. 일반적으로 개발 팀은 구현 시 컨텍스트 데이터를 추가한 다음 관리자는 해당 데이터를 지정된 보고서 세트에 적용하도록 [처리 규칙을](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/t-processing-rules.html) 설정합니다.


## 설정

XDM 데이터를 수신하도록 분석을 설정하려면

1. Adobe [Experience Platform 웹 SDK](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/configuring-the-sdk.html) 설치 및 [구성](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/installing-the-sdk.html).

2. 적용 가능한 보고서 세트가 원하는 데이터에 매핑되어 있는지 확인합니다. XDM 데이터는 Adobe Experience Platform에서 보고서 세트로 자동 전송됩니다.

