---
description: emarsys용 Data Connectors 통합은 Analytics 변수를 사용하여 다양한 emarsys 지표를 추적합니다.
title: Analytics 변수
uuid: 4d5e087c-f495-4aab-9ad1-9b901d34a254
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Analytics 변수{#analytics-variables}

emarsys용 Data Connectors 통합은 Analytics 변수를 사용하여 다양한 emarsys 지표를 추적합니다.

emarsys 통합에 사용할 이벤트 및 eVar를 식별한 후 [Admin Console](https://docs.adobe.com/content/help/ko-KR/analytics/admin/admin-tools/c-admin-tools.html)에서 활성화합니다.

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
   <td colname="col1"> event (numeric) </td> 
   <td colname="col2"> 총 바운스 수 </td> 
   <td colname="col3"> <p>emarsys에서 자동으로 가져옵니다. </p> </td> 
   <td colname="col4"> <p>총 바운스 수 이벤트를 사용하면 배달 문제로 인해 수신자에게 배달되지 않은 이메일 메시지 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> event (numeric) </td> 
   <td colname="col2"> 클릭됨 </td> 
   <td colname="col3"> <p>emarsys에서 자동으로 가져옵니다. </p> </td> 
   <td colname="col4"> <p>클릭됨 이벤트를 사용하면 이메일 메시지를 클릭한 방문자 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> event (numeric) </td> 
   <td colname="col2"> 열림 </td> 
   <td colname="col3"> <p>emarsys에서 자동으로 가져옵니다. </p> </td> 
   <td colname="col4"> <p>열림 이벤트를 사용하면 이메일 메시지를 연 방문자 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> event (numeric) </td> 
   <td colname="col2"> 보냄 </td> 
   <td colname="col3"> <p>emarsys에서 자동으로 가져옵니다. </p> </td> 
   <td colname="col4"> <p>전송함 이벤트를 사용하여 전송된 이메일 메시지 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> event (numeric) </td> 
   <td colname="col2"> 가입 해지됨 </td> 
   <td colname="col3"> <p>emarsys에서 자동으로 가져옵니다. </p> </td> 
   <td colname="col4"> <p>가입 해지됨 이벤트를 사용하면 이메일 메시지를 열었지만 나중에 가입 해지 링크를 클릭하여 조직에서 발송하는 향후 이메일 메시지를 거부한 방문자 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> 수신자 ID </td> 
   <td colname="col3"> <p>자동화된 수집 방법 또는 JavaScript 플러그인을 통해 이메일 링크의 쿼리 매개 변수에서 수집됩니다. </p> </td> 
   <td colname="col4"> 수신자 ID </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar 또는 s.campaign </td> 
   <td colname="col2"> 메시지 ID </td> 
   <td colname="col3"> <p>자동화된 수집 방법 또는 JavaScript 플러그인을 통해 이메일 링크의 쿼리 매개 변수에서 수집됩니다. </p> </td> 
   <td colname="col4"> 이 값은 캠페인 변수에 저장되는 경우가 많습니다. </td> 
  </tr> 
 </tbody> 
</table>

