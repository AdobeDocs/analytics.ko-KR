---
title: 분류 세트 통합 관리
description: 하나 이상의 분류 세트를 단일 분류 세트로 통합하는 방법을 알아봅니다.
exl-id: 0be97ca4-56c3-4642-9347-924812e88e8c
feature: Classifications
source-git-commit: 77599d015ba227be25b7ebff82ecd609fa45a756
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 3%

---

# 분류 통합 관리

유사한 분류 데이터를 포함하는 분류 세트가 여러 개 있는 경우 이를 단일 분류 세트로 통합할 수 있습니다. 두 개 이상의 분류 세트를 통합하면 Adobe은 각 개별 분류 세트의 모든 분류 데이터를 포함하는 새 분류 세트를 생성합니다. 통합은 데이터를 여러 보고서 세트에 업로드한 경우 유용합니다. 또는 동일한 분류 데이터를 포함하고 있는 차원을 단일 워크플로우에 병합하려는 경우.

Adobe Analytics에서 분류 세트 통합 관리자를 보려면 제품 관리자 액세스 권한이 있어야 합니다.



분류 통합을 관리하려면 다음을 수행합니다.

1. 기본 인터페이스에서 **[!UICONTROL 구성 요소]**&#x200B;를 선택한 다음 **[!UICONTROL 분류 집합]**&#x200B;을 선택하십시오.
1. **[!UICONTROL 분류 세트]**&#x200B;에서 **[!UICONTROL 통합]** 탭을 선택합니다.


## 분류 통합 관리자

**[!UICONTROL 분류 세트 - 통합]** 관리자에 다음 인터페이스 요소가 있습니다.

![분류 세트 - 통합 관리자](assets/classifications-sets-consolidations.png)



### 분류 통합 목록

➊ 목록에는 작성 및 유효성이 확인되었으며 통합 중일 수 있는 분류 통합이 표시됩니다. 목록은 다음과 같습니다.

| 열 | 설명 |
|---|---|
| **[!UICONTROL 통합 이름]** | 분류 이름은 통합을 설정합니다. |
| **[!UICONTROL 현재 작업]** | 분류와 연관된 작업이 통합을 설정합니다. |
| **[!UICONTROL 상태]** | 분류 상태는 통합을 설정합니다. 가능한 값은 **[!UICONTROL 생성됨]**, **[!UICONTROL 취소됨]**, **[!UICONTROL 취소]**, **[!UICONTROL 확인]**, **[!UICONTROL 유효성 검사 실패]**, **[!UICONTROL 확인됨]**, **[!UICONTROL 비교]**, **[!UICONTROL 비교 실패]**, **[!UICONTROL 통합]**, **[!UICONTROL 제출됨]**, **[!UICONTROL 통합]**, **[!UICONTROL 통합 실패]**, **[!UICONTROL 통합 성공]**, **[!UICONTROL 승인 대기 중]**, **[!UICONTROL 완료]**, **[!UICONTROL 입니다. 실패]** 또는 **[!UICONTROL 완료]**. |
| **[!UICONTROL 생성 시간]** | 분류 생성 시간은 통합을 설정합니다. |
| **[!UICONTROL 완료 시간]** | 분류 통합이 완료되는 시간입니다. |


분류 통합 목록에서 열의 크기를 조정하려면 다음을 수행할 수 있습니다.

* 열 구분자 위로 마우스를 가져간 후 열 구분자를 원하는 열 너비로 드래그합니다.
* ![V자형 화살표](/help/assets/icons/ChevronDown.svg)를 선택하고 **[!UICONTROL 열 크기 조정]**&#x200B;을 선택합니다. [크기 조정] 단추가 있는 세로줄을 사용하면 원하는 로 열 크기를 조정할 수 있습니다.

분류 통합 목록에서 열을 정렬하려면

* ![V자형 화살표](/help/assets/icons/ChevronDown.svg)를 선택하고 **[!UICONTROL 오름차순 정렬]** 또는 **[!UICONTROL 내림차순 정렬]**&#x200B;을 선택합니다. 화살표(↑↓)는 열과 열이 정렬되는 방식을 나타냅니다.

### 검색 및 단추

분류 통합 목록의 맨 위에 있는 ➋ 영역에서 다음을 수행할 수 있습니다.

* 분류 통합에 대해 ![검색](/help/assets/icons/Search.svg)을 검색합니다. 결과는 분류 통합 목록에 표시됩니다. 검색을 지우려면 ![CrossSize200](/help/assets/icons/CrossSize200.svg)을(를) 선택하십시오.
* 분류 세트 통합 목록에 적용된 필터를 제거합니다. 필터를 제거하려면 ![CrossSize100](/help/assets/icons/CrossSize100.svg)을(를) 선택하십시오.
* 새 분류 세트를 생성하여 통합을 설정합니다. ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL 새로 만들기]**&#x200B;를 선택하여 분류 세트 통합 대화 상자를 열고 새 분류 세트 통합을 정의합니다.
* 분류 통합 목록의 열을 정의합니다. ![ColumnSetting](/help/assets/icons/ColumnSetting.svg)을(를) 선택하고 **[!UICONTROL 테이블 사용자 지정]** 대화 상자에서 **[!UICONTROL 표시할 열 선택]** 아래에 표시할 열을 선택합니다. 열 설정을 적용하려면 **[!UICONTROL 적용]**&#x200B;을 선택하세요.


### 작업 표시줄

분류 세트 목록에서 하나 이상의 분류 세트를 선택하면 파란색 작업 모음 ➌이(가) 나타납니다. 작업 표시줄에서 다음 작업을 사용할 수 있습니다.

| 아이콘 | 액션 | 설명 |
|---|---|---|
| ![편집](/help/assets/icons/Edit.svg) | **[!UICONTROL 편집]** | [분류 세트 통합 편집](process.md#edit-a-consolidation) |
| ![세부 정보 보기](/help/assets/icons/ViewDetail.svg) | **[!UICONTROL 보기]** | 분류 세트 통합의 세부 정보를 확인합니다. 상태에 따라 통합을 [승인](process.md#approve)하거나 [취소](process.md#cancel)할 수 있습니다. |


### 필터 패널

![필터](/help/assets/icons/Filter.svg)를 선택하여 분류 통합 목록을 필터링할 수 있는 필터 패널 ➍을(를) 표시합니다. 다음을 필터링할 수 있습니다.

* **[!UICONTROL 상태]**. 가능한 값 중 하나를 선택하여 상태의 분류 통합 목록을 필터링합니다. |
* **[!UICONTROL 완료 시간]**. 가능한 값 중 하나를 선택하여 완료 시간에 분류 통합 목록을 필터링합니다.
* **[!UICONTROL 생성 시간]**. 가능한 값 중 하나를 선택하여 완료 시간에 분류 통합 목록을 필터링합니다.


필터 패널을 숨기려면 ![필터](/help/assets/icons/Filter.svg) **[!UICONTROL 필터 숨기기]**&#x200B;를 선택하십시오.

[필터] 패널에 표시된 필터는 미리 로드된 분류 통합에 대한 옵션을 반영합니다.


<!--

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Consolidations]**

Once a consolidation is run, the original classification sets are removed, with the consolidated classification set taking their place. Click **[!UICONTROL Add]** to [Create a consolidation](process.md).

## Filter classification sets

The left side of the Classification set consolidation manager provides filter settings to locate the desired consolidation. Clicking the filter icon toggles the filter settings visibility. You can filter consolidations by **[!UICONTROL Status]**, **[!UICONTROL Completion time]**, or **[!UICONTROL Creation time]**.

![Classification set consolidation filters](../../assets/classification-set-consolidation-filters.png)

Additional filter options are available above the Classification set consolidation manager columns:

* **[!UICONTROL Search by title]**: Search for consolidations by name.
* **Show/Hide columns**: Toggle visibility for any column besides [!UICONTROL Name].

## Classification set consolidation manager columns

The following columns are available in the Classification set consolidation manager:

* **[!UICONTROL Name]**: The name of the consolidation.
* **[!UICONTROL Current job]**: The current job. 
* **[!UICONTROL Status]**: The status of the consolidation. 
* **[!UICONTROL Creation date]**: The date and time that the consolidation was created.
* **[!UICONTROL Completion date]**: The date and time that the consolidation completed (or failed).

-->
