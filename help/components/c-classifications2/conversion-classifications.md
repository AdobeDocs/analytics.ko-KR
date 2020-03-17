---
description: 분류는 값을 그룹으로 분류하고 그룹 수준으로 보고하는 데 사용됩니다. 예를 들어 모든 유료 검색 캠페인을 "팝 뮤직 용어" 같은 카테고리로 분류하고 인스턴스(클릭스루라고도 함) 같은 지표와 관련한 해당 카테고리의 성공 및 성공 이벤트로의 전환을 보고합니다.
subtopic: Classifications
title: 전환 분류
topic: Admin tools
uuid: 4c8726c9-f527-44e1-be01-8c7b3b5c20f0
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 전환 분류

분류는 값을 그룹으로 분류하고 그룹 수준으로 보고하는 데 사용됩니다. 예를 들어 모든 유료 검색 캠페인을 &quot;팝 뮤직 용어&quot; 같은 카테고리로 분류하고 인스턴스(클릭스루라고도 함) 같은 지표와 관련한 해당 카테고리의 성공 및 성공 이벤트로의 전환을 보고합니다.

## 전환 분류 {#concept_B4B1478A8CB540599AC9D4A58CA4B6FE}

분류는 값을 그룹으로 분류하고 그룹 수준으로 보고하는 데 사용됩니다. 예를 들어 모든 유료 검색 캠페인을 *팝 뮤직 용어* 같은 카테고리로 분류하고 인스턴스(클릭스루라고도 함) 같은 지표와 관련한 해당 카테고리의 성공 및 성공 이벤트로의 전환을 보고합니다.

전환 분류를 사용하면 전환 변수를 분류할 수 있습니다. 한 번 분류하면, 키 데이터를 사용하여 생성할 수 있는 어떤 보고서도 관련 데이터 속성을 사용하여 생성할 수 있습니다.

분류를 활성화한 후에 [분류 가져오기](/help/components/c-classifications2/c-classifications-importer/c-working-with-saint.md)를 사용하여 해당 분류에 특정 값을 할당할 수 있었습니다.

## 전환 분류 설명 {#section_4A98DD5F5C314B9DAEE710AEE4EE51D4}

<table id="table_0B72C485467348E2A34BF913441F4AF5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 이름 </span> </td> 
   <td colname="col2"> 분류 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 활성화된 날짜(텍스트만)</span> </td> 
   <td colname="col2"> <p>텍스트 분류가 캠페인 변수의 날짜 범위인지 여부를 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 옵션(텍스트만)</span> </td> 
   <td colname="col2">이 분류에 사용 가능한 분류 값 목록을 만듭니다. 캠페인 변수와 함께 <span class="wintitle">옵션</span>을 사용하여 <span class="wintitle">캠페인 관리자</span>에서 분류에 대해 지원되는 값 목록을 사용자에게 제공합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 숫자 유형(숫자만)</span> </td> 
   <td colname="col2">숫자 분류에서 숫자 유형을 지정합니다. 옵션에는 <span class="wintitle">숫자</span>, <span class="wintitle">백분율</span> 및 <span class="wintitle">통화</span>가 포함됩니다. </td> 
  </tr> 
 </tbody> 
</table>

## 전환 분류 추가 {#task_D535D09E3EAF4CD1A15A6B93C0BB1BB5}

<!-- 

t_classification_conversion.xml

 -->

관리자에서 전환 분류를 추가하는 방법을 설명하는 단계입니다.

1. **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;를 클릭합니다.
1. 보고서 세트 선택.
1. **[!UICONTROL 설정 편집]** > **[!UICONTROL 전환]** > **[!UICONTROL 전환 분류]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 분류 유형 선택]** 드롭다운 목록에서 분류를 추가하려는 변수를 선택합니다.

   ![단계 정보](assets/sub_class_create.png)

1. **[!UICONTROL 분류 편집]** 아이콘으로 마우스를 가져간 다음 **[!UICONTROL 분류 추가]**&#x200B;를 선택합니다.
1. **[!UICONTROL 유형 선택]** 필드에서 변수에 추가하려는 분류 유형을 선택합니다.

   옵션에는 **[!UICONTROL 텍스트]** 및 **[!UICONTROL 숫자]**&#x200B;가 포함됩니다. 분류 유형에 대한 자세한 내용은 [분류에 대하여](/help/components/c-classifications2/c-classifications.md)를 참조하십시오.
1. **[!UICONTROL 테스트 분류]** 대화 상자에서 원하는 대로 분류를 구성합니다.

   이러한 요소에 대한 자세한 내용은 [전환 분류 설명](/help/components/c-classifications2/conversion-classifications.md#section_4A98DD5F5C314B9DAEE710AEE4EE51D4)을 참조하십시오.

1. **[!UICONTROL 드롭다운 목록]** 대화 상자에서, 옵션을 추가하거나 제거합니다.

   옵션을 추가하면 이 분류에 사용 가능한 분류 값 목록이 만들어집니다. 캠페인 변수와 함께 이 옵션을 사용하여 캠페인 관리자에서 분류에 대해 지원되는 값 목록을 사용자에게 제공할 수 있습니다. 거의 변경되지 않거나 절대 변경되지 않는 작은 수의 허용된 값이 있는 분류 차원에 대해 사용하십시오. 예를 들어, 실버, 골드 및 팬티엄과 같이 다양한 수준의 고객 충성도를 대상으로 하는 다양한 캠페인을 실행할 수 있습니다. 그런 다음 드롭다운 목록을 사용하여 수락되는 값만 세 수준과 일치하는 값이 되도록 할 수 있습니다. 다른 값을 사용하는 경우는 무시됩니다.
1. **[!UICONTROL 저장을 클릭합니다]**.

## 전환 분류 삭제 {#task_566651BC245944618A6A833E58211FDE}

<!-- 

t_classification_delete_conversion.xml

 -->

더 이상 필요하지 않은 전환 분류를 삭제합니다.

1. 세트 헤더에서 **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;를 클릭하여 보고서 세트 관리자를 엽니다.
1. 보고서 세트 선택.
1. **[!UICONTROL 설정 편집]** > **[!UICONTROL 전환]** > **[!UICONTROL 전환 분류]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 분류 유형 선택]** 드롭다운 목록에서 분류를 삭제하려는 변수를 선택합니다.
1. **[!UICONTROL 분류 편집]** 아이콘으로 마우스를 가져간 다음 **[!UICONTROL 분류 삭제]**&#x200B;를 선택합니다.
1. 분류 삭제 대화 상자에서 **[!UICONTROL 삭제]**&#x200B;를 클릭합니다.
