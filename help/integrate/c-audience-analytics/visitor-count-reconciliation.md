---
description: Adobe Analytics 및 Adobe Audience Manager에는 유사한 정의가 있지만, 여러 가지 이유로 인해 100% 정렬되지 않은 방문자 지표가 있습니다.
seo-description: Adobe Analytics 및 Adobe Audience Manager에는 유사한 정의가 있지만, 여러 가지 이유로 인해 100% 정렬되지 않은 방문자 지표가 있습니다.
seo-title: 방문자 수 차이
title: 방문자 수 차이
uuid: c3bbb887-bd02-4c1c-9a2b-64811c0ef56a
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 방문자 수 차이

Adobe Analytics 및 Adobe Audience Manager에는 유사한 정의가 있지만, 여러 가지 이유로 인해 100% 정렬되지 않은 방문자 지표가 있습니다.

방문자 지표은 다음과 같습니다.

<table id="table_F9FE107A89934C3B854C55D7D76AC6E8"> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> 지표 </th> 
   <th colname="col3" class="entry"> 정의 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <p><a href="https://marketing.adobe.com/resources/help/en_US/aam/segment-builder-data.html" format="html" scope="external"> AAM: 총 세그먼트 채우기</a> </p> </td> 
   <td colname="col3"> <p>전환 확인 기간 동안 세그먼트 회원이었던 장치(Experience Cloud ID)의 개수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><a href="https://marketing.adobe.com/resources/help/en_US/aam/segment-builder-data.html" format="html" scope="external"> AAM: 실시간 세그먼트 채우기</a> </p> </td> 
   <td colname="col3"> <p>전환 확인 기간 동안 세그먼트 회원이었으며, 속성을 방문한 장치(Experience Cloud ID)의 개수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analytics: 고유 방문자 수 </p> </td> 
   <td colname="col3"> <p>보고 기간 중 귀하의 속성을 방문한 고유 방문자 수를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analytics: Experience Cloud ID를 가진 방문자 </p> </td> 
   <td colname="col3"> <p>보고 기간 중 Experience Cloud ID를 가진 방문자로, 속성을 방문한 고유 방문자 수를 표시합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

AAM 실시간 세그먼트 채우기 및 Audience Analytics 보고 내에 사용된 Experience Cloud ID를 가진 Analytics 방문자가 가장 유사합니다. 그러나 조만간 여러 요인으로 인해 이들 사이의 약간의 불일치가 있을 것입니다. 기여 요소는 다음과 같습니다.

<table id="table_A391B37CC077456F8BB83BAA3C640EF6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> AAM: 실시간 세그먼트 채우기 </th> 
   <th colname="col3" class="entry"> Analytics: Experience Cloud ID를 가진 방문자 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>시간대 </p> </td> 
   <td colname="col2"> <p>UTC(협정 세계시) </p> </td> 
   <td colname="col3"> <p>보고서 세트별로 지정 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 지정 필터 </p> </td> 
   <td colname="col2"> <p>아니오 </p> </td> 
   <td colname="col3"> <p>예, 예: IP 필터, 보트 필터 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>150개 세그먼트 제한 </p> </td> 
   <td colname="col2"> <p>아니오 </p> </td> 
   <td colname="col3"> <p>예 - Analytics 개수는 150개 세그먼트 통합 제한에 따라 최대 5%까지 영향을 받을 수 있습니다. 잘림이 발생한 경우 "대상자 제한에 도달함"이 대상 이름 차원에 나타납니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

See [Understanding Segments in Analytics and Audience Manager](../../integrate/c-audience-analytics/aam-analytics-segments.md#concept_AB72F76AFAF14F82A5BB17809925813B) for additional explanation on the nuances between Analytics and Audience Manager data and segmentation.
