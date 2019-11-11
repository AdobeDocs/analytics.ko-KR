---
description: Adobe Analytics에서 Dynamic Tag Management를 배포하는 데 사용되는 쿠키 전역 설정에 대한 필드 설명입니다.
keywords: Dynamic Tag Management;쿠키;방문자 ID;방문자 네임스페이스;도메인 기간;fp 도메인 기간;트랜잭션 ID;쿠키 수명
seo-description: Adobe Analytics에서 Dynamic Tag Management를 배포하는 데 사용되는 쿠키 전역 설정에 대한 필드 설명입니다.
seo-title: 쿠키
solution: Experience Cloud,Analytics,Dynamic Tag Management
title: 쿠키
uuid: 9c81ecbb-0f02-4c1a-a5a5-426cdea57f38
translation-type: tm+mt
source-git-commit: 9b946238b48fa4532d136d2f7aa0187fdabd005b

---


# 쿠키

Adobe Analytics에서 [!UICONTROL Dynamic Tag Management]를 배포하는 데 사용되는 쿠키 전역 설정에 대한 필드 설명입니다.

*`Property`* &gt; 편집 도구 &gt;  쿠키

<table id="table_2758C770C91B4025AD74009B360D71F7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 방문자 ID </td> 
   <td colname="col2"> <p>온라인 및 오프라인 시스템 모두에서 고객을 나타내는 고유한 값. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 방문자 네임스페이스 </td> 
   <td colname="col2"> <p>쿠키가 설정된 도메인을 식별하는 변수입니다. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> 도메인 점 수 </td> 
   <td colname="col2"> <p>페이지 URL의 도메인에 있는 점의 수를 파악하여 Analytics 쿠키 <code> s_cc</code> 및 <code> s_sq</code>가 설정되는 도메인. 이 변수는 일부 플러그인에서 플러그인의 쿠키를 설정할 올바른 도메인을 결정할 때 사용하기도 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> FP 도메인 점 수 </td> 
   <td colname="col2"> <p>The <span class="term"> fpCookieDomainPeriods</span> variable is for cookies set by JavaScript (<code> s_sq</code>, <code> s_cc</code>, plug-ins) that are inherently first-party cookies, even if your implementation uses the third-party <span class="filepath"> 2o7.net</span> or <span class="filepath"> omtrdc.net</span> domains. </p> <p><a href="/help/implement/js-implementation/c-variables/configuration-variables.md"  >s.fpCookieDomainPeriods</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 거래 ID </td> 
   <td colname="col2"> <p>오프라인 활동을 일으킨 온라인 거래를 나타내는 고유한 값. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 쿠키 라이프타임 </td> 
   <td colname="col2"> <p>쿠키의 수명을 결정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

