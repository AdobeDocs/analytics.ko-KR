---
description: 대상을 사용하면 웹 사이트 성능을 측정하고 대상이 되는 목표를 기준으로 진행 상황을 추적할 수 있습니다. 예를 들어 지리적 영역에서 오는 방문자 수, 주문당 매출 또는 특정 레퍼러에서 오는 히트 수를 증가시킬 수 있습니다.
title: 타겟
topic: Reports and analytics
uuid: bfe29dc8-8da8-4107-8bb1-4a7494f12bc9
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 타겟

대상을 사용하면 웹 사이트 성능을 측정하고 대상이 되는 목표를 기준으로 진행 상황을 추적할 수 있습니다. 예를 들어 지리적 영역에서 오는 방문자 수, 주문당 매출 또는 특정 레퍼러에서 오는 히트 수를 증가시킬 수 있습니다.

## 타겟 {#concept_6516E81923E845198B7FC5D8F81DC35C}

대상을 사용하면 웹 사이트 성능을 측정하고 대상이 되는 목표를 기준으로 진행 상황을 추적할 수 있습니다. 예를 들어 지리적 영역에서 오는 방문자 수, 주문당 매출 또는 특정 레퍼러에서 오는 히트 수를 증가시킬 수 있습니다.

대상을 만들 때 측정하려는 지표 또는 eVar을 선택하거나 선택한 지표에 대해 전체 사이트를 측정하도록 선택할 수 있습니다.

예를 들어 웹 사이트의 고유 방문자 수를 측정하고 이것을 대상으로 사용할 수 있습니다. 이 경우 전체 웹 사이트를 선택합니다. 그러나 시카고의 웹 사이트를 방문하는 고유 방문자 수를 대상으로 지정하려면 전체 사이트를 확인하는 대신 해당 eVar를 지정할 수 있습니다.

## 대상 필드 설명 {#section_44DFFB4A7AC54D65BC2345411686B2AD}

**[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Targets]**.

페이지의 필드 및 옵션에 대한 [!UICONTROL Add/Edit Target] 설명입니다.

<table id="table_E08728BECC204DF59F0AC99957A68CAE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Target 이름  </td> 
   <td colname="col2"><span class="wintitle">대상 관리자</span> 페이지에 표시되는 대상 이름이 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 적용 대상 </td> 
   <td colname="col2"> 전체 사이트 또는 선택한 특성이나 eVar에 대상을 적용할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 항목 선택 </td> 
   <td colname="col2"> <p>관련 항목에 대해 고급 검색을 수행할 수 있도록 선택한 특성 또는 eVar에 대한 선택 양식이 표시됩니다. 예를 들어 eVar <span class="uicontrol">국가</span>를 선택하면 항목 목록을 사용해서 국가를 지정할 수 있습니다. eVar <span class="uicontrol">제품</span>을 선택하면 항목 목록을 사용해서 제품을 지정할 수 있습니다. 커스텀 인사이트 변수도 메뉴에 나열됩니다. 커스텀 인사이트 변수를 설정하여 방문자 연령 범위를 측정하는 경우 항목 목록은 18-24, 25-35 등과 같은 연령 범위를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 지표 </td> 
   <td colname="col2">지표에 대상을 적용할 수 있습니다. 이 메뉴는 지정된 eVar에 적용되는 지표만 표시합니다. 예를 들어 <span class="uicontrol">제품</span>을 eVar로 선택하는 경우 <span class="uicontrol">페이지 종료</span> 같은 지표는 적용되지 않습니다. <span class="uicontrol">페이지 종료</span> 지표는 웹 페이지 eVar에 적용할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 기간 </td> 
   <td colname="col2"> <p>대상의 <span class="uicontrol">날짜 범위</span> 및 <span class="uicontrol">세부 기간</span> 설정을 정의할 수 있습니다. 날짜 범위 사양에 따라 일부 세부 기간 옵션은 적용되지 않습니다. 지표에 대한 값을 입력할 때 각 세부 기간 설정에 해당하는 값을 입력합니다. 예를 들어 날짜 범위가 2월 한 달이고 세부 기간을 주별로 선택한 경우 2월의 각 주에 해당하는 값을 입력합니다. 각 세부 기간 설정에 대한 대상 보고서가 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 값 </td> 
   <td colname="col2"> <p>기간 및 선택한 지표에 대한 대상 값을 지정할 수 있습니다. 이 값은 도달하려는 대상 숫자입니다. 예를 들어 매출을 기준으로 해당 월에 $10,000의 매출을 대상로 한 경우 해당 월의 값 필드에 10000을 입력합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 대상 추가 {#task_94915391E26E4F808F2538AA92BC7E71}

대상을 추가하는 방법을 설명하는 단계입니다.

<!-- 

t_add_a_target.xml

 -->

1. 클릭 **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Targets]**.
1. 페이지에서 [!UICONTROL Target Manager] 을 클릭합니다 **[!UICONTROL Add New]**.
1. [타겟 필드 설명](/help/analyze/reports-analytics/targets.md#section_44DFFB4A7AC54D65BC2345411686B2AD)에 설명되어 있는 옵션을 구성합니다.
1. 클릭 **[!UICONTROL OK]**.

## 대상 편집 {#task_946C558D2ECC4922ABD4A5A6183A095A}

1. 클릭 **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Targets]**.
1. In the **[!UICONTROL Manage]** column, click the **[!UICONTROL Edit]** icon.
1. [타겟 필드 설명](/help/analyze/reports-analytics/targets.md#section_44DFFB4A7AC54D65BC2345411686B2AD)에 설명되어 있는 옵션을 구성합니다.
1. 클릭 **[!UICONTROL OK]**.
