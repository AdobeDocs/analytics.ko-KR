---
description: 이 참조 테이블은 마케팅 채널 처리 규칙 페이지에서 선택할 수 있는 필드, 옵션 및 히트 속성을 정의합니다.
solution: Analytics
subtopic: Marketing channels
title: 마케팅 채널 처리 규칙 - 정의
topic: Reports and analytics
uuid: 4e71ff5b-912a-4dc0-9c22-4be74c5e3cc0
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 마케팅 채널 처리 규칙 - 정의

이 참조 테이블은 마케팅 채널 처리 규칙 페이지에서 선택할 수 있는 필드, 옵션 및 히트 속성을 정의합니다.

<table id="table_C18A0F1C9E214EB585A29801BA2400F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>용어 </p> </th> 
   <th colname="col2" class="entry"> <p>정의 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>모두 </p> </td> 
   <td colname="col2"> <p>번호가 매겨진 형식의 모든 규칙이 참인 경우에만 이 채널을 활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>임의 </p> </td> 
   <td colname="col2"> <p>규칙 세트의 일부 규칙이 참이면 이 채널을 활성화합니다. 이 옵션은 번호가 매겨진 규칙에 두 개 이상의 규칙이 있는 경우에만 사용할 수 있습니다. </p> </td> 
  </tr>
  <tr> 
   <td colname="col1"> <p>AMO ID </p> </td> 
   <td colname="col2"> <p>Advertising Cloud 및 Advertising Analytics 통합에서 사용하는 기본 추적 코드. 이러한 통합 중 하나가 활성화되면 추적 코드 접두사를 사용하여 Advertising Cloud 특정 채널을 식별할 수 있습니다. "AMO ID"는 검색의 경우 "AL", 표시의 경우 "AC", Social의 경우 "AO"로 시작합니다. AMO ID가 마케팅 채널에서 사용될 때 클릭/비용/노출 수 지표는 올바른 채널로 귀속될 수 있습니다(구성하지 않으면 이러한 지표는 직접 또는 없음으로 표시됨). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AMO ED ID </p> </td> 
   <td colname="col2"> <p>Advertising Cloud에서 사용하는 보조 추적 코드. 이 추적 코드의 주요 목적은 데이터를 다시 Ad Cloud로 전송하는 키 역할을 하는 것입니다. 또한 두 개의 별도 마케팅 채널로 보려는 경우 디스플레이 ClickThrough와 디스플레이 ViewThrough를 식별하는 데에도 사용할 수 있습니다. 이 작업은 "AMO EF ID"에 대한 마케팅 채널 논리가 디스플레이 클릭스루 횟수에 대해 ":d"로 종료되거나 "AMO EF ID"가 디스플레이 뷰스루의 경우 ":i"로 끝나게 되면 수행할 수 있습니다. 표시를 두 개의 채널로 분할하지 않으려면 AMO ID 차원을 대신 사용하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>전환 변수 </p> </td> 
   <td colname="col2"> <p>이 보고서 세트에 대해 활성화된 eVar들로 구성되며 이러한 변수가 페이지의 Adobe 코드를 통해 설정된 경우에만 적용됩니다. </p> <p><a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/oms_sc_implement.pdf"  > 구현 안내서</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>존재 </p> </td> 
   <td colname="col2"> <p>다음을 포함하여 여러 가지 선택 사항이 있습니다. </p> <p> 
     <ul id="ul_FE39B5F36235441FB757CC73CA2C4F51"> 
      <li id="li_6DC09918D69B443091AB94DB773D5189"> <p> <span class="uicontrol">존재하지 않음</span>: 히트 속성이 요청에 존재하지 않음을 나타냅니다. 예를 들어 추천 도메인에서 사용자가 URL을 입력하거나 책갈피를 클릭할 경우, 추천 도메인 속성이 존재하지 않습니다. </p> </li> 
      <li id="li_3AB958F997974682824E85014CA266D6"> <p> <span class="uicontrol"> 비어 있음</span>: eVar 또는 쿼리 문자열 매개 변수 같은 히트 속성이 존재하지만 히트 속성과 연관된 값은 없다는 것을 나타냅니다. </p> </li> 
      <li id="li_25EDA39748D141BA8173CC4C41035ABA"> <p> <span class="uicontrol"> 포함하지 않음 </span>:예를 들어, 참조 도메인에 특정 값이 포함되지 않도록 지정할 수 있습니다(포함 선택 항목 사용 대신). <span class="term"></span> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>다음으로 채널 식별 </p> </td> 
   <td colname="col2"> <p><span class="wintitle">마케팅 채널 관리자</span> 페이지에 추가한 마케팅 채널과 규칙을 연관시킵니다. </p> <p>See <a href="/help/components/c-marketing-channels/c-channels.md"   > Add marketing channels </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>유료 검색 발견 규칙 일치 </p> </td> 
   <td colname="col2"> <p>Adobe가 발견한 유료 검색. 유료 검색은 검색 엔진이 해당 기업 사이트를 나열하는 대가로 비용을 지불하는 검색 유형입니다. 유료 검색은 보통 검색 결과의 상단 또는 오른쪽에 나타납니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>자연어 검색 발견 규칙 일치 </p> </td> 
   <td colname="col2"> <p>Adobe 보고에 의해 발견된 무료 검색 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>레퍼러가 내부 URL 필터를 일치시킴 </p> </td> 
   <td colname="col2"> <p> 페이지 URL이 관리 도구의 보고서 세트에 대해 정의된 대로 내부 URL 필터와 일치하는 방문입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>레퍼러가 내부 URL 필터를 일치시키지 않음 </p> </td> 
   <td colname="col2"> <p>참조하는 URL이 관리 도구의 보고서 세트에 대해 정의된 대로 내부 URL 필터와 일치하지 않습니다. 이 설정을 <span class="term"> Page URL </span> and <span class="term"> Exists </span> to set up a catch-all rule, so that no visits land in the <a href="/help/components/c-marketing-channels/c-faq.md#no-channel-identified" > No Channel Identified </a> section of the report. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>내부 URL 필터와 일치하는 히트 무시 </p> </td> 
   <td colname="col2"> <p>(레퍼러의 경우) 외부에서 추천한 사이트에서 온 히트만 추적합니다. 일반적으로, 내부 트래픽을 포함하기를 원하지 않는 한 이 옵션을 계속 사용하도록 설정하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>방문의 첫 번째 페이지임 </p> </td> 
   <td colname="col2"> <p>Adobe 보고에 의해 발견된 첫 방문 페이지 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 </p> </td> 
   <td colname="col2"> <p>Adobe의 웹 비콘을 사용하여 태그되는 사이트의 웹 페이지의 페이지 이름. This value is equivalent to <span class="varname"> s.pageName </span>. 예로는 홈 <span class="varname"> 페이지 </span> 및 <span class="varname"> 정보 등이 </span>있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 도메인 </p> </td> 
   <td colname="col2"> <p>방문자가 들어오는 페이지의 도메인(예: <span class="filepath">products.example.co.uk</span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 도메인 및 경로 </p> </td> 
   <td colname="col2"> <p><span class="filepath">products.example.co.uk/mens/pants/overview.html</span>과 같은 도메인과 경로 . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 루트 도메인(TLD+1) </p> </td> 
   <td colname="col2"> <p>방문자가 들어오는 페이지의 루트 도메인(예: <span class="filepath">example.co.uk</span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 URL </p> </td> 
   <td colname="col2"> <p>사이트에서 웹 페이지의 URL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>조회 도메인 </p> </td> 
   <td colname="col2"> <p>방문자가 사용자 사이트를 방문하기 전에 있었던 도메인(예: <span class="filepath">abcsite.com</span> 대 <span class="filepath">xyzsite.com</span>에서 온 레퍼러). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>쿼리 문자열 매개 변수 </p> </td> 
   <td colname="col2"> <p>If a page URL on your site looks like <span class="filepath"> https://example.com/?page=12345&amp;cat=1 </span>, then page and cat are both query string parameters. (See <span class="filepath"> https://en.wikipedia.org/wiki/Query_string </span>.) </p> <p>규칙 세트당 하나의 쿼리 문자열 매개 변수만 지정할 수 있습니다. 쿼리 문자열 매개 변수를 추가하려면 연산자로 <span class="uicontrol">ANY</span>를 사용한 다음, 새 쿼리 문자열 매개 변수를 규칙에 추가하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>레퍼러 </p> </td> 
   <td colname="col2"> <p>방문자가 사이트에 오기 전에 있었던 웹 페이지 위치(전체 URL). 레퍼러는 정의된 도메인 외부에 존재합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>참조 도메인 및 경로 </p> </td> 
   <td colname="col2"> <p>참조 도메인과 URL 경로의 연결. 해당 예는 다음과 같습니다. </p> <p> <span class="filepath"> www.example.com/products/id/12345 </span> </p> <p> <span class="filepath"> ad.example.com/foo </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>참조 매개 변수 </p> </td> 
   <td colname="col2"> <p>레퍼러 URL의 쿼리 문자열 매개 변수. 예를 들어 방문자가 <span class="filepath">example.com/?page=12345&amp;cat=1</span>에서 온 경우 page 및 cat가 참조 매개 변수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>참조 루트 도메인 </p> </td> 
   <td colname="col2"> <p>레퍼러의 루트 도메인. 레퍼러는 정의된 도메인 외부에 존재합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>검색 엔진 </p> </td> 
   <td colname="col2"> <p>Google이나 Yahoo! 같이 방문자를 사용자 사이트로 연결시킨 검색 엔진. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>검색 키워드 </p> </td> 
   <td colname="col2"> <p>검색 엔진을 사용하여 검색을 수행하는 데 사용되는 단어 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>검색 엔진 + 키워드 </p> </td> 
   <td colname="col2"> <p>검색 엔진을 고유하게 식별하는 검색 키워드 및 검색 엔진의 연결. 예를 들어 computer라는 단어를 검색하는 경우, 검색 엔진과 키워드는 다음과 같이 식별됩니다. </p> 
    <code>
      Search&nbsp;Tracking&nbsp;Code&nbsp;= &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"&lt;search_type&gt;:&lt;search&nbsp;engine&gt;:&lt;search&nbsp;keyword&gt;"&nbsp;where &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;search_type&nbsp;=&nbsp;"n"&nbsp;or&nbsp;"p",&nbsp;search_engine&nbsp;=&nbsp;"Google",&nbsp;and&nbsp;search_keyword&nbsp;= &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"computer" 
    </code> <p><b></b> 참고:n = natural;p = 유료 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>채널의 값을 다음으로 설정 </p> </td> 
   <td colname="col2"> <p>방문자를 사이트로 유도하는 마케팅 채널을 파악할 수 있을 뿐만 아니라, 방문자의 사이트 활동에 대한 크레딧을 얻는 채널 내의 배너 광고, 검색 키워드 또는 이메일 캠페인을 파악할 수 있습니다. 이 ID는 채널과 함께 저장되는 채널 값입니다. 종종 이 값은 랜딩 페이지 또는 참조 URL에 삽입되는 캠페인 ID입니다. 또한 검색 엔진 및 검색 키워드 조합이거나 특정 채널에서 온 방문자를 가장 올바르게 식별하는 참조 URL일 수도 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
