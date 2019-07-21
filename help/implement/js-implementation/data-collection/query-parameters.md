---
description: 다음 표는 데이터 수집으로 전송되는 각 분석 변수에 대한 값을 포함하는 쿼리 매개 변수를 나열합니다.
keywords: Analytics 구현
seo-description: 다음 표는 데이터 수집으로 전송되는 각 분석 변수에 대한 값을 포함하는 쿼리 매개 변수를 나열합니다.
seo-title: 데이터 수집 쿼리 매개 변수
solution: Analytics
title: 데이터 수집 쿼리 매개 변수
topic: 개발자 및 구현
uuid: 4 D 5 AF 486-DF 27-42 FE-BB 9 C -28938 DDDF 2 B 2
translation-type: tm+mt
source-git-commit: 5a30ea6ac47ddd8612728e488afda868491a1ddc

---


# 데이터 수집 쿼리 매개 변수

다음 표는 데이터 수집으로 전송되는 각 분석 변수에 대한 값을 포함하는 쿼리 매개 변수를 나열합니다.

이 정보는 [패킷 분석기를](../../../implement/impl-testing/packet-monitor.md#concept_490DF35E06D44234A91B5FC57C0BF258)[사용할 수 있습니다](../../../implement/js-implementation/c-variables/dynvars-overview.md#concept_B016789733A94070A9EAB209EEC05262).

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
   <td> <code> c. <span class="varname"> [key] </code></span> </td> 
   <td> <p>s.contextData </p> </td> 
   <td> <p>없음 </p> </td> 
   <td> <p>키-값 쌍은 다음 형식 중 하나로 지정됩니다. </p> <p> <code> &lt;my.a&gt;red&lt;/my.a&gt; </code> </p> <p>또는: </p> <p> <code> &lt;my&gt;&lt;a&gt;red&lt;/a&gt;&lt;/my&gt; </code> </p> <p>이러한 각 예제는 <code>my.a = red</code>의 컨텍스트 데이터 값이 됩니다 . 여러 개의 키-값 쌍을 지정할 수 있습니다. </p> <p>In the query string, this context data variable would appear as <code> c.&amp;my.a=red </code> </p> </td> 
  </tr> 
  <tr> 
   <td> c1 - c75 </td> 
   <td> s.prop1 - s.prop75 </td> 
   <td> 모든 사용자 지정 트래픽 보고서 </td> 
   <td> 사용자 지정 트래픽 보고에서 사용되는 트래픽 변수  </td> 
  </tr> 
  <tr> 
   <td> cc </td> 
   <td> s.currencyCode </td> 
   <td> 없음 </td> 
   <td> 사이트에서 사용되는 통화 유형 </td> 
  </tr> 
  <tr> 
   <td> cdp </td> 
   <td> s.cookieDomainPeriods </td> 
   <td> 없음 </td> 
   <td> 쿠키 추적을 위해 수동으로 설정된 도메인 내 기간 수 </td> 
  </tr> 
  <tr> 
   <td> ce </td> 
   <td> s.charSet </td> 
   <td> 없음 </td> 
   <td> 이미지 요청의 문자 인코딩 </td> 
  </tr> 
  <tr> 
   <td> cl </td> 
   <td> s.cookieLifetime(s_vi 쿠키 라이프타임은 초 단위) </td> 
   <td> 없음 </td> 
   <td>  방문자 쿠키의 수명입니다. </td> 
  </tr> 
  <tr> 
   <td> ch </td> 
   <td> s.channel </td> 
   <td> 사이트 컨텐츠 | 사이트 섹션 </td> 
   <td> 트래픽 보고에서 사용되는 사이트 섹션 변수 </td> 
  </tr> 
  <tr> 
   <td> cp </td> 
   <td> 조회 유형 </td> 
   <td> 조회 유형 </td> 
   <td> 동작이 직접 상호 작용 전경의 결과인지 아니면 장치에서 직접 상호 작용 배경 없이 보내는 것인지를 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td> ct </td> 
   <td> 없음 </td> 
   <td> 방문자 프로필 | 기술 | 연결 유형 </td> 
   <td> 연결 유형(모뎀, LAN 등, IR 브라우저에서만 채울 수 있음) </td> 
  </tr> 
  <tr> 
   <td> <code> D </code> </td> 
   <td> dynamicVariablePrefix </td> 
   <td> 없음 </td> 
   <td> <p>지침은 <a href="../../../implement/js-implementation/c-variables/dynvars-overview.md#concept_B016789733A94070A9EAB209EEC05262" format="dita" scope="local"> 동적 변수 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td> events 또는 ev </td> 
   <td> s.events </td> 
   <td> 사이트 트래픽 | 구입, 장바구니, 사용자 지정 이벤트 </td> 
   <td> 페이지에서 발생하는 커머스 및 사용자 지정 이벤트, 전환 보고서에서 사용됨 </td> 
  </tr> 
  <tr> 
   <td> g </td> 
   <td> 없음 </td> 
   <td> 없음 </td> 
   <td> 페이지의 현재 URL최대 255바이트 </td> 
  </tr> 
  <tr> 
   <td> -g </td> 
   <td> 없음 </td> 
   <td> 없음 </td> 
   <td> 255바이트보다 긴 페이지 URL은 분할되어 처음 255바이트는 g= 매개 변수에 나타나고 나머지 바이트는 -g= 쿼리 매개 변수의 쿼리 문자열 뒤쪽에 나옵니다. </td> 
  </tr> 
  <tr> 
   <td> h1 - h5 </td> 
   <td> s.hier1 - s.hier5 </td> 
   <td> 사이트 컨텐츠 | 계층 보고서 </td> 
   <td> 트래픽 보고에서 사용되는 계층 변수 </td> 
  </tr> 
  <tr> 
   <td> hp </td> 
   <td> 없음 </td> 
   <td> 방문자 프로필 | 방문자 홈 페이지 </td> 
   <td> 현재 페이지가 브라우저의 홈 페이지인지 나타냄(Y 또는 N, IE 브라우저에서만 채우기 가능) </td> 
  </tr> 
  <tr> 
   <td> j </td> 
   <td> 없음 </td> 
   <td> 방문자 프로필 | 기술 | Javascript 버전 </td> 
   <td> 현재 설치된 JavaScript 버전을 표시(일반적으로 1.x)  </td> 
  </tr> 
  <tr> 
   <td> k </td> 
   <td> 없음 </td> 
   <td> 방문자 프로필 | 기술 | 쿠키 </td> 
   <td> 브라우저의 쿠키 지원 여부(Y, N 또는 U) </td> 
  </tr> 
  <tr> 
   <td> l1-l3 </td> 
   <td> s.list1 - s.list3 </td> 
   <td> 사용자 지정 전환 </td> 
   <td> 변수로 전달된 후 보고를 위해 개별 라인 항목으로 보고되는 구분 기호로 구분된 값의 목록입니다. </td> 
  </tr> 
  <tr> 
   <td> mid </td> 
   <td> 없음 </td> 
   <td> 없음 </td> 
   <td> Experience Cloud 방문자 ID </td> 
  </tr> 
  <tr> 
   <td> ndh </td> 
   <td> 없음 </td> 
   <td> 없음 </td> 
   <td> 이미지 요청이 JS 파일에서 시작되었는지 여부를 표시(1 또는 0) </td> 
  </tr> 
  <tr> 
   <td> ns </td> 
   <td> s.visitorNameSpace </td> 
   <td> 없음 </td> 
   <td> 쿠키를 어느 도메인에 설정하는지 지정 </td> 
  </tr> 
  <tr> 
   <td> oid </td> 
   <td> s.objectID </td> 
   <td> 사이트 컨텐츠 | 링크 | ClickMap </td> 
   <td> 마지막 페이지에 대한 개체 식별자, ClickMap에서 사용됨 </td> 
  </tr> 
  <tr> 
   <td> ot </td> 
   <td> 없음 </td> 
   <td> 사이트 컨텐츠 | 링크 | ClickMap </td> 
   <td> 마지막 페이지에 대한 개체 태그 이름, ClickMap에서 사용됨 </td> 
  </tr> 
  <tr> 
   <td> p </td> 
   <td> 없음 </td> 
   <td> 방문자 프로필 | 기술 | Netscape 플러그인  </td> 
   <td> 세미콜론 구분 브라우저 플러그인 이름 </td> 
  </tr> 
  <tr> 
   <td> pageName(또는 gn) </td> 
   <td> s.pageName </td> 
   <td> 사이트 컨텐츠 &gt; 페이지 </td> 
   <td> 보고의 지정된 페이지 이름 </td> 
  </tr> 
  <tr> 
   <td> pageType(또는 gt) </td> 
   <td> s.pageType </td> 
   <td> 사이트 컨텐츠 | 페이지를 찾을 수 없음 </td> 
   <td> 404 페이지인지 여부를 나타냄('오류' 또는 비어 있음) </td> 
  </tr> 
  <tr> 
   <td> pccr </td> 
   <td> 없음 </td> 
   <td> 없음 </td> 
   <td> 새로운 방문자에게만 발생, 무한 리디렉션 방지(항상 참) </td> 
  </tr> 
  <tr> 
   <td> pe </td> 
   <td> s.linkType </td> 
   <td> 사이트 컨텐츠 | 링크 | 종료 링크, 파일 다운로드, 사용자 지정 링크  </td> 
   <td> 사용자 지정 링크 히트 실행 유형 결정 </td> 
  </tr> 
  <tr> 
   <td> pev1 </td> 
   <td> 없음 </td> 
   <td> 사이트 컨텐츠 | 링크 | 종료 링크, 파일 다운로드, 사용자 지정 링크  </td> 
   <td> 사용자 지정 링크 히트가 발생한 URL  </td> 
  </tr> 
  <tr> 
   <td> pev2 </td> 
   <td> 없음 </td> 
   <td> 사이트 컨텐츠 | 링크 | 종료 링크, 파일 다운로드, 사용자 지정 링크  </td> 
   <td> 사용자 지정 링크의 친숙한 이름  </td> 
  </tr> 
  <tr> 
   <td> pev3 </td> 
   <td> 없음 </td> 
   <td> 모든 비디오 보고서  </td> 
   <td> 레거시 비디오 보고서의 이정표 추적에 사용, v15에서 사용 안 함  </td> 
  </tr> 
  <tr> 
   <td> pf </td> 
   <td> 없음 </td> 
   <td> 없음 </td> 
   <td> Adobe에서만 사용할 수 있습니다. 변경하지 마십시오. </td> 
  </tr> 
  <tr> 
   <td> pid </td> 
   <td> 없음 </td> 
   <td> 사이트 컨텐츠 | 링크 | ClickMap </td> 
   <td> 마지막 페이지에 대한 페이지 식별자, ClickMap에서 사용됨 </td> 
  </tr> 
  <tr> 
   <td> pidt </td> 
   <td> 없음 </td> 
   <td> 사이트 컨텐츠 | 링크 | ClickMap </td> 
   <td> 마지막 페이지에 대한 페이지 식별자 유형, ClickMap에서 사용됨 </td> 
  </tr> 
  <tr> 
   <td> products(또는 pl) </td> 
   <td> s.products </td> 
   <td> 제품 | 제품 </td> 
   <td> 전환 보고에서 사용되는 제품 변수 </td> 
  </tr> 
  <tr> 
   <td> purchaseID(또는 pi) </td> 
   <td> s.purchaseID </td> 
   <td> 없음 </td> 
   <td> 구입 중복 제거에 사용, 부풀려진 매출 방지 </td> 
  </tr> 
  <tr> 
   <td> r </td> 
   <td> s.referrer </td> 
   <td> 모든 트래픽 소스 보고서  </td> 
   <td> 참조 URL </td> 
  </tr> 
  <tr> 
   <td> s </td> 
   <td> 없음 </td> 
   <td> 방문자 프로필 | 기술 | 모니터 해상도  </td> 
   <td> 화면 해상도(너비 x 높이) </td> 
  </tr> 
  <tr> 
   <td> server(또는 sv) </td> 
   <td> s.server </td> 
   <td> 사이트 컨텐츠 | 서버 </td> 
   <td> 페이지의 서버, 트래픽 보고에서 사용됨 </td> 
  </tr> 
  <tr> 
   <td> state </td> 
   <td> s.state </td> 
   <td> 방문자 프로필 | 방문자 주 </td> 
   <td> 변수에서 정의한 대로 시/도를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td> t </td> 
   <td> (자동, 사용자 지정 타임스탬프가 없는 모든 히트에서 전송됨) </td> 
   <td> 없음 </td> 
   <td> <p><code>t</code> 매개 변수는 다음 형식을 갖습니다. </p> 
    <code>dd/mm/yyyy &amp; amp; nbsp; hh: MM: SS &amp; amp; nbsp; D &amp; amp; nbsp; 오프셋 </code>
  <p>D는 요일을 지정하는 <code>0-6</code> 범위의 숫자이고 <code>OFFSET</code>은 다음을 나타냅니다. </p> 
    <code>오프셋 및 amp; nbsp; From &amp; amp; nbsp; GMT &amp; amp; nbsp; In &amp; amp; nbsp; 시간 (&amp; amp); nbsp; * &amp; amp; nbsp; 60 &amp; amp; nbsp; * &amp; amp; nbsp; -amp; nbsp; 1 </code>
  <p> 예: </p> 
    <code>23/09/2016 &amp; amp; nbsp; 14:00:00 &amp; amp; nbsp; 1 &amp; amp; nbsp; 420 </code>
  </td> 
  </tr> 
  <tr> 
   <td> <code> ts </code> </td> 
   <td> <p>timestamp </p> </td> 
   <td> 없음 </td> 
   <td> <p>해당 히트와 함께 계산 및 전송되는 사용자 지정 타임스탬프. 보통 오프라인 추적에 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> v </td> 
   <td> 없음 </td> 
   <td> 방문자 프로필 | 기술 | Java </td> 
   <td> Java 활성화(Y 또는 N) </td> 
  </tr> 
  <tr> 
   <td> v0 </td> 
   <td> s.campaign </td> 
   <td> 캠페인 | 추적 코드 </td> 
   <td> 전환 보고에서 사용되는 캠페인 변수 </td> 
  </tr> 
  <tr> 
   <td> v1-v75 </td> 
   <td> s.eVar1-s.eVar75 </td> 
   <td> 모든 사용자 지정 전환 보고서 </td> 
   <td> 사용자 지정 보고에서 사용되는 전환 변수 </td> 
  </tr> 
  <tr> 
   <td> vid </td> 
   <td> <p>s.visitorID </p> </td> 
   <td> 없음 </td> 
   <td> 방문자의 고유 ID - 방문자 ID 변수. </td> 
  </tr> 
  <tr> 
   <td> vmk </td> 
   <td> s.vmk </td> 
   <td> 없음 </td> 
   <td> 방문자 마이그레이션 키, 타사에서 자사 쿠키로의 마이그레이션에 사용. 가치 하락. </td> 
  </tr> 
  <tr> 
   <td> vvp </td> 
   <td> s.variableProvider </td> 
   <td> 없음 </td> 
   <td> Genesis 통합에서 사용됨 </td> 
  </tr> 
  <tr> 
   <td> xact </td> 
   <td> s.transactionID </td> 
   <td> 없음 </td> 
   <td> 온라인 데이터와 오프라인 데이터의 연결에 사용되는 거래 ID </td> 
  </tr> 
  <tr> 
   <td> zip </td> 
   <td> s.zip </td> 
   <td> 방문자 프로필 | 방문자 우편 번호 </td> 
   <td> 변수에서 정의한 대로 우편 번호 결정 </td> 
  </tr> 
  <tr> 
   <td> 이미지 요청 URL의 /5/(모바일 프로토콜) 또는 /1/(비모바일 프로토콜)입니다. </td> 
   <td> 없음 </td> 
   <td> 없음 </td> 
   <td> <p> 방문자 식별을 위해 쿠키와 기타 방법이 사용되는 순서를 제어합니다.  </p> </td> 
  </tr> 
 </tbody> 
</table>

