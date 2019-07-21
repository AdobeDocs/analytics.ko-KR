---
description: 사용 가능한 호스팅 옵션을 한 개 이상 사용하여 다이내믹 태그 관리를 배포할 수 있습니다.
keywords: Analytics 구현; 구현 방법; 다이내믹 태그 관리; DTM; 호스팅; 호스팅 옵션; Akamai; 자체 호스팅; 자체 호스팅; FTP 배달; FTP 호스팅; 라이브러리 다운로드
seo-description: 사용 가능한 호스팅 옵션을 한 개 이상 사용하여 다이내믹 태그 관리를 배포할 수 있습니다.
seo-title: 호스팅 옵션 구성
solution: Analytics
title: 호스팅 옵션 구성
topic: 개발자 및 구현
uuid: 04268 F 2 D-E 76 F -4 FE 4-8 FCC-F 0 DB 3 A 016502
translation-type: tm+mt
source-git-commit: 6250335d05c8e7799802fce26192896a7a6598fe

---


# 호스팅 옵션 구성

You can deploy [!UICONTROL Dynamic Tag Management] using one or more of the available hosting options.

[!UICONTROL 다이내믹 태그 관리에서는 필요한 JavaScript 파일을 호스팅하는 많은 옵션을 제공합니다.]

호스팅에 대한 자세한 내용은 다이내믹 태그 관리 제품 문서에서 [내장 코드 및 호스팅 옵션](https://marketing.adobe.com/resources/help/en_US/dtm/deployment.html)을 참조하십시오.

포함 탭에서 호스팅 옵션을 선택합니다.

<table id="table_229298207DB64838B6F2477DFFAE073F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 호스팅 옵션 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 구현 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Akamai </p> </td> 
   <td colname="col2"> <p> 가장 간단히 구현할 수 있는 호스팅 옵션입니다. </p> <p>글로벌하게 분산된 게재 네트워크입니다. </p> <p>추가적인 타사 인프라 종속성(DNS 조회, Akamai 가용성)을 추가합니다. </p> <p>자세한 내용은 다이내믹 태그 관리 제품 설명서에서 <a href="https://marketing.adobe.com/resources/help/en_US/dtm/akamai.html" format="html" scope="external">Akamai</a>를 참조하십시오. </p> </td> 
   <td colname="col3"> 
    <ol id="ol_EF148EF091A645B3962B084963B3C0B0"> 
     <li id="li_7ECE0C331EEE4907A563D581DF1DFEFE">다이내믹 태그 관리는 사용자 지정 JavaScript 라이브러리를 생성합니다. </li> 
     <li id="li_8E2C858290EF4665B2F45ACAFA121CB3">다이내믹 태그 관리는 사용자 지정 JavaScript 라이브러리를 Akamai로 내보냅니다. </li> 
     <li id="li_CE88B10B6E844A56BBB8C575A9363BA9">타겟 웹 사이트는 Akamai가 호스팅하는 다이내믹 태그 관리 라이브러리를 페이지 수준에서 직접 참조합니다. </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 자체 호스팅: FTP 게재 </td> 
   <td colname="col2"> <p><span class="term"> 푸시</span> 접근 방식입니다. </p> <p>이 솔루션에서는 웹 컨텐츠 서버에서 사용할 수 있는 FTP 서버와 자격 증명이 있어야 사용자 지정 다이내믹 태그 관리 라이브러리의 변경 사항을 게시할 수 있습니다. </p> <p>자세한 내용은 다이내믹 태그 관리 제품 설명서에서 <a href="https://marketing.adobe.com/resources/help/en_US/dtm/deployment_ftp.html" format="html" scope="external">FTP</a>를 참조하십시오. </p> </td> 
   <td colname="col3"> 
    <ol id="ol_60348F9C991D4F2B9457006B0F98C834"> 
     <li id="li_24A141C3C7074BF9897C022A22CAE78C">다이내믹 태그 관리는 사용자 지정 JavaScript 라이브러리를 생성합니다. </li> 
     <li id="li_E1E0843060F7447E853EA416A0B033BE">다이내믹 태그 관리는 FTP를 통해 사용자 지정 JavaScript 라이브러리를 호스트 서버로 내보냅니다. </li> 
     <li id="li_EAF5D2ABD03B4911A0CFA464AD8791CE">타겟 웹 사이트는 사용자 지정 다이내믹 태그 관리 라이브러리를 로컬로 참조합니다. </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 자체 호스팅: 라이브러리 다운로드 </td> 
   <td colname="col2"> <p><span class="term"> 애플리케이션이 사용자 지정 JavaScript 라이브러리를
 내보낼 수 있는 풀</span> 접근 방식입니다 <!-- to Amazon S3-->. 여기에서 라이브러리는 호스팅되는 서버 측 프로세스로 액세스할 수 있습니다. </p> <p>또한 라이브러리는 다이내믹 태그 관리 인터페이스에서 바로 웹 다운로드를 통해 사용할 수 있습니다. </p> <p>이 솔루션에서는 다이내믹 태그 관리 라이브러리를 수동으로 검색하고 게시하거나, Akamai에서 웹 컨텐츠 서버로 라이브러리를 가져오는 자동화된 프로세스를 만들어야 합니다. </p> <p>이 접근 방식은 설정하는 데 시간이 가장 오래 걸리지만 가장 안전하고 유연한 옵션이기도 합니다. </p> <p>최신 버전의 라이브러리 파일을 참조하는지 확인하려면 명령을 사용합니다. </p> <p>자세한 내용은 다이내믹 태그 관리 제품 설명서에서 <a href="https://marketing.adobe.com/resources/help/en_US/dtm/deployment_download.html" format="html" scope="external">라이브러리 다운로드</a>를 참조하십시오. </p> </td> 
   <td colname="col3"> 
    <ol id="ol_F40B721306FE473496BD657262DFD585"> 
     <li id="li_4EA4D6B555CE4E9CA476C7550C18C061">다이내믹 태그 관리는 사용자 지정 JavaScript 라이브러리를 생성합니다. </li> 
     <li id="li_BA40EBD7AD1546F29D8A209034D06477">다이내믹 태그 관리는 사용자 지정 JavaScript 라이브러리를 Akamai로 내보냅니다. </li> 
     <li id="li_E107E69E386A40F3B067F9991C2979AF">사용자 지정 다이내믹 태그 관리 라이브러리는 수동으로 또는 프로그래밍 방식으로 웹 컨텐츠 서버로 이동됩니다. </li> 
     <li id="li_0809038453B544168A20CE09D7E5AC59">타겟 웹 사이트는 사용자 지정 다이내믹 태그 관리 라이브러리를 로컬로 참조합니다. </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

호스팅 옵션을 두 개 이상 사용할 수 있습니다. 예를 들면 Akamai를 사용하여 스테이징된 파일을 호스트할 수 있지만, 프로덕션 사이트를 자체 호스팅할 수 있습니다. 각 호스팅 유형에는 고유한 포함 코드가 있으며, 페이지에는 포함 코드를 한 개만 추가할 수 있습니다.
