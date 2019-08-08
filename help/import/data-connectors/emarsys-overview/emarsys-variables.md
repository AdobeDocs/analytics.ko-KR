---
description: Emarsys 용 데이터 커넥터 통합은 Analytics 변수를 사용하여 다양한 emarsys 지표를 추적합니다.
seo-description: Emarsys 용 데이터 커넥터 통합은 Analytics 변수를 사용하여 다양한 emarsys 지표를 추적합니다.
seo-title: Analytics 변수
title: Analytics 변수
uuid: 4 D 5 E 087 C-F 495-4 AAB -9 AD 1-9 B 901 D 34 A 254
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Analytics 변수{#analytics-variables}

Emarsys 용 데이터 커넥터 통합은 Analytics 변수를 사용하여 다양한 emarsys 지표를 추적합니다.

Emarsys 통합과 함께 사용할 이벤트와 evar를 파악한 후 [관리 콘솔에서 활성화합니다](https://microsite.omniture.com/t2/help/en_US/reference/index.html?f=conversion_var_admin).

**필수 변수**

<table id="table_5B8F3A1EB55D4BB48F669FB84C857256"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 변수 유형 </th> 
   <th colname="col2" class="entry"> 이름 </th> 
   <th colname="col3" class="entry"> 채우기 방법 </th> 
   <th colname="col4" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이벤트 (숫자) </td> 
   <td colname="col2"> 총 바운스 수 </td> 
   <td colname="col3"> <p>Emarsys에서 자동으로 가져오기 </p> </td> 
   <td colname="col4"> <p>총 바운스 이벤트를 사용하면 배달 문제로 인해 수신자에게 배달되지 않은 이메일 메시지 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 (숫자) </td> 
   <td colname="col2"> 클릭함 </td> 
   <td colname="col3"> <p>Emarsys에서 자동으로 가져오기 </p> </td> 
   <td colname="col4"> <p>클릭한 이벤트를 통해 이메일 메시지를 클릭한 방문자 수를 확인할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 (숫자) </td> 
   <td colname="col2"> 열림 </td> 
   <td colname="col3"> <p>Emarsys에서 자동으로 가져오기 </p> </td> 
   <td colname="col4"> <p>열린 이벤트를 통해 이메일 메시지를 연 방문자 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 (숫자) </td> 
   <td colname="col2"> sent </td> 
   <td colname="col3"> <p>Emarsys에서 자동으로 가져오기 </p> </td> 
   <td colname="col4"> <p>보내기 이벤트를 사용하면 전송된 이메일 메시지 수를 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 (숫자) </td> 
   <td colname="col2"> 가입 해지 </td> 
   <td colname="col3"> <p>Emarsys에서 자동으로 가져오기 </p> </td> 
   <td colname="col4"> <p>가입 취소된 이벤트를 사용하면 이메일을 연 다음 가입 해지 링크를 클릭하여 조직에서 향후의 이메일 메시지를 옵트아웃할 수 있는 방문자 수를 확인할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Recipient ID </td> 
   <td colname="col3"> <p>자동 수집 방법 또는 JavaScript 플러그인을 통해 이메일 링크의 쿼리 매개 변수에서 수집되었습니다. </p> </td> 
   <td colname="col4"> Recipient ID </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar 또는 s. campaign </td> 
   <td colname="col2"> 메시지 ID </td> 
   <td colname="col3"> <p>자동 수집 방법 또는 JavaScript 플러그인을 통해 이메일 링크의 쿼리 매개 변수에서 수집되었습니다. </p> </td> 
   <td colname="col4"> 이 값은 종종 캠페인 변수에 저장됩니다. </td> 
  </tr> 
 </tbody> 
</table>

