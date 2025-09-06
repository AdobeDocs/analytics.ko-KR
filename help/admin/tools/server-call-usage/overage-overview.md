---
description: Adobe Analytics 서버 호출 사용 기능에 대한 개요.
title: 서버 호출 사용량 개요
feature: Server Call Usage
exl-id: d3d64f1e-f01b-4b9e-9aee-c14e574fc40b
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 80%

---

# 서버 호출 사용량

Adobe Analytics 서버 호출 사용량은 브라우저 및 모바일 서버 호출 사용량 데이터 모두에 대한 투명성 요청을 해결합니다. 다음에 액세스할 수 있습니다.

* 서버 호출 사용량 데이터를 추적하고 이를 계약 한도와 비교하는 서버 호출 사용량 대시보드. (Adobe Analytics에서 > [!UICONTROL **관리자**] > [!UICONTROL **서버 호출 사용량**]&#x200B;을 선택합니다.)
* 초과 사용을 방지하기 위해 경고를 설정할 수 있는 경고 빌더의 서버 호출 사용량 경고 유형(Adobe Analytics에서 [!UICONTROL **구성 요소**] > [!UICONTROL **경고**] 선택)

서버 호출 사용의 주요 이점은 다음과 같습니다.

* 계약상 서버 호출 사용량 한도에 대한 모바일 사용량 포함하여 서버 호출 사용량 및 약정 데이터에 대한 **가시성**&#x200B;을 제공합니다.
* 초과 사용에 대한 위험 또는 발생을 알리고, 초과 사용 발생 가능성에 대해 준비/조치하도록 **경고**&#x200B;를 제공합니다.

## 사전 요구 사항 {#section_49AE590FFC7C4E8A83C640C4AAA581AA}

* **권한:** 서버 호출 사용량 대시보드와 경고 빌더 또는 경고 관리자에 액세스하려면 Adobe Analytics 관리자여야 합니다.
* **권한:** 관리자는 관리자가 아닌 사용자에게 액세스 권한을 부여할 수 있습니다. 이 권한을 **[!UICONTROL 서버 호출 사용량]**&#x200B;이라고 합니다. [서버 호출 사용 권한](#server-call-usage-permission)을 참조하세요.

## 중요한 용어 {#terminology}

다음 용어는 서버 호출 사용을 이해하는 데 중요합니다.

<table id="table_4E97F85F13344A2C962FA4FA5A51642E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 용어 </th> 
   <th colname="col2" class="entry"> 정의 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>서버 호출 </p> </td> 
   <td colname="col2"> <p>서버 호출은 데이터를 처리할 수 있도록 Adobe 서버로 보내는 인스턴스로서, "히트" 또는 "이미지 요청"이라고도 합니다. 가장 일반적인 서버 호출 유형은 페이지 보기입니다. 페이지 보기는 방문자가 웹 사이트에서 페이지를 보고 Adobe로 서버 호출이 생성되며 정보를 수집, 처리한 후 보고서 지표에 포함할 때 발생합니다. </p> <p>데이터를 처리하기 위해 Adobe로 보내지만 새 페이지 보기로 기록되지 않는 종료 링크 및 파일 다운로드 등의 다른 서버 호출 유형이 있습니다. "제외된" 페이지 보기 횟수도 (예: IP 주소 범위를 구성하여 보고서에서 제외) Adobe에서 수신 및 처리하지만 보고서에는 표시되지 않기 때문에 호출로 취급됩니다. </p> <p><b>주 서버 호출</b>: 웹 사이트 방문자 브라우저 또는 데이터 삽입 API에서 직접 받은 요청입니다. 기본 방문 횟수 (페이지 보기 횟수), 기본 사용자 지정 이벤트, 기본 다운로드 이벤트 및 기본 종료 이벤트를 포함합니다. </p> <p><b>보조 서버 호출</b>: 다중 세트 태그로 만들었거나 VISTA 규칙으로 복사하고 이동한 주 서버 호출의 사본입니다. 보조 서버 호출이 VISTA 규칙에 따라 다른 보고서 세트로 복사되지 않고 이동되면 누적된 보조 호출은 기본 서버 호출에서 차감됩니다. </p> <p><b>모바일 기본 서버 호출 </b> </p> <p>Mobile SDK 중 하나에서 직접 받은 요청입니다. trackAction, trackState, trackApp Crashes, trackActionFromBackground, trackLocation, trackBeacon, trackPushMessageClickThrough, trackTimedActionBacklog, trackLifetimeValueIncrease를 포함합니다.</p> <p><b>모바일 보조 서버 호출</b> </p> <p>다중 세트 태그로 만들었거나 VISTA 규칙으로 복사하고 이동한 주 서버 호출의 사본. 보조 서버 호출이 VISTA 규칙에 따라 다른 보고서 세트로 복사되지 않고 이동되면 누적된 보조 호출은 기본 서버 호출에서 차감됩니다. </p> <p>참고: 계약에 따라 귀사에 모바일 서버 호출 (기본 또는 보조)에 대해서만 권한이 부여된 경우 웹과 모바일 특정 사용량은 모두 모바일 특정 약정에 따라 계산됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>청구 회사(청구 ID) </p> </td> 
   <td colname="col2"> <p>서버 호출에 대해 청구되는 법인입니다. 예를 들어, adobe.com이 있습니다. 각 청구 회사에는 청구 고객을 고유하게 식별하는 데 사용되는 청구 ID가 있습니다. 청구 ID는 Experience Cloud Orgs에 연결될 수 있습니다. 조직과 청구 ID 간의 관계가 항상 1:1인 것은 아닙니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그인 회사 </p> </td> 
   <td colname="col2"> <p>한 청구 회사에 <a href="https://helpx.adobe.com/kr/analytics/kb/multiple-login-companies.html">여러 로그인 회사</a>가 있을 수 있습니다. 로그인 회사는 조직에서 사용한 보고서 세트들의 컬렉션입니다. 일부 조직에는 조직의 여러 부분에 해당되는 여러 로그인 회사가 있습니다. 이 기능은 많은 보고서 세트가 회사의 다른 직원에게는 적용되지 않는 다양한 비즈니스 단위를 관리하는 대기업에서 특히 유용합니다. </p> <p>주로 이들은 회사의 지역 자회사입니다. 이 예는 로그인 회사 및 연관된 보고서 세트를 보여 줍니다. </p> 
    <ul id="ul_8C756C7972D04F5E89D6E32BB06D26C3"> 
     <li id="li_EA6257FED7854B6FAA071926D0F8A07C">adobe.worldwide: RS1, RS2, RS3, RS4 </li> 
     <li id="li_3EAFB556849E4CCC9D96D5A3492EC898">adobe.us: RS1, RS2 </li> 
     <li id="li_572FFB3F4BF545BDB13102D82CE5E50C">adobe.in: RS3 </li> 
     <li id="li_B6ACBA35E18A427AA83F76BD38E502D7">adobe.de: RS4 </li> 
    </ul> <p>참고: 청구 회사 내의 <u>모든</u> 보고서 세트에 대한 서버 호출 사용량 데이터는 해당 <a href="/help/admin/tools/server-call-usage/overage-overview.md">권한</a>이 있는 모든 사용자가 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud 조직 </p> </td> 
   <td colname="col2"> <p>조직은 관리자가 그룹과 사용자를 구성하고, Experience Cloud에서 Single Sign-On을 제어할 수 있도록 하는 항목입니다. 조직은 모든 Experience Cloud 제품 및 솔루션을 포괄하는 로그인 회사와 같은 기능을 합니다. </p> <p>대부분의 경우 조직은 회사 이름입니다. 그렇지만 한 회사에 여러 조직이 있을 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>서버 호출 약정 </p> </td> 
   <td colname="col2"> <p>귀사가 Adobe와의 계약에 서명하면 Adobe Sales 팀은 귀사, 고객, 계약 기간 과정에 발생할 것으로 예상되는 서버 호출 유형 (기본, 보조, 모바일 기본, 모바일 보조) 및 수와 동일시합니다. 총 서버 호출 약정입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용 기간 </p> </td> 
   <td colname="col2"> <p>이 총 서버 호출 약정은 서버 호출 사용량을 모니터링하기 위해 더 작은 사용 기간(예: 3개월)으로 구분되므로 매년 비교하기가 쉽습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>계약 기간 </p> </td> 
   <td colname="col2"> <p>계약 기간은 여러 해 동안 지속될 수 있습니다. 귀사에 계약 기간 3년 동안 6백만 개의 서버 호출 약정이 있다고 가정해 봅시다. 서버 호출 사용량을 모니터링하기 위해 이 3년을 더 작은 사용 기간으로 구분하면 연차별로 쉽게 비교할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 서버 호출 사용량 권한 {#permission}

서버 호출 사용량 권한은 Analytics 관리자에게 자동으로 부여됩니다. 이를 통해 사용자는 대시보드를 보고 서버 호출 경고를 작성할 수 있습니다. 관리자는 이 권한을 관리자가 아닌 사용자에게 부여하도록 선택할 수 있습니다.

>[!NOTE]
>
>귀사는 서버 호출 사용량에 접근할 수 있는 로그인 회사를 선택할 수 있습니다.

<table id="table_86256AD8B4554F369439A8FDF2F545E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 권한 이름 </th> 
   <th colname="col3" class="entry"> Adobe Analytics (기존 로그인)에 로그인한 경우 권한 부여 </th> 
   <th colname="col4" class="entry"> Adobe Experience Cloud에 로그인한 경우 권한 부여 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>서버 호출 사용량 </p> </td> 
   <td colname="col3"> 
    <ol id="ol_13A984328D264488B7045DC7521A5F55"> 
     <li id="li_ACDA518C7D184084AC1DFA7B38C67314">sc.omniture.com을 통해 Analytics에 로그인합니다. </li> 
     <li id="li_066D90AB071941C3869EDAFCE981707A"><span class="ignoretag"> <span class="uicontrol"> 관리자 </span> &gt; <span class="uicontrol"> 모든 관리자 </span> &gt; <span class="uicontrol"> 사용자 관리 </span> &gt; <span class="uicontrol"> 그룹 </span> &gt; <span class="uicontrol"> 모든 보고서 액세스 편집 </span> &gt; <span class="uicontrol"> Analytics 도구 </span> &gt; <span class="uicontrol"> 사용자 지정 </span> &gt; <span class="uicontrol"> 서버 호출 사용량 </span> </span>(으)로 이동합니다. </li> 
    </ol> </td> 
   <td colname="col4"> 
    <ol id="ol_518673ED323A4C5993A3B9F4BA09E405"> 
     <li id="li_56FF685A3B454ECEA5F16BB591A60034">login.experiencecloud.adobe.com에 로그인합니다.</li> 
     <li id="li_FA1AE0F19DEF4AB2AA77B22CCA2995F9"><span class="uicontrol">Analytics</span>를 클릭합니다. </li> 
     <li id="li_22A4CBB84B5A451780873BBE67E6E6EF"><span class="ignoretag"> <span class="uicontrol"> 제품 </span> &gt; <span class="uicontrol"> 제품 프로필 </span> &gt; <span class="uicontrol"> 권한 </span> &gt; <span class="uicontrol"> Analytics 도구 </span> &gt; <span class="uicontrol"> 서버 호출 사용량 </span> </span>(으)로 이동합니다. </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>
