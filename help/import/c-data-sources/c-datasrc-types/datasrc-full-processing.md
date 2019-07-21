---
description: 데이터 소스는 표준 서버 호출로서 데이터를 처리할 때 다음 변수를 지원합니다(범용 > 전체 처리).
seo-description: 데이터 소스는 표준 서버 호출로서 데이터를 처리할 때 다음 변수를 지원합니다(범용 > 전체 처리).
seo-title: 전체 처리
solution: Analytics
subtopic: Data Sources
title: 전체 처리
topic: 개발자 및 구현
uuid: 590 AE 89 C -6 E 17-453 B-B 701-CE 1 ADBEA 6 FA 4
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# 전체 처리

데이터 소스는 표준 서버 호출로서 데이터를 처리할 때 다음 변수를 지원합니다(범용 &gt; 전체 처리).

전체 처리 데이터 소셜 데이터는 지정된 시간에 Adobe 서버에서 수신한 것처럼 처리됩니다(각 히트에서 타임스탬프 수신).

* [방문자 프로필](../../../import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#section_6065627D0C144506965F562C80AE67F8)
* [항목 참조](../../../import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#section_92BAE76639E3404E97276B1BE0581078)

## 방문자 프로필 {#section_6065627D0C144506965F562C80AE67F8}

전체 처리 데이터 소스 데이터는 분리된 방문자 프로필을 사용하여 처리되므로, 업로드한 데이터의 방문자 ID가 JavaScript나 다른 AppMeasurement 라이브러리를 사용하여 수집한 데이터와 일치하더라도 방문자 프로필들은 eVar 할당 측면에서 연결되어 있지 않습니다.

예약, 방문자 ID가 "user@example.com"인 방문자는 캠페인 변수에 저장된 "봄맞이 세일"이라는 마케팅 캠페인에서 사이트를 방문하고, 나중에 여러분이 동일한 방문자 ID를 사용하여 거래를 업로드하는 경우, "봄맞이 세일" 캠페인은 전체 처리 데이터 소스를 사용하여 업로드한 어떤 매출이나 성공 이벤트에 대해서도 크레딧을 받지 않습니다.

## 항목 참조 {#section_92BAE76639E3404E97276B1BE0581078}

<table id="table_AAC04491D643467B9C80FDEF88130B13"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> JavaScript 변수 </th> 
   <th colname="col2" class="entry"> 전체 처리 열 변수 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>campaign </p> </td> 
   <td colname="col2"> <p>campaign </p> </td> 
   <td colname="col3"> <p>전환 캠페인 추적 코드. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>channel </p> </td> 
   <td colname="col2"> <p>channel </p> </td> 
   <td colname="col3"> <p>채널 문자열(예: 스포츠 섹션). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>currencyCode </p> </td> 
   <td colname="col2"> <p>currencyCode </p> <p>Note:  This variable is also supported by Standard data sources as <code> currency code </code>. </p> </td> 
   <td colname="col3"> <p>매출 통화 코드(예: USD). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>timestamp </p> </td> 
   <td colname="col2"> <p>날짜 </p> </td> 
   <td colname="col3"> <p>ISO 8601 날짜 형식 <code>YYYY-MM-DDThh:mm:ss±UTC_offset</code>(예: <code>2013-09-01T12:00:00-07:00</code>) 또는 Unix 시간 형식(1970년 1월 1일 이후 경과한 초를 나타내는 숫자)을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eVar<i>N</i> </p> </td> 
   <td colname="col2"> <p>eVar<i>N</i>, 즉 &lt;eVar2&gt;…&lt;/eVar2&gt; </p> </td> 
   <td colname="col3"> <p>전환 eVar 이름. 최대 75개의 eVar를 가질 수 있습니다( <span class="varname"> Evar 1 </span> - <span class="varname"> evar 75 </span>). </p> <p>eVar 이름(eVar12) 또는 친숙한 이름(광고 캠페인 3)을 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>events </p> </td> 
   <td colname="col2"> <p>events </p> </td> 
   <td colname="col3"> <p><a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/events.html" format="https" scope="external">s.events</a> 변수와 동일한 구문을 사용하여 형식이 지정된 이벤트 문자열. </p> <p>예: </p> 
    <code>scadd, event 1, event 7 </code>
  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>hier<i>N</i> </p> </td> 
   <td colname="col2"> <p>hier<i>N</i>, 즉 &lt;hier2&gt;…&lt;/hier2&gt; </p> </td> 
   <td colname="col3"> <p>계층 이름. 최대 5개의 계층을 가질 수 있습니다( <span class="varname"> hier1</span> - <span class="varname">hier5 </span>). </p> <p>기본 계층 이름(<span class="varname">hier2</span>) 또는 친숙한 이름(<span class="term">Yankees</span>)을 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>linkName </p> </td> 
   <td colname="col2"> <p>linkName </p> </td> 
   <td colname="col3"> <p>링크 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>linkType </p> </td> 
   <td colname="col2"> <p>linkType </p> </td> 
   <td colname="col3"> <p>링크 유형. 지원되는 값은 다음과 같습니다. </p> 
    <ul id="ul_E441013055A9447AB6C3FB05B6099F7D"> 
     <li id="li_A33F66F30B60479284F72AE3AD4BF499"> <b>d</b>: 다운로드 링크 </li> 
     <li id="li_182F695AA2D044DAB036BAFE38BC3915"> <b>e</b>: 종료 링크 </li> 
     <li id="li_4FD4D542D1774607860BEF41C1B090D1"> <b>o</b>: 사용자 정의 링크. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>linkURL </p> </td> 
   <td colname="col2"> <p>linkURL </p> </td> 
   <td colname="col3"> <p>링크의 HREF. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pageName </p> </td> 
   <td colname="col2"> <p>pageName </p> </td> 
   <td colname="col3"> <p>페이지 이름 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pageType </p> </td> 
   <td colname="col2"> <p>pageType </p> </td> 
   <td colname="col3"> <p>페이지 유형("오류 페이지"). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pageURL </p> </td> 
   <td colname="col2"> <p>pageURL </p> </td> 
   <td colname="col3"> <p>Page URL (for example, <code>https://www.mysite.com/index.html)</code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>products </p> </td> 
   <td colname="col2"> <p>products </p> </td> 
   <td colname="col3"> <p>제품 목록(예: <code>"Sports;Ball;1;5.95") </code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>prop1 - prop75 </p> </td> 
   <td colname="col2"> <p>prop<i>N</i>, 즉 &lt;prop2&gt;…&lt;/prop2&gt; </p> </td> 
   <td colname="col3"> <p>속성 번호 문자열(예: <span class="term"> 스포츠 섹션 </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>purchaseID </p> </td> 
   <td colname="col2"> <p>purchaseID </p> </td> 
   <td colname="col3"> <p>구매 ID 번호. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>s_account </p> </td> 
   <td colname="col2"> <p>reportSuiteID </p> </td> 
   <td colname="col3"> <p>히트를 할당할 보고서 세트 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server </p> </td> 
   <td colname="col2"> <p>server </p> </td> 
   <td colname="col3"> <p>서버 문자열. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>state </p> </td> 
   <td colname="col2"> <p>state </p> </td> 
   <td colname="col3"> <p>전환 상태 문자열. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>zip </p> </td> 
   <td colname="col2"> <p>zip </p> </td> 
   <td colname="col3"> <p>전환 우편번호. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 표는 JavaScript 라이브러리 사용 시 자동으로 채워지는 트래픽 변수를 포함합니다. 이러한 속성은 연결된 변수가 없지만 데이터 소스를 통해 가져올 수 있습니다.

<table id="table_FDBC5BD225644AA09078C0570BE709FE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>전체 처리 열 변수 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>browserHeight </p> </td> 
   <td colname="col2"> <p>브라우저 높이, 픽셀 단위(예: 768). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>browserWidth </p> </td> 
   <td colname="col2"> <p>브라우저 너비, 픽셀 단위(예: 1024). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>charSet </p> </td> 
   <td colname="col2"> <p>웹 사이트에 지원되는 문자 집합. 예를 들어 UTF-8, ISO-8859-1 등입니다.  </p> <p>전체 목록은 <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/multibyte/index.html" format="https" scope="external">멀티바이트 문자 집합</a>(국제) 백서를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickAction </p> </td> 
   <td colname="col2"> <p>방문자 클릭 맵에 대한 개체 식별자(oid) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickActionType </p> </td> 
   <td colname="col2"> <p>방문자 클릭 맵에 대한 개체 식별자 유형(oidt) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickContext </p> </td> 
   <td colname="col2"> <p>방문자 클릭 맵에 대한 페이지 식별자(pid) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickContextType </p> </td> 
   <td colname="col2"> <p>방문자 클릭 맵에 대한 페이지 식별자 유형(pidt) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickSourceID </p> </td> 
   <td colname="col2"> <p>방문자 클릭 맵에 대한 소스 색인(oi) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickTag </p> </td> 
   <td colname="col2"> <p>방문자 클릭 맵에 대한 개체 태그 이름(ot) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>colorDepth </p> </td> 
   <td colname="col2"> <p>모니터 색상 깊이, 비트 단위(예: 24). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>connectionType </p> </td> 
   <td colname="col2"> <p>방문자의 연결 유형( <span class="term"> LAN </span> 또는 <span class="term"> modem </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cookiesEnabled </p> </td> 
   <td colname="col2"> <p>방문자가 퍼스트 파티 세션 쿠키를 지원 여부에 따라 Y 또는 N. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>currencyCode </p> </td> 
   <td colname="col2"> <p>웹 사이트에서 사용되는 기본 통화 코드.  </p> <p>예를 들어 USD=미국 달러, EUR = 유로, JPY = 일본 엔화 등입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>homePage </p> </td> 
   <td colname="col2"> <p>Y 또는 N -- 현재 페이지가 방문자의 홈 페이지인지 여부. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>javaEnabled </p> </td> 
   <td colname="col2"> <p>Y 또는 N -- 방문자의 Java 활성화 여부. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>javaScriptVersion </p> </td> 
   <td colname="col2"> <p>JavaScript 버전(예: 1.3). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>plugins </p> </td> 
   <td colname="col2"> <p>세미콜론으로 구분된 브라우저 플러그인 이름 목록. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>propN </p> </td> 
   <td colname="col2"> <p>속성에 대한 속성 값. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>referrer </p> </td> 
   <td colname="col2"> <p>페이지 레퍼러의 URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>resolution </p> </td> 
   <td colname="col2"> <p>모니터 해상도(예: 1024x768). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>scXmlVer </p> </td> 
   <td colname="col2"> <p>마케팅 보고서 XML 요청 버전 번호(예: 1.0). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>timezone </p> </td> 
   <td colname="col2"> <p>방문자의 시간대와 GMT의 시차, 시간 단위(예: -8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>visitorID </p> </td> 
   <td colname="col2"> <p>방문자 ID 번호. </p> </td> 
  </tr> 
 </tbody> 
</table>

