---
description: 'null'
title: 구현 로드맵
uuid: 988bcca5-67ae-4e3f-97e6-6a42030b1962
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 구현 로드맵

## 새 사용자 {#section_77433E4FC5ED4C6BAFC1E72EB61C4503}

Adobe Analytics를 처음 사용하는 경우 [Adobe Analytics 시작](https://marketing.adobe.com/resources/help/en_US/analytics/getting-started/) 가이드를 사용하여 Analytics 보고서 세트 시작하기를 사용하여 첫 번째 제품군(데이터 저장소)을 빠르게 작성할 수 있습니다. 그런 다음 [Experience Platform Launch](https://docs.adobelaunch.com/)/ko-KR/를 사용하여 Analytics 코드를 배포할 수 있습니다.

## 구현 로드맵 {#section_E3DD8D199B744FFB9E9B386A44220206}

<table id="table_1683413EA0E34DBC9291832647B68E96"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 단계.  </th> 
   <th colname="col1" class="entry"> 작업 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <img  src="assets/step1_icon.png" id="image_21F30BBFC0A249F8B0E1A50EBBEED77D" /> </td> 
   <td colname="col1"> 구현 방법 선택. </td> 
   <td colname="col2"> <p>Analytics를 구현하는 일반적인 방법은 다음과 같습니다. </p> <p> 
     <ul id="ul_A7475867861540EFBD77AEE8C6DAD418"> 
      <li id="li_035E2619670F4D04A7F708625A9C01EF"> <a href="https://docs.adobelaunch.com/"> Experience Platform Launch</a>(권장) <p>이 안내서는 Adobe 웹 사이트 태그 및 모바일 SDK 관리 기능 사용에 대해 알고 있어야 하는 모든 것과 그러한 기능을 구현하는 방법을 알려 줍니다. </p> </li> 
      <li id="li_996FA2F5B0E149399CED391AB5235D8A"> <a href="/help/implement/c-implement-with-dtm/dtm-implementation-overview.md"> Dynamic Tag Management </a> <p>이 안내서에는 Dynamic Tag Management 구현을 안내하는 Analytics 관련 정보가 포함되어 있습니다. </p> </li> 
      <li id="li_18E6AD6D864246D0BA26DAA1D91DD811"> <a href="/help/implement/js-implementation/javascript-implementation-overview.md"> JavaScript </a> <p>이 안내서에는 데이터 수집 변수에 대한 설명과 <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/video/video_js.html">비디오</a>를 포함하여 데이터 수집 코드를 JavaScript로 구현하는 방법에 대한 자세한 설명이 포함되어 있습니다 . </p> </li> 
      <li id="li_85EC7A0AC5E04EE6981ED72A88C5D1FD"> <a href="https://marketing.adobe.com/resources/help/en_US/reference/developer.html"> Analytics SDK </a> <p>Analytics SDK를 사용하여 다음을 관리합니다. </p> <p> 
        <ul id="ul_F67F2E1964724800A84445A36DFB8E86"> 
         <li id="li_9C43F051EB5B4EA7A4C14EC1513DB824"> <a href="https://marketing.adobe.com/resources/help/en_US/mobile/ios/analytics_main.html"> iOS의 모바일 앱 </a> </li> 
         <li id="li_4354E44EB8B3494A88578C1621EF5BAC"> <a href="https://marketing.adobe.com/resources/help/en_US/mobile/android/analytics_main.html"> Android의 모바일 앱 </a> </li> 
        </ul> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step2_icon.png" id="image_02CFDC007BF1486AA312698EBFFA79F7" /> </td> 
   <td colname="col1"> ID 서비스를 설정합니다. </td> 
   <td colname="col2"> <p>(이전 <span class="term">방문자 ID 서비스</span>.) <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-analytics.html">Analytics에 대한 ID 서비스 설정</a>을 참조하십시오. </p> 
    <draft-comment> 
     <p><code> VisitorAPI.js </code>에서 파일 시작 부분에 방문자 ID 초기화 코드를 추가합니다. </p> 
     <code class="syntax javascript">
       var&nbsp;visitor&nbsp;=&nbsp;Visitor.getInstance("INSERT-MCORG-ID-HERE"); 
      visitor.trackingServer&nbsp;=&nbsp;"INSERT-TRACKING-SERVER-HERE";&nbsp;//&nbsp;same&nbsp;as&nbsp;s.trackingServer 
      visitor.trackingServerSecure&nbsp;=&nbsp;"INSERT-SECURE-TRACKING-SERVER-HERE";&nbsp;//same&nbsp;as&nbsp;s.trackingServerSecure 
      /* 
      &nbsp;==============&nbsp;DO&nbsp;NOT&nbsp;ALTER&nbsp;ANYTHING&nbsp;BELOW&nbsp;THIS&nbsp;LINE&nbsp;!&nbsp;============
     </code> 
     <ul id="ul_769BA118CC244308A805079C2CBECC12"> 
      <li id="li_D366EBDE24CB433EA523DB228CB2FAF1"> <code> "INSERT-MCORG-ID-HERE" </code> - (필수) 이 Adobe Experience Cloud 조직 ID는 회사가 Adobe Experience Cloud에 대한 프로비저닝을 받으면 관리자에게 전송됩니다. </li> 
      <li id="li_4F9704A6A6EA4334A3758F99B8D67C9D"> <code> "INSERT-TRACKING-SERVER-HERE" </code> - (필수) Analytics 추적 서버. </li> 
      <li id="li_C578420458D649228E54D9809AF62627"> <code> "INSERT-SECURE-TRACKING-SERVER-HERE" </code> - (ssl이 활성화되어 있을 경우 필수) Analytics 보안 추적 서버. </li> 
     </ul> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step3_icon.png" id="image_76B61DEABE3849CCB39135FDD7399EAA" /> </td> 
   <td colname="col1"> 선택한 구현 메서드를 사용하여 페이지 코드를 업데이트하고 배포합니다. </td> 
   <td colname="col2"> <p>Place the page code just after the opening <code> &lt;body&gt; </code> tag on each page you want to track. 최소한 다음 변수를 업데이트하십시오. </p> 
    <ul id="ul_29200A6E8DA14386BDA242AD8B270FEB"> 
     <li id="li_FB24D2CB9241401A83BD13EE342A7810"> <code> var s=s_gi("INSERT-RSID-HERE") </code> </li> 
     <li id="li_463A35BA06CC4618B4AF17CD7E83AED5"> <code> s.pageName="INSERT-NAME-HERE" // for example, s.pageName=document.title </code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step4_icon.png" id="image_B255E5EAE7BB43FC946D0E9DFCA83003" /> </td> 
   <td colname="col1"> 구현의 유효성을 검사합니다. </td> 
   <td colname="col2"> <p> <a href="/help/implement/impl-testing/impl-validation/impl-validation.md"> 테스트 및 유효성 검사</a>는 구현 유효성 검사에 대한 정보를 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step5_icon.png" id="image_844E896941E2489A943BE10AD710ED36" /> </td> 
   <td colname="col1"> Adobe Experience Cloud 디버거를 사용하여 데이터가 전송되고 있는지 확인합니다. </td> 
   <td colname="col2"> <p><a href="/help/implement/impl-testing/debugger.md"> Experience Cloud Debugger</a>를 설치합니다. 설치가 끝나면 페이지 코드를 배포한 페이지를 불러온 다음 디버거를 엽니다. 디버거가 전송된 수집 데이터에 대한 정보를 표시합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 추가 정보 {#section_64B6A948DF4A4B5E9E1D22549F8C508B}

[!UICONTROL Experience Platform Launch], [!UICONTROL Dynamic Tag Management] 및 JavaScript 메서드의 차이점에 대한 자세한 내용은 [구현 방법 선택](/help/implement/c-implementation-methods/choose-implementation-method.md)을 참조하십시오.

시작 프로세스에 대한 간략한 개요 및 첫 번째 Analytics 보고서 세트를 빠르게 설정에 대한 도움말을 보려면 Analytics 시작하기 안내서에서 [Analytics 구현 시작하기](https://marketing.adobe.com/resources/help/en_US/dtm/get_started.html)를 참조하십시오.
