---
title: 웹 SDK 업그레이드 도우미의 웹 SDK 구현
description: 업그레이드 도우미가 기존 태그 규칙에 추가하는 웹 SDK 작업을 검토합니다.
feature: Implementation Basics
role: Admin, Developer, Leader
badge: Beta
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: e4f5f438-eabb-4c54-9133-b817e3d125f5
    internal-label: Use cases
  - id: c24fe15a-643a-47bd-8278-5e027df49785
    internal-label: Implementation basics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 629efca210346d32b8555c60f7db15d1d8285b20
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%
---
# 웹 SDK 구현

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_websdkimplementation"
>title="웹 SDK 구현"
>abstract="업그레이드 도우미가 규칙에 추가하는 웹 SDK 작업을 검토합니다. Adobe Analytics 작업이 그대로 유지됩니다. 구성 요소를 선택하여 현재 구성과 웹 SDK 구성을 나란히 비교합니다. 대기열에 넣은 구성 요소만 마이그레이션에 추가됩니다."

<!-- markdownlint-enable MD034 -->

업그레이드 도우미는 선택한 구성 요소와 [XDM 매핑](xdm-mapping.md)을 사용하여 각 Adobe Analytics 작업 바로 다음에 규칙에 Web SDK 작업을 추가합니다. Analytics 작업은 그대로 유지되므로 이러한 규칙은 Adobe Analytics 및 웹 SDK 모두에 데이터를 전송합니다. 대부분의 데이터 요소는 변경되지 않고 전달되며 규칙은 이름별로 해당 요소를 계속 참조합니다.

**[!UICONTROL 유형 변경]** 열은 마이그레이션을 완료하면 각 구성 요소에 어떤 작업을 수행하는지 보여 줍니다.

* **[!UICONTROL 웹 SDK 작업이 추가됨]**: 업그레이드 도우미가 웹 SDK 작업을 규칙에 추가합니다.
* **[!UICONTROL 변경 없음]**: 구성 요소가 변경되지 않은 상태로 전달됩니다.
* **[!UICONTROL 차단됨]**: 업그레이드 도우미가 웹 SDK 작업을 추가하기 전에 구성 요소를 검토해야 합니다. 구성 요소를 선택하여 무엇이 차단되는지 확인합니다.

현재 구성을 웹 SDK 구성과 나란히 비교할 구성 요소를 선택합니다. 추가 컨텍스트가 필요한 경우 업그레이드 도우미가 태그 UI의 구성 요소에 연결됩니다.

대기열에 넣은 구성 요소가 마이그레이션에 추가됩니다. 구성 요소를 큐에 넣으려면 목록에서 해당 구성 요소를 선택하거나 세부 정보에서 **[!UICONTROL 큐]**&#x200B;를 선택하십시오. 다시 제거하려면 **[!UICONTROL 큐에서 제거]**&#x200B;를 선택하십시오. 업그레이드 도우미는 [마이그레이션을 완료](final-review.md#finalize)할 때까지 태그 속성을 변경하지 않습니다.

업그레이드 도우미는 AI를 사용하여 웹 SDK 작업을 생성하며 결과가 정확하지 않거나 완료되지 않을 수 있습니다. 작업을 생성해도 사이트에서 작동 방식이 확인되지 않으므로 라이브러리를 게시하기 전에 테스트하십시오.
