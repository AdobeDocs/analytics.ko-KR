---
title: 웹 SDK 업그레이드 도우미에서의 최종 검토
description: 웹 SDK 마이그레이션을 검토하고 완료한 다음 결과 태그 라이브러리를 프로덕션에 게시합니다.
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
source-wordcount: '469'
ht-degree: 0%
---
# 최종 검토

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_finalreview"
>title="최종 검토"
>abstract="사용할 Experience Platform 샌드박스를 선택한 다음 이 마이그레이션이 만들거나 변경하는 모든 것을 검토합니다. 마이그레이션을 완료할 때까지 아무 것도 변경되지 않습니다. 완료되면 업그레이드 도우미가 모든 항목을 한 번에 만들고, 태그 변경 내용을 새 라이브러리에 추가하고, 이 마이그레이션을 읽기 전용으로 만듭니다. 그런 다음 해당 라이브러리를 프로덕션에 직접 게시합니다."

<!-- markdownlint-enable MD034 -->

최종 검토는 마이그레이션의 마지막 단계입니다. 이 시각화는 마이그레이션이 Experience Platform 및 태그 속성에서 만들거나 변경하는 모든 것을 보여 줍니다.

## 마이그레이션이 만드는 내용 검토 {#review}

먼저 마이그레이션이 리소스를 생성하는 Experience Platform 샌드박스를 선택합니다. 샌드박스를 선택할 때까지 마이그레이션을 완료할 수 없습니다.

그런 다음 업그레이드 도우미는 마이그레이션을 완료하면 만들거나 변경하는 모든 것을 나열합니다.

* **[!UICONTROL XDM]**: 필요한 사용자 지정 필드 그룹과 함께 XDM 매핑 이름을 딴 새 스키마. 표준 필드 그룹이 이미 있으므로 스키마는 해당 그룹을 있는 그대로 사용합니다. 이 섹션은 [XDM 매핑](xdm-mapping.md#schema)에서 새 스키마를 만들도록 선택한 경우에만 나타납니다.
* **[!UICONTROL 데이터 세트]**: 개발용 데이터 세트와 프로덕션용 데이터 세트 두 개. 각 이름은 마이그레이션 다음에 지정됩니다(예: `My migration - Development`).
* **[!UICONTROL 데이터스트림]**: 데이터 세트와 같은 방식으로 이름이 지정된 개발용 데이터스트림과 프로덕션용 데이터스트림 두 개.
* **[!UICONTROL Adobe 태그]**: 마이그레이션 후 이름이 지정된 새 라이브러리(예: `Library - "My migration"`). 라이브러리에는 웹 SDK 작업에 필요한 확장 구성과 함께 마이그레이션이 변경되는 규칙 및 데이터 요소가 포함되어 있습니다.

## 마이그레이션 완료 {#finalize}

마이그레이션을 완료할 때까지 업그레이드 도우미는 태그 속성을 변경하거나 Experience Platform에서 아무 것도 만들지 않습니다.

>[!IMPORTANT]
>
>마이그레이션을 완료하면 읽기 전용이 됩니다. **[!UICONTROL 마이그레이션]** 페이지에서 열어 만든 내용을 볼 수 있지만 다시 변경하거나 완료할 수는 없습니다. 새 라이브러리는 아직 개발 중이므로 라이브러리를 게시하기 전에 태그 UI에서 태그 변경 사항을 편집하거나 제거할 수 있습니다.

1. **[!UICONTROL 아티팩트 만들기]**&#x200B;를 선택하십시오.
1. **[!UICONTROL 이러한 권장 사항 확인]** 대화 상자에서 **[!UICONTROL 계속]**&#x200B;을 선택합니다.
1. **[!UICONTROL 이 마이그레이션을 완료하시겠습니까?]** 대화 상자에서 **[!UICONTROL 완료]**&#x200B;를 선택합니다.

업그레이드 도우미는 모든 항목을 한 번에 만들고 진행 상황을 표시합니다. 새 라이브러리에 태그 변경 사항을 추가하지만 라이브러리는 게시되지 않습니다.

## 변경 사항 게시 {#publish}

마이그레이션을 완료한 후 태그 게시 플로우를 통해 새 라이브러리를 이동합니다.

1. 개발 환경에서 라이브러리를 빌드하고 테스트하여 웹 SDK 구현에서 예상한 데이터를 보내는지 확인합니다.
1. 승인을 위해 라이브러리를 제출하고 스테이징 환경에서 테스트합니다.
1. 라이브러리를 승인하고 프로덕션에 게시합니다.

태그 사용 안내서에서 [게시 흐름](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/publishing/publishing-flow)을 참조하십시오.
