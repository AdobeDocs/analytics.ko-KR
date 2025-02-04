---
description: Analysis Workspace에서 테이블을 필터링하고 정렬하는 방법에 대해 설명하는 설명서입니다.
title: 자유 형식 테이블 필터링 및 정렬
feature: Freeform Tables
role: User, Admin
exl-id: 15fea9e2-f8d8-4489-9a44-e74a351b8f36
source-git-commit: 1ce002a513860ce15dc8a70825d26795fd93eb1d
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 43%

---

# 자유 형식 테이블 필터링 및 정렬

Analysis Workspace의 자유 형식 테이블은 대화형 데이터 분석을 위한 기반입니다. 그에 따라 자유 형식 테이블은 수천 개의 정보 행을 포함할 수 있습니다. 데이터를 필터링하고 정렬하는 것은 가장 중요한 정보를 효율적으로 표시하는 데 필수적인 부분이 될 수 있습니다.


## 테이블 필터링

Analysis Workspace의 필터는 가장 중요한 정보를 표시하는 데 도움이 됩니다.

>[!NOTE]
>
> 이 섹션에 설명된 대로 동적 차원 항목만 필터링할 수 있습니다. 정적 차원 항목은 필터링할 수 없습니다. 자세한 내용은 [자유 형식 테이블의 동적 차원 항목과 정적 차원 항목](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md)을 참조하십시오.

여러 메서드를 사용하여 자유 형식 테이블에서 행을 필터링할 수 있습니다.

- 테이블에서 특정 행 제외
- 표에 필터 적용
- 대상 필터 사용

각 메서드가 [자유 형식 테이블 합계](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md)에 미치는 영향을 읽어 보십시오.

### 테이블에서 특정 행 제외

![필터](/help/assets/icons/Filter.svg) **[!UICONTROL 필터]**&#x200B;를 사용하지 않고도 테이블에서 특정 행을 빠르게 제외할 수 있습니다.

>[!NOTE]
>
>이 섹션에 설명된 대로 행을 제외하면 [!UICONTROL 항상 항목 제외] 규칙이 [!UICONTROL 고급] 필터 대화 상자에 자동으로 추가됩니다. ![필터](/help/assets/icons/Filter.svg) 필터 아이콘을 선택한 다음 [**[!UICONTROL 고급 표시]**](#apply-a-simple-or-advanced-filter-to-a-table)를 선택하여 적용된 규칙을 볼 수 있습니다.

자유 형식 테이블에서 특정 행을 제외하려면 다음을 수행합니다.

1. 제외할 행을 마우스로 가리킨 다음 ![닫기](/help/assets/icons/Close.svg)를 선택합니다.

   행 범위를 선택하려면 ***shift***&#x200B;를 누르고 있거나, 여러 행을 선택하려면 ***cmd*** 키(Mac의 경우) 또는 ***ctrl*** 키(Windows의 경우)를 누르고 있습니다.

<!--### Right-click > Delete selected rows

Note: this option does not seem to work. AN-338422

1. Select 1 or more rows. 
1. Right-click and select **[!UICONTROL Delete Selected Rows]**. 

   This action will remove the rows from the table and apply a table filter.-->


### 표에 단순 또는 고급 필터 적용

자유 형식 테이블에서 데이터를 필터링하려면 다음 작업을 수행하십시오.

1. 필터링할 데이터가 포함된 열 위로 마우스를 가져갑니다. <!--only some types of columns show the filter... Which? Just Dimensions?-->

1. 표시되는 경우 ![필터](/help/assets/icons/Filter.svg) **필터**&#x200B;을(를) 선택하십시오.

   ![필터 아이콘을 강조 표시하는 자유 형식 테이블.](assets/table-filter-icon.png)

   **[!UICONTROL 검색]** 대화 상자에서 다음 옵션을 사용할 수 있습니다.

   ![단순 필터링](assets/filter-simple.png){width="500"}

   | 옵션 | 함수 |
   |---------|----------|
   | [!UICONTROL **값 없음 포함**] | 선택한 차원에 대한 값이 없는 데이터의 테이블에 **[!UICONTROL 값 없음]** 행을 표시하려면 이 옵션을 선택하십시오. **[!UICONTROL 값 없음]** 행을 숨기려면 이 옵션을 선택 취소합니다. |
   | [!UICONTROL **검색어 또는 구**] | 필터링 기준으로 사용할 단어나 구를 지정합니다. 지정한 단어 또는 정확한 구문을 포함하는 행만 표시됩니다. |


1. (선택 사항) 다른 기준 또는 여러 기준으로 필터링하려면 [!UICONTROL **고급 설정 표시**]&#x200B;를 선택합니다.

   다음 고급 필터 옵션을 사용할 수 있습니다.

   ![단순 필터링](assets/filter-advanced.png){width=500}

   | 옵션 | 함수 |
   |---------|----------|
   | [!UICONTROL **값 없음 포함**] | 선택한 차원에 대한 값이 없는 데이터의 테이블에 **[!UICONTROL 값 없음]** 행을 표시하려면 이 옵션을 선택하십시오. **[!UICONTROL 값 없음]** 행을 숨기려면 이 옵션을 선택 취소합니다. |
   | [!UICONTROL **일치**] | 지정한 모든 기준을 충족하는 데이터만 표시하려면 [!UICONTROL **모든 기준이 충족되는 경우**]&#x200B;를 선택합니다. 이 옵션은 일반적으로 더 세분화된 데이터를 보여 줍니다.<br/><br/>지정한 필터 조건 중 하나를 충족하는 데이터를 표시하려면 [!UICONTROL **조건을 충족하는 경우**]&#x200B;를 선택합니다. 이 옵션은 일반적으로 덜 세분화된 데이터를 보여 줍니다. |
   | [!UICONTROL **기준**] | 다음 필터 옵션 중에서 선택하십시오.<br/><ul><li>[!UICONTROL **구문 포함**](기본값): 지정한 구문을 정확히 포함하는 데이터만 필터링된 결과에 포함됩니다. 단어는 [!UICONTROL **단어 또는 구문 검색 필드**]&#x200B;에 지정된 순서를 따라야 합니다.</li><li>[!UICONTROL **검색어를 하나라도 포함**]: 지정한 구문에서 하나 이상의 단어를 포함하는 데이터만 필터링된 결과에 포함됩니다. </li><li>[!UICONTROL **모든 검색어 포함**]: 지정한 구문의 모든 단어를 포함하는 데이터만 필터링된 결과에 포함됩니다. 단어는 [!UICONTROL **단어 또는 구문 검색 필드**]&#x200B;에 지정된 순서를 따르지 않아도 됩니다.</li><li>[!UICONTROL **검색어 포함 안 함**]: 지정한 구문의 단어를 포함하지 않는 데이터만 필터링된 결과에 포함됩니다. </li><li>[!UICONTROL **구문 포함 안 함**]: 지정한 구문을 포함하지 않는 데이터만 필터링된 결과에 포함됩니다. 단어는 [!UICONTROL **단어 또는 구문 검색 필드**]&#x200B;에 지정된 순서를 따라야 합니다.</li><li>[!UICONTROL **같음**]: 지정한 구문과 정확히 일치하는 데이터만 필터링된 결과에 포함됩니다. </li><li>[!UICONTROL **같지 않음**]: 지정한 구문과 정확히 일치하지 않는 데이터만 필터링된 결과에 포함됩니다. </li><li>[!UICONTROL **다음으로 시작**]: 지정한 단어 또는 정확한 구문으로 시작하는 데이터만 필터링된 결과에 포함됩니다. </li><li>[!UICONTROL **다음으로 끝남**]: 지정한 단어 또는 정확한 구문으로 끝나는 데이터만 필터링된 결과에 포함됩니다. </li></ul>![추가](/help/assets/icons/Add.svg) [!UICONTROL **행 추가**]&#x200B;를 선택하여 여러 필터 조건을 추가하십시오. [!UICONTROL **일치**]&#x200B;에 대해 선택하는 옵션은 **[!UICONTROL 모든 기준이 충족되는 경우]** 또는 **[!UICONTROL 모든 기준이 충족되는 경우]**&#x200B;을 결정합니다. |
   | [!UICONTROL **항상 항목 제외**] | 필터링된 데이터에서 제외하려는 항목의 이름을 지정합니다. |

1. 데이터를 필터링하려면 **[!UICONTROL 적용]**&#x200B;을 선택하십시오. 모든 입력을 지우려면 **[!UICONTROL 지우기]**&#x200B;를 선택하십시오. 취소하고 대화 상자를 닫으려면 **[!UICONTROL 취소]**&#x200B;를 선택하십시오. <br/>색이 지정된 ![필터](/help/assets/icons/FilterColored.svg) **필터** 아이콘은 테이블에 필터를 적용할 때 세부 정보를 표시하고 표시합니다.


## 테이블 정렬

Analysis Workspace에서 차원 또는 지표인 열을 기준으로 자유 형식 테이블의 데이터를 정렬할 수 있습니다. 화살표는 데이터가 정렬되는 방법을 나타냅니다(**↓**(내림차순), **↑**).

![정렬](assets/sorting.gif)
