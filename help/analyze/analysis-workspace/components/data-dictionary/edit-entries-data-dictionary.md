---
description: Analysis Workspace의 데이터 사전을 사용하면 용도, 승인, 중복 등의 Analysis Workspace의 다양한 구성 요소를 분류하고 추적할 수 있습니다.
title: 데이터 사전의 항목 편집
feature: Components
role: Admin
source-git-commit: 7e105b4cd22187411dedd663080703e6daec91f5
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 63%

---

# 데이터 사전의 구성 요소 항목 편집

{{release-limited-testing}}

Analytics 관리자는 지정된 보고서 세트에 대한 데이터 사전의 구성 요소 항목을 편집할 수 있습니다. 모든 변경 사항은 보고서 세트의 모든 사용자에게 표시됩니다.

데이터 사전의 구성 요소를 편집하는 방법:

1. 편집할 구성 요소가 포함된 Analysis Workspace 프로젝트로 이동합니다.

1. Analysis Workspace의 왼쪽 레일에서 **데이터 사전** 아이콘을 선택합니다. (데이터 사전에 액세스하는 다른 방법은 [데이터 사전 개요](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md)의 “데이터 사전 액세스”에 설명되어 있음)

   데이터 사전 창이 표시됩니다.

   ![데이터 사전 관리자 보기](assets/data-dictionary-admin.png)

1. 드롭다운 메뉴에서 올바른 보고서 세트가 선택되었는지 확인하십시오. 기본적으로 이미 있는 보고서 세트가 표시됩니다.

1. (선택 사항) 검색 필드에서 편집하려는 구성 요소의 이름을 입력하기 시작합니다.

   구성 요소 이름 옆에 구성 요소 유형을 나타내는 아이콘이 표시됩니다.

   | 아이콘 | 의미 |
   |---------|----------|
   | ![Dimension 아이콘](assets/dimension-icon.png) | 다음을 나타냅니다 **차원**. Dimension은 Adobe에서 제공합니다. 기존 차원을 수정할 수 없으며 새 차원을 만들 수 없습니다. |
   | ![지표 아이콘](assets/default-metric-icon.png) | 다음을 나타냅니다 **표준 지표** (계산되지 않음). 표준 지표는 Adobe에서 제공하며 수정할 수 없습니다. |
   | ![Adobe 아이콘](assets/default-calc-metric-icon.png) | 다음을 나타냅니다 **계산된 지표 템플릿** 또는 **세그먼트 템플릿**. 이러한 구성 요소는 Adobe에서 제공하므로 수정할 수 없습니다. |
   | ![계산기 아이콘](assets/calculated-metric-icon-created.png) | 다음을 나타냅니다 **계산된 지표** 이는 조직의 Analytics 관리자가 만들었습니다. |
   | ![세그먼트 아이콘](assets/segment-icon.png) | 다음을 나타냅니다 **세그먼트**. 이러한 세그먼트는 Adobe이 제공하거나 조직의 Analytics 관리자가 만들 수 있습니다. |
   | ![날짜 범위 아이콘](assets/date-range-icon.png) | 다음을 나타냅니다 **날짜 범위**. 이 날짜 범위는 Adobe이 제공하거나 조직의 Analytics 관리자가 만들 수 있습니다. |

{{dd-filter-criteria}}

1. 구성 요소 목록에서 편집할 구성 요소를 선택합니다.

1. 구성 요소 이름 옆에 있는 **편집** 아이콘 ![데이터 사전 편집 아이콘](assets/data-dictionary-edit-icon.png)을 선택합니다.

1. 구성 요소에 대한 다음 정보를 편집합니다.

   {{dd-component-information}}

1. **저장** 아이콘 ![데이터 사전 저장 아이콘](assets/data-dictionary-save-icon.png)을 클릭하여 변경 사항을 저장합니다.
