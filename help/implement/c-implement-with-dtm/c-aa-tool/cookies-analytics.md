---
description: Adobe Analytics에서 다이내믹 태그 관리를 배포하는 데 사용되는 쿠키 전역 설정에 대한 필드 설명입니다.
keywords: 다이내믹 태그 관리; 쿠키; 방문자 ID; 방문자 네임스페이스; 도메인 기간; FP 도메인 기간; 거래 ID; 쿠키 라이프타임
seo-description: Adobe Analytics에서 다이내믹 태그 관리를 배포하는 데 사용되는 쿠키 전역 설정에 대한 필드 설명입니다.
seo-title: 쿠키
solution: Marketing Cloud, 분석, 다이내믹 태그 관리
title: 쿠키
uuid: 9 c 81 ecbb -0 f 02-4 c 1 a-a 5 a 5-426 cdea 57 f 38
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# 쿠키

Field descriptions for the Cookies global settings used for deploying [!UICONTROL Dynamic Tag Management] in Adobe Analytics.

**[!UICONTROL *`Property`*]** &gt;** [! Uicontrol ![](assets/settings_gear.png)

Edit Tool]** &gt; **[!UICONTROL Cookies]**

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
   <td colname="col2"> <p>페이지 URL의 도메인에 있는 점의 수를 파악하여 Analytics 쿠키 <code>s_cc</code> 및 <code>s_sq</code>가 설정되는 도메인. 이 변수는 일부 플러그인에서 플러그인의 쿠키를 설정할 올바른 도메인을 결정할 때 사용하기도 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> FP 도메인 점 수 </td> 
   <td colname="col2"> <p>the <span class="term"> Fpcookiedomainperiods</span> 변수는 구현에서 타사 2 o 7. net 또는 omtrdc. net 도메인을 사용하는 경우에도 기본적으로 퍼스트 파티 쿠키인 JavaScript 설정 쿠키 (<code> s_ sq</code>, <code> s_ cc</code>, <span class="filepath"> plug-ins)</span> <span class="filepath"> 에 사용됩니다</span> . </p> <p><a href="../../../implement/js-implementation/c-variables/configuration-variables.md#concept_8FCA630706334F54B4DCB607378BCD00" format="dita" scope="local"> s. fpcookiedomainperiods</a>를 참조하십시오. </p> </td> 
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

