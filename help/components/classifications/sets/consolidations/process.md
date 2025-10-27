---
title: 분류 통합 생성 및 편집
description: 분류 통합을 만들고, 검증하고, 실행하고, 승인하고, 취소하는 방법에 대해 설명합니다.
exl-id: f36bcbcb-0ed0-44a7-a6a9-b28fd244fb27
feature: Classifications
source-git-commit: ec49a5fd5771e4ca0a35ead681b556336bbc7031
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 1%

---

# 분류 통합 생성 및 편집

분류 세트 통합을 사용하면 여러 데이터 세트에서 분류를 가져와서 하나로 결합할 수 있습니다. 이 인터페이스를 사용하여 처음부터 끝까지 분류 세트 통합을 생성합니다. 이 인터페이스는 기존 분류에서 분류 세트로 이동하는 조직에 가장 중요합니다. 이미 분류 세트를 사용하는 대부분의 조직은 이 통합 워크플로우를 사용할 필요가 없습니다.

## 통합 만들기

분류 통합을 만들려면 기본 Adobe Analytics 인터페이스에서 다음을 수행합니다.

1. **[!UICONTROL 구성 요소]** 메뉴에서 **[!UICONTROL 분류 집합]**&#x200B;을(를) 선택하십시오.
1. **[!UICONTROL 분류 세트]** 관리자에서 **[!UICONTROL 통합]** 탭을 선택합니다.
1. **[!UICONTROL 분류 세트 - 통합]** 관리자에서 ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL 새로 만들기]**&#x200B;를 선택합니다.
1. **[!UICONTROL 새 통합]** 대화 상자에서

   ![분류 세트 - 새 통합](assets/classifications-sets-consolidations-new.png)
   1. **[!UICONTROL 이름]**&#x200B;을(를) 입력하십시오. 예: `Consolidation Example`.
   1. **[!UICONTROL 설명(선택 사항)]**&#x200B;을 입력하십시오. (예: `Example classification set`)
   1. **[!UICONTROL 문제 알림]**&#x200B;에 하나 이상의 이메일 주소(쉼표로 구분)를 입력하십시오. 문제에 대해 이러한 사용자에게 이메일 알림이 전송됩니다.
   1. **[!UICONTROL 일치하는 분류 집합]** 드롭다운 메뉴에서 분류 집합을 선택합니다.

      **[!UICONTROL Source 분류 세트]** 왼쪽 목록은 선택한 분류 목록과 유사하며 통합에 사용할 수 있는 분류 세트로 채워집니다.

   1. 왼쪽 목록에서 통합할 분류 세트를 선택하고 선택한 ![키](/help/assets/icons/Key.svg) **[!UICONTROL _분류 세트_]** 아래의 오른쪽 목록에 선택한 세트를 놓습니다.

      목록에서 개별 및 선택한 분류 세트를 이동할 수 있습니다. 끌어다 놓기를 통해 ![키](/help/assets/icons/Key.svg) **[!UICONTROL _분류 집합_]**&#x200B;을 선택한 분류 집합으로 바꿀 수도 있습니다.

   1. **[!UICONTROL 저장]**&#x200B;을 선택하여 분류 통합을 저장합니다. 취소하려면 **[!UICONTROL 취소]**&#x200B;를 선택합니다.

저장하면 분류 통합이 통합에 대해 자동으로 검증됩니다. 이 검증을 통해 각 개별 분류 세트가 이 통합에 유효한지 확인할 수 있습니다. 성공하면 분류 통합 목록의 항목에 **[!UICONTROL 확인됨]** 상태가 표시됩니다.

통합을 생성한 후 다음 단계를 수행합니다.

* 초기 구성을 변경한 경우 [분류 통합의 유효성을 다시 확인](#re-validate)합니다.
* 분류 통합을 [실행](#run)합니다.
* 분류 통합을 [승인](#approve)합니다.



<!--
         
  

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Consolidations]** > **[!UICONTROL Add]**

The following fields are available when creating a consolidation:

* **[!UICONTROL Name]**: The name of the consolidation.
* **[!UICONTROL Notify of issues]**: A comma-delimited list of email addresses that are notified of issues with this consolidation.
* **[!UICONTROL Dataset to match]**: A drop-down list of all classification sets.

Once you select a classification set, a table with two columns appears:

* The right column contains all classification sets that you want to consolidate. It starts with the classification set selected using the above drop-down list.
* The left column contains all classification sets eligible to be merged with the originally selected dataset. **Schemas must exactly match to be eligible for consolidation**. If schemas do not match the selected classification set, they do not appear in this left column.

Drag the desired classification sets from the available column on the left to the consolidation column on the right. Once the consolidation is given a name and two or more classification sets are in the right column, click **[!UICONTROL Save & Continue]**.

-->

## 통합 편집

분류 통합을 편집하려면 기본 Adobe Analytics 인터페이스에서 다음을 수행합니다.

1. **[!UICONTROL 구성 요소]** 메뉴에서 **[!UICONTROL 분류 집합]**&#x200B;을(를) 선택하십시오.
1. **[!UICONTROL 분류 세트]** 관리자에서 **[!UICONTROL 통합]** 탭을 선택합니다.
1. **[!UICONTROL 분류 세트 통합]** 관리자에서:
   1. 분류 통합의 이름을 선택합니다. **[!UICONTROL 통합: _분류 통합 이름_]**대화 상자가 나타납니다. 모양새 및 사용 가능한 작업은 통합의 현재 상태와 분류 통합을 수정할 수 있는 옵션이 있는지 여부에 따라 달라집니다.

      | 사용 가능한 작업 | 설명 |
      |---|---|
      | ![취소](/help/assets/icons/Cancel.svg) **[!UICONTROL 취소]** | [통합을 취소](#cancel)합니다. |
      | ![확인 표시](/help/assets/icons/Checkmark.svg) **[!UICONTROL 다시 유효성 검사]** | [통합의 유효성을 다시 검사합니다](#re-validate). |
      | ![재생](/help/assets/icons/Play.svg) **[!UICONTROL 실행]** | [통합 실행](#run). |
      | ![ThumbUp](/help/assets/icons/ThumbUp.svg) **[!UICONTROL 승인]** | [통합을 승인](#approve)합니다. |



### 재검증

통합: 분류 통합 대화 상자에서 분류 통합의 유효성을 다시 검사할 수 있습니다. ![경고](/help/assets/icons/Alert.svg)는 통합을 다시 구성해야 하는 통합 관련 문제에 대한 추가 정보를 제공할 수 있습니다.

![분류 세트 - 통합 유효성 재검사](assets/classifications-sets-consolidations-validated.png)

분류 통합의 유효성을 다시 검사하려면 다음을 수행하십시오.

1. 통합을 생성하는 데 사용한 것과 동일한 드래그 앤 드롭 인터페이스를 사용하여 통합을 재구성합니다.
1. ![확인 표시](/help/assets/icons/Checkmark.svg) **[!UICONTROL 다시 유효성 검사]**&#x200B;를 선택합니다. 유효성 검사에서는 각 개별 분류 세트가 이 통합에 유효한지 확인합니다. 성공하면 알림 메시지가 표시됩니다. ![확인 표시](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL 확인을 위한 통합을 제출했습니다!]**
1. 대화 상자를 닫으려면 ![CrossSize400](/help/assets/icons/CrossSize400.svg)을(를) 선택하십시오. 또는 ![재생](/help/assets/icons/Play.svg) 실행을 선택하여 통합을 실행하거나 ![취소](/help/assets/icons/Cancel.svg) 취소를 선택하여 분류를 취소합니다.



<!--
Once you have created a consolidation, a list of source datasets appears on the right. The **[!UICONTROL Validate]** button makes sure that each individual classification set is valid for this consolidation. You can reorder the classification steps here to determine priority in cases of mismatched classification values. **The highest classification set in the list overwrites any mismatched values in other classification sets.**

-->

### 실행

분류 통합이 성공적으로 검증되면 통합을 실행할 수 있습니다.

분류 통합을 실행하려면

1. ![재생](/help/assets/icons/Play.svg) **[!UICONTROL 실행]**&#x200B;을 선택합니다. 알림 메시지에 ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL 처리를 위한 통합을 제출했습니다!]**
1. 대화 상자를 닫으려면 ![CrossSize400](/help/assets/icons/CrossSize400.svg)을(를) 선택하십시오.


### 승인

분류 통합이 실행되면 통합 상태는 **[!UICONTROL 승인 대기 중]**&#x200B;입니다. 분류 통합을 승인하면 개별 분류 세트가 통합된 분류 세트로 대체되며 개별 분류 세트가 제거됩니다.

![분류 세트 - 승인 대기 중인 통합](assets/classifications-sets-consolidations-waitingforapproval.png)

분류 세트 통합을 승인하려면

1. **[!UICONTROL 유사성 보고서]**&#x200B;를 사용하여 통합을 검토하십시오. 이 보고서에는 다음 열이 있는 테이블이 표시됩니다.

   * **[!UICONTROL 분류 세트 이름]**: 분류 세트의 이름입니다.
   * **[!UICONTROL 불일치]**: 키 값이 원본 분류 집합과 일치하지 않는 행의 비율입니다. 불일치 비율이 높으면, 불일치는 분류 데이터가 너무 다르다는 표시일 수 있다. 선택한 분류 세트에 유사한 분류 데이터가 있는지 확인하십시오.
   * **[!UICONTROL 없음]**: 키 값이 ![키](/help/assets/icons/Key.svg) 분류 집합에는 있지만 원본 분류 집합에는 없는 행의 비율입니다. 없는 모든 행은 통합 분류 세트에 추가됩니다.

1. 분류 통합이 승인될 준비가 되면 ![확인 표시](/help/assets/icons/Checkmark.svg) **[!UICONTROL 승인]**&#x200B;을 선택합니다. **[!UICONTROL 통합을 승인하시겠습니까?확인을 묻는 대화 상자가]**&#x200B;개 있습니다. **[!UICONTROL 승인]**&#x200B;을 선택하여 통합을 승인합니다. 취소하려면 **[!UICONTROL 취소]**&#x200B;를 선택합니다.

승인되면 통합된 분류 세트가 생성됩니다. 상태가 **[!UICONTROL 완료]**(으)로 설정되어 있습니다.


### 취소

승인 전에 분류 통합을 취소할 수 있습니다.

분류 통합을 취소하려면,

1. **[!UICONTROL 취소]**&#x200B;를 선택하십시오.

   통합이 취소되면 통합을 재개할 수 없습니다.
1. 통합을 취소하려면 **[!UICONTROL 통합 취소]**&#x200B;를 선택하십시오. 취소를 되돌리려면 **[!UICONTROL 뒤로 이동]**&#x200B;을 선택하십시오.
