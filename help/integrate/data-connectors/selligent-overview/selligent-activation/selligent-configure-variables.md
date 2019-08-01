---
description: 이 통합을 사용하려면 각 보고서 세트 구현에 대해 2 개의 Evar가 예약되어야 합니다.
seo-description: 이 통합을 사용하려면 각 보고서 세트 구현에 대해 2 개의 Evar가 예약되어야 합니다.
seo-title: Selligent에 대한 Analytics 변수 구성
solution: Analytics
title: Selligent에 대한 Analytics 변수 구성
uuid: 3 B 7 B 8 B 4 B -7614-4439-BCB 0-DBDEC 5304844
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Configure Analytics Variables for Selligent{#configure-analytics-variables-for-selligent}

이 통합을 사용하려면 각 보고서 세트 구현에 대해 2 개의 Evar가 예약되어야 합니다.

이러한 Evar 외에도, Analytics에서 보려는 Selligent의 데이터에 따라 몇 개의 이벤트가 예약될 수 있습니다. 이러한 Evar 및 이벤트는 다음과 같이 설명됩니다.

<table id="table_2FFB865DBD80412F90DA8E224B12FB62"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 변수 유형 </th> 
   <th colname="col2" class="entry"> 변수 이름 </th> 
   <th colname="col3" class="entry"> 사용 방법 </th> 
   <th colname="col4" class="entry"> 설정 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> 메시지 ID </td> 
   <td colname="col3"> to capture the individual email message campaign identification. </td> 
   <td colname="col4"> <p><b>상태</b>: enabled </p> <p><b>할당</b>: 최신 항목 </p> <p><b>다음 이후에 만료</b>: «비즈니스 의사 결정» </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> EV AR </td> 
   <td colname="col2"> Recipient ID </td> 
   <td colname="col3"> 이메일 캠페인을 클릭한 고객에 대한 익명 ID를 캡처합니다. </td> 
   <td colname="col4"> <p><b>상태</b>: enabled </p> <p><b>할당</b>: 최신 항목 </p> <p><b>다음 이후에 만료</b>: «비즈니스 의사 결정» </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> sent </td> 
   <td colname="col3"> Selligent에서 보낸 이메일의 수를 저장합니다. </td> 
   <td colname="col4"> <p><b></b>유형: Numeric </p> <p><b>기여도</b>: enabled </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 배달됨 </td> 
   <td colname="col3"> 배달된 이메일의 수를 저장합니다. </td> 
   <td colname="col4"> <p><b></b>유형: Numeric </p> <p><b>기여도</b>: enabled </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 보기 횟수 </td> 
   <td colname="col3"> 을 클릭하여 본 고유한 이메일의 수를 저장합니다. </td> 
   <td colname="col4"> <p><b></b>유형: Numeric </p> <p><b>기여도</b>: enabled </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 클릭 수 </td> 
   <td colname="col3"> 을 클릭하여 이메일을 클릭한 횟수를 저장합니다. </td> 
   <td colname="col4"> <p><b></b>유형: Numeric </p> <p><b>기여도</b>: enabled </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 바운스됨 </td> 
   <td colname="col3"> 바운스된 이메일의 수를 저장합니다. </td> 
   <td colname="col4"> <p><b></b>유형: Numeric </p> <p><b>기여도</b>: enabled </p> </td> 
  </tr> 
 </tbody> 
</table>

