---
title: 웹 SDK 업그레이드 도우미의 감사 결과
description: 웹 SDK으로 마이그레이션하기 전에 태그 구성 요소에 대한 선택적 정리 권장 사항을 검토하고 해결하십시오.
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
source-wordcount: '335'
ht-degree: 2%
---
# 감사 결과

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_upgradeassistant_auditfindings"
>title="감사 결과"
>abstract="결과는 아무것도 참조하지 않는 데이터 요소와 같이 마이그레이션하기 전에 정리할 수 있는 규칙과 데이터 요소를 가리킵니다. 검색 결과를 수락하여 마이그레이션에 권장되는 변경 사항을 포함하거나, 구성 요소를 그대로 두는 것을 거부합니다. 데이터 소스에 이벤트에 설명을 추가합니다."

<!-- markdownlint-enable MD034 -->

업그레이드 도우미는 [구성 요소 선택](component-selection.md)에서 선택한 규칙과 데이터 요소를 확인하고 마이그레이션하기 전에 정리할 규칙에 플래그를 지정합니다.

* 통합할 수 있는 중복 규칙 또는 이벤트와 조건을 공유하는 규칙입니다
* 데이터 정확도에 영향을 줄 수 있는 규칙 작업 시퀀스
* 통합할 수 있는 중복 데이터 요소
* 사용하지 않을 수 있으며 비활성화할 수 있는 데이터 요소

데이터 소스에 이벤트에 설명을 추가합니다. 원하는 만큼 결과를 확인하거나 [Mapper 준비](mapper-prep.md)를 바로 계속할 수 있습니다.

## 검색 결과 검토 {#review}

검색 결과를 선택하여 다음을 포함한 세부 정보를 확인합니다.

* 검색 결과에 대한 설명
* 구성 요소의 현재 구성
* 구성 요소가 사용되는 위치는 태그 속성과 Adobe Analytics 모두에서

각 검색 결과에는 검색 유형에 따라 권장되는 작업이 포함됩니다. 예를 들어, 아무것도 참조하지 않는 데이터 요소에 대해 권장되는 작업은 비활성화하는 것입니다.

>[!IMPORTANT]
>
>사용되지 않음으로 플래그가 지정된 데이터 요소는 여전히 동적으로 또는 태그 외부에서 참조될 수 있습니다. 검색 결과를 수락하기 전에 제안된 변경 사항, 사용자 지정 코드, 작업 순서 및 참조를 확인하여 원하는 동작을 유지하는지 확인하십시오.

## 결과 해결 {#resolve}

검색 결과의 권장 조치를 취하면 검색 결과가 수락됩니다. 업그레이드 도우미는 마이그레이션에 변경 내용을 추가하고 [마이그레이션을 완료](final-review.md#finalize)할 때 적용합니다. 변경하지 않으려면 검색 결과를 대신 거부하십시오.

마음이 바뀌면 수락되거나 거절된 검색을 다시 열 수 있습니다. 여러 결과를 한 번에 업데이트하려면 목록에서 선택합니다.
