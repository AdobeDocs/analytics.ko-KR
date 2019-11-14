---
description: Analytics를 배포할 때 링크 추적을 위한 Dynamic Tag Management 필드 설명입니다.
keywords: Dynamic Tag Management;link tracking;enable clickmap;track download links;download extensions;track outbound links;keep url parameters
solution: Experience Cloud,Analytics,Dynamic Tag Management
title: 링크 추적
uuid: 982b744b-5696-4c31-b1d1-410486b0eedd
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 링크 추적

Analytics를 배포할 때 링크 추적을 위한 Dynamic Tag Management 필드 설명입니다.

**[!UICONTROL *`Property`*]** &gt; **[!UICONTROL   ![](assets/settings_gear.png)

편집 도구]** &gt; **[!UICONTROL 링크 추적]**

<table id="table_F23FB0B284E74B66A107B1D69D22A51C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ClickMap 활성화 </td> 
   <td colname="col2"> <p>방문자 클릭 맵 데이터를 모으는지 여부를 결정합니다. </p> <p>Analytics 사용자의 <a href="/help/implement/js-implementation/c-variables/configuration-variables.md"  > s.trackInlineStats</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 다운로드 링크 추적 </td> 
   <td colname="col2"> <p>사이트의 다운로드 가능 파일에 대한 링크를 추적합니다. </p> <p>See <a href="/help/implement/js-implementation/c-variables/configuration-variables.md">Configuration Variables</a>.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 확장 기능 다운로드 </td> 
   <td colname="col2"> <p>나열된 확장자를 가진 파일에 대한 링크가 사이트에 포함된 경우 해당 링크의 URL이 보고에 나타납니다. </p>See <a href="/help/implement/js-implementation/c-variables/configuration-variables.md">Configuration Variables</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 아웃바운드 링크 추적 </td> 
   <td colname="col2"> <p>클릭한 링크가 종료 링크인지 여부를 결정합니다. </p> <p>See <a href="/help/implement/js-implementation/c-variables/configuration-variables.md">Configuration Variables</a>. </p> <p><b>단일 페이지 앱 고려 사항: </b>일부 SPA 웹 사이트의 코딩 방식 때문에 SPA 사이트의 페이지에 대한 내부 연결이 아웃바운드 링크로 보일 수 있습니다. </p> <p>다음 방법 중 하나를 사용해 SPA 사이트에서 유래한 아웃바운드 링크를 추적할 수 있습니다. </p> 
    <ul id="ul_A4179633ED0644C3BA5F548A58CA4EC9"> 
     <li id="li_1959FBF14E42469FA8724B37EB58BC54"> <p>SPA의 아웃바운드 링크를 추적하지 않으려면 <span class="wintitle">추적 안 함</span> 섹션에 항목을 삽입합니다. </p> <p>예: <span class="filepath">https://testsite.com/spa/#</span> </p> <p>이 호스트에 대한 모든 # 링크가 무시됩니다. 다른 호스트에 대한 모든 아웃바운드 링크는 추적됩니다(예: <span class="filepath"></span>https://www.google.com). </p> </li> 
     <li id="li_37DD4D37887243FB928C9C04ACE9D39E"> <p>SPA에서 추적하려는 링크가 있으면 <span class="wintitle">항상 추적</span> 섹션을 사용합니다. </p> <p>예를 들어 <span class="filepath">spa/#/about</span> 페이지가 있으면 <span class="wintitle">항상 추적</span> 섹션에 "about"을 삽입할 수 있습니다. </p> <p>about 페이지는 유일하게 추적되는 아웃바운드 링크이며 페이지의 다른 모든 링크(예: <span class="filepath"></span>https://www.google.com)는 추적되지 않습니다. </p> </li> 
    </ul> <p>이 두 옵션은 상호 배타적인 성격으로 동시에 선택할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> URL 매개 변수 유지 </td> 
   <td colname="col2"> <p>쿼리 문자열을 유지합니다. </p> <p>See <a href="/help/implement/js-implementation/c-variables/configuration-variables.md">Configuration Variables</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>
