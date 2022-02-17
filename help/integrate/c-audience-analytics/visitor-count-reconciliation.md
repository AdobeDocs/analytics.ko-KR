---
description: Adobe Analytics 및 Adobe Audience Manager에는 유사한 정의가 있지만, 여러 가지 이유로 인해 100% 정렬되지 않은 방문자 지표가 있습니다.
title: 방문자 수 차이
feature: Audience Analytics
exl-id: be5a935a-c3a2-4ab4-8cd7-ed54a37932c8
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 100%

---

# 방문자 수 차이

Adobe Analytics 및 Adobe Audience Manager에는 유사한 정의가 있지만, 여러 가지 이유로 인해 100% 정렬되지 않은 방문자 지표가 있습니다.

방문자 지표는 다음과 같습니다.

<table id="table_F9FE107A89934C3B854C55D7D76AC6E8"> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> 지표 </th> 
   <th colname="col3" class="entry"> 정의 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <p><a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder-data.html?lang=ko-KR"  > AAM: 총 세그먼트 채우기</a> </p> </td> 
   <td colname="col3"> <p>전환 확인 기간 동안 세그먼트 멤버였던 디바이스(Experience Cloud ID)의 개수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder-data.html"  > AAM: 실시간 세그먼트 채우기</a> </p> </td> 
   <td colname="col3"> <p>전환 확인 기간 동안 세그먼트 멤버였으며, 속성을 방문한 디바이스(Experience Cloud ID)의 개수입니다. </p> </td> 
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
   <td colname="col2"> <p>UTC (협정 세계시) </p> </td> 
   <td colname="col3"> <p>보고서 세트별로 지정 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 지정 필터 </p> </td> 
   <td colname="col2"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>예. 예: IP 필터, 보트 필터 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>150개 세그먼트 제한 </p> </td> 
   <td colname="col2"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>예 - Analytics 개수는 150개 세그먼트 통합 제한에 따라 최대 5%까지 영향을 받을 수 있습니다. 자르기가 발생하면 대상 이름 차원에 "대상 제한에 도달했습니다."가 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

[Analytics 및 Audience Manager의 세그먼트 이해](/help/integrate/c-audience-analytics/aam-analytics-segments.md)에서 Analytics와 Audience Manager 데이터 및 세그먼테이션의 뉘앙스에 대한 설명을 참조하십시오.
