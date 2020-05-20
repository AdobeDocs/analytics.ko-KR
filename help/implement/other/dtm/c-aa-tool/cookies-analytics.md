---
description: Adobe Analytics에서 Dynamic Tag Management를 배포하는 데 사용되는 쿠키 전역 설정에 대한 필드 설명입니다.
keywords: Dynamic Tag Management;cookies;visitor id;visitor namespace;domain periods;fp domain periods;transaction id;cookie lifetime
solution: Experience Cloud,Analytics,Dynamic Tag Management
title: 쿠키
uuid: 9c81ecbb-0f02-4c1a-a5a5-426cdea57f38
translation-type: ht
source-git-commit: dfe8409b13fcf67eae6a0c404f83c1209f89ae12

---


# 쿠키

Adobe Analytics에서 [!UICONTROL Dynamic Tag Management]를 배포하는 데 사용되는 쿠키 전역 설정에 대한 필드 설명입니다.

*`Property`* > 편집 도구 > 쿠키

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
   <td colname="col1"> 도메인 마침표 </td> 
   <td colname="col2"> <p>페이지 URL의 도메인에 있는 점의 수를 파악하여 Analytics 쿠키 <code> s_cc</code> 및 <code> s_sq</code>가 설정되는 도메인. 이 변수는 일부 플러그인에서 플러그인의 쿠키를 설정할 올바른 도메인을 결정할 때 사용하기도 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> FP 도메인 마침표 </td> 
   <td colname="col2"> <p><span class="term">fpCookieDomainPeriods</span> 변수는 구현에 타사 <code> s_sq</code> 2o7.net<code> s_cc</code> 또는 <span class="filepath"> omtrdc.net</span> 도메인을 사용하는 경우에도 기본적으로 자사 쿠키인 JavaScript 설정 쿠키(<span class="filepath">, </span>, plug-ins)에 사용됩니다. </p> <p><a href="/help/implement/vars/config-vars/fpcookiedomainperiods.md"  >s.fpCookieDomainPeriods</a>를 참조하십시오. </p> </td> 
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

