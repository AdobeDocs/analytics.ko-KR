---
title: Analytics에서 XDM 데이터 사용
description: Adobe Analytics에서 Experience Platform의 XDM 데이터 사용 개요
feature: AEP Edge
exl-id: 6f1282fb-8d4a-4d88-9be0-1c939c22cb92
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 100%

---

# Analytics에서 Adobe Experience Platform Edge 데이터 사용

[AEP (Adobe Experience Platform) Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html)를 사용하여 데이터를 Adobe Analytics로 전송할 수 있습니다. [XDM (Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR)을 Analytics에서 사용하는 형식으로 변환하여 작동합니다.

Analytics는 다음 두 가지 메서드를 통해 XDM 데이터를 수집합니다.

* XDM 스키마에서 자동 매핑
* 컨텍스트 데이터에 수동 매핑

## 자동 매핑

자동 매핑은 일반적인 Analytics 데이터 수집에 포함된 JSON 개체를 자동으로 채우는 XDM의 기본 [스키마](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=ko-KR)를 사용합니다. XDM에서 구성된 보고서 세트에 자동으로 매핑된 Analytics 변수에서는 개발자 지원을 통합할 필요가 없습니다. Platform Web SDK 사용 설명서에서 [Analytics에서 자동으로 매핑된 변수](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/adobe-analytics/automatically-mapped-vars.html)를 참조하십시오.

## 수동 매핑

[](xdm-manual.md)Analytics에 대한 XDM 데이터의 수동 매핑은 [Analytics 컨텍스트 데이터](../vars/page-vars/contextdata.md) 변수를 사용합니다. 이러한 변수는 적용 가능한 스키마에 해당하는 JSON 개체에 배치됩니다. 일반적으로 개발 팀은 구현 시 컨텍스트 데이터를 추가한 다음 관리자가 [처리 규칙](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md)을 설정하여 해당 데이터를 지정된 보고서 세트에 적용합니다.

## 설정

XDM 데이터를 수신하도록 Analytics를 설정하려면 다음을 수행하십시오.

1. [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR)를 설치하고 [구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=ko-KR)합니다.

2. 적용 가능한 보고서 세트가 원하는 데이터에 매핑되어 있는지 확인합니다. XDM 데이터는 Adobe Experience Platform에서 보고서 세트로 자동 전송됩니다.
