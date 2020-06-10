---
title: Analytics에서 XDM 데이터 사용
description: 'Adobe Analytics에서 Experience Platform의 XDM 데이터 사용 개요 '
translation-type: tm+mt
source-git-commit: a28a05047e95d12343fd94f7b11e5cabf7fac070
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 100%

---


# Analytics에서 Adobe Experience Platform Edge 데이터 사용

[AEP(Adobe Experience Platform) Web SDK](https://docs.adobe.com/content/help/ko-KR/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html)를 사용하여 데이터를 Adobe Analytics로 전송할 수 있습니다. [XDM(Experience Data Model)](https://docs.adobe.com/content/help/ko-KR/experience-platform/xdm/home.html)을 Analytics에서 사용하는 형식으로 변환하여 작동합니다.

Analytics는 다음 두 가지 메서드를 통해 XDM 데이터를 수집합니다.

* XDM 스키마에서 자동 매핑
* 컨텍스트 데이터에 수동 매핑

## 자동 매핑

[](xdm-manual.md)자동 매핑은 일반적인 Analytics 데이터 수집에 포함된 JSON 개체를 자동으로 채우는 XDM의 기본 [스키마](https://docs.adobe.com/content/help/ko-KR/experience-platform/xdm/schema/composition.html)를 사용합니다. XDM에서 구성된 보고서 세트에 자동으로 매핑된 Analytics 변수에서는 개발자 지원을 통합할 필요가 없습니다.

## 수동 매핑

Analytics에 대한 XDM 데이터의 수동 매핑은 [Analytics 컨텍스트 데이터](../vars/page-vars/contextdata.md) 변수를 사용합니다. 이러한 변수는 적용 가능한 스키마에 해당하는 JSON 개체에 배치됩니다. 일반적으로 개발 팀은 구현 시 컨텍스트 데이터를 추가한 다음 관리자가 [처리 규칙](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md)을 설정하여 해당 데이터를 지정된 보고서 세트에 적용합니다.

## 설정

XDM 데이터를 수신하도록 Analytics를 설정하려면 다음을 수행하십시오.

1. [Adobe Experience Platform Web SDK](https://docs.adobe.com/content/help/ko-KR/experience-platform/edge/fundamentals/configuring-the-sdk.html)를 설치하고 [구성](https://docs.adobe.com/content/help/ko-KR/experience-platform/edge/fundamentals/installing-the-sdk.html)합니다.

2. 적용 가능한 보고서 세트가 원하는 데이터에 매핑되어 있는지 확인합니다. XDM 데이터는 Adobe Experience Platform에서 보고서 세트로 자동 전송됩니다.
