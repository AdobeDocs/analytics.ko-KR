---
description: 다음은 가상 보고서 세트 만들기를 시작하기 전에 주의해야 할 몇 가지 사항입니다.
keywords: 가상 보고서 세트
title: 가상 보고서 세트 만들기
feature: Reports & Analytics 기본 사항
uuid: 022a6656-808e-4c92-b7ec-4d2a42e84fa8
exl-id: 5ff6ff1a-5b99-41cc-a3a7-928197ec9ef9
translation-type: tm+mt
source-git-commit: cddf2a76ca36914f133379959b7cbb5246bdd695
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 100%

---

# 가상 보고서 세트 만들기

다음은 가상 보고서 세트 만들기를 시작하기 전에 주의해야 할 몇 가지 사항입니다.

* 관리자가 아닌 사용자에게는 가상 보고서 세트 관리자가 표시되지 않습니다.
* 가상 보고서 세트를 공유할 수 없습니다. &quot;공유&quot;는 그룹/권한을 통해 수행됩니다.
* 가상 보고서 세트 관리자에서는 자신의 가상 보고서 세트만 볼 수 있습니다. 다른 모든 사용자의 가상 보고서 세트를 표시하려면 &quot;모두 표시&quot;를 클릭해야 합니다.

1. **[!UICONTROL 구성 요소]** > **[!UICONTROL 가상 보고서 세트]**&#x200B;로 이동합니다.
1. **[!UICONTROL 추가를 클릭합니다 +]**.

   ![](assets/new_vrs.png)

1. 다음 필드를 채웁니다.

<table id="table_0F85B56480BB46CBA5BE236BBD70156D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">  이름  </td> 
   <td colname="col2"> <p>가상 보고서 세트 이름은 상위 보고서 세트에서 상속되지 않으므로 구분해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 설명 </td> 
   <td colname="col2"> <p>비즈니스 사용자의 혜택에 대한 설명을 추가합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 태그 </td> 
   <td colname="col2"> <p>태그를 추가하여 보고서 세트를 구성할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 그룹  </td> 
   <td colname="col2"> <p>이 VRS에 대한 액세스 권한을 원하는 권한 그룹을 선택합니다.  (<span class="ignoretag"><span class="uicontrol">관리</span> &gt; <span class="uicontrol">사용자 관리</span> &gt; <span class="uicontrol">그룹</span></span>에서 그룹 권한을 관리할 수도 있습니다.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상위 보고서 세트 </td> 
   <td colname="col2"> <p>이 가상 보고서 세트에 다음 설정을 상속하는 보고서 세트입니다. 대부분의 서비스 수준 및 기능 (예: eVar 설정, 처리 규칙, 분류 등)이 상속됩니다. VRS에서 상속한 이러한 설정을 변경하려면 상위 보고서 세트를 편집해야 합니다 (<span class="ignoretag"><span class="uicontrol">관리</span> &gt; <span class="uicontrol">보고서 세트</span></span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간대 </td> 
   <td colname="col2"> <p>시간대 선택은 선택 사항입니다. </p> <p>시간대를 선택하면 VRS와 함께 저장됩니다. 시간대를 선택하지 않으면 상위 보고서 세트의 시간대가 사용됩니다. </p> <p>VRS를 편집할 때 VRS와 함께 저장된 시간대가 드롭다운 선택기에 표시됩니다. 시간대 지원이 추가되기 전에 VRS가 생성된 경우 상위 보고서 세트의 시간대가 드롭다운 선택기에 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 세그먼트 </td> 
   <td colname="col2"> <p>한 개 세그먼트를 추가하거나 <a href="https://docs.adobe.com/content/help/ko-KR/analytics/components/segmentation/segmentation-workflow/seg-build.html"  >세그먼트를 스택</a>할 수 있습니다. </p> <p> <p>참고: 2개의 세그먼트를 스택할 때 AND 문으로 연결됩니다. 이것을 OR 문으로 변경할 수 없습니다. </p> </p> <p>현재 가상 보고서 세트에 사용된 세그먼트를 삭제하거나 수정하려고 하면 경고가 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
