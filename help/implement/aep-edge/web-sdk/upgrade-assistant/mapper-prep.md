---
title: 웹 SDK 업그레이드 도우미의 매퍼 준비
description: 보고서 세트에서 Analytics 변수를 검토하고 XDM 매핑으로 진행할 변수를 선택합니다.
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
source-wordcount: '507'
ht-degree: 0%
---
# 매퍼 준비

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_mapperprep"
>title="매퍼 준비"
>abstract="태그 속성이 각 보고서 세트에 보내는 Analytics 변수를 검토합니다. 여기서 선택하는 변수는 XDM 매핑으로 전달됩니다. 탭을 사용하여 최근 데이터를 확인하고, 중복 변수를 찾고, 보고서 세트 간 설정을 비교할 수 있습니다."

<!-- markdownlint-enable MD034 -->

업그레이드 도우미는 태그 속성이 데이터를 보내는 보고서 세트를 식별한 다음 구현의 Analytics 변수를 각 보고서 세트의 구성 및 최근 데이터와 비교합니다. 이 단계를 사용하여 [XDM 매핑](xdm-mapping.md)에 전달할 변수를 결정하십시오.

업그레이드 도우미는 보고서 세트를 사용하여 구현에서 설정하는 변수와 구성 방법을 이해합니다. 활동 데이터는 지난 90일을 포함합니다.

## 변수 활동 {#variable-activity}

**[!UICONTROL 변수 활동]** 탭에는 [변수 분석](#variable-analysis)에서 매핑하도록 선택한 보고서 세트에 대한 Analytics 변수가 나열되며, 각 보고서 세트가 지난 90일 동안 데이터를 수집했는지 여부를 보여 줍니다.

선택하는 변수는 XDM 매핑으로 전달됩니다. 더 이상 데이터를 수집하지 않거나 웹 SDK 구현에서 필요하지 않은 변수를 지우는 것이 좋습니다. 최근 활동이 없는 변수가 계속 사용 중일 수 있습니다. 예를 들어 계절이거나 트래픽이 낮은 경우 이를 지우려면 먼저 필요하지 않은지 확인하십시오.

전달하는 각 목록 변수 및 목록 prop에 대해 해당 값을 구분하는 구분 기호를 입력합니다. 업그레이드 도우미는 Adobe Analytics에서 구분 기호를 가져올 수 없으며 각 구분 기호에 구분 기호가 있을 때까지 계속할 수 없습니다.

## 변수 분석 {#variable-analysis}

태그 속성이 둘 이상의 보고서 세트에 데이터를 전송하는 경우 먼저 매핑할 보고서 세트를 선택합니다. **[!UICONTROL 변수 분석]** 탭은 매핑하기 전에 결정이 필요할 수 있는 변수에 플래그를 지정합니다.

* 동일한 데이터를 수집하는 것처럼 보이는 변수입니다. 동일한 정보를 캡처하는지 확인한 다음, 이러한 정보를 단일 변수로 병합할지 또는 별도로 유지할지 여부를 결정합니다.
* 최근에 데이터를 수집하지 않은 변수입니다.
* 값이 모두 &quot;지정되지 않음&quot;인 변수.

## 보고서 세트 비교 {#compare}

Tags 속성이 둘 이상의 보고서 세트에 데이터를 전송하는 경우 **[!UICONTROL 보고서 세트 비교]** 탭은 최대 3개의 해당 보고서 세트에서 각 변수의 설정을 비교합니다. 스키마에 매핑하기 전에 보고서 세트 간에 다르게 구성된 변수를 찾는 데 사용합니다.

## 보고서 세트 데이터 업데이트 {#refresh}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_mapperprep_refresh"
>title="보고서 세트 데이터 새로 고침"
>abstract="변수 설정 및 최근 데이터를 포함하여 이 태그 속성에 연결된 보고서 세트를 다시 검사한 다음 변수 분석을 다시 실행합니다. 업그레이드 도우미가 보고서 세트를 아직 찾지 못한 경우 먼저 태그 속성에서 찾습니다. 선택 및 결정은 유지됩니다."

<!-- markdownlint-enable MD034 -->

이 단계에서 업그레이드 도우미가 분석하는 보고서 세트를 변경할 수 있습니다. 마이그레이션이 진행되는 동안 보고서 세트 구성이 변경되면 **[!UICONTROL 보고서 세트 데이터 새로 고침]**&#x200B;을 선택하여 분석을 다시 실행하십시오. 업그레이드 도우미는 기존의 선택 및 결정을 유지합니다.

완료되면 **[!UICONTROL 저장 및 계속]**&#x200B;을 선택하여 [XDM 매핑](xdm-mapping.md)(으)로 이동합니다.
