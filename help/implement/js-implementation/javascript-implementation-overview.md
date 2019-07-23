---
description: Analytics를 사용하기 시작하려면 보고에 표시할 보고서 세트로 데이터를 보내야 합니다.
keywords: Analytics 구현; Javascript; Javascript 구현; Appmeasurement; Appmeasurement 다운로드; Identity Service; Visitorapi. js; 캐싱; Appmeasurement 압축
seo-description: Analytics를 사용하기 시작하려면 보고에 표시할 보고서 세트로 데이터를 보내야 합니다.
seo-title: JavaScript 구현 개요
solution: Analytics
title: JavaScript 구현 개요
topic: 개발자 및 구현
uuid: bb 661 d 8 c-faf 9-4454-ac 3 c -0 c 1 a 4 c 0 a 9336
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# JavaScript 구현 개요

Analytics를 사용하기 시작하려면 보고에 표시할 보고서 세트로 데이터를 보내야 합니다.

The easiest and recommended way to send data to [!DNL Analytics] is by using [Dynamic Tag Management](../../implement/c-implement-with-dtm/dtm-implementation-overview.md). 그러나 경우에 따라 이전 JavaScript 메서드를 사용하여 Analytics를 구현할 수 있습니다.

>[!NOTE]
>
>이 섹션에서는 Analytics를 구현하는 기존 방법을 설명합니다. 모든 Analytics 고객은 Experience Cloud 태그를 배포하는 표준 방법인 [다이내믹 태그 관리](https://marketing.adobe.com/resources/help/en_US/dtm/)에 액세스할 수 있습니다.

## 구현 절차 {#section_73961BAD5BB4430A95E073DE5C026277}

데이터를 모으는 코드 페이지를 성공적으로 구현하기 위해서는, 새로운 컨텐츠를 웹 사이트에 업로드할 수 있도록 호스팅 서버에 대한 액세스 권한을 가지고 있어야 합니다. 코드를 구현할 기존 사이트가 있으면 유용합니다. 

다음은 기초 Analytics 구현 단계입니다.

<table id="table_1683413EA0E34DBC9291832647B68E96"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 단계 </th> 
   <th colname="col1" class="entry"> 작업 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <img  src="assets/step1_icon.png" id="image_21F30BBFC0A249F8B0E1A50EBBEED77D" /> </td> 
   <td colname="col1"> 방문자 ID 서비스에서 JavaScript용 AppMeasurement를 다운로드하십시오.  </td> 
   <td colname="col2"> <p>다운로드는 <a href="https://marketing.adobe.com/resources/help/en_US/reference/?f=code_manager_admin" format="http" scope="external">Code Manager</a>에서 제공됩니다 . </p> <p>이 다운로드 ZIP에는 여러 파일이 포함되어 있습니다. <code> AppMeasurement.js</code> 및 <code>VisitorAPI.js</code>는 Analytics를 구현할 때 관련된 파일입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step2_icon.png" id="image_02CFDC007BF1486AA312698EBFFA79F7" /> </td> 
   <td colname="col1"> ID 서비스를 설정합니다. </td> 
   <td colname="col2"> <p>(Formerly <span class="term"> Visitor ID service </span>.) See <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-analytics.html" format="https" scope="external"> Set Up the Identity Service for Analytics </a>. </p> 
    <draft-comment> 
     <p><code>VisitorAPI.js</code>에서 파일 시작 부분에 방문자 ID 초기화 코드를 추가합니다. </p> 
     <code class="syntax javascript">var visitor = Visitor. getinstance ("INSERT-MCORG-ID-HERE"); visitor. trackingserver = "INSERT-TRACKING-SERVER-HERE"; // s. trackingserver visitor. trackingserversecure = "INSERT-SECURE-TRACKING-SERVER-HERE" 와 동일함; //same as s. trackingserversecure/* = = do not alter anything below this line = = </code>
      <ul id="ul_769BA118CC244308A805079C2CBECC12"> 
      <li id="li_D366EBDE24CB433EA523DB228CB2FAF1"> <code> " INSERT-MCORG-ID-HERE " </code> - (필수) 회사가 Adobe Experience Cloud에 대한 프로비저닝을 받으면 이 Adobe Experience Cloud 조직 ID가 관리자에게 전송됩니다. </li> 
      <li id="li_4F9704A6A6EA4334A3758F99B8D67C9D"> <code> "INSERT-TRACKING-SERVER-HERE"</code> - (필수) Analytics 추적 서버. </li> 
      <li id="li_C578420458D649228E54D9809AF62627"> <code> "INSERT-SECURE-TRACKING-SERVER-HERE"</code> - (ssl이 활성화되어 있을 경우 필수) Analytics 보안 추적 서버. </li> 
     </ul> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step3_icon.png" id="image_76B61DEABE3849CCB39135FDD7399EAA" /> </td> 
   <td colname="col1"> <code>AppMeasurement.js</code>를 업데이트합니다 . </td> 
   <td colname="col2"> <p><a href="../../implement/js-implementation/appmeasure-mjs-pagecode.md#section_4351543F2D6049218E18B48769D471E2" format="dita" scope="local">AppMeasurement.js 코드 예제</a>를 복사해서 <code>AppMeasurement.js</code> 파일 앞부분에 붙여넣습니다. 최소한 다음 변수를 업데이트하십시오. </p> 
    <ul id="ul_62FA640BD2604E589650A92158272615"> 
     <li id="li_54E56B483B3A416EA27D7B540D60E39F"> <code> s.account="INSERT-RSID-HERE" </code> </li> 
     <li id="li_00A958289BB045379B436F13287E03D5"> <code> s.trackingServer="INSERT-TRACKING-SERVER-HERE" </code> </li> 
     <li id="li_C0779ADF780440ED876236AEB1FB5DCC"> <code> s.visitorNamespace = "INSERT-NAMESPACE-HERE" </code> </li> 
     <li id="li_93072B656C134D8C89195B7F2D7D8F05"> <code> s.visitor = Visitor.getInstance("INSERT-MCORG-ID-HERE") </code> </li> 
    </ul> <p> See <a href="https://helpx.adobe.com/analytics/kb/determining-data-center.html" format="https" scope="external"> Correctly populate the trackingServer and trackingServerSecure variable </a> or contact Client Care if you are unsure about any of these values. 이 변수들이 올바로 설정되지 않으면, 구현해도 데이터가 수집되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step4_icon.png" id="image_B255E5EAE7BB43FC946D0E9DFCA83003" /> </td> 
   <td colname="col1"> <code>AppMeasurement.js</code>와 <code>VisitorAPI.js</code>를 호스팅합니다 . </td> 
   <td colname="col2"> <p>코어 JavaScript 파일은 사이트의 모든 페이지에서 액세스할 수 있는 웹 서버에 호스팅되어야 합니다. 다음 단계에서 이 파일에 대한 경로가 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step5_icon.png" id="image_844E896941E2489A943BE10AD710ED36" /> </td> 
   <td colname="col1"> 모든 사이트 페이지에서 <code>AppMeasurement.js</code> 및 <code>VisitorAPI.js</code>를 참조하십시오. </td> 
   <td colname="col2"> <p> 각 페이지의 <code>&lt;head&gt;</code> 또는 &lt;body&gt; 태그에 다음 코드 행을 추가하여 방문자 ID 서비스를 포함하십시오. <code>VisitorAPI.js</code>는 <code>AppMeasurement.js</code> 앞에 포함되어야 합니다. </p> 
    <code class="syntax html">&lt; script language = "javascript" type = "text/javascript" src = "https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/VisitorAPI.js" &gt; &lt;/script &gt; </code>
  <p> 다음 코드 행을 각 페이지의 <code>&lt;head&gt;</code> 또는 <code>&lt;body&gt;</code> 태그에 추가하여 JavaScript용 AppMeasurement를 포함합니다. </p> 
    <code class="syntax html">&lt; script language = "javascript" type = "text/javascript" src = "https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/AppMeasurement.js" &gt; &lt;/script &gt; </code>
  </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step6_icon.png" id="image_1C4293CA98F04EE2ADA69EAB95BDE8B1" /> </td> 
   <td colname="col1"> 페이지 코드를 업데이트하고 배포합니다. </td> 
   <td colname="col2"> <p><a href="../../implement/js-implementation/appmeasure-mjs-pagecode.md#section_042412C29CC249E298F19B2BC2F43CE7" format="dita" scope="local">예제 페이지 코드</a>를 복사해서 추적하려는 각 페이지의 <code>&lt;body&gt;</code> 태그를 연 바로 다음에 붙여넣습니다. 최소한 다음 변수를 업데이트하십시오. </p> 
    <ul id="ul_29200A6E8DA14386BDA242AD8B270FEB"> 
     <li id="li_FB24D2CB9241401A83BD13EE342A7810"> <code> var s=s_gi("INSERT-RSID-HERE") </code> </li> 
     <li id="li_463A35BA06CC4618B4AF17CD7E83AED5"> <code> s.pageName="INSERT-NAME-HERE" // 예: s.pageName=document.title </code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step7_icon.png" id="image_A423CBF386AF4E5986E8CBB6E31CD3E5" /> </td> 
   <td colname="col1"> DigitalPulse Debugger를 사용하여 데이터가 전송되었는지 확인합니다. </td> 
   <td colname="col2"> <p>Add the <a href="../../implement/impl-testing/debugger.md#concept_B26FFE005EDD4E0FACB3117AE3E95AA2" format="dita" scope="local">Adobe Debugger</a> 북마클릿을 설치합니다. 설치가 끝나면 페이지 코드를 배포한 페이지를 불러온 다음 디버거를 엽니다. 디버거가 전송된 수집 데이터에 대한 정보를 표시합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 캐시 {#section_4E2D1D962DF046418134C43CFC49AD4A}

JavaScript 파일은 처음에 로드된 후 방문자의 브라우저에 캐싱되며 일반적으로 세션당 한 번 이상 다운로드되지 않습니다. 이 파일은 사이트의 모든 페이지에서 사용되더라도 각 페이지에서 다운로드되지 않습니다. 대부분의 웹 사이트에서 사용자는 평균적으로 세션당 여러 번 페이지를 보기 때문에 여러 번 사용되는 JavaScript를 이 파일로 전송하면 다운로드되는 전체 데이터가 줄어들 수 있습니다.

## AppMeasurement 압축용 JavaScript {#section_C10BBC84C81C414088F97363D29E021B}

H 코드(JavaScript 1.0용 AppMeasurement는 사전에 압축되어 있음)의 페이지 무게(크기)가 걱정되는 경우에는, GZIP을 사용한 파일 압축을 고려해 보는 것이 좋습니다. GZIP은 모든 주요 브라우저에서 지원되며, JavaScript 압축보다 나은 성능을 제공하여 코어 [!DNL s_code.js] JavaScript 파일을 압축 및 압축 해제할 수 있도록 해줍니다.

다음 링크는 사이트에서 GZIP 기능을 사용하여 [!DNL s_code.js] JavaScript 코드의 압축을 처리할 수 있는 방법을 이해하는 데 도움이 됩니다.

[Apache 모듈 mod_deflate](https://httpd.apache.org/docs/2.0/mod/mod_deflate.html)

[Tomcat 및 Flex로 gzip 압축 활성화](https://www.cubicleman.com/2007/04/06/enabling-gzip-compression-with-tomcat-and-flex/)
