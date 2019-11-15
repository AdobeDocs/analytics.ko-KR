---
description: Adobe Analytics 배포를 위한 Dynamic Tag Management자의 일반 설정에 대한 필드 설명입니다.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;general settings;eu compliance;character set;currency code;tracking server;ssl tracking server
solution: Analytics
title: 일반
topic: Developer and implementation
uuid: 93008719-6fb6-4e39-9a75-c937fe3247b9
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 일반

Adobe Analytics 배포를 위한 DTM의 일반 설정에 대한 필드 설명입니다.

**[!UICONTROL &lt;속성&gt;]** &gt; ![](assets/settings_gear.png) **[!UICONTROL 편집 도구]** &gt; **[!UICONTROL 일반]**

<table id="table_DD8DA303698041D296DD5DB080AF7971"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="keyword">Adobe Analytics</span>에 대한 EU 규정 준수 활성화  </p> </td> 
   <td colname="col2"> <p> EU 개인 정보 쿠키를 기반으로 추적을 활성화 또는 비활성화합니다. </p> <p>페이지가 로드될 때 시스템에서는 <span class="filepath">sat_track</span>이라는 쿠키가 설정되어 있는지(또는 <span class="wintitle">속성 편집</span> 페이지에 지정된 사용자 지정 쿠키 이름) 확인합니다. 다음 정보를 고찰하십시오. </p> 
    <ul id="ul_42A6D728F0BC4FBABB0069EFB66DCB01"> 
     <li id="li_227CB14326344AA3980F20C7EACF2AD2"> <p> 쿠키가 없거나 쿠키가 있어도  <span class="term">true</span> 이외의 값으로 설정되어 있는 경우 이 설정을 활성화하면 도구 로드가 생략됩니다. 이것은 그 도구를 사용하는 규칙의 어떠한 부분도 적용되지 않음을 의미합니다. </p> <p>규칙에 EU 규정 준수 분석이 설정되어 있고 타사 코드가 있고, 쿠키가  <span class="term">false</span>로 설정되어 있어도 타사 코드가 실행됩니다. 하지만 분석 변수는 설정되지 않습니다. </p> </li> 
     <li id="li_1E74E02D7E4646ACA86D862A1D3C6679"> 쿠키가 있지만  <span class="term"> true</span>로 설정되어 있는 경우에는 도구가 정상적으로 로드됩니다. </li> 
    </ul> <p>방문자가 옵트아웃하면 <span class="filepath">sat_track</span>(또는 사용자 지정 이름이 지정된) 쿠키를 <span class="term">false</span>로 설정해야 합니다. 사용자 지정 코드를 사용하여 다음을 완수할 수 있습니다. </p> <p> 
     <code>
       _satellite.setCookie("sat_track",&amp;nbsp;"false"); 
     </code> </p> <p> 방문자가 나중에 옵트인할 수 있도록 하려면 해당 쿠키를 <span class="term">true</span>로 설정하는 메커니즘이 있어야 합니다. </p> <p> 
     <code>
       _satellite.setCookie("sat_track",&amp;nbsp;"true"); 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>문자 집합 </p> </td> 
   <td colname="col2"> <p>사용 가능한 문자 인코딩 집합을 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>통화 코드 </p> </td> 
   <td colname="col2"> <p>선택할 수 있는 지원되는 통화 코드를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>추적 서버 </p> </td> 
   <td colname="col2"> <p>이미지 요청 및 쿠키가 작성되는 도메인. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL 추적 서버 </p> </td> 
   <td colname="col2"> <p>이미지 요청 및 쿠키가 작성되는 도메인. 보안 페이지에 사용됩니다. If 정의되지 않으면 SSL 데이터가 <span class="term"> trackingServer </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>데이터 센터 </p> </td> 
   <td colname="col2"> <p>데이터 수집에 사용되는 Adobe 데이터 센터. </p> </td> 
  </tr> 
 </tbody> 
</table>

