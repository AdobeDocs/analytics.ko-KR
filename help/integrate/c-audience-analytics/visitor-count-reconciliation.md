---
description: Adobe Analytics 및 Adobe Audience Manager에는 유사한 정의가 있지만, 여러 가지 이유로 인해 100% 정렬되지 않은 방문자 지표가 있습니다.
title: 방문자 수 차이
feature: Audience Analytics
exl-id: be5a935a-c3a2-4ab4-8cd7-ed54a37932c8
TQID: 'https://experienceleague.adobe.com/ksfYYDZ6G9vH7WEZVh-JsN93Rl-jsZTe9-CQADSwnfI'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
subfeature_v2: id: a97e0d8c-238a-47ee-8d81-16bd45309bed
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 312
ht-degree: 56%

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
   <td colname="col2"> <p><a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder-data.html?lang=ko-KR"  > Adobe Audience Manager: 총 세그먼트 채우기</a> </p> </td> 
   <td colname="col3"> <p>전환 확인 기간 동안 세그먼트 멤버였던 디바이스(Experience Cloud ID)의 개수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder-data.html?lang=ko-KR"  > Adobe Audience Manager: 실시간 세그먼트 채우기</a> </p> </td> 
   <td colname="col3"> <p>전환 확인 기간 동안 세그먼트 멤버였으며, 속성을 방문한 디바이스(Experience Cloud ID)의 개수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analytics: 고유 방문자 </p> </td> 
   <td colname="col3"> <p>보고 기간 동안 사용자의 속성에 도달한 고유 방문자 수를 보여 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analytics: Experience Cloud ID를 가진 방문자 수 </p> </td> 
   <td colname="col3"> <p>보고 기간 동안 Experience Cloud ID를 사용하여 속성에 도달한 고유 방문자 수를 보여줍니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

Adobe Audience Manager 실시간 세그먼트 모집단과 Audience Analytics 보고 내에서 사용되는 Experience Cloud ID가 있는 Analytics 방문자 수가 가장 비슷할 것입니다. 그러나 단기적으로는 몇 가지 요인으로 인해 둘 사이에 약간의 불일치가 있을 것입니다. 기여 요인은 다음과 같습니다.

<table id="table_A391B37CC077456F8BB83BAA3C640EF6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> Adobe Audience Manager: 실시간 세그먼트 채우기 </th> 
   <th colname="col3" class="entry"> Analytics: Experience Cloud ID를 가진 방문자 수 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>시간대 </p> </td> 
   <td colname="col2"> <p>UTC (협정 세계시) </p> </td> 
   <td colname="col3"> <p>보고서 세트별로 지정됨 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 정의 필터 </p> </td> 
   <td colname="col2"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>예. 예: IP 필터, 보트 필터 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>150개 세그먼트 제한 </p> </td> 
   <td colname="col2"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>예 - Analytics 수는 150개 세그먼트 통합 제한의 영향을 최대 5%까지 받을 수 있습니다. 자르기가 발생하면 대상자 이름 차원에 "대상자 제한에 도달했습니다."가 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

[Analytics 및 Audience Manager의 세그먼트 이해](/help/integrate/c-audience-analytics/aam-analytics-segments.md)에서 Analytics와 Audience Manager 데이터 및 세그먼테이션의 뉘앙스에 대한 설명을 참조하십시오.
