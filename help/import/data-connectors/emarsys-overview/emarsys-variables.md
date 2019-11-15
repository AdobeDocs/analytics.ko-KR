---
description: emarsys에 대한 데이터 커넥터 통합에서는 Analytics 변수를 사용하여 다양한 emarsys 지표를 추적합니다.
title: Analytics 변수
uuid: 4d5e087c-f495-4aab-9ad1-9b901d34a254
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Analytics 변수{#analytics-variables}

emarsys에 대한 데이터 커넥터 통합에서는 Analytics 변수를 사용하여 다양한 emarsys 지표를 추적합니다.

emarsys 통합에 사용할 이벤트 및 eVar를 식별한 후 관리 콘솔에서 [활성화합니다](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/c-admin-tools.html).

**필수 변수**

<table id="table_5B8F3A1EB55D4BB48F669FB84C857256"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 변수 유형 </th> 
   <th colname="col2" class="entry">  이름  </th> 
   <th colname="col3" class="entry"> 채우기 방법 </th> 
   <th colname="col4" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이벤트(숫자) </td> 
   <td colname="col2"> 총 바운스 수 </td> 
   <td colname="col3"> <p>emarsys에서 자동으로 가져오기 </p> </td> 
   <td colname="col4"> <p>총 바운스 수 이벤트를 사용하면 배달 문제로 인해 수신자에게 배달되지 않은 이메일 메시지 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트(숫자) </td> 
   <td colname="col2"> 클릭됨 </td> 
   <td colname="col3"> <p>emarsys에서 자동으로 가져오기 </p> </td> 
   <td colname="col4"> <p>클릭된 이벤트를 사용하면 이메일 메시지를 클릭한 방문자 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트(숫자) </td> 
   <td colname="col2"> 열림 </td> 
   <td colname="col3"> <p>emarsys에서 자동으로 가져오기 </p> </td> 
   <td colname="col4"> <p>열림 이벤트를 사용하면 이메일 메시지를 연 방문자 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트(숫자) </td> 
   <td colname="col2"> 전송 </td> 
   <td colname="col3"> <p>emarsys에서 자동으로 가져오기 </p> </td> 
   <td colname="col4"> <p>전송 이벤트를 사용하면 전송된 이메일 메시지 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트(숫자) </td> 
   <td colname="col2"> 구독 취소 </td> 
   <td colname="col3"> <p>emarsys에서 자동으로 가져오기 </p> </td> 
   <td colname="col4"> <p>가입 취소 이벤트는 이메일을 열었지만 나중에 조직에서 이메일 메시지를 옵트아웃하기 위해 가입 해지 링크를 클릭한 방문자 수를 확인할 수 있도록 해줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Recipient ID </td> 
   <td colname="col3"> <p>자동화된 수집 방법 또는 JavaScript 플러그인을 통해 이메일 링크의 쿼리 매개 변수에서 수집됩니다. </p> </td> 
   <td colname="col4"> Recipient ID </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar or s.campaign </td> 
   <td colname="col2"> 메시지 ID </td> 
   <td colname="col3"> <p>자동화된 수집 방법 또는 JavaScript 플러그인을 통해 이메일 링크의 쿼리 매개 변수에서 수집됩니다. </p> </td> 
   <td colname="col4"> 이 값은 종종 캠페인 변수에 저장됩니다. </td> 
  </tr> 
 </tbody> 
</table>

