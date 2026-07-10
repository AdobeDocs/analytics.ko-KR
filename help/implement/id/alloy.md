---
title: 웹 SDK JavaScript 라이브러리를 사용한 방문자 식별
description: 웹 SDK JavaScript 라이브러리를 구현할 때 방문자를 올바르게 식별합니다.
exl-id: e650d6b1-6e29-4a9c-98dd-8482f50968d1
TQID: 'https://experienceleague.adobe.com/k9u260HKJg6hhs7REAQ3-uE4pHvrUPBv6x8yLjZ5tvc'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e4f5f438-eabb-4c54-9133-b817e3d125f5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 2%

---

# 웹 SDK JavaScript 라이브러리를 사용한 방문자 식별

Adobe Experience Platform 웹 SDK JavaScript 라이브러리(`alloy.js`)는 Adobe Analytics을 포함한 모든 Adobe CX 엔터프라이즈 애플리케이션에 대한 데이터 수집에 대한 통합적이고 현대적인 접근 방식을 제공합니다. 대부분의 고객은 일반적으로 [Web SDK 태그 확장](web-sdk-extension.md)을 구현하지만, Web SDK JavaScript 라이브러리를 단독으로 사용하거나 타사 태그 관리 시스템 내에서 사용할 수 있습니다. 최신 버전의 라이브러리를 다운로드하려면 GitHub에서 [Alloy](https://github.com/adobe/alloy)을(를) 참조하십시오.

ID 데이터는 XDM의 [`identityMap`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/identity/identity-map)을(를) 사용하여 사용자 지정 ID 및 여러 네임스페이스를 지원하도록 확장할 수 있습니다. Adobe에서는 고급 시나리오에 다른 ID 관리 옵션을 사용하여 ECID를 Analytics의 기본 식별자로 사용하는 것이 좋습니다.

조직에서 웹 SDK JavaScript 라이브러리를 사용하여 Adobe Analytics으로 데이터를 전송하는 경우 방문자 식별을 위해 최소 구성이 필요합니다. Experience Platform ID 서비스는 기본적으로 라이브러리에 대해 만들어지며, `configure` 명령에서 **[!UICONTROL Edge 도메인]**&#x200B;을(를) 설정해야 합니다. 이 필드를 원하는 값으로 설정하면 추가 구성 없이 방문자 식별이 작동합니다.
