---
title: 웹 SDK 업그레이드 도우미에서 마이그레이션 관리
description: 웹 SDK 업그레이드 도우미에서 마이그레이션을 만들고, 보고, 엽니다.
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
source-wordcount: '397'
ht-degree: 0%
---
# 마이그레이션 관리

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_migrations"
>title="마이그레이션"
>abstract="각 마이그레이션은 하나의 태그 속성에 있는 Adobe Analytics 구현을 웹 SDK으로 업그레이드합니다. 마이그레이션을 열어 중지한 지점에서 계속하거나 &#39;새로 만들기&#39;를 선택하여 시작하세요."

**[!UICONTROL 마이그레이션]** 페이지는 Web SDK 업그레이드 도우미의 시작점입니다. 각 마이그레이션의 진행 상황, 상태, 만든 사람 등 조직의 마이그레이션이 나열됩니다. 이 페이지에서는 마이그레이션을 생성하거나 기존 마이그레이션을 열 수 있습니다.

## 마이그레이션 만들기 {#create}

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_newmigration"
>title="새 마이그레이션"
>abstract="마이그레이션할 태그 속성과 해당 속성의 라이브러리를 선택합니다. 업그레이드 도우미는 마이그레이션을 만들 때 라이브러리의 스냅샷을 만듭니다. 마이그레이션 스냅숏 이후에 라이브러리에 대해 수행된 변경 사항은 포함되지 않습니다. 마이그레이션을 완료할 때까지 태그 속성이 변경되지 않습니다."

<!-- markdownlint-enable MD034 -->

마이그레이션을 만들기 전에 [필수 구성 요소](overview.md#prerequisites)를 충족하는지 확인하세요.

1. **[!UICONTROL 마이그레이션]** 페이지에서 **[!UICONTROL 새로 만들기]**&#x200B;를 선택합니다.
1. 마이그레이션 이름과 설명(선택 사항)을 입력합니다.
1. 마이그레이션할 태그 속성을 선택합니다.
1. 태그 라이브러리를 선택합니다. 마이그레이션을 만들 때 업그레이드 도우미는 이 라이브러리에 있는 대로 구현 스냅숏을 만듭니다. 이후에 라이브러리에 수행한 변경 사항은 마이그레이션에 반영되지 않습니다.
1. **[!UICONTROL 만들기]**&#x200B;를 선택합니다.

새 마이그레이션이 목록에 나타납니다. [구성 요소 선택](component-selection.md)을 시작하려면 여세요.

## 마이그레이션 열기 {#open}

마이그레이션 이름을 선택하여 엽니다. 마이그레이션 단계가 왼쪽 탐색에 나타납니다. 완료된 단계로 돌아가서 원하는 만큼 자주 검토하거나 변경할 수 있지만 아직 도달하지 않은 단계는 사용할 수 없습니다.

업그레이드 도우미는 단계를 진행할 때 진행 상황을 저장하므로 마이그레이션을 종료하고 나중에 다시 볼 수 있습니다. [마이그레이션을 완료](final-review.md#finalize)할 때까지 구성한 항목이 적용되지 않습니다. 마이그레이션을 완료하면 마이그레이션이 읽기 전용으로 설정됩니다. 여전히 열어 만든 내용을 볼 수 있지만 변경할 수는 없습니다.

## 기타 마이그레이션 작업 {#actions}

마이그레이션 행을 선택하여 사용 가능한 작업을 표시합니다.

* **[!UICONTROL 계속]**: 마이그레이션을 엽니다.
* **[!UICONTROL 중복 실행]**: 마이그레이션의 복사본을 만듭니다.
* **[!UICONTROL 이름 바꾸기]**: 마이그레이션의 이름과 설명을 변경합니다.
* **[!UICONTROL 보관]**: 마이그레이션 상태를 **[!UICONTROL 보관]**(으)로 변경합니다.
* **[!UICONTROL 마이그레이션 삭제]**: 마이그레이션을 영구적으로 삭제합니다. 실행을 취소할 수 없습니다.
