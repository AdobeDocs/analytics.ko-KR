---
description: 처리 규칙을 사용하여 읽고 쓸 수 있는(별다른 명시가 없는 경우) 차원입니다.
subtopic: Processing rules
title: 처리 규칙에 사용 가능한 차원
feature: Processing Rules
exl-id: ffd7a1d6-2c9d-41e7-9c75-9e47b6f9c283
source-git-commit: 35e7c8bccb8524fa5e87cae223f0854956c7528a
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 100%

---

# 처리 규칙에 사용 가능한 차원

처리 규칙을 사용하여 읽고 쓸 수 있는(별다른 명시가 없는 경우) 차원입니다.

## 사용자 정의 값 및 컨텍스트 데이터 {#section_7A5E1810CAC34B0BBC69F8F5F7C75AA5}

<table id="table_5011C501D5DC489E87A42FFC51DEB40D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 값 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>사용자 정의 값 </p> </td> 
   <td colname="col2"> <p>처리 규칙 동작 시 직접 입력된 사용자 정의 텍스트 또는 값. 이러한 값은 후속 조건 및 규칙에서 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>연결된 값 </p> </td> 
   <td colname="col2"> <p>두 값을 결합하여 작성된 값. 예를 들어 범주와 페이지 이름을 결합하여 하위 범주를 만들 수 있습니다. 이러한 값은 후속 조건 및 규칙에서 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>수정된 값 </p> </td> 
   <td colname="col2"> <p>처리 규칙을 사용하여 변수 값을 변경하면 후속 조건 및 규칙에서 변경된 값이 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>컨텍스트 데이터 변수 </p> </td> 
   <td colname="col2"> <p>히트와 함께 전송된 명명된 변수입니다. </p> <p>참고: 컨텍스트 데이터 변수에 포함된 모든 데이터는 보고 변수로 복사되어야 보고서에 표시됩니다. 컨텍스트 데이터 변수가 클릭스트림 데이터 피드 등의 모든 보고 인터페이스에서 볼 수 있는 것은 아닙니다. </p> <p> <a href="/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md"> eVar에 컨텍스트 데이터 변수 복사 </a> </p> <p> <a href="/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md"> 컨텍스트 데이터 변수를 사용하여 이벤트 설정 </a> </p> <p> <a href="/help/implement/vars/page-vars/contextdata.md"> 컨텍스트 데이터 변수</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 트래픽 변수 {#section_225156106F8B41F8BC1E68D58DDC2652}

<table id="table_575F618C59DC4933BC77F935518EAE39"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>prop 1-75 </p> </td> 
   <td colname="col2"> <p> <code> prop1 - prop75</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>계층 구조 1-5 </p> </td> 
   <td colname="col2"> <p> <code> hier1 - hier5</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사이트 섹션 </p> </td> 
   <td colname="col2"> <p> <code> s.channel </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>서버 </p> </td> 
   <td colname="col2"> <p> <code> s.server </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 히트 속성 {#section_07E69A86A47741A083FD84F112EB80D0}

<table id="table_9011B1FA462B4DBBAA58FC2D6D638DA1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 속성 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>보고서 세트 ID (읽기 전용) </p> </td> 
   <td colname="col2"> <p>처리 규칙이 실행되는 보고서 세트. 이것은 AppMeasurement에서 지정된 원본 보고서 세트가 아닐 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 이름 </p> </td> 
   <td colname="col2"> <p> <code> s.pageName</code> </p> <p>참고: 링크 추적 호출은 처리 규칙에 도달하기 전에 <code>pageName</code> 변수를 제거합니다. 처리 규칙을 사용하여 페이지 이름 값을 다시 삽입하는 경우 히트는 링크 추적 호출이 아닌 페이지 조회수로 간주됩니다. Adobe는 페이지 이름을 수정하기 전에 페이지 이름이 이미 설정되어 있는지 확인하는 것을 권장합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 URL </p> </td> 
   <td colname="col2"> <code> s.pageURL</code> 또는 <code> s.pageURL</code>이 지정되지 않은 경우 현재 페이지 URL <p>참고: 링크 추적 호출은 처리 규칙에 도달하기 전에 <code>pageURL</code> 변수를 제거합니다. 처리 규칙을 사용하여 페이지 URL 값을 다시 삽입하는 경우 히트는 링크 추적 호출이 아닌 페이지 조회수로 간주됩니다. Adobe는 페이지 URL을 수정하기 전에 페이지 URL이 이미 설정되어 있는지 확인할 것을 권장합니다 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>쿼리 문자열 매개변수 </p> </td> 
   <td colname="col2"> <p>현재 URL에 지정된 쿼리 문자열 매개변수의 값이거나 매개변수가 없을 경우에는 null입니다. URL <b>https://www.example.com/a.html?cid=ad1&amp;node=4</b>의 경우 쿼리 문자열 매개변수 <span class="syntax codeph"> cid</span>의 값은 <b>ad1</b>이고, 쿼리 문자열 매개변수 <span class="syntax codeph"> node</span>값은 <b>4</b>입니다. </p> <p>JavaScript AppMeasurement H.25.2 이전 버전을 실행하는 경우 페이지 URL이 255자 이후에 잘릴 수 있습니다. JavaScript AppMeasurement H.25.3(2013년 1월 릴리스) 이후 버전은 처리 규칙에 전체 URL을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 경로 </p> </td> 
   <td colname="col2"> <p>페이지 URL의 경로. URL <b>https://www.example.com/news/a.html?cid=ad1</b>의 경로는 <span class="syntax codeph"> news/a.html</span>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 도메인 </p> </td> 
   <td colname="col2"> <p>URL에 지정된 전체 호스트 이름. https://<span class="syntax codeph"> en.main.example.co.uk</span>/index.jsp?q=value </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 루트 도메인 </p> </td> 
   <td colname="col2"> <p>페이지 호스트 이름의 마지막 두 섹션입니다. https://en.main.example.<span class="syntax codeph"> co.uk</span>/index.jsp?q=value </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 쿼리 문자열 </p> </td> 
   <td colname="col2"> <p>URL의 전체 쿼리 문자열. https://en.main.example.co.uk/index.jsp?<span class="syntax codeph"> q=value</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>참조*(읽기 전용) </p> </td> 
   <td colname="col2"> <p>HTTP 참조 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>참조 쿼리 문자열 매개변수(읽기 전용) </p> </td> 
   <td colname="col2"> <p>참조 URL에 지정된 쿼리 문자열 매개변수의 값이거나 매개변수가 없을 경우에는 null입니다. URL <b>https://www.example.com/a.html?cid=ad1&amp;node=4</b>의 경우 쿼리 문자열 매개변수 <span class="syntax codeph"> cid</span>의 값은 <b>ad1</b>이고, 쿼리 문자열 매개변수 <span class="syntax codeph"> node</span>값은 <b>4</b>입니다. </p> <p>JavaScript AppMeasurement H.25.2 이전 버전을 실행하는 경우 페이지 URL이 255자 이후에 잘릴 수 있습니다. JavaScript AppMeasurement H.25.3(2013년 1월 릴리스) 이후 버전은 처리 규칙에 전체 URL을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>참조 도메인(읽기 전용) </p> </td> 
   <td colname="col2"> <p>레퍼러의 전체 호스트 이름입니다. https://<span class="syntax codeph"> en.main.example.co.uk</span>/index.jsp?q=value </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>참조 루트 도메인(읽기 전용) </p> </td> 
   <td colname="col2"> <p>레퍼러 호스트 이름의 마지막 두 섹션입니다. https://en.main.example.<span class="syntax codeph"> co.uk</span>/index.jsp?q=value </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>참조 쿼리 문자열(읽기 전용) </p> </td> 
   <td colname="col2"> <p>참조 URL에 포함된 쿼리 문자열 매개변수입니다. https://en.main.example.co.uk/index.jsp?<span class="syntax codeph"> q=value</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>IP 주소(읽기 전용) </p> </td> 
   <td colname="col2"> <p>브라우저에서 보고한 IP 주소입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 에이전트(읽기 전용) </p> </td> 
   <td colname="col2"> <p>브라우저에서 보고한 사용자 에이전트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AppMeasurement 코드 버전(읽기 전용) </p> </td> 
   <td colname="col2"> <p>요청을 작성하기 위해 사용된 appMeasurement 라이브러리의 버전. 이미지 비콘을 사용할 때 이것을 처리 규칙을 사용하여 읽힌 사용자 정의 값으로 채울 수 있습니다. 이 값은 URL의 다음 위치에 나타납니다. </p> <p>https://server.net/b/ss/report-suite-ID/1/<span class="syntax codeph"> CODEVERSION</span>/... </p> </td> 
  </tr> 
 </tbody> 
</table>

## 전환 변수 {#section_311856B21B3B49DBAA0539CFA06C409F}

<table id="table_E28729026EDA485989178A3B887B5983"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>eVar 1-N </p> </td> 
   <td colname="col2"> <p> <code> evar1</code> - <code> evarN</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>캠페인 추적 코드 </p> </td> 
   <td colname="col2"> <p> <code> s.campaign</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>통화 코드 </p> </td> 
   <td colname="col2"> <p> <code> s.currencyCode</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>목록 변수 1-3 </p> </td> 
   <td colname="col2"> <p> <code> s.list1</code> - <code> s.list3</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>구매 ID </p> </td> 
   <td colname="col2"> <p> <code> s.purchaseID</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>거래 ID </p> </td> 
   <td colname="col2"> <p> <code> s.transactionID </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>방문자 주 </p> </td> 
   <td colname="col2"> <p> <code> s.state</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>방문자 Zip/우편번호 </p> </td> 
   <td colname="col2"> <p> <code> s.zip</code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 성공 이벤트 {#section_C1946FEB64FC4F579671EC5E0D06AE8A}

처리 규칙은 이벤트를 설정할 수 있지만 이벤트를 조건으로 읽을 수 없습니다.

<table id="table_926ED12B58CA4FB685D799DC6EE567C0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이벤트 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Event 1-1000 </p> <p>(SiteCatalyst 15 고객이면 이벤트 1-100) </p> </td> 
   <td colname="col2"> <p> <code> event1</code> - <code> event1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>구매, scView, scAdd 및 기타 장바구니 이벤트 </p> </td> 
   <td colname="col2"> <p>사전 정의된 이벤트입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
