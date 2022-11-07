---
description: 방문자 마이그레이션은 방문자 ID 쿠키를 하나의 도메인에서 다른 도메인으로 마이그레이션하는 프로세스입니다.
keywords: Analytics 구현
title: 방문자 마이그레이션
topic-fix: Developer and implementation
feature: Analytics Basics
exl-id: d44628c8-902f-4e60-b819-41d5537407d8
source-git-commit: ac9e4934cee0178fb00e4201cc3444d333a74052
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 97%

---

# 방문자 마이그레이션

방문자 마이그레이션은 방문자 ID 쿠키를 하나의 도메인에서 다른 도메인으로 마이그레이션하는 프로세스입니다.

방문자 마이그레이션을 통해 데이터 수집 도메인을 변경할 때 방문자 식별 쿠키를 보존할 수 있습니다. 데이터 수집 도메인은 다음 이유로 변경될 수 있습니다.

* `2o7.net`에서 `adobedc.net`으로 이동합니다.

* [Experience Cloud 방문자 ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ko-KR)를 구현하고 있으며 CNAME/자사 데이터 수집 도메인에서 `adobedc.net`, `2o7.net` 또는 `omtrdc.net`으로 이동합니다.

* cname/자사 데이터 수집 ( [자사 쿠키)](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=ko-KR)으로 이동하는 경우.

* 특정 CNAME에서 다른 CNAME으로 이동하는 경우 (도메인 변경)

방문자 마이그레이션을 구성한 후에 사용자가 방문자 ID 쿠키 없이 새로운 도메인을 방문하면 서버가 이전 데이터 수집 호스트 이름으로 리디렉션하고 사용 가능한 방문자 ID 쿠키를 회수한 다음 다시 새로운 도메인으로 리디렉션합니다. 이전 호스트 이름에서 방문자 ID가 발견되지 않으면 새로운 ID가 생성됩니다. 이는 방문자당 한 번만 이루어집니다.

## 방문자 마이그레이션 프로세스 {#section_FF0C5C5CAEF343FFA1892B29311F7160}

다음 테이블은 방문자 마이그레이션에 필요한 작업을 나열합니다.

<table id="table_7B2535FC3E264216A299686415C6B21C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 작업 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>시작하기:</b> <a href="https://helpx.adobe.com/kr/marketing-cloud/contact-support.html"  >고객 지원 센터에 문의</a>하여 마이그레이션하려는 도메인과 활성화하려는 마이그레이션 기간(30일, 60일 또는 90일)을 알려 줍니다. 비보안 및 보안 도메인을 포함해야 합니다. </p> </td> 
   <td colname="col3"> <p>마이그레이션할 대상 및 원본 도메인에 대한 <i>exact</i> 구문을 포함한 목록을 작성합니다. </p> 
    <ul id="ul_067EC5C7619141A6BDFBC209C9FD47E2"> 
     <li id="li_0723D948465A49C1871B81207AEDC4DC">example.112.2o7.net &gt; metrics.example.com </li> 
     <li id="li_B0CA15A593BD4AB9802E33A3FF037C7A">example.102.112.2o7.net &gt; smetrics.example.com </li> 
    </ul> <p>마이그레이션 호스트 이름은 Adobe 데이터 수집 서버에서 구성됩니다. 다음 단계를 계획할 수 있도록 고객 지원 센터가 언제 변경이 있을지 알려 줄 것입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>구성 변경 후 6시간 이상</b>: Analytics JavaScript 코드에서 <code> s.trackingServer</code> 및 <code> s.trackingServerSecure</code> 변수를 업데이트하여 새 데이터 수집 서버를 사용합니다. </p> </td> 
   <td colname="col3"> <p>이 변경 사항을 적용한 후 <a href="https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html"> Experience Cloud debugger</a>를 사용하여 Analytics 이미지 요청이 업데이트된 데이터 수집 서버로 이동하는지 확인합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Analytics 코드를 업데이트한 직후</b>: 이전 데이터 수집 도메인으로의 리디렉션이 발생하는지를 확인하는 테스트를 사이트에 대해 수행합니다. </p> </td> 
   <td colname="col3"> <p>Use a <a href="../implement/validate/packet-monitor.md"> 패킷 모니터</a>를 사용하여 처음으로 사이트에 액세스할 때 또는 쿠키를 지운 후, 200 (OK) HTTP 상태 코드 앞에 두 개의 302 (리디렉션) HTTP 상태 코드가 표시되는지 확인합니다. 리디렉션이 실패하는 경우 즉시 고객 지원 센터에 연락하여 마이그레이션이 바르게 구성되도록 하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>전체 마이그레이션 기간</b>: 이전 활성 호스트 이름에 대해 DNS 레코드를 유지합니다. </p> </td> 
   <td colname="col3"> <p>이전 호스트 이름은 DNS를 통해 해결되어야 하며 그렇지 않으면 쿠키 마이그레이션이 발생하지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
