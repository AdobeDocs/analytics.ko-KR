---
description: Analysis Workspace의 데이터 사전을 사용하면 용도, 승인, 중복 등의 Analysis Workspace의 다양한 구성 요소를 분류하고 추적할 수 있습니다.
title: 데이터 사전 보기
feature: Components
role: User, Admin
source-git-commit: 8edd7b1b90e2ac3137bea734e5a0f1cb8004e743
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 62%

---

# 데이터 사전의 구성 요소 정보 보기

{{release-limited-testing}}

데이터 사전을 사용하면 구성 요소 설명, 유사한 구성 요소, 구성 요소가 자주 사용되는 다른 구성 요소 등 구성 요소에 대한 정보를 볼 수 있습니다.

데이터 사전의 구성 요소에 대한 정보 보기:

1. 확인할 구성 요소가 포함된 Analysis Workspace 프로젝트로 이동합니다.

1. Analysis Workspace의 왼쪽 레일에서 [!UICONTROL **데이터 사전**] 아이콘을 선택합니다. (데이터 사전에 액세스하는 다른 방법은 [데이터 사전 개요](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md)의 “데이터 사전 액세스”에 설명되어 있음)

   데이터 사전 창이 표시됩니다.

   ![data-dictionary.png](assets/data-dictionary.png)

   <!--double-check this screenshot. I mocked the admin view up a bit to get rid of the Dictionary health tab.-->

1. 보려는 구성 요소가 포함된 보고서 세트가 드롭다운 메뉴에서 선택되어 있는지 확인합니다. 기본적으로 이미 있는 보고서 세트가 표시됩니다.

1. (선택 사항) 검색 필드에서 확인하려는 구성 요소의 이름을 입력하기 시작합니다.

   구성 요소 이름 옆에 구성 요소 유형을 나타내는 아이콘이 표시됩니다.

   | 아이콘 | 의미 |
   |---------|----------|
   | ![Dimension 아이콘](assets/dimension-icon.png) | 다음을 나타냅니다 **차원**. Dimension은 Adobe에서 제공합니다. 기존 차원을 수정할 수 없으며 새 차원을 만들 수 없습니다. |
   | ![지표 아이콘](assets/default-metric-icon.png) | 다음을 나타냅니다 **표준 지표** (계산되지 않음). 표준 지표는 Adobe에서 제공하며 수정할 수 없습니다. |
   | ![Adobe 아이콘](assets/default-calc-metric-icon.png) | 다음을 나타냅니다 **계산된 지표 템플릿**. 이는 Adobe에서 제공하며 수정할 수 없는 계산된 지표입니다. |
   | ![계산기 아이콘](assets/calculated-metric-icon-created.png) | 다음을 나타냅니다 **계산된 지표** 이는 조직의 Analytics 관리자가 만들었습니다. <!-- Delete all the comments... Components with this icon can be modified by an Analytics administrator. New calculated metrics can be created by an Analytics administrator, as described in [Metrics](/help/analyze/analysis-workspace/components/apply-create-metrics.md). --> |
   | ![세그먼트 아이콘](assets/segment-icon.png) | 다음을 나타냅니다 **세그먼트**. 이러한 세그먼트는 Adobe이 제공하거나 조직의 Analytics 관리자가 만들 수 있습니다.<!-- Segments that were created byComponents with this icon can be modified by an Analytics administrator, as described in [Edit component entries in the Data Dictionary](/help/analyze/analysis-workspace/components/data-dictionary/edit-entries-data-dictionary.md). New calculated metrics can also be created by an Analytics administrator, as described in [Metrics](/help/analyze/analysis-workspace/components/apply-create-metrics.md). --> |
   | ![날짜 범위 아이콘](assets/date-range-icon.png) | 다음을 나타냅니다 **날짜 범위**. 이 날짜 범위는 Adobe이 제공하거나 조직의 Analytics 관리자가 만들 수 있습니다. <!-- Components with this icon can be modified by an Analytics administrator. New date ranges can also be created by an Analytics administrator, as described in [Create custom date ranges](/help/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.md). --> |

{{dd-filter-criteria}}

1. 구성 요소 목록에서 확인할 구성 요소를 선택합니다.

   구성 요소에 대한 다음 정보가 표시됩니다.

   {{dd-component-information}}

1. (선택 사항) 데이터 사전에서 Analysis Workspace로 구성 요소를 드래그합니다.