---
title: 웹 SDK 업그레이드 도우미의 구성 요소 선택
description: 웹 SDK 마이그레이션에 포함할 태그 규칙, 데이터 요소 및 확장을 선택합니다.
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
source-wordcount: '401'
ht-degree: 0%
---
# 구성 요소 선택

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_componentselection"
>title="구성 요소 선택"
>abstract="이 마이그레이션에 포함할 규칙, 데이터 요소 및 확장을 선택합니다. Adobe Analytics 구현에 적극적으로 기여하는 구성 요소가 기본적으로 선택됩니다. 이후 단계는 여기에서 선택한 구성 요소에서만 작동합니다."

구성 요소 선택은 마이그레이션의 첫 번째 단계입니다. 이를 사용하여 마이그레이션에 포함할 태그 속성에서 규칙, 데이터 요소 및 확장을 선택합니다.

업그레이드 도우미는 태그 속성의 구성 요소를 **[!UICONTROL 규칙]**, **[!UICONTROL 데이터 요소]** 및 **[!UICONTROL 확장]** 탭으로 구성합니다. 각 탭에는 [마이그레이션을 만들 때](manager.md#create) 업그레이드 도우미가 사용한 라이브러리의 스냅숏을 기반으로 해당 형식의 모든 속성 구성 요소가 나열됩니다. 기본적으로 Adobe Analytics 구현에 적극적으로 기여하는 구성 요소만 선택됩니다. 구성 요소를 선택하거나 선택 취소할 수 있습니다.

**[!UICONTROL 게시됨]** 열은 각 구성 요소가 선택한 라이브러리의 일부인지 여부를 표시합니다. 라이브러리에 포함되지 않은 구성 요소는 태그 속성에 존재하지만 해당 라이브러리에는 없습니다. 이 기준으로 목록을 필터링하려면 **[!UICONTROL Source]** 필터를 사용하십시오.

Adobe Target, Adobe Audience Manager 또는 타사 확장용 구성 요소와 같이 Adobe Analytics과 관련이 없는 구성 요소를 포함할 수 있지만 업그레이드 도우미는 웹 SDK으로 변환하지 않습니다.

선택하는 구성 요소에 따라 이후 단계 작동이 결정됩니다. 예를 들어, [감사 결과](audit-findings.md)에서 정리용으로 플래그를 지정할 수 있도록 아무 것도 참조하지 않는 데이터 요소를 포함할 수 있습니다.

## 구성 요소 세부 사항 보기 {#details}

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_componentselection_tagsusage"
>title="태그 사용"
>abstract="이 구성 요소를 사용하는 규칙, 데이터 요소 및 확장입니다. 확장 사용에는 확장 구성 설정만 포함됩니다. 규칙 내의 사용량은 규칙 사용량에 나타납니다."

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_componentselection_analyticsusage"
>title="분석 사용"
>abstract="이 구성 요소가 할당되는 Adobe Analytics 변수는 변수 유형별로 그룹화됩니다."

<!-- markdownlint-enable MD034 -->

구성 요소의 이름과 사용 위치를 보여 주는 패널을 열려면 구성 요소 이름을 선택합니다.

* **[!UICONTROL 태그 사용]**: 구성 요소를 사용하는 규칙, 데이터 요소 및 확장입니다. **[!UICONTROL 확장 사용]**&#x200B;에서는 확장 구성 설정만 다룹니다. 규칙 내의 사용량은 **[!UICONTROL 규칙 사용]**&#x200B;에 나타납니다.
* **[!UICONTROL Analytics 사용]**: 변수 유형별로 그룹화된 구성 요소가 할당된 Adobe Analytics 변수입니다.

태그 UI에서 구성 요소를 보려면 패널 상단에서 해당 이름을 선택합니다.

완료되면 **[!UICONTROL 저장 및 계속]**&#x200B;을 선택하여 [감사 결과](audit-findings.md)(으)로 이동합니다.