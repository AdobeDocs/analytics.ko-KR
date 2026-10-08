---
title: 웹 SDK 업그레이드 도우미
description: Adobe Analytics 태그 확장을 Adobe Experience Platform 웹 SDK으로 마이그레이션하는 작업을 계획하고 실행합니다.
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
source-wordcount: '534'
ht-degree: 3%
---
# 웹 SDK 업그레이드 도우미

웹 SDK 업그레이드 도우미는 Adobe Analytics 태그 확장을 Adobe Experience Platform 웹 SDK으로 마이그레이션하는 작업을 계획하고 실행하는 데 도움이 됩니다. 안내가 있는 단일 작업 영역으로의 마이그레이션을 가져오므로 구조화되고 추적 가능한 방식으로 기존 태그 구현에서 웹 SDK으로 이동할 수 있습니다.

## 업그레이드 도우미 작동 방식 {#how-it-works}

각 마이그레이션은 하나의 태그 속성에서 Adobe Analytics 구현과 함께 작동합니다. 업그레이드 도우미는 웹 SDK 작업을 제거하지 않고 기존 규칙에 웹 Adobe Analytics 작업을 추가하므로 구현은 웹 SDK과 함께 데이터를 Adobe Analytics에 계속 전송합니다.

업그레이드 도우미는 Adobe Analytics 구성 요소만 변환합니다. Adobe Target, Adobe Audience Manager 또는 타사 확장과 같은 다른 확장의 구성 요소를 포함할 수 있지만 업그레이드 도우미는 해당 구성 요소를 Web SDK으로 변환하지 않습니다.

업그레이드 도우미는 다음 단계를 안내하고 각 단계는 이전 단계에서 내린 결정을 기반으로 합니다.

1. **[구성 요소 선택](component-selection.md)**: 마이그레이션에 포함할 규칙, 데이터 요소 및 확장을 선택합니다.
1. **[감사 결과](audit-findings.md)**: 선택한 구성 요소에 대한 선택적 정리 권장 사항을 검토합니다.
1. **[매퍼 준비](mapper-prep.md)**: 보고서 세트의 Analytics 변수를 검토하고 전달할 변수를 선택하십시오.
1. **[XDM 매핑](xdm-mapping.md)**: Analytics 변수를 XDM 스키마의 필드에 매핑합니다.
1. **[웹 SDK 구현](web-sdk-implementation.md)**: 업그레이드 도우미가 규칙에 추가하는 웹 SDK 작업을 검토하십시오.
1. **[최종 검토](final-review.md)**: Experience Platform 샌드박스를 선택하고 마이그레이션이 만드는 내용을 검토하고 마이그레이션을 완료합니다.

각 단계는 마이그레이션의 일부를 구성하며 완료된 단계로 돌아가서 원하는 만큼 자주 검토하거나 변경할 수 있습니다. 마이그레이션을 완료할 때까지 업그레이드 도우미는 Experience Platform에서 태그 속성을 변경하거나 아무것도 만들지 않습니다. 완료되면 업그레이드 도우미가 모든 항목을 한 번에 만들고 태그 변경 내용을 새 라이브러리에 추가합니다. 그런 다음 해당 라이브러리를 테스트하고 태그 게시 플로우를 사용하여 프로덕션에 게시합니다.

>[!IMPORTANT]
>
>업그레이드 도우미는 AI(인공 지능)를 사용하여 XDM 필드 매핑 및 웹 SDK 규칙 구성과 같은 권장 사항을 생성합니다. 이러한 권장 사항은 정확하지 않거나 완전하지 않을 수 있습니다. 변경 사항을 프로덕션에 게시하기 전에 확인하십시오.

## 사전 요구 사항 {#prerequisites}

마이그레이션을 만들기 전에 다음을 수행해야 합니다.

* 업그레이드 도우미에 필요한 [권한](#permissions)입니다.
* Adobe Analytics 확장을 사용하는 태그 속성입니다.
* 마이그레이션할 구현이 포함된 해당 속성의 라이브러리입니다. 라이브러리는 published를 포함하여 모든 상태에 있을 수 있습니다. 태그 사용 안내서에서 [라이브러리](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/publishing/libraries)를 참조하십시오.

### 권한 {#permissions}

업그레이드 도우미에는 다음 액세스 권한이 필요합니다. 조직의 Experience Platform 제품 관리자와 협력하여 누락된 권한을 가져옵니다.

| 액세스 유형 | 필수 여부 |
| --- | --- |
| [Experience Platform 권한](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#permissions) | <ul><li>[!UICONTROL 스키마 보기]</li><li>[!UICONTROL 스키마 관리]</li><li>[!UICONTROL 데이터 세트 보기]</li><li>[!UICONTROL 데이터 세트 관리]</li><li>[!UICONTROL ID 네임스페이스 보기]</li></ul> |
| 제품 액세스 | <ul><li>데이터 수집(태그)</li><li>Adobe Analytics</li></ul> |
| [태그 권한](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/administration/user-permissions) | [!UICONTROL 속성 관리] |

준비가 되면 [마이그레이션을 만듭니다](manager.md#create).
