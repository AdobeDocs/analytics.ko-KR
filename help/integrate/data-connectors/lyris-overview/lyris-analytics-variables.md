---
description: 각 보고서 세트 구현에 대해 예약할 Evar 및 이벤트를 설명합니다.
seo-description: 각 보고서 세트 구현에 대해 예약할 Evar 및 이벤트를 설명합니다.
seo-title: Lyris 용 Adobe Analytics 변수 구성
solution: Analytics
title: Lyris 용 Adobe Analytics 변수 구성
uuid: 12 E 150 C 4-052 A -481 C -8 C 27-EF 45 EE 801977
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Configure Adobe Analytics variables for Lyris{#configure-adobe-analytics-variables-for-lyris}

각 보고서 세트 구현에 대해 예약할 Evar 및 이벤트를 설명합니다.

이 통합을 사용하려면 각 보고서 세트 구현에 대해 최소 2 개의 Evar가 예약되어야 합니다. 이러한 Evar 외에도, Analytics에서 보고자 하는 Lyris 데이터에 따라 몇 개의 이벤트를 예약할 수 있습니다. 이러한 Evar 및 이벤트는 아래 표에 설명되어 있습니다.

<table id="table_43E32344E9E54FED8491F28047249329"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 변수 유형 </th> 
   <th colname="col2" class="entry"> 변수 이름 </th> 
   <th colname="col3" class="entry"> 변수의 사용 방법 </th> 
   <th colname="col4" class="entry"> 설정 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> 메시지 ID </td> 
   <td colname="col3"> 개별 이메일 메시지 캠페인 식별을 캡처하려면 </td> 
   <td colname="col4"> <p>상태: enabled </p> <p>할당: 최신 항목 </p> <p>다음 이후에 만료: «비즈니스 의사 결정» </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Email Recipient ID </td> 
   <td colname="col3"> 이메일 캠페인을 클릭한 고객에 대한 익명 ID를 캡처하려면 </td> 
   <td colname="col4"> <p>상태: enabled </p> <p>할당: 최신 항목 </p> <p>다음 이후에 만료: «비즈니스 의사 결정» </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 전송된 이메일 </td> 
   <td colname="col3"> No. Lyris에서 보낸 이메일 </td> 
   <td colname="col4">유형: Numeric <p>기여도: enabled </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 열어본 이메일 </td> 
   <td colname="col3"> No. 열린 이메일 </td> 
   <td colname="col4">유형: Numeric <p>기여도: enabled </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 열렸던 고유 이메일 </td> 
   <td colname="col3"> No. 열린 고유한 이메일 </td> 
   <td colname="col4">유형: Numeric <p>기여도: enabled </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 이메일 클릭스루 </td> 
   <td colname="col3"> No. 이메일을 클릭한 횟수 </td> 
   <td colname="col4">유형: Numeric <p>기여도: enabled </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 이메일 바운스 </td> 
   <td colname="col3"> No. 반송된 이메일 </td> 
   <td colname="col4">유형: Numeric <p>기여도: enabled </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> Lyris - 이메일 가입 해지 </td> 
   <td colname="col3"> No. 비활성화된 이메일 구독 </td> 
   <td colname="col4">유형: Numeric <p>기여도: enabled </p> </td> 
  </tr> 
 </tbody> 
</table>

