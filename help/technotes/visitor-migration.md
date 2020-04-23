---
description: 방문자 마이그레이션은 방문자 ID 쿠키를 하나의 도메인에서 다른 도메인으로 마이그레이션하는 프로세스입니다.
keywords: Analytics Implementation
title: 방문자 마이그레이션
topic: Developer and implementation
uuid: af31928c-85d7-407f-a583-0c8f2852ceb3
translation-type: tm+mt
source-git-commit: 5e47974fcf95625def21a9011ad981197ae39c99

---


# 방문자 마이그레이션

방문자 마이그레이션은 방문자 ID 쿠키를 하나의 도메인에서 다른 도메인으로 마이그레이션하는 프로세스입니다.

방문자 마이그레이션을 사용하면 데이터 수집 도메인을 변경할 때 방문자 식별 쿠키를 보존할 수 있습니다. 데이터 수집 도메인은 다음과 같은 이유로 변경될 수 있습니다.

* `2o7.net`에서 `omtrdc.net`([지역별 데이터 수집](https://marketing.adobe.com/resources/help/ko_KR/whitepapers/rdc/))으로 이동하는 경우

* [Experience Cloud 방문자 ID 서비스](https://marketing.adobe.com/resources/help/ko_KR/mcvid/)를 구현하고 CNAME/퍼스트 파티 데이터 수집 도메인에서 `2o7.net` 또는 `omtrdc.net`([지역별 데이터 수집](https://marketing.adobe.com/resources/help/ko_KR/whitepapers/rdc/))으로 이동하는 경우

* `2o7.net` 또는 `omtrdc.net`에서 CNAME/자사 데이터 수집([자사 쿠키](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/))으로 이동하는 경우

* 한 CNAME에서 다른 CNAME으로 이동(도메인 변경).

방문자 마이그레이션이 구성되면 사용자가 방문자 ID 쿠키 없이 새 도메인을 방문하면 서버가 이전 데이터 수집 호스트 이름으로 리디렉션하고 사용 가능한 방문자 ID 쿠키를 검색한 다음 다시 새 도메인으로 리디렉션합니다. 이전 호스트 이름에서 방문자 ID를 찾을 수 없는 경우 새 ID가 생성됩니다. 이것은 방문자당 한 번만 발생합니다.

## 방문자 마이그레이션 프로세스 {#section_FF0C5C5CAEF343FFA1892B29311F7160}

다음 표에는 방문자 마이그레이션에 필요한 작업이 나열되어 있습니다.

<table id="table_7B2535FC3E264216A299686415C6B21C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 작업 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>시작하기:</b> <a href="https://helpx.adobe.com/kr/marketing-cloud/contact-support.html"  >고객 지원 센터에 문의</a>하여 마이그레이션하려는 도메인과 활성화하려는 마이그레이션 기간(30일, 60일 또는 90일)을 알려줍니다. 비보안 및 보안 도메인을 포함해야 합니다. </p> </td> 
   <td colname="col3"> <p>마이그레이션하고 마이그레이션할 도메인의 <i>정확한</i> 구문을 사용하여 목록을 만듭니다. </p> 
    <ul id="ul_067EC5C7619141A6BDFBC209C9FD47E2"> 
     <li id="li_0723D948465A49C1871B81207AEDC4DC">example.112.2o7.net &gt; metrics.example.com </li> 
     <li id="li_B0CA15A593BD4AB9802E33A3FF037C7A">example.102.112.2o7.net &gt; smetrics.example.com </li> 
    </ul> <p>마이그레이션 호스트 이름은 Adobe 데이터 수집 서버에서 구성됩니다. 고객 지원 센터에서 변경 사항이 있는 시기를 알려주시면 다음 단계를 계획할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>구성 변경 후 6시간 이상</b>: Analytics JavaScript 코드에서 <code> s.trackingServer</code> 및 <code> s.trackingServerSecure</code> 변수를 업데이트하여 새 데이터 수집 서버를 사용합니다. </p> </td> 
   <td colname="col3"> <p>After you make this change, use a <a href="../implement/validate/packet-monitor.md"> packet monitor</a> to verify that the Analtyics image request is going to the updated data collection server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Analytics 코드를</b>업데이트한 즉시:사이트를 테스트하여 이전 데이터 수집 도메인으로의 리디렉션이 발생하는지 확인합니다. </p> </td> 
   <td colname="col3"> <p>Use a <a href="../implement/validate/packet-monitor.md"> packet monitor</a> to verify that when you access your site for the first time, or after clearing cookies, you see two 302 (redirect) HTTP status codes before the 200 (OK) HTTP status code. 이러한 리디렉션이 실패할 경우 고객 지원 센터에 즉시 연락하여 마이그레이션이 올바르게 구성되었는지 확인하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>전체 마이그레이션 기간</b>:이전 호스트 이름에 대한 DNS 레코드를 활성화합니다. </p> </td> 
   <td colname="col3"> <p>이전 호스트 이름은 DNS를 통해 확인되어야 하며 그렇지 않으면 쿠키 마이그레이션이 발생하지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 사용되지 않는 visitorMigrationKey 및 visitorMigrationServer 변수 {#section_32FCEE2575944D039EA0FEBFB5814259}

2013년 3월 현재 `visitorMigrationKey`, `visitorMigrationServer` 및 `visitorMigrationServerSecure` 데이터 수집 변수는 더 이상 사용되지 않습니다. 이러한 변수에 포함되었던 데이터는 이제 보안 향상을 위해 Adobe 서버에 저장됩니다.
