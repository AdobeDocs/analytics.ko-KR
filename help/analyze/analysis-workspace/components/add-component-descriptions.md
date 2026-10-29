---
description: 관리자가 보고서 세트 또는 데이터 사전을 사용하여 구성 요소에 설명을 추가하는 방법을 알아봅니다.
title: 구성 요소 설명 추가
feature: Components
role: Admin
exl-id: db36ee4a-66e2-45d1-8b7a-49570b5fce93
TQID: https://experienceleague.adobe.com/8z9vnSfrxEb1nkOlTTlHrp3BdElFJmTjbsSLBGbE7Gs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
    internal-label: Dashboards
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
    internal-label: Components
  - id: c45e2849-b5ab-4ac6-8df1-bbe34c2dd79e
    internal-label: Data Dictionary
  - id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2
    internal-label: VRS
  - id: ef60b66e-5984-4336-ba72-6d978b1b6f87
    internal-label: Report suites
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: b3d9fb81837398b349496ec261dc1d0ba3df3645
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 20%
---
# 구성 요소 설명 추가

설명을 통해 Analysis Workspace에서 프로젝트를 구축하거나 보고서를 볼 때 다양한 구성 요소를 가장 잘 사용하는 방법을 알 수 있습니다.

Analytics 관리자는 보고서 세트 내에 있거나 Analysis Workspace 내에서 직접 데이터 사전을 사용하여 구성 요소(차원, 지표, 세그먼트 및 날짜 범위)에 대한 설명을 추가할 수 있습니다.

## 보고서 세트

보고서 세트의 구성 요소에 설명을 추가할 수 있습니다.

1. **[!UICONTROL 관리자]** > **[!UICONTROL 모든 관리자]** > **[!UICONTROL 보고서 세트]**&#x200B;를 선택합니다.
1. 보고서 세트 관리자에서 구성 요소 설명을 제공할 보고서 세트를 선택합니다.
1. **[!UICONTROL 설정 편집]** > **[!UICONTROL 전환]** > **[!UICONTROL 전환 변수]**&#x200B;를 선택합니다.
1. 전환 변수에 대한 세부 정보를 표시하려면 ![추가](/help/assets/icons/Add.svg)를 선택하십시오.
1. **[!UICONTROL 설명]**&#x200B;에 대한 확인란을 선택하고 설명을 추가하십시오.
1. 설명을 추가할 다른 변수에 대해 4단계와 5단계를 반복합니다.
1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.

>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [구성 요소 설명 추가](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/intro-to-analytics/customizing-the-ui/adding-dimension-and-metric-descriptions){target="_blank"}를 참조하십시오.

>[!ENDSHADEBOX]


## 데이터 사전 {#add-descriptions}

Analysis Workspace의 데이터 사전을 통해 사용자와 관리자 모두가 Analytics 환경의 구성 요소를 추적하고 더 잘 이해할 수 있습니다. 데이터 사전을 사용하면 Analytics 관리자가 Analysis Workspace 내에서 직접 구성 요소 설명을 추가할 수 있습니다.

데이터 사전의 구성 요소 설명을 편집하는 방법에 대한 자세한 내용은 [데이터 사전의 구성 요소 항목 편집](/help/analyze/analysis-workspace/components/data-dictionary/edit-entries-data-dictionary.md)을 참조하십시오.

데이터 사전에 대한 일반적인 정보는 [데이터 사전 개요](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md)를 참조하십시오.

>[!MORELIKETHIS]
>
>[보고서 구성 요소 설정](/help/components/vrs/vrs-components.md)
>[데이터 사전 구성 요소 항목](/help/analyze/analysis-workspace/components/data-dictionary/edit-entries-data-dictionary.md)
>

## 자동으로 설명 생성

{{release-limited-testing-section}}

Adobe Analytics은 각 설명을 수동으로 작성하는 대신 생성 AI를 사용하여 설명을 작성할 수 있습니다. 단일 구성 요소에 대한 설명을 생성하거나 동시에 여러 구성 요소에 대한 설명을 생성할 수 있습니다.

생성된 설명:

* 길이는 3문장밖에 되지 않습니다.
* **[!UICONTROL AI를 사용하여 Adobe에서 생성됨]**&#x200B;이라는 텍스트로 끝나므로 사용자는 설명이 생성되었음을 알 수 있습니다.
* 생성된 후 편집할 수 있습니다.

### 사전 요구 사항

설명을 생성하려면 먼저 조직에서 특정 생성 AI 법률 약관에 동의해야 합니다. 조직에서 이 약관에 동의하지 않은 경우 설명을 생성하는 옵션이 흐리게 표시됩니다. 옵션 옆에 있는 정보 아이콘 ![정보](/help/assets/icons/InfoOutline.svg)을(를) 선택하여 기능을 사용하도록 설정하는 방법을 배우거나 조직의 관리자 또는 Adobe 계정 팀에 문의하십시오.

### 설명을 생성하는 방법

생성된 설명은 구성 요소의 정의 및 구성 요소가 보고서 세트에 사용되는 방법에 대한 추가 컨텍스트를 기반으로 합니다. 예를 들면 다음과 같습니다.

* 차원의 상위 항목
* 구성 요소와 함께 자주 사용되는 구성 요소

계산된 지표 또는 세그먼트가 다른 세그먼트를 참조할 때 생성된 설명은 참조된 세그먼트의 정의를 설명합니다.

### 다양한 위치에서 설명 생성

Adobe Analytics의 다음 영역에서 설명을 생성할 수 있습니다. 일부 위치에서는 여러 구성 요소에 대한 설명을 생성할 수 있지만 다른 위치에서는 생성하지 않습니다.

설명을 생성하는 방법을 배우려면 위치를 선택하십시오.

| 위치 | 지원되는 구성 요소 | 단일 구성 요소 | 여러 구성 요소 |
| --- | --- | --- | --- |
| [데이터 사전](/help/analyze/analysis-workspace/components/data-dictionary/edit-entries-data-dictionary.md) | <ul><li>차원</li><li>지표</li><li>계산된 지표</li><li>세그먼트</li><li>날짜 범위</li></ul> | 예 | 예 |
| [세그먼트 빌더](/help/components/segmentation/segmentation-workflow/seg-build.md) | 세그먼트 | 예 | 아니요 |
| [세그먼트 관리자](/help/components/segmentation/segmentation-workflow/seg-manage.md#action-bar) | 세그먼트 | 아니요 | 예 |
| [계산된 지표 빌더](/help/components/calculated-metrics/workflow/c-build-metrics/cm-build-metrics.md) | 계산된 지표 | 예 | 아니요 |
| [계산된 지표 관리자](/help/components/calculated-metrics/workflow/cm-manager.md#action-bar) | 계산된 지표 | 아니요 | 예 |
| [날짜 범위 빌더](/help/analyze/analysis-workspace/components/calendar-date-ranges/create.md#date-range-builder) | 날짜 범위 | 예 | 아니요 |
| [날짜 범위 관리자](/help/analyze/analysis-workspace/components/calendar-date-ranges/manage.md#action-bar) | 날짜 범위 | 아니요 | 예 |

{style="table-layout:auto"}