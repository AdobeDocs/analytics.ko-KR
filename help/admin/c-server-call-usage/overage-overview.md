---
description: 'null'
title: 서버 호출 사용량 개요
uuid: 6e014364-efc1-4769-a0b5-cf105c0ed9b1
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 서버 호출 사용량 개요

## 서버 호출 사용량을 모니터링하고 경고하는 이유는 무엇입니까? {#section_060C29BF1D00444B85892AD1FCF55290}

Adobe Analytics Server 호출 사용 기능은 브라우저 및 모바일 서버 호출 사용 데이터에 대한 투명도 요청에 대해 해결합니다. 다음과 같은 액세스 권한을 제공합니다.

* 서버 호출 소비 데이터를 추적하고 계약 제한과 비교하는 서버 호출 사용 대시보드입니다.(**[!UICONTROL Analytics > Admin > Server Call Usage]**)
* A Server Call Usage alert type in the Alert Builder that lets you set up alerts to prevent overages (**[!UICONTROL Analytics > Components >Alerts]**)

서버 호출 사용의 주요 이점은 다음과 같습니다.

* **계약** 서버 호출 사용 제한에 대한 모바일 소비를 포함하여 서버 호출 소비 및 약정 데이터를 표시합니다.
* **오버레이의 위험이나 발생을 알리고 초과 발생의 발생 가능성에 대해 준비하거나 조치를 취하기 위한 경고입니다** .

Previously, while you could access monthly server call consumption data under  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Billing]** , this data was only updated 6 days after billing had closed for that month. 또한 데이터에 모바일 사용량이 포함되지 않았습니다. 또한 이 기능은 **[!UICONTROL Billing Information]** > **[!UICONTROL Analytics]** 아래에 있는 현재 **[!UICONTROL Reports]** 보고서를 대체합니다.

## 전제 조건 {#section_49AE590FFC7C4E8A83C640C4AAA581AA}

* **권한:** 서버 호출 사용량 대시보드 및 경고 빌더/관리자에 액세스하려면 Adobe Analytics 관리자여야 합니다.
* **권한:** 관리자는 관리자가 아닌 사용자에게 액세스 권한을 부여할 수 있습니다.권한이 호출됩니다 **[!UICONTROL Server Call Usage]**. [서버 호출 사용량 권한](/help/admin/c-server-call-usage/overage-overview.md#section_FCC58EB635954A32990D4E67B52B4369)을 참조하십시오.

## 중요한 용어 {#section_CBA348A039F34563B097CD8890AB358D}

다음은 서버 호출 사용에 대한 필수 용어에 대한 간략한 입문입니다.

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
   <td colname="col2"> <p>"히트" 또는 "이미지 요청"이라고도 하는 서버 호출은 데이터를 Adobe 서버로 전송하여 처리하는 인스턴스입니다. 가장 일반적인 서버 호출 유형은 페이지 보기입니다. 페이지 보기는 방문자가 웹 사이트에서 페이지를 보고 Adobe로 서버 호출이 생성되며 정보를 수집, 처리한 후 보고서 지표에 포함할 때 발생합니다. </p> <p>종료 링크 및 파일 다운로드 등 다른 유형의 서버 호출은 데이터를 Adobe로 전송하여 처리하지만 새 페이지 보기로 기록되지는 않습니다. "제외된" 페이지 보기(예: 구성하는 IP 주소 범위에 의해 보고서에서 제외)도 Adobe가 수신하여 처리하지만 보고서에 표시되지 않기 때문에 서버 호출입니다. </p> <p><b>주 서버 호출</b>:웹 사이트 방문자 브라우저 또는 데이터 삽입 API에서 직접 받은 요청입니다. 기본 히트(페이지 보기), 기본 사용자 지정 이벤트, 기본 다운로드 이벤트 및 기본 종료 이벤트를 포함합니다. </p> <p><b>보조 서버 호출</b>:다중 세트 태그로 만들었거나 VISTA 규칙으로 복사/이동한 주 서버 호출의 사본. 보조 서버 호출이 VISTA 규칙에 의해 다른 보고서 세트로 이동(복사되지 않음)된 경우, 누적된 보조 호출은 주 서버 호출에서 제외됩니다. </p> <p><b>모바일 기본 서버 호출 </b> </p> <p>Mobile SDK 중 하나에서 직접 받은 요청입니다. trackAction, trackState, trackApp Crashes, trackActionFromBackground, trackLocation, trackBeacon, trackPushMessageClickThrough, trackTimedActionBacklog, trackLifetimeValueIncrease를 포함합니다.</p> <p><b>모바일 보조 서버 호출</b> </p> <p>다중 세트 태그로 만들었거나 VISTA 규칙으로 복사하고 이동한 주 서버 호출의 사본. 보조 서버 호출이 VISTA 규칙에 의해 다른 보고서 세트로 이동(복사되지 않음)된 경우, 누적된 보조 호출은 주 서버 호출에서 제외됩니다. </p> <p>참고: 계약에 따라 귀사에 모바일 서버 호출(기본 또는 보조)에 대해서만 권한이 부여된 경우 웹과 모바일 특정 사용량은 모두 모바일 특정 약정에 따라 계산됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>청구 회사(청구 ID) </p> </td> 
   <td colname="col2"> <p>서버 호출에 대한 청구를 받는 법인. 예: adobe.com. 각 청구 회사에는 청구 고객을 고유하게 식별하는 데 사용되는 청구 ID가 있습니다. 청구 ID를 여러 Experience Cloud 조직에 연결할 수 있습니다.조직과 청구 ID 사이에 항상 1:1 관계가 있는 것은 아닙니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그인 회사 </p> </td> 
   <td colname="col2"> <p>한 청구 회사에 <a href="https://helpx.adobe.com/kr/analytics/kb/multiple-login-companies.html">여러 로그인 회사</a>가 있을 수 있습니다. 로그인 회사는 조직에서 사용하는 보고서 세트의 컬렉션입니다. 일부 조직에는 조직의 다른 부분에 적용되는 여러 로그인 회사가 있습니다. 이 기능은 많은 보고서 세트가 회사의 다른 사용자에게 적용되지 않는 여러 비즈니스 단위를 처리하는 대기업에서 특히 유용합니다. </p> <p>종종 회사의 지역 자회사가 있습니다. 이 예는 로그인 회사 및 관련 보고서 세트를 보여줍니다. </p> 
    <ul id="ul_8C756C7972D04F5E89D6E32BB06D26C3"> 
     <li id="li_EA6257FED7854B6FAA071926D0F8A07C">adobe.worldwide:RS1, RS2, RS3, RS4 </li> 
     <li id="li_3EAFB556849E4CCC9D96D5A3492EC898">adobe.us:RS1, RS2 </li> 
     <li id="li_572FFB3F4BF545BDB13102D82CE5E50C">adobe.in:RS3 </li> 
     <li id="li_B6ACBA35E18A427AA83F76BD38E502D7">adobe.de:RS4 </li> 
    </ul> <p>참고: 청구 회사 내의 <u>모든</u> 보고서 세트에 대한 서버 호출 사용량 데이터는 해당 <a href="/help/admin/c-server-call-usage/overage-overview.md#section_FCC58EB635954A32990D4E67B52B4369">권한</a>이 있는 모든 사용자가 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud 조직 </p> </td> 
   <td colname="col2"> <p> 조직은 관리자가 그룹과 사용자를 구성하고, Experience Cloud에서 단일 사인온을 제어할 수 있도록 하는 항목입니다. 조직은 모든 Experience Cloud 제품 및 솔루션을 포괄하는 로그인 회사와 같은 기능을 합니다. </p> <p>대부분의 경우 조직은 회사 이름입니다. 그러나 회사는 많은 조직을 보유할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>서버 호출 약정 </p> </td> 
   <td colname="col2"> <p>회사가 Adobe와 계약을 체결하면, Adobe 영업 팀은 사용자와 고객, 유형(기본, 보조, 모바일 기본, 모바일 보조) 및 계약 기간 동안 발생할 것으로 예상되는 대략적인 서버 호출 수를 식별합니다. 총 서버 호출 약정입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용 기간 </p> </td> 
   <td colname="col2"> <p>서버 호출 사용 모니터링을 위해 이 총 서버 호출 약정은 연간 비교를 용이하게 하기 위해 더 적은 사용 기간(예: 3개월)으로 분류됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>계약 기간 </p> </td> 
   <td colname="col2"> <p>계약 기간은 여러 해가 될 수 있습니다. 귀사에 3년 계약 기간 동안 600만 건의 서버 호출 약정을 체결했다고 가정해 봅시다. 서버 호출 사용량을 모니터링하기 위해 이 3년을 더 작은 사용 기간으로 구분하면 연차별로 쉽게 비교할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 서버 호출 사용량 권한 {#section_FCC58EB635954A32990D4E67B52B4369}

서버 호출 사용 권한은 Analytics 관리자에게 자동으로 부여됩니다. 대시보드를 보고 서버 호출 경고를 만들 수 있습니다. 관리자는 관리자가 아닌 사람에게 이 권한을 부여하도록 선택할 수 있습니다.

>[!NOTE] 귀사는 서버 호출 사용량에 접근할 수 있는 로그인 회사를 선택할 수 있습니다.

<table id="table_86256AD8B4554F369439A8FDF2F545E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 권한 이름 </th> 
   <th colname="col3" class="entry"> Adobe Analytics에 로그인한 경우 권한 부여(기존 로그인) </th> 
   <th colname="col4" class="entry"> Adobe Experience Cloud에 로그인한 경우 권한 부여 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>서버 호출 사용량 </p> </td> 
   <td colname="col3"> 
    <ol id="ol_13A984328D264488B7045DC7521A5F55"> 
     <li id="li_ACDA518C7D184084AC1DFA7B38C67314">sc.omniture.com을 통해 Analytics에 로그인합니다. </li> 
     <li id="li_066D90AB071941C3869EDAFCE981707A"><span class="ignoretag"><span class="uicontrol">관리</span> &gt; <span class="uicontrol">사용자 관리</span> &gt; <span class="uicontrol">그룹</span> &gt; <span class="uicontrol">모두 보고서 액세스 권한 편집</span> &gt; <span class="uicontrol">Analytics 도구</span> &gt; <span class="uicontrol">사용자 지정</span> &gt; <span class="uicontrol">서버 호출 사용량</span></span>으로 이동합니다. </li> 
    </ol> </td> 
   <td colname="col4"> 
    <ol id="ol_518673ED323A4C5993A3B9F4BA09E405"> 
     <li id="li_56FF685A3B454ECEA5F16BB591A60034">login.experiencecloud.adobe.com에 로그인합니다.</li> 
     <li id="li_FA1AE0F19DEF4AB2AA77B22CCA2995F9"><span class="uicontrol">Analytics</span>를 클릭합니다. </li> 
     <li id="li_22A4CBB84B5A451780873BBE67E6E6EF"><span class="ignoretag"><span class="uicontrol">제품</span> &gt; <span class="uicontrol">제품 프로필</span> &gt; <span class="uicontrol">권한</span> &gt; <span class="uicontrol">Analytics 도구</span> &gt; <span class="uicontrol">서버 호출 사용량</span></span>으로 이동합니다. </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

