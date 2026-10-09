---
title: 웹 SDK 업그레이드 도우미의 XDM 매핑
description: 웹 SDK 마이그레이션의 일부로 XDM 스키마의 필드에 Adobe Analytics 변수를 매핑합니다.
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
source-git-commit: 212d38950264a33b925b7281c241992cadca2bfb
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 3%
---
# XDM 매핑

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_xdmmapping"
>title="XDM 매핑"
>abstract="선택한 Analytics 변수를 XDM 스키마의 필드에 매핑합니다. 업그레이드 도우미는 AI가 제안하는 매핑을 사용하여 새 스키마를 생성하거나 이미 가지고 있는 스키마에 변수를 매핑할 수 있습니다. 계속하기 전에 모든 매핑을 검토하십시오."

<!-- markdownlint-enable MD034 -->

웹 SDK은 [XDM(Experience Data Model)](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/home) 필드를 사용하여 데이터를 전송하므로 [Mapper 준비](mapper-prep.md)에서 전달하는 각 Analytics 변수에는 XDM 스키마에서 일치하는 필드가 필요합니다. 이 단계에서는 스키마를 선택하고 변수를 해당 필드에 매핑합니다.

## 스키마 선택 {#schema}

다음 두 가지 방법 중 하나로 매핑을 빌드할 수 있습니다.

* **새 스키마를 만듭니다**: 업그레이드 도우미는 Analytics 변수를 분석하여 각 변수에 대한 XDM 필드를 제안한 다음 검토할 해당 제안에서 스키마를 생성합니다.
* **기존 스키마 사용**: Experience Platform에 이미 있는 스키마를 선택한 다음 각 변수를 직접 필드에 매핑합니다.

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_xdmmapping_fieldgroups"
>title="필드 그룹 환경 설정"
>abstract="업그레이드 도우미가 스키마를 빌드할 때 선호하는 필드 그룹 유형을 선택합니다. 표준 필드 그룹은 Adobe에 의해 정의됩니다. 사용자 정의 필드 그룹은 조직에서 정의합니다."

<!-- markdownlint-enable MD034 -->

새 스키마를 만들 때 업그레이드 도우미가 표준 또는 사용자 지정 필드 그룹을 선호하는지 여부도 선택합니다. 표준 필드 그룹은 Adobe에서 정의하는 반면, 사용자 지정 필드 그룹은 조직에서 정의합니다. XDM 설명서에서 [필드 그룹](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/schema/composition#field-group)을(를) 참조하십시오.

## 매핑 검토 {#review}

매핑에는 매핑되는 XDM 필드와 함께 각 Analytics 변수가 나열되며 전체 스키마 미리보기가 옆에 표시됩니다. 스키마를 일부 선택하여 해당 목록에 매핑되는 변수로 목록을 필터링합니다. 개별 매핑과 스키마 자체를 조정할 수 있습니다.

업그레이드 도우미는 AI를 사용하여 매핑을 제안하므로 결과가 정확하지 않거나 완전하지 않을 수 있습니다. 계속하기 전에 모든 매핑을 검토하십시오. 업그레이드 도우미는 [마이그레이션을 완료](final-review.md#finalize)할 때까지 Experience Platform에서 스키마를 만들지 않습니다.

완료되면 **[!UICONTROL 저장 및 계속]**&#x200B;을 선택하여 매핑을 저장하고 [웹 SDK 구현](web-sdk-implementation.md)(으)로 이동합니다. 매핑을 저장한 후 변경하려면 **[!UICONTROL 편집]**&#x200B;을 선택하고 변경한 다음 **[!UICONTROL 저장 및 계속]**&#x200B;을 다시 선택하십시오. 이 방법으로 저장하지 않은 변경 사항은 마이그레이션을 완료할 때 포함되지 않습니다.
