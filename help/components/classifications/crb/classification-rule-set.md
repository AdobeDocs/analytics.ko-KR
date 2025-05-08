---
description: 규칙 세트는 특정 변수에 대한 분류 규칙 그룹입니다. 규칙 세트에 변수를 적용합니다. 1개의 변수에 여러 규칙 세트를 만들려면 각 규칙 세트를 여러 보고서 세트에 적용해야 합니다.
title: 분류 규칙 세트
feature: Classifications
exl-id: 5c118541-d143-4947-b693-514d7042abe6
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 89%

---

# 분류 규칙 세트 (기존)

*이 페이지에서는 [분류 규칙 빌더](classification-rule-builder.md)의 일부로 분류 규칙 집합에 대해 설명합니다. Adobe Analytics에서 데이터를 분류하는 현재 방법은 [분류 세트](../sets/overview.md)를 참조하십시오.*

규칙 세트는 특정 변수에 대한 분류 규칙 그룹입니다. 규칙 세트에 변수를 적용합니다. 1개의 변수에 여러 규칙 세트를 만들려면 각 규칙 세트를 여러 보고서 세트에 적용해야 합니다.

## 분류 규칙 빌더 페이지 {#section_C60B0888C76D49C596EF19F11808B718}

**[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 분류 규칙 빌더]**

다음 필드와 옵션은 [!UICONTROL 분류 규칙 빌더]에서 사용할 수 있습니다.

<table id="table_A5D92409969747E39E041216A5AA32CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="/help/components/classifications/crb/classification-rule-set.md"  > 규칙 세트 추가</a> </p> </td> 
   <td colname="col2"> <p>규칙 세트를 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>규칙 </p> </td> 
   <td colname="col2"> 세트에 포함된 규칙 수를 표시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>상태 </p> </td> 
   <td colname="col2"> 초안 또는 활성과 같은 규칙 세트의 활동 상태를 표시합니다. 활성 규칙은 매일 처리되며, 일반적으로 한 달 이전의 분류 데이터를 조사합니다. 이 규칙은 자동으로 새로운 값을 확인하고 분류를 업로드합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마지막 변경 </p> </td> 
   <td colname="col2"> 규칙 세트가 언제 편집되었는지 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>복제 </p> </td> 
   <td colname="col2"> 규칙 세트를 다른 변수에 적용하거나 다른 보고서 세트의 동일한 변수에 적용할 수 있도록 규칙 세트를 복제(복사)합니다. </td> 
  </tr> 
 </tbody> 
</table>

## 분류 규칙 세트 만들기 {#create-classification-rule-set}

분류 규칙 세트의 이름을 지정하고, 변수를 적용하고 덮어쓰기 설정을 지정합니다.

1. (사전 요구 사항) **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;에서 분류 구조를 정의합니다.

   변수에 대해 분류가 하나 이상 정의되어 있어야 변수가 [!UICONTROL 새 규칙 세트] 패널에 표시됩니다.

   **[!UICONTROL 관리자]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 트래픽]** > **[!UICONTROL 트래픽 분류]**(또는 **[!UICONTROL 전환]** > **[!UICONTROL 전환 분류]**)에서 변수에 대한 분류를 만들 수 있습니다. 그런 다음, 변수를 선택하고 **[!UICONTROL 분류 추가]**&#x200B;를 클릭합니다.

1. 규칙 세트를 만들려면, **[!UICONTROL 관리]** > **[!UICONTROL 분류 규칙 빌더]** > **[!UICONTROL 규칙 세트 추가]**&#x200B;를 클릭합니다.

   ![](assets/new_rule_set.png)

1. 규칙 세트의 이름을 지정한 다음, **[!UICONTROL 규칙 세트 만들기]**&#x200B;를 클릭합니다.
1. 편집할 규칙 세트를 선택합니다.

   ![](assets/classification_rules_page.png)

1. **[!UICONTROL 보고서 세트 및 변수 선택]**&#x200B;을 클릭합니다.

   보고서 세트 및 변수 목록은 로그인 회사의 모든 보고서 세트에서 사용할 수 있는 모든 분류된 변수로 채워집니다. 보고서 세트의 단일 변수는 하나의 규칙 세트에만 속할 수 있습니다.

   자세한 내용은 [분류 규칙 빌더](/help/components/classifications/crb/classification-rule-definitions.md) 페이지의 정의에서 *`Variable`*&#x200B;을(를) 참조하십시오.
1. 사용할 보고서 세트와 변수를 지정한 다음, **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
1. 규칙 세트에 [분류 규칙을 추가](/help/components/classifications/crb/classification-rule-set.md)하여 계속 진행합니다.
