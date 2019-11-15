---
description: 다음 표는 데이터 수집으로 전송되는 각 분석 변수에 대한 값을 포함하는 쿼리 매개 변수를 나열합니다.
keywords: Analytics Implementation
solution: Analytics
title: 데이터 수집 쿼리 매개 변수
topic: Developer and implementation
uuid: 4d5af486-df27-42fe-bb9c-28938dddf2b2
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 데이터 수집 쿼리 매개 변수

다음 표는 데이터 수집으로 전송되는 각 분석 변수에 대한 값을 포함하는 쿼리 매개 변수를 나열합니다.

이 정보는  [패킷 분석기](/help/implement/impl-testing/packet-monitor.md)를 사용할 때, 수동으로 이미지 요청을 구성할 때 또는 [동적 변수](/help/implement/js-implementation/c-variables/dynvars-overview.md)를 사용할 때 참조할 수 있습니다.

<table id="table_5442E15BF0AE4BDA92DDADD1C08F7C13"> 
 <thead> 
  <tr> 
   <th class="entry"> 매개 변수 </th> 
   <th class="entry"> Analytics 변수 </th> 
   <th class="entry"> 채워진 보고서 </th> 
   <th class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> aamlh </td> 
   <td colname="col2"> 없음 </td> 
   <td colname="col3"> 없음 </td> 
   <td colname="col4"> Audience Manager 위치 힌트(Experience Cloud 공유 프로필 통합에 사용됨) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> aamb </td> 
   <td colname="col2"> 없음 </td> 
   <td colname="col3"> 없음 </td> 
   <td colname="col4"> Audience Manager Blob(Experience Cloud 공유 프로필 통합에 사용됨) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> aid </td> 
   <td colname="col2"> 없음 </td> 
   <td colname="col3"> 없음 </td> 
   <td colname="col4"> Analytics 방문자 ID </td> 
  </tr> 
  <tr> 
   <td> AQB </td> 
   <td> 없음 </td> 
   <td> 없음 </td> 
   <td> 이미지 요청 시작을 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td> AQE </td> 
   <td> 없음 </td> 
   <td> 없음 </td> 
   <td> 이미지 요청의 끝, 즉 요청이 잘리지 않았음을 나타냅니다.  </td> 
  </tr> 
  <tr> 
   <td> bh </td> 
   <td> 없음 </td> 
   <td> 방문자 프로필 | 기술 | 브라우저 높이 </td> 
   <td> 브라우저 창 높이(픽셀 단위) </td> 
  </tr> 
  <tr> 
   <td> bw </td> 
   <td> 없음 </td> 
   <td> 방문자 프로필 | 기술 | 브라우저 너비 </td> 
   <td> 브라우저 창 너비(픽셀 단위) </td> 
  </tr> 
  <tr> 
   <td> c </td> 
   <td> 없음 </td> 
   <td> 방문자 프로필 | 기술 | 모니터 색상 깊이 </td> 
   <td> 색상 품질(비트) </td> 
  </tr> 
  <tr> 
   <td> </td><td><p></p></td><td><p></p></td><td><p></p><p><code> &lt;my.a&gt;red&lt;/my.a&gt; </code></p><p></p><p><code> &lt;my&gt;&lt;a&gt;red&lt;/a&gt;&lt;/my&gt; </code></p><p><code> my.a = red </code></p><p><code> c.&my.a=red </code></p></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td><code> D </code></td><td></td><td></td><td><p></p></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td><p><code> t </code></p><code>
      dd/mm/yyyy&amp;nbsp;hh:mm:ss&amp;nbsp;D&amp;nbsp;OFFSET 
    </code><p><code> 0-6 </code><code> OFFSET </code></p><code>
      offset&amp;nbsp;from&amp;nbsp;GMT&amp;nbsp;in&amp;nbsp;hours&amp;nbsp;*&amp;nbsp;60&amp;nbsp;*&amp;nbsp;-&amp;nbsp;1 
    </code><p></p><code>
      23/09/2016&amp;nbsp;14:00:00&amp;nbsp;1&amp;nbsp;420 
    </code></td></tr><tr><td><code> ts </code></td><td><p></p></td><td></td><td><p></p></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td><p></p></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td><p></p></td></tr></tbody></table>

