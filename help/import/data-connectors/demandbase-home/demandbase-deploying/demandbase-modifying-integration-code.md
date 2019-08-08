---
description: 대부분의 경우, 데이터 커넥터 마법사에서 생성된 통합 코드를 수정하지 않아도 됩니다.
seo-description: 대부분의 경우, 데이터 커넥터 마법사에서 생성된 통합 코드를 수정하지 않아도 됩니다.
seo-title: 통합 코드 수정
title: 통합 코드 수정
uuid: 3 F 49 A 29 B-AD 38-4967-894 A-EF 7 ECF 4 D 268 F
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# 통합 코드 수정{#modifying-the-integration-code}

대부분의 경우, 데이터 커넥터 마법사에서 생성된 통합 코드를 수정하지 않아도 됩니다.

그러나 조정해야 하는 경우 일부 코드 설정이 아래에 설명되어 있습니다.

<table id="table_5405A73CEFD44466B3C39559F4A037C9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 코드 설정 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> s.maxDelay </td> 
   <td colname="col2">Adobe Analytics 이미지 요청이 Analytics 수집 서버로 시작하기 전에 Demandbase 데이터가 대기할 최대 밀리초 수입니다. <p>참고: 이 설정은 통합 모듈을 통해 실행될 수 있는 모든 통합에 적용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._key </td> 
   <td colname="col2"> Demandbase API Key. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ apiurl </td> 
   <td colname="col2"> Demandbase API 용 URL 템플릿입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._delim </td> 
   <td colname="col2"> Demandbase 차원 값을 Adobe Analytics로 보낼 때 사용하는 구분 기호입니다. 이 설정을 변경하면 기본 분류 규칙이 제대로 작동하지 않을 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ settnt </td> 
   <td colname="col2">true 인 경우 통합 코드는 숨겨진 mbox를 사용하여 Demandbase 차원을 프로필 매개 변수로 Adobe Target에 보내려고 시도합니다. <p>참고: 이렇게 하려면 mbox. js 코드가 페이지에 있어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ tntvarprefix </td> 
   <td colname="col2"> 이 문자열은 Adobe Target로 보내기 전에 각 Demandbase 차원 이름에 추가됩니다. 예를 들어, 이 설정에 «db_» 값이 있으면 «industry» 차원이 Adobe Target로 «db_ industry» 로 전송됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ dimensionsarray </td> 
   <td colname="col2"> Adobe Analytics로 전송되는 표준 demandbase 차원입니다. 이 설정을 수정하지 않는 것이 좋습니다. «max_ size» 속성은 잘림이 발생하기 전에 차원에 허용되는 문자 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ Dimensionsarraycustom </td> 
   <td colname="col2"> Adobe Analytics로 전송되는 사용자 지정 Demandbase 차원입니다. «max_ size» 속성은 잘림이 발생하기 전에 차원에 허용되는 문자 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ cname </td> 
   <td colname="col2"> Demandbase API 커뮤니케이션의 상태를 유지하는 데 사용되는 세션 쿠키의 이름. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ contextname </td> 
   <td colname="col2"> 표준 차원을 Adobe Analytics로 전송하는 데 사용되는 contextdata 변수의 이름. 이 설정을 수정하지 않는 것이 좋습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _ db._ Contextnamecustom </td> 
   <td colname="col2"> Adobe Analytics로 사용자 지정 차원을 전송하는 데 사용되는 contextdata 변수의 이름입니다. 이 설정을 수정하지 않는 것이 좋습니다. </td> 
  </tr> 
 </tbody> 
</table>

