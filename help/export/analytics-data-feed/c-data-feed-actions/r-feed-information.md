---
description: '[피드 정보] 섹션을 사용하여 피드의 이름을 지정하고, 피드 실행에 사용할 보고서 세트를 지정하고, 피드 반복을 파악하고, 피드가 시작되고 끝나는 때를 지정합니다.'
keywords: 데이터 피드; 정보; name; 보고서 세트; 완료 시 이메일이메일; interval; 피드; 처리 지연; 지연; 시작; end; date; 연속 피드
seo-description: '[피드 정보] 섹션을 사용하여 피드의 이름을 지정하고, 피드 실행에 사용할 보고서 세트를 지정하고, 피드 반복을 파악하고, 피드가 시작되고 끝나는 때를 지정합니다.'
seo-title: 피드 정보
solution: Analytics
title: 피드 정보
uuid: adf 92 f 42-a 957-4 de 0-a 5 a 1-683 f 2933 af 04
translation-type: tm+mt
source-git-commit: 5a30ea6ac47ddd8612728e488afda868491a1ddc

---


# 피드 정보

[피드 정보] 섹션을 사용하여 피드의 이름을 지정하고, 피드 실행에 사용할 보고서 세트를 지정하고, 피드 반복을 파악하고, 피드가 시작되고 끝나는 때를 지정합니다.

![](assets/feed-info.jpg)

<table id="table_C98C7C3CE4194BEF819E792793EBC517">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 필드 </th>
   <th colname="col2" class="entry"> 설명 </th>
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>이름(필수) </p> </td>
   <td colname="col2"> <p>피드 이름을 입력합니다. </p> <p>이름은 선택된 보고서 세트 내에서 고유해야 하며 길이는 최대 255자일 수 있습니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>보고서 세트(필수) </p> </td>
   <td colname="col2"> <p>피드 쿼리에 대한 보고서 세트를 지정합니다. </p> <p>하나 이상의 보고서 세트를 선택해야 합니다. 동일한 보고서 세트를 두 번 나열할 수 없습니다. </p> <p>로그인한 사용자가 사용할 수 있는 모든 비가상 보고서 세트를 사용할 수 있습니다. </p></td>
  </tr>
  <tr>
   <td colname="col1"> <p>완료 시 전자 메일 보내기(필수) </p> </td>
   <td colname="col2"> <p>피드 배달 업데이트를 받을 이메일 수신자를 지정합니다. </p> <p>이 필드는 비워둘 수 없습니다. 형식이 올바로 지정된 이메일 주소를 포함해야 합니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>피드 간격(필수) </p> </td>
   <td colname="col2"> <p>예약 반복을 지정합니다. </p> <p>참고: 데이터 피드 zip 파일의 잠재적인 크기를 고려하여 ETL 프로세스에서 64비트 zip 유틸리티를 사용하는지 확인하십시오. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>프로세싱 지연(선택 사항) </p> </td>
   <td colname="col2"> <p>각 예약 인스턴스에 적용할 지연을 지정합니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>시작 및 종료 날짜(필수) </p> <p>지속 피드(선택 사항) </p> </td>
   <td colname="col2"> <p>피드가 시작되는 날짜와 종료되는 날짜를 예약합니다. </p> <p>
     <ul id="ul_509977336CD34032924B48E043E8CBC7">
      <li id="li_BFB5B6ADCB184D839C9BA42DB3DCAF32">시작 날짜: 오늘 날짜를 기본값으로 지정 </li>
      <li id="li_34F8DB45D9B54076840D1A0B782812D3">종료 날짜: 내일 날짜를 기본값으로 지정 </li>
     </ul>
     </p> </td>
  </tr>
 </tbody>
</table>