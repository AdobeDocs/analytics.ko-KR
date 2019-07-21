---
description: 세그먼트 빌더에서 만든 모든 세그먼트가 Data Warehouse와 호환되는 것은 아닙니다. 이 표에는 지원되는 기능이 표시되어 있습니다.
seo-description: 세그먼트 빌더에서 만든 모든 세그먼트가 Data Warehouse와 호환되는 것은 아닙니다. 이 표에는 지원되는 기능이 표시되어 있습니다.
seo-title: Data Warehouse 세그먼트 기능
solution: Analytics
title: Data Warehouse 세그먼트 기능
topic: 세그먼트
uuid: 370258 C 5-8614-4434-871 C -41753 ED 77 F 5 C
translation-type: tm+mt
source-git-commit: 26bba9528873c983852754056a5495c4004d25e6

---


# Data Warehouse 세그먼트 기능

Not all segments created in the Segment Builder are compatible with [!DNL Data Warehouse]. 이 표에는 지원되는 기능이 표시되어 있습니다.

<table id="table_BBB1DAFDF85041598FA4AF869172CF7F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis </th> 
   <th colname="col3" class="entry"> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>제외</b> </td> 
   <td colname="col2"> 모든 수준에서 지원됨 </td> 
   <td colname="col3"> 최상위 수준의 특수 경우에만 지원됨 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>순차적 세그먼트</b> </td> 
   <td colname="col2"> 지원됨 </td> 
   <td colname="col3"> 지원되지 않음 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>AND 및 OR은 제한없이 조합할 수 있음</b> </td> 
   <td colname="col2"> 지원됨 </td> 
   <td colname="col3"> 일부 제한 적용 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>중첩 컨테이너</b> </td> 
   <td colname="col2"> 지원됨 </td> 
   <td colname="col3"> 일부 제한 적용(범위가 감소해야 함. 예를 들어 방문자는 히트를 포함할 수 있지만 그 반대는 가능하지 않음) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>차원</b> </td> 
   <td colname="col2">세그먼트 빌더의 <span class="uicontrol">정의</span> 필드로 차원을 드래그하여 놓아 제품 호환성을 확인합니다. 예를 들어, 이러한 차원은 분석 작업 공간, 보고 및 분석, 애드혹 분석에서만 지원됩니다. 
    <ul id="ul_BD708CC3A16743F49F998D1046EC70A3"> 
     <li id="li_240DA619D50B4336ACD9117BF59AF10A">시작 서버 </li> 
     <li id="li_222D4D4116674EF8A52945CCB9C78719">시작 카테고리 </li> 
     <li id="li_5A43C846E2EA4EFCB892DE9E0607C68C">시작 날짜 </li> 
     <li id="li_8E9CABBE04FC4A7A9A5D2BDD34AD3C87">모든 검색 페이지 등급 </li> 
    </ul> </td> 
   <td colname="col3"> 세그먼트 빌더의 <span class="uicontrol">정의</span> 필드로 차원을 드래그하여 놓아 제품 호환성을 확인합니다. 예를 들어 다음 차원은 Data Warehouse에서만 지원됩니다. 
    <ul id="ul_61A5B314CCCF497DB0385324E3309E22"> 
     <li id="li_1254089BDFAE4E0F8E51CB1511BBBF53">IP 주소 </li> 
     <li id="li_D8E040F77A8C46A084547F4FE685CB10">페이지 URL </li> 
     <li id="li_4C79AE900CF6458780C124143DC6FA5B">방문자 ID </li> 
     <li id="li_4EC10645DE9740609D8DDFD4F668FE67">Experience Cloud 방문자 ID </li> 
    </ul> <p>The following dimensions <b>cannot </b>be used in Data Warehouse segments: </p> 
    <ul id="ul_FE143F6D1ABF45DAA444E1B5691C7D4F"> 
     <li id="li_E77F3CC45BA04674B857FE5AB19D56F1">모든 검색 페이지 등급 </li> 
     <li id="li_95E1549C13F14BA0B32686401EE78E31">오전/오후 </li> 
     <li id="li_6F1C8FC2E7674A0CA14B70B65784D896">날짜 </li> 
     <li id="li_79D1A91D741D4CCC937D07906D71F964">요일 </li> 
     <li id="li_4008565353084611BD782B98D50C0611">일 </li> 
     <li id="li_F87D78F125874087BFF74FAAE2BA46F5">비즈니스 단위 입력 </li> 
     <li id="li_53DA4E64C6714CFF90D164245D01C16A">입력(입력으로 시작하는 모든 차원, 시작 페이지 제외) </li> 
     <li id="li_7F26B0E54A4A48319F31D8FC499D1CF2">종료(종료로 시작하는 모든 차원, 종료 링크 및 종료 페이지 제외) </li> 
     <li id="li_1877D2D8A95B43F29CAA426BF2FE4996">계층(계층으로 시작하는 모든 차원) </li> 
     <li id="li_DF0BCC63ED274ABEA1C5A28274936310">히트 깊이 </li> 
     <li id="li_98BE56213E1A4FD28D4858D53C46D23E">조회 유형 </li> 
     <li id="li_52ECB31657DF4180BDB9C8D21CC74313">시간(일) </li> 
     <li id="li_93716207F2614822ACB84100B35D27BC">월 </li> 
     <li id="li_FFC8E1F7092C4876A7E9F2365CC234B9">페이지를 찾을 수 없음 </li> 
     <li id="li_7A070C8E0F664F5AB554555B17D0E4E6">유료 검색 </li> 
     <li id="li_12228C18BF90463C8D8394FB810843D3">사분기 </li> 
     <li id="li_1833B6E2011C4757A60CAA2C98B35AFA">재방문 주기 </li> 
     <li id="li_39154CD74A534D9AA09C701FE1E2C521">단일 페이지 방문 횟수 </li> 
     <li id="li_84BDE34DD577488881E8842D2DE72D3C">이벤트까지 남은 시간 </li> 
     <li id="li_552BE3414CC949B3B24BE99298945874">페이지 체류 시간 - 버킷 지정됨 </li> 
     <li id="li_33D815E04CB3493C82BE33E958C2D7B9">방문당 체류 시간 - 그룹화됨 </li> 
     <li id="li_76F2BB88B8CD456DB50D04F36BB7854B">옵트아웃 이유 추적 중 </li> 
     <li id="li_07345E08D0584CEC99128A0542587019">미국 주 </li> 
     <li id="li_3D6BD9E927334B9BBC29E602D1103F7A">평일/주말 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>세그먼트 스택</b> </td> 
   <td colname="col2"> 지원됨 </td> 
   <td colname="col3"> 지원되지 않음 </td> 
  </tr> 
 </tbody> 
</table>

