---
description: Adobe Analytics 배포의 자동 구성에 대한 FAQ입니다. 자동 구성 방법은 AppMeasurement 코드를 알아서 관리해줍니다.
keywords: 다이내믹 태그 관리; Plugins; 스테이징; 현재 설정에 대한 효과; 개정 내역; 잠재적 위험보고서 세트 ID; 통화 코드; 추적 서버; SSL 추적 서버; 사용자 지정 코드; 라이브러리 관리
seo-description: Adobe Analytics 배포의 자동 구성에 대한 FAQ입니다. 자동 구성 방법은 AppMeasurement 코드를 알아서 관리해줍니다.
seo-title: Adobe Analytics 도구에 대한 FAQ
solution: Marketing Cloud, Analytics, Target, 다이내믹 태그 관리
title: Adobe Analytics 도구에 대한 FAQ
uuid: 8 FCEF 893-E 305-4 A 95-A 033-9066 A 56 B 09 CD
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# Adobe Analytics 도구에 대한 FAQ

Adobe Analytics 배포의 자동 구성에 대한 FAQ입니다. The automatic configuration method manages the [!DNL AppMeasurement] code for you.

<table id="table_A50D00E2C47A473B92DA800FB08FE640"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 질문 </th> 
   <th colname="col2" class="entry"> 답변 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> DTM을 통해 Adobe Analytics를 구현할 때 플러그인을 어디에 추가해야 합니까? </p> </td> 
   <td colname="col2"> <p> DTM을 사용하여 <code>s_code</code>를 수동으로 호스팅하는 경우 일반적인 Adobe Analytics 구현의 경우처럼 호스팅된 <code>s_code</code>와 동일한 편집기에 플러그인을 추가할 수 있습니다. </p> <p>However, it is also an option to place the plugins in the editor within the <span class="term"> Customize Page Code</span> section of the tool settings. 두 가지 구현 방법의 효과는 같습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>새 버전의 도구에서 구성을 변경할 경우 프로덕션에 게시하기 전에 스테이징에서 도구를 테스트할 수 있습니까? </p> </td> 
   <td colname="col2"> <p>예.  </p> <p>모든 변경 사항은 일반적인 경우처럼 프로덕션 환경에 배포하기 전에 스테이징에서 테스트할 수 있습니다. 스테이징에서 문제가 확인되어 게시하지 않기로 선택해도 새 통합이 릴리스되기 전처럼 프로덕션 코드는 계속 작동합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>수동 구성(기존 도구의 기본 설정)에서 자동 구성으로 전환하는 경우 현재 설정이 영향을 받습니까? </p> </td> 
   <td colname="col2"> <p>아니오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>수동 라이브러리 관리에서 [Adobe에서 관리]로 전환하는 경우 현재의 설정이나 코드가 영향을 받습니까? </p> </td> 
   <td colname="col2"> <p>지정한 사용자 코드는 기본 <span class="keyword">AppMeasurement</span> 라이브러리로 덮어쓰여집니다. 코드가 계속 실행될 수 있도록 도구 구성이 끝난 후에 이 코드를 새 <span class="wintitle">사용자 지정 페이지 코드</span> 섹션으로 이동해야 합니다. 이 방법을 사용하면 <span class="keyword">AppMeasurement</span> 라이브러리를 사용자의 사용자 지정 코드와는 별도로 관리(및 업그레이드)할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>새로운 통합이 릴리스될 때 <span class="keyword">Adobe Analytics</span> 도구의 개정 내역이 보존됩니까? </p> </td> 
   <td colname="col2"> <p>예.  </p> </td> 
  </tr> 
 </tbody> 
</table>

See [Add Adobe Analytics Tool](../../../implement/c-implement-with-dtm/c-aa-tool/analytics-dtm.md#concept_FBA6679A0B79490F8296437F11E5E4F8) for configuration information.

## 잠재적인 위험 요소 {#section_201BF9E0EB7D4BC2B72A617543C2030B}

현재 [!DNL Adobe Analytics]를 사용하고 있는 경우 통합이 데이터 수집 문제를 유발할 가능성이 약간 있습니다. 이러한 문제는 릴리스 후에 프로덕션에 라이브러리를 게시하는 경우에만 발생할 수 있습니다. 프로덕션 코드는 게시가 진행될 때까지 그대로 남아 있습니다.

이러한 문제를 방지하려면 다음을 확인하십시오.

* 보고서 세트 ID를 도구에 올바르게 입력해야 합니다.
* 도구의 보고서 세트 ID가 [!DNL AppMeasurement] 코드의 ID와 일치해야 합니다.
* 현재 코드, 문자 세트, 추적 서버 및 SSL 추적 서버 구성 필드가 지원되는 값으로 올바르게 설정되어야 합니다.
* Custom code is defined in [!DNL Library Management].

