---
title: 분류 세트 관리
description: Adobe Analytics에서 분류 세트를 관리합니다.
exl-id: b1a6721b-8e5d-4ee6-af6b-cda31c9f8b00
feature: Classifications
source-git-commit: d5e1432569516d13d2de30a2cb30cebb067ab783
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 5%

---

# 분류 세트 관리

분류 세트 관리 인터페이스에서 분류 세트를 생성, 이름 변경, 편집, 통합, 삭제 및 태그를 지정할 수 있습니다. 특정 분류 세트를 필터링하고 검색할 수도 있습니다.

분류 세트를 관리하려면

1. Adobe Analytics 상단 메뉴 모음에서 **[!UICONTROL 구성 요소]**&#x200B;를 선택한 다음 **[!UICONTROL 분류 세트]**&#x200B;를 선택합니다.
1. **[!UICONTROL 분류 세트]**&#x200B;에서 **[!UICONTROL 분류 세트]** 탭을 선택합니다.

## 분류 세트 관리자

**[!UICONTROL 분류 집합]** 관리자에 다음 인터페이스 요소가 있습니다.

![분류 집합 관리자](assets/classification-sets-manage.png)


### 분류 세트 목록

**[!UICONTROL 분류 세트]** 목록 ➊에 모든 분류 세트가 표시됩니다. 목록은 다음과 같습니다.

| 열 | 설명 |
|---|---|
| **[!UICONTROL 분류 집합]** | 분류 세트의 이름입니다. [분류 집합을 편집](create.md#edit-a-classification-set)할 이름을 선택하십시오. |
| **[!UICONTROL 구독]** | 분류 세트가 적용되는 구독 수입니다. |
| **[!UICONTROL 분류]** | 분류 세트에 포함된 분류 차원의 수입니다. |
| **[!UICONTROL 자동화]** | 클라우드 위치에서 데이터를 자동으로 가져오도록 분류 세트를 구성합니까? 이 자동화는 [분류 세트 스키마](manage/schema.md)의 일부로 구성할 수 있습니다. |
| **[!UICONTROL 마지막 수정일]** | 분류 세트를 마지막으로 수정한 타임스탬프입니다. |

분류 세트 목록에서 열의 크기를 조정하려면 다음을 수행할 수 있습니다.

* 열 구분자 위로 마우스를 가져간 후 열 구분자를 원하는 열 너비로 드래그합니다.
* ![V자형 화살표](/help/assets/icons/ChevronDown.svg)를 선택하고 **[!UICONTROL 열 크기 조정]**&#x200B;을 선택합니다. [크기 조정] 단추가 있는 세로줄을 사용하면 원하는 로 열 크기를 조정할 수 있습니다.

분류 세트 목록에서 열을 정렬하려면

* ![V자형 화살표](/help/assets/icons/ChevronDown.svg)를 선택하고 **[!UICONTROL 오름차순 정렬]** 또는 **[!UICONTROL 내림차순 정렬]**&#x200B;을 선택합니다. 화살표(↑↓)는 열과 열이 정렬되는 방식을 나타냅니다.

### 검색 및 단추

분류 세트 목록의 맨 위에 있는 ➋ 영역에서 다음을 수행할 수 있습니다.

* 분류 집합을 ![검색](/help/assets/icons/Search.svg)합니다. 결과는 분류 세트 목록에 표시됩니다. 검색을 지우려면 ![CrossSize200](/help/assets/icons/CrossSize200.svg)을(를) 선택하십시오.
* 분류 세트 목록에 적용된 필터를 제거합니다. 필터를 제거하려면 ![CrossSize100](/help/assets/icons/CrossSize100.svg)을(를) 선택하십시오.
* ![MoreCircle](/help/assets/icons/MoreCircle.svg)을(를) 선택하여 1000개의 분류 세트를 추가로 로드합니다. 처음에는 분류 세트 목록에 최대 1000개의 분류 세트가 표시됩니다.
* ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL 새로 만들기]**&#x200B;를 선택하여 [새 분류 집합을 만들기](create.md#create-a-classification-set)합니다.
* 분류 세트 목록의 열을 정의합니다. ![ColumnSetting](/help/assets/icons/ColumnSetting.svg)을(를) 선택하고 **[!UICONTROL 테이블 사용자 지정]** 대화 상자에서 **[!UICONTROL 표시할 열 선택]** 아래에 표시할 열을 선택합니다. 열 설정을 적용하려면 **[!UICONTROL 적용]**&#x200B;을 선택하세요.


### 작업 표시줄

분류 세트 목록에서 하나 이상의 분류 세트를 선택하면 파란색 작업 모음 ➌이(가) 나타납니다. 작업 표시줄에서 다음 작업을 사용할 수 있습니다.

| 아이콘 | 액션 | 설명 |
|---|---|---|
| ![편집](/help/assets/icons/Edit.svg) | **[!UICONTROL 편집]** | 분류 세트 빌더에서 [분류 세트를 편집](create.md#edit-a-classification-set)합니다. |
| ![이름 바꾸기](/help/assets/icons/Rename.svg) | **[!UICONTROL 이름 바꾸기]** | 분류 세트의 이름을 변경합니다.<br/>**[!UICONTROL 이름 바꾸기: _분류 집합_]**&#x200B;대화 상자에서 새 이름을 입력하고&#x200B;**[!UICONTROL 이름 바꾸기]**&#x200B;를 선택합니다. |
| ![병합](/help/assets/icons/Merge.svg) | **[!UICONTROL 통합]** | [분류 집합을 통합](/help/components/classifications/sets/consolidations/manage.md)합니다. |
| ![삭제](/help/assets/icons/Delete.svg) | **[!UICONTROL 삭제]** | 분류 세트를 삭제합니다.<br/>**[!UICONTROL 분류 집합 _삭제_를 수행하시겠습니까?]** 대화 상자가 나타납니다. 분류 세트의 삭제는 실행 취소할 수 없습니다. 이 분류 세트를 사용하는 모든 예약된 프로젝트 또는 통합은 예약된 프로젝트를 다시 저장하거나 예약된 통합을 다시 검증할 때까지 이 분류 세트의 정의를 계속 사용합니다. 분류 세트를 삭제하려면 **[!UICONTROL 삭제]**&#x200B;를 선택하십시오. |
| ![레이블](/help/assets/icons/Label.svg) | **[!UICONTROL 태그]** | 분류 세트에 태깅합니다.<br/>**[!UICONTROL 태그: _분류 집합_]**&#x200B;대화 상자의&#x200B;**[!UICONTROL 태그]**&#x200B;드롭다운 메뉴에서 태그를 하나 이상 선택하여 태그를 추가합니다. 또는 새 태그를 하나 이상 입력합니다. 태그를 제거하려면 ![CrossSize100](/help/assets/icons/CrossSize100.svg)을(를) 사용하십시오. <br/>태그를 저장하려면&#x200B;**[!UICONTROL 저장]**&#x200B;을 선택하십시오. |


### 필터 패널

분류 집합 목록을 필터링할 수 있는 필터 패널 ![을(를) 표시하려면 &#x200B;](/help/assets/icons/Filter.svg)필터➍를 선택하십시오. 다음을 필터링할 수 있습니다.

* **[!UICONTROL 태그]**. 하나 이상의 태그를 선택하여 태그의 분류 세트 목록을 필터링합니다.
* **[!UICONTROL 보고서 세트]**. 하나 이상의 보고서 세트를 선택하여 보고서 세트의 분류 세트 목록을 필터링합니다.

필터 패널을 숨기려면 ![필터](/help/assets/icons/Filter.svg) **[!UICONTROL 필터 숨기기]**&#x200B;를 선택하십시오.

[필터] 패널에 표시된 필터는 미리 로드된 분류 세트에 대한 옵션을 반영합니다.


<!-- old content

The Classification set manager allows you to create, edit, or delete classification sets.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]**

Classification sets consist of **Subscriptions** (report suite and dimension combinations) and **Classification names** (dimensions containing classification data). Subscriptions are configured under [Settings](settings.md), while classification names are configured under [Schema](schema.md).

## Filter classification sets

The left side of the Classification set manager provides filter settings to locate the desired classification set. Clicking the filter icon toggles the filter settings visibility. You can filter classification sets by **[!UICONTROL Tags]** or **[!UICONTROL Report suite]**.

![Classification set filters](../../assets/classification-set-filters.png)

Note that 1,000 classification sets are preloaded at a time. The filters shown in the left rail reflect the options for the sets that are preloaded.

## Classification set manager columns

The following columns are available in the Classification set manager:

* **[!UICONTROL Classification set]**: The classification set name. Clicking a classification set name edits its [settings](settings.md).
* **[!UICONTROL Subscriptions]**: The number of subscriptions that this classification set applies to.
* **[!UICONTROL Classifications]**: The number of classification dimensions that the classification set contains.
* **[!UICONTROL Automated]**: Determines if the classification set is configured to automatically import data from a cloud location. Automation can be configured in the classification set's [schema](schema.md).
* **[!UICONTROL Last Modified]**: The date and time that the classification set was last modified.

## Create or edit options

The following buttons are available in the Classification set manager:

* **[!UICONTROL Add]**: [Create](create.md) a classification set.
* **[!UICONTROL Search by title]**: Search for classification sets by name.
* **[!UICONTROL Load more]**: The Classification set manager initially displays up to 1000 classification sets. This button loads 1000 more classification sets.
* **Show/Hide columns**: Toggle visibility for any column besides [!UICONTROL Classification set].

Select one or more classification sets by clicking the checkbox next to the desired classification set. Selecting a classification set reveals the following options:

* **[!UICONTROL Tag]**: Add one or more tags to the selected classification sets, which allows you to organize or group classification sets to make them easier to locate in the future.
* **[!UICONTROL Delete]**: Deletes the classification set. Classification dimensions based on this classification set are no longer available. Scheduled projects using the deleted classification set continue using dependent dimensions until you resave the scheduled project.
* **[!UICONTROL Consolidate]**: Start a new [consolidation](../consolidations/process.md).
* **[!UICONTROL Rename]**: Rename the selected classification set.

-->