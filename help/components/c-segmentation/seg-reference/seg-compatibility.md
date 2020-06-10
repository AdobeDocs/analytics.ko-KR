---
description: 세그먼트 빌더에서 만든 모든 세그먼트가 Data Warehouse와 호환되는 것은 아닙니다. 이 표에는 지원되는 기능이 표시되어 있습니다.
title: Data Warehouse 세그먼트 기능
topic: Segments
uuid: 370258c5-8614-4434-871c-41753ed77f5c
translation-type: tm+mt
source-git-commit: a28a05047e95d12343fd94f7b11e5cabf7fac070
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 96%

---


# Data Warehouse 세그먼트 기능

세그먼트 빌더에서 만든 모든 세그먼트가 [!DNL Data Warehouse]와 호환되는 것은 아닙니다. 이 표에는 지원되는 기능이 표시되어 있습니다.

<table> 
 <thead> 
  <tr> 
   <th> </th> 
   <th> Analysis Workspace, Reports &amp; Analytics, Ad Hoc Analysis </th> 
   <th> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td > <b>컨테이너 제외</b> </td> 
   <td> 모든 수준에서 지원됨 </td> 
   <td> 최상위 수준의 특수 경우에만 지원됨 </td> 
  </tr> 
  <tr> 
   <td> <b>순차적 세그먼트</b> </td> 
   <td> 지원됨 </td> 
   <td> 지원되지 않음 </td> 
  </tr> 
  <tr> 
   <td> <b>AND 및 OR은 제한없이 조합할 수 있음</b> </td> 
   <td> 지원됨 </td> 
   <td> 일부 제한 적용. 표 아래의 *참고*를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td> <b>중첩 컨테이너</b> </td> 
   <td> 지원됨 </td> 
   <td> 일부 제한 적용(범위가 감소해야 함. 예를 들어 방문자는 히트를 포함할 수 있지만 그 반대는 가능하지 않음) </td> 
  </tr> 
  <tr> 
   <td> <b>차원</b> </td> 
   <td>세그먼트 빌더의 <span class="uicontrol">정의</span> 필드로 차원을 드래그하여 놓아 제품 호환성을 확인합니다. 예를 들어 이러한 차원은 Analysis Workspace, Reports &amp; Analytics과 Ad Hoc Analysis에서만 지원됩니다. 
    <ul> 
     <li>시작 서버 </li> 
     <li>시작 카테고리 </li> 
     <li>시작 날짜 </li> 
     <li>모든 검색 페이지 등급 </li> 
    </ul> </td> 
   <td> 세그먼트 빌더의 <span class="uicontrol">정의</span> 필드로 차원을 드래그하여 놓아 제품 호환성을 확인합니다. 예를 들어 다음 차원은 Data Warehouse에서만 지원됩니다. 
    <ul> 
     <li>IP 주소 </li> 
     <li>페이지 URL </li> 
     <li>방문자 ID </li> 
     <li>Experience Cloud 방문자 ID </li> 
    </ul> <p>Data Warehouse 세그먼트에서는 다음 차원을 <b>사용할 수 없습니다</b>. </p> 
    <ul> 
     <li>모든 검색 페이지 등급 </li> 
     <li>오전/오후 </li> 
     <li>날짜 </li> 
     <li>요일 </li> 
     <li>일 </li> 
     <li>비즈니스 단위 입력 </li> 
     <li>입력(입력으로 시작하는 모든 차원, 시작 페이지 제외) </li> 
     <li>종료(종료로 시작하는 모든 차원, 종료 링크 및 종료 페이지 제외) </li> 
     <li>계층(계층으로 시작하는 모든 차원) </li> 
     <li>히트 깊이 </li> 
     <li>히트 유형 </li> 
     <li>시간(일) </li> 
     <li>월 </li> 
     <li>페이지를 찾을 수 없음 </li> 
     <li>유료 검색 </li> 
     <li>사분기 </li> 
     <li>반환 주기 </li> 
     <li>단일 페이지 방문 횟수 </li> 
     <li>이벤트까지 남은 시간 </li> 
     <li>페이지 체류 시간 - 버킷 지정됨 </li> 
     <li>방문당 체류 시간 - 그룹화됨 </li> 
     <li>옵트아웃 이유 추적 중 </li> 
     <li>미국 주 </li> 
     <li>평일/주말 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <b>세그먼트 스택</b> </td> 
   <td> 지원됨 </td> 
   <td> 지원되지 않음 </td> 
  </tr>
  <tr>
    <td><b>'Equals any of' 및 'Does not equal any of' 연산자</b></td>
    <td>지원됨</td>
    <td>지원되지 않음</td>
  </tr>
 </tbody> 
</table>

*참고: Data Warehouse는`AND/OR`을 사용할 때`exclusion`또는`without`컨테이너를 사용하는 모든 경우를 지원하지는 않습니다. 이러한 조합을 사용하는 경우 Data Warehouse에서는`A AND NOT B`(또는&#x200B;**이 특성을 포함**하고&#x200B;**이 특성을 제외**)로 다시 쓸 수 있는 세그먼트만 지원합니다.*
