---
description: 계산된 지표 권한은 관리자 수준 사용자와 관리자가 아닌 사용자 간에 다릅니다.
seo-description: 계산된 지표 권한은 관리자 수준 사용자와 관리자가 아닌 사용자 간에 다릅니다.
seo-title: 계산된 지표 역할 기반 권한
title: 계산된 지표 역할 기반 권한
uuid: 7 c 14 d 32 d -370 c -4 afa -8 f 80-5 bbd 8 fc 12 ec 7
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 계산된 지표: 역할 기반 권한

계산된 지표 권한은 관리자 수준 사용자와 관리자가 아닌 사용자 간에 다릅니다.

<table id="table_13F72FD90C964B86BD4B51E6F51ED292"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col02" class="entry"> 선택 사항에서 </th> 
   <th colname="col2" class="entry"> 공유 </th> 
   <th colname="col3" class="entry"> 보기/관리 </th> 
   <th colname="col4" class="entry"> 승인 </th> 
   <th colname="col5" class="entry"> 적용 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>관리자 수준 사용자</b> </td> 
   <td colname="col02"> 관리자는 계산된 지표를 만들 수 있을 뿐만 아니라 사용자 권한을 제한하는 <a href="https://marketing.adobe.com/resources/help/en_US/reference/groups.html" format="https" scope="external">그룹</a>을 만들어 계산된 지표를 만들 수도 있습니다. </td> 
   <td colname="col2"> 전체 회사, 사용자 그룹 및 개별 사용자와 공유할 수 있습니다. </td> 
   <td colname="col3"> <span class="keyword"> [! Uicontrol Reports &amp; Analytics] </span>: 보기/편집/삭제 등을 수행할 수 있습니다. 계산된 지표를 보거나 편집하거나 삭제할 수 있습니다. <p> <span class="keyword"> Ad Hoc Analysis</span> 및 <span class="keyword">Report Builder</span>: 보기/편집/삭제 등을 수행할 수 있습니다. 계산된 지표를 보거나 편집하거나 삭제할 수 있습니다. </p> </td> 
   <td colname="col4"> 계산된 지표를 표준으로 승인할 수 있습니다. </td> 
   <td colname="col5"> 전체 조직 내에서 어떤 계산된 지표도 적용할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>관리자 이외 수준의 사용자</b> </td> 
   <td colname="col02"> 기본적으로 사용자는 계산된 지표를 만들 수 있습니다. 하지만 관리자가 이러한 권한을 제한할 수 있습니다. </td> 
   <td colname="col2"> 개별 사용자와만 공유할 수 있습니다. </td> 
   <td colname="col3"> 본인의 계산된 지표만 보거나 편집하거나 삭제할 수 있습니다. <p>관리자가 아닌 사용자는 공유 지표를 볼 수 있도록 모든 구성 요소 이벤트에 액세스할 수 있어야 합니다(관리 콘솔의 권한이 여전히 적용됨). </p> <p>대시보드 또는 예약된 보고서가 관리자가 아닌 사용자와 공유되고 여기에 이 사용자와 공유된 지표가 없을 경우, 보고서는 적용된 지표로 실행됩니다(이벤트를 볼 권한이 있다는 가정 하에). 하지만 이 사용자는 정의를 보거나 지표를 편집할 수 없게 됩니다. </p> </td> 
   <td colname="col4"> 승인된 계산된 지표만 사용할 수 있고 승인됨으로 표시할 수 없습니다. </td> 
   <td colname="col5"> 본인의 계산된 지표와 본인이 공유하는 세그먼트만 적용할 수 있습니다. </td> 
  </tr> 
 </tbody> 
</table>

