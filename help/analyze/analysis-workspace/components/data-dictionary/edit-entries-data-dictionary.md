---
description: Analysis Workspace의 데이터 사전을 사용하면 Analysis Workspace에서 의도한 사용, 승인된 사용, 중복 등을 포함하여 다양한 구성 요소를 카탈로그화하고 추적할 수 있습니다.
title: 데이터 사전의 항목 편집
feature: Components
role: Admin
exl-id: 4f15cad2-596e-41c3-89aa-4456d8e94fa0
source-git-commit: 8f7c6a0d1477b599b05aeb7b74c4ee96531d294d
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 85%

---

# 데이터 사전의 구성 요소 항목 편집

Analytics 관리자는 지정된 보고서 세트에 대한 데이터 사전의 구성 요소 항목을 편집할 수 있습니다. 모든 변경 사항은 보고서 세트의 모든 사용자에게 표시됩니다.

데이터 사전의 구성 요소를 편집하는 방법:

1. 편집할 구성 요소가 포함된 Analysis Workspace 프로젝트로 이동합니다.

1. Analysis Workspace의 왼쪽 레일에서 **데이터 사전** 아이콘을 선택합니다. 데이터 사전에 액세스하는 다른 방법은 [데이터 사전 액세스](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md#access-the-data-dictionary)에 설명되어 있습니다.

   데이터 사전 창이 표시됩니다.

   ![데이터 사전 관리자 보기](assets/data-dictionary-admin.png)

1. 드롭다운 메뉴에서 올바른 보고서 세트가 선택되었는지 확인하십시오. 기본적으로 이미 있는 보고서 세트가 표시됩니다.

1. (선택 사항) 검색 필드에서 편집하려는 구성 요소의 이름을 입력하기 시작합니다.

   구성 요소 유형은 색상 및 아이콘으로 식별할 수 있습니다. **차원**(![차원 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Data_18_N.svg))은 주황색, **세그먼트**(![세그먼트 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg))는 파란색, **날짜 범위**(![날짜 범위 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg))는 보라색, **지표**(![지표 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg))는 녹색입니다. Adobe 아이콘은 계산된 지표 템플릿 또는 세그먼트 템플릿을 나타내고 계산기 아이콘(![계산기 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg))은 조직의 Analytics 관리자가 만든 계산된 지표를 나타냅니다.

1. (선택 사항) **필터** 아이콘 ![데이터 사전 필터 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg)을 선택한 후 다음 필터 옵션 중 하나를 선택하여 구성 요소 목록을 필터링합니다.

   | 옵션 | 함수 |
   |---------|----------|
   | **[!UICONTROL 승인됨]** | 관리자가 승인한 구성 요소만 표시합니다. |
   | **[!UICONTROL 즐겨찾기]** | 즐겨찾기 목록에 있는 구성 요소만 해당됩니다. 즐겨찾기 목록에 구성 요소를 추가하는 방법에 대한 자세한 내용은 [구성 요소 개요](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)를 참조하십시오. |
   | **[!UICONTROL 차원]** | 차원 구성 요소만 해당됩니다. (이 옵션은 데이터 사전에 처음 액세스할 때 **[!UICONTROL 빠른 필터]** 탭에서도 사용할 수 있음) |
   | **[!UICONTROL 지표]** | 지표 구성 요소만 해당됩니다. (이 옵션은 데이터 사전에 처음 액세스할 때 **[!UICONTROL 빠른 필터]** 탭에서도 사용할 수 있음) |
   | **[!UICONTROL 세그먼트]** | 세그먼트인 구성 요소만 해당됩니다. (이 옵션은 데이터 사전에 처음 액세스할 때 **[!UICONTROL 빠른 필터]** 탭에서도 사용할 수 있음) |
   | **[!UICONTROL 날짜 범위]** | 날짜 범위인 구성 요소만 해당됩니다. (이 옵션은 데이터 사전에 처음 액세스할 때 **[!UICONTROL 빠른 필터]** 탭에서도 사용할 수 있음) |
   | **[!UICONTROL 모두 표시]** | 모든 구성 요소. 이 옵션은 관리자만 사용할 수 있습니다. |
   | **[!UICONTROL 승인되지 않음]** | 아직 관리자가 승인됨으로 표시하지 않은 구성 요소만 해당됩니다. 관리자가 검토 및 승인이 필요한 구성 요소를 식별할 때 유용합니다. 이 옵션은 관리자만 사용할 수 있습니다. |
   | **[!UICONTROL 설명 누락]** | 설명 필드에 아직 설명이 없는 구성 요소만 표시됩니다. 이 옵션은 관리자만 사용할 수 있습니다. |
   | **[!UICONTROL 중복 항목 표시]** | <p>선택한 보고서 세트에 있는 다른 구성 요소와 이름 또는 정의가 동일한 구성 요소만 해당됩니다. 이름 또는 정의가 정확히 일치하는 항목만 중복 항목으로 표시할 수 있습니다.</p><p>이 옵션은 관리자만 사용할 수 있습니다.</p><p>**참고:** 정의의 경우 여기에는 사용자가 만든 구성 요소는 물론 Adobe에서 제공하는 구성 요소도 포함됩니다. 이름의 경우 여기에는 사용자가 만든 구성 요소만 포함되고 Adobe에서 제공하는 구성 요소는 포함되지 않습니다. Adobe 제공 구성 요소의 중복 이름 표시는 향후 릴리스에 추가될 예정입니다.</p> |
   | **[!UICONTROL 최근 데이터 없음]** | 지난 90일 동안 데이터를 수집하지 않은 구성 요소만 해당됩니다. 이 옵션은 관리자만 사용할 수 있습니다. |
   | **[!UICONTROL Adobe에서 생성됨]** <!-- I don't see this option--> | Adobe에서 만든 구성 요소만 표시합니다.  Adobe Target을 예로 들 수 있습니다. 조직의 관리자 또는 다른 사용자가 만든 구성 요소는 표시되지 않습니다. |

   {style="table-layout:auto"}

1. (선택 사항) 구성 요소 목록을 정렬하려면 **정렬** 아이콘 ![구성 요소 정렬 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SortOrderDown_18_N.svg)을 선택한 후 다음 필터링 옵션 중 하나를 선택하십시오.

   | 옵션 | 함수 |
   |---------|----------|
   | [!UICONTROL **권장**] | 목록 맨 위에 권장되는 순서로 구성 요소를 정렬합니다. 귀하 또는 귀사의 다른 사용자가 가장 자주 그리고 가장 최근에 사용한 구성 요소가 목록의 위쪽에 표시됩니다. |
   | [!UICONTROL **알파벳**] | 구성 요소를 알파벳순으로 정렬합니다. |
   | [!UICONTROL **범주**] | 구성 요소 유형(치수, 지표, 세그먼트, 날짜 범위)에 따라 구성 요소를 정렬합니다. |

   {style="table-layout:auto"}

1. 구성 요소 목록에서 편집할 구성 요소를 선택합니다.

1. 구성 요소 이름 옆에 있는 **편집** 아이콘 ![데이터 사전 편집 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg)을 선택합니다.

1. 구성 요소에 대한 다음 정보를 편집합니다.

   | 옵션 | 함수 |
   |---------|----------|
   | **[!UICONTROL 승인됨]** | <p>관리자가 구성 요소를 검토하고 승인했음을 나타냅니다.</p><p>구성 요소가 승인된 후 관리자는 **승인됨** 버튼을 선택하여 승인을 제거할 수 있습니다.</p> |
   | **[!UICONTROL 승인 필요]** | <p>관리자가 아직 구성 요소를 검토하고 승인하지 않았음을 나타냅니다.</p><p>관리자에게는 **[!UICONTROL 승인]** 옵션이 표시됩니다. 이 옵션을 선택하면 구성 요소가 사용자에게 “승인됨”으로 표시됩니다.</p> |
   | **[!UICONTROL 설명]** | 구성 요소의 의도된 기능을 설명합니다. (이 정보는 [구성 요소 설명 추가](/help/analyze/analysis-workspace/components/add-component-descriptions.md)에 설명된 대로 Analytics 관리자가 추가함) |
   | **[!UICONTROL 다음과 함께 자주 사용됨]** | <p>현재 보고 있는 구성 요소와 함께 가장 일반적으로 사용되는 구성 요소를 표시합니다.</p><p>지표, 계산된 지표, 차원, 세그먼트 및 날짜 범위의 5가지 기본 구성 요소 유형에서 최대 5가지 구성 요소가 표시됩니다.</p><p>이 목록은 지난 90일 동안의 데이터를 기반으로 합니다. 볼 수 있는 액세스 권한이 있는 구성 요소만 표시됩니다.</p><p>관리자는 **[!UICONTROL 항상 포함]** 및 **[!UICONTROL 항상 제외]** 드롭다운 영역에서 원하는 구성 요소를 선택해서 이 섹션에서 사용자에게 표시되는 구성 요소를 조정할 수 있습니다. 사용자에게 표시되는 구성 요소를 조정하기 전에 먼저 **모두 표시** 필터를 적용하여 나와 공유되지 않은 구성 요소가 표시되는지 확인합니다.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p> |
   | **[!UICONTROL 다음과 유사]** | <p>현재 보고 있는 구성 요소와 유사한 이름이 있는 구성 요소를 표시합니다.</p><p>지표, 계산된 지표, 차원, 세그먼트 및 날짜 범위의 5가지 기본 구성 요소 유형에서 최대 5가지 구성 요소가 표시됩니다.</p><p>볼 수 있는 액세스 권한이 있는 구성 요소만 표시됩니다.</p><p>보고서 세트의 모든 중복 구성 요소도 여기에 표시됩니다. Analytics 관리자는 [데이터 사전 상태 모니터링](/help/analyze/analysis-workspace/components/data-dictionary/monitor-data-dictionary-health.md)에 설명된 대로 모든 중복 구성 요소를 식별하고 제거해야 합니다.</p><p>관리자는 **[!UICONTROL 항상 포함]** 및 **[!UICONTROL 항상 제외]** 드롭다운 영역에서 원하는 구성 요소를 선택해서 이 섹션에서 사용자에게 표시되는 구성 요소를 조정할 수 있습니다. 사용자에게 표시되는 구성 요소를 조정하기 전에 먼저 **모두 표시** 필터를 적용하여 나와 공유되지 않은 구성 요소가 표시되는지 확인합니다.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p><p>**참고:** 현재 **다음과 유사** 섹션에는 사용자가 만든 구성 요소만 포함되고 Adobe에서 제공하는 구성 요소는 포함되지 않습니다. Adobe 제공 구성 요소는 향후 릴리스에 추가될 예정입니다.</p> |
   | **[!UICONTROL 태그]** | 구성 요소에 적용된 모든 태그가 표시됩니다. 관리자 액세스 권한이 있는 사용자는 구성 요소를 편집할 때 태그를 추가할 수 있습니다. |
   | **[!UICONTROL 구성 요소 유형]** | 차원, 지표, 세그먼트 또는 날짜 범위 등 구성 요소의 유형을 나열합니다. |
   | **[!UICONTROL 작성자]** | 구성 요소를 생성한 사용자 이름을 표시합니다. |
   | **[!UICONTROL 미리보기]** | Analysis Workspace에서 구성 요소가 어떻게 보이는지 미리보기를 표시합니다. |
   | **[!UICONTROL 마지막 수정일]** | 구성 요소가 마지막으로 수정된 날짜를 표시합니다. 이 섹션은 세그먼트, 계산된 지표 및 날짜 범위를 볼 때 표시됩니다. |

   {style="table-layout:auto"}

1. **저장** 아이콘 ![데이터 사전 저장 아이콘](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SaveFloppy_18_N.svg)을 클릭하여 변경 사항을 저장합니다.
