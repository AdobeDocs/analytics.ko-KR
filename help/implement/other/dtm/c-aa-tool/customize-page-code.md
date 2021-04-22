---
description: Analytics를 배포할 때 Dynamic Tag Management의 필드 설명을 사용하여 페이지 코드를 사용자 지정합니다.
keywords: Dynamic Tag Management;페이지 코드 사용자 지정;편집기 열기;실행
solution: Experience Cloud,Analytics,Target
title: 페이지 코드 사용자 지정
uuid: b7cad069-3eb8-4388-b0b0-34f54001e05f
exl-id: 24c2d10d-7985-43b1-b62f-0bb05ebf6fbc
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '110'
ht-degree: 100%

---

# 페이지 코드 사용자 지정

Analytics를 배포할 때 Dynamic Tag Management의 필드 설명을 사용하여 페이지 코드를 사용자 지정합니다.

**[!UICONTROL `Property`]** > **[!UICONTROL 편집 도구]** ![](assets/settings_gear.png) > **[!UICONTROL 페이지 코드 사용자 지정]**

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
   <td colname="col2"> <p><code> s_code</code>에 들어 있는 최종 <code> s.t()</code> 호출 전에 트리거해야 하는 모든 JavaScript API 호출을 삽입할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>실행 </p> </td> 
   <td colname="col2"> <p> <b>UI 설정 전</b>: 인터페이스 설정이 사용자 지정 코드보다 우선합니다 (예를 들어 인터페이스의 설정이 활성화되었을 때 eVar을 재정의하려는 경우). </p> <p> <b>UI 설정 후</b>: 사용자 지정 코드가 인터페이스 설정보다 우선합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
