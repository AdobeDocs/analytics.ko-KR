---
description: Analytics를 배포할 때 Dynamic Tag Management의 필드 설명을 사용하여 페이지 코드를 사용자 지정합니다.
keywords: Dynamic Tag Management;customize page code;open editor;execute
solution: Experience Cloud,Analytics,Target,Dynamic Tag Management
title: 페이지 코드 사용자 지정
uuid: b7cad069-3eb8-4388-b0b0-34f54001e05f
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 페이지 코드 사용자 지정

Analytics를 배포할 때 Dynamic Tag Management의 필드 설명을 사용하여 페이지 코드를 사용자 지정합니다.

Analytics 도구와 동시에 코드가 실행되도록 플러그인을 추가합니다. Analytics 플러그인에 대한 자세한 내용은 [구현 플러그인](/help/implement/js-implementation/plugins/impl-plugins.md).

**[!UICONTROL *`Property`*]** &gt; **[!UICONTROL   ![](assets/settings_gear.png)

편집 도구]** &gt; **[!UICONTROL 페이지 코드 사용자 지정]**

<table id="table_A4676A5FEE814DF9A05DA0E56F8B4C6D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>편집기 열기 </p> </td> 
   <td colname="col2"> <p>You can insert any JavaScript call that must be triggered before the final <code> s.t()</code> call, which is contained in the <code> s_code</code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>실행 </p> </td> 
   <td colname="col2"> <p> <b>UI 설정 전</b>: 인터페이스 설정이 사용자 지정 코드보다 우선합니다(예를 들어 인터페이스의 설정이 활성화되었을 때 eVar을 재정의하려는 경우). </p> <p> <b>UI 설정 후</b>: 사용자 지정 코드가 인터페이스 설정보다 우선합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

