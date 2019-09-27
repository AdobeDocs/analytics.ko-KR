---
description: 사용 가능한 측정 라이브러리 나열
keywords: Analytics 구현;수집;데이터;수집
seo-description: 사용 가능한 측정 라이브러리 나열
seo-title: 추가 라이브러리 개요
solution: Analytics
title: 추가 라이브러리 개요
topic: 개발자 및 구현
uuid: 1ec291f6-07 파섹
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# 추가 라이브러리 개요

사용 가능한 측정 라이브러리 나열

다음 테이블은 모든 가용 플랫폼에서 분석 데이터 수집에 사용할 수 있는 라이브러리를 설명합니다. 자세한 정보는 [분석에서의 데이터 수집](https://marketing.adobe.com/resources/help/en_US/reference/usecase_sending_data_to_sc.html)을 참조하십시오.

<table id="table_B01E5B7E5DEB42A28AB851E640A6F08E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 위치 </th> 
   <th colname="col2" class="entry"> 옵션 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 웹 브라우저 </td> 
   <td colname="col2"> <p>모든 Experience Cloud 고객은 모든 솔루션에 대한 JavaScript 및 HTML 페이지 태그를 웹 사이트로 배포하는 표준인 <a href="https://marketing.adobe.com/resources/help/en_US/dtm/" format="https" scope="external">다이내믹 태그 관리</a>에 액세스할 수 있습니다. </p> <p>JavaScript 및 HTML 측정을 구현하는 다른 방법은 <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/" format="http" scope="external">Analytics 구현 안내서</a>에 설명되어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 웹 서버 </td> 
   <td colname="col2"> <p>웹 서버의 기본 PHP 및 Java 라이브러리를 사용하여 분석 데이터를 보낼 수 있습니다. </p> <p>데이터 삽입 API를 통해 HTTP POST 및 GET을 사용하여 데이터 수집 서버로 XML 데이터를 직접 보낼 수 있고 데이터 소스를 통해 쉼표로 구분된 히트 데이터를 분석으로 직접 보낼 수 있습니다. </p> 
    <ul id="ul_B602F4D6610D46D6BA65F943E5BA296C"> 
     <li id="li_4F0A3CC0E5CD4F5AAEECF60A3D81C737"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/php/oms_sc_appmeasure_php.pdf" format="http" scope="external"> PHP AppMeasurement</a> </li> 
     <li id="li_D2431479035F45F4AB4CE0AF11B4C89C"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/java/oms_sc_appmeasure_java.pdf" format="http" scope="external"> Java AppMeasurement</a> </li> 
     <li id="li_74B5B70A2E7349EE9FB9721442D0C845"> <a href="https://marketing.adobe.com/developer/documentation/data-insertion/c-data-insertion-api" format="https" scope="external"> 데이터 삽입 API</a> </li> 
     <li id="li_45F309B87FFC40DF9EF0F263C3FB416A"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/datasources/" format="http" scope="external"> Data Sources</a> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 모바일 장치 </td> 
   <td colname="col2"> <p>기본 라이브러리는 iOS, Android, Windows Phone 8, Blackberry, Symbian 및 기타 OS용으로 제공됩니다. </p> 
    <ul id="ul_DB6A44A2FF724B5BB36973FDFB8353A5"> 
     <li id="li_2B97BA81591747638D620A23881411F6"> <a href="https://marketing.adobe.com/resources/help/en_US/mobile/ios/" format="http" scope="external"> iOS AppMeasurement 4.x</a>(최신 버전) </li> 
     <li id="li_DDC430E5119542EE8DC42D23EE99C4CC"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/ios/" format="http" scope="external"> iOS AppMeasurement 3.x</a> </li> 
     <li id="li_6323CE2240FD490292B39884BB00559C"> <a href="https://marketing.adobe.com/resources/help/en_US/mobile/android/" format="http" scope="external"> Android AppMeasurement 4.x</a>(최신 버전) </li> 
     <li id="li_AD7A2B3DD96A43FF8DEB003D49A02F5B"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/android/" format="http" scope="external"> Android AppMeasurement 3.x</a> </li> 
     <li id="li_46CB3ED239BC42419C996BFDF33046AE"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/wp8/" format="http" scope="external"> Windows Phone 8 AppMeasurement 3.x</a>(최신 버전) </li> 
     <li id="li_B4B01EDE735B4D6C97AAF468DBB64580"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/dotnet/oms_sc_appmeasure_dotnet.pdf" format="http" scope="external"> Silverlight, .NET, XBOX 및 Windows Phone 7 AppMeasurement</a> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Flash </td> 
   <td colname="col2"> <p>ActionScript를 사용하는 Flash 앱은 데스크탑과 웹에서 측정 가능합니다. </p> <p> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/flash/oms_sc_appmeasure_flash.pdf" format="http" scope="external"> Flash, Flex 및 OSMF AppMeasurement</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 데스크톱 </td> 
   <td colname="col2"> 
    <ul id="ul_44CAE5F5DEA94EAF9743DDB2863E906F"> 
     <li id="li_584B634DF4194FEEA48B8DABFB77454B"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/winrt/" format="http" scope="external"> Windows 8 AppMeasurement 3.x용 WinRT </a>(최신 버전) </li> 
     <li id="li_A3613B71AD2E47CD96C8943117D75B0B"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/osx/" format="http" scope="external"> OS X AppMeasurement 3.x</a>(최신 버전) </li> 
     <li id="li_2FBE124EF9C943E092C1C5FDA5CDDEB8"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/java/oms_sc_appmeasure_java.pdf" format="http" scope="external"> Java AppMeasurement</a> </li> 
     <li id="li_ED11FA429E70488A80C27455401887DF"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/dotnet/oms_sc_appmeasure_dotnet.pdf" format="http" scope="external"> Silverlight, .NET, XBOX 및 Windows Phone 7 AppMeasurement</a> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 비디오 </td> 
   <td colname="col2"> <p>다음 가이드에서 모든 플랫폼에 대한 비디오 측정이 제공됩니다. </p> 
    <ul id="ul_5C56F82F45264F63ABA184C48B27EE18"> 
     <li id="li_140B692CA3BE476BA024C37E7AE4872F"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/hbvideo/" format="http" scope="external"> 하트비트 비디오 측정</a>(최신 버전) </li> 
     <li id="li_021D77CB25A54647A71F4AE7144EE788"> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/video/" format="http" scope="external"> 마일스톤 비디오 측정</a> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

<p class="- topic/p head"> <b class="+ topic/ph hi-d/b ">REST 및 SOAP 웹 서비스</b>(<a href="https://marketing.adobe.com/developer/" format="https" scope="external">개발자 연결</a>에서) </p>

* [시작하기](https://marketing.adobe.com/developer/get-started/introduction/c-introduction)
* [API 문서 홈](https://marketing.adobe.com/developer/documentation)

