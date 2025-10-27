---
title: 분류 세트 만들기
description: 분류 세트를 만들 때 사용 가능한 필드 및 설명을 만드는 방법을 알아봅니다.
exl-id: 6d692d90-8cc7-4306-a780-58d03db45be8
feature: Classifications
source-git-commit: 2ced7cd61c4119347be2ef0fba9b8d60ee6c4df2
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 2%

---

# 분류 세트 만들기 및 편집

분류 세트 관리자에서 [만들기](#create-a-classification-set) 및 [편집](#edit-a-classification-set) 분류 세트를 만듭니다.

## 분류 세트 만들기

분류 세트를 만들려면 다음 작업을 수행하십시오.

1. Adobe Analytics 상단 메뉴 모음에서 **[!UICONTROL 구성 요소]**&#x200B;를 선택한 다음 **[!UICONTROL 분류 세트]**&#x200B;를 선택합니다.
1. **[!UICONTROL 분류 세트]**&#x200B;에서 **[!UICONTROL 분류 세트]** 탭을 선택합니다.
1. ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL 새로 만들기]**&#x200B;를 선택합니다.
1. **[!UICONTROL 새 분류 집합 추가]** 대화 상자에서:

   ![분류 세트 - 새 분류 세트 추가](assets/classifications-sets-new.png)

   1. **[!UICONTROL 이름]**&#x200B;을(를) 입력하십시오. 예: `Classification Set Example`.
   1. **[!UICONTROL 설명(선택 사항)]**&#x200B;을 입력하십시오. (예: `Example classification set`)
   1. **[!UICONTROL 문제 알림]**&#x200B;에 하나 이상의 이메일 주소(쉼표로 구분)를 입력하십시오. 문제에 대해 이러한 사용자에게 이메일 알림이 전송됩니다.
   1. 분류 집합의 **[!UICONTROL 유형]**&#x200B;을(를) 선택하십시오. 가능한 유형은 다음과 같습니다.
      * **[!UICONTROL 기본]**. 기본 분류 세트는 Adobe Analytics에서 수집된 차원에 적용됩니다. 기본 분류는 세분화된 차원 값을 보다 의미 있는 데이터 수준으로 그룹화(분류)하는 방법입니다. 예를 들어, 검색 데이터의 테마를 이해하기 위해 내부 검색 키워드를 내부 검색 카테고리로 그룹화할 수 있습니다. 또는 색상 또는 카테고리별로 제품 SKU를 분류합니다.
         * 하나 이상의 **[!UICONTROL 구독]**&#x200B;을 입력하십시오.  분류 세트에 여러 **[!UICONTROL 보고서 세트]** 및 **[!UICONTROL Dimension]** 조합을 정의할 수 있습니다.

         * ![보고서 세트](/help/assets/icons/CrossSize400.svg) 및 **[!UICONTROL 키 Dimension]** 조합을 삭제하려면 **[!UICONTROL CrossSize400]**&#x200B;을(를) 선택하십시오.

        다른 분류 세트에 이미 있는 **[!UICONTROL 보고서 세트]** 및 **[!UICONTROL 키 Dimension]** 조합을 추가하면 조합 아래에 빨간색 경고가 표시됩니다. **[!UICONTROL 기존 항목에 추가]**&#x200B;를 선택하여 다른 분류 집합을 열고 [스키마에 분류를 추가](schema.md)하거나 차원을 변경할 수 있습니다.
      * **[!UICONTROL 조회]**. 일반적으로 하위 또는 하위 분류라고 하는 조회 테이블은 기본 분류의 분류입니다. 조회는 원래 차원이 아닌 분류 값에 대한 메타데이터입니다. 예를 들어 *Product* 차원의 기본 분류는 *색상 코드*&#x200B;일 수 있습니다. *색상 이름*&#x200B;의 조회 테이블을 *색상 코드*&#x200B;에 연결하여 각 색상 코드를 설명할 수 있습니다.
1. **[!UICONTROL 저장]**&#x200B;을 선택하여 분류 집합을 저장합니다. 정의를 취소하려면 **[!UICONTROL 취소]**&#x200B;를 선택하십시오.
1. 분류 세트에 대한 스키마를 정의하려면 **[!UICONTROL 분류 세트]** 관리자에서 새로 만든 분류 세트를 선택하여 [분류 세트를 편집](#edit-a-classification-set)합니다.


## 분류 세트 편집

분류 세트를 편집하려면:

1. Adobe Analytics 상단 메뉴 모음에서 **[!UICONTROL 구성 요소]**&#x200B;를 선택한 다음 **[!UICONTROL 분류 세트]**&#x200B;를 선택합니다.
1. **[!UICONTROL 분류 세트]**&#x200B;에서 **[!UICONTROL 분류 세트]** 탭을 선택합니다.
1. 분류 세트의 제목을 선택합니다.
1. **[!UICONTROL 분류 세트: _분류 세트 제목_]**대화 상자에서 분류 세트에 대한 [설정](settings.md) 및 [스키마](schema.md)을(를) 정의할 수 있습니다.
1. 완료되면 **[!UICONTROL 저장]**&#x200B;을 선택하여 변경 내용을 저장합니다. 취소하려면 **[!UICONTROL 취소]**&#x200B;를 선택합니다.


<!--


### Schema

In the Schema tab 





You can use the Classification set manager to create a classification set.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]** > **[!UICONTROL Add]**

When creating a classification set, the following fields are available.

* **[!UICONTROL Name]**: A text field used to identify the classification set. This field cannot be edited upon creation, but can be renamed later.
* **[!UICONTROL Column Name]**: The name of the first classification dimension that you want to create. This field is the dimension name used in Analysis Workspace, and the column name when exporting classification data. You can add more column names after the classification set is created.
* **[!UICONTROL Type]**: Radio buttons that indicate the type of classification.
  * **[!UICONTROL Primary]**: Apply to dimensions collected in Analytics. They are a way to group (classify) granular dimension values into more meaningful levels of data. For example, you might want to group internal search keywords into internal search categories, to better understand themes in your search data.
  * **[!UICONTROL Lookup]**: Commonly referred to as child or subclassifications, a lookup table is a classification of a primary classification. It is metadata about a classification value, rather than the original dimension. For example, the Product variable might have a primary classification of 'Color code'. A lookup table of 'Color name' could then be attached to 'Color code' to further explain what each code means.
* **[!UICONTROL Subscriptions]** The report suites and dimensions that this classification set applies to. You can add multiple report suite and dimension combinations to a classification set.

![Create a Classification set](../../assets/classification-set-create.png)

If a classification set exists for a given report suite + variable, the classification is added to the schema instead. A given report suite + variable combination cannot belong to multiple classification sets.

-->