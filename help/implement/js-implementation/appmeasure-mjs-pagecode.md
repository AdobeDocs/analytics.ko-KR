---
description: 이 섹션은 사이트의 페이지와 핵심 JavaScript 파일에 대한 예제 코드를 포함합니다.
keywords: Analytics 구현;appmeasurement.js 코드;예제 페이지 코드
seo-description: 이 섹션은 사이트의 페이지와 핵심 JavaScript 파일에 대한 예제 코드를 포함합니다.
seo-title: 페이지 코드 및 글로벌 구성 예
solution: Analytics
subtopic: JavaScript AppMeasurement
title: 페이지 코드 및 글로벌 구성 예
topic: 개발자 및 구현
uuid: e8880d77-172b-42e5-8187-ce371aa9eff9
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 페이지 코드 및 글로벌 구성 예

이 섹션은 사이트의 페이지와 핵심 JavaScript 파일에 대한 예제 코드를 포함합니다.

>[!IMPORTANT]
>
>이 예제는 [JavaScript 구현](../../implement/js-implementation/javascript-implementation-overview.md)의 일부로서 배포되는 방문자 ID 서비스를 사용합니다. 모든 사이트 페이지에서 방문자 API JavaScript 파일을 포함하기 전에 AppMeasurement에서 방문자 ID 서비스를 활성화하면 방문자 카운트가 중복될 수 있습니다. 방문자 카운트 중복을 피하려면 방문자 ID 서비스에 설명된 프로세스를 이해하고 [방문자 ID 서비스](../../implement/js-implementation/c-unique-visitors/visid-service.md#concept_230F8759826E47789EA8DEE08FA09B07).

## 예제 AppMeasurement.js 코드 {#section_4351543F2D6049218E18B48769D471E2}

>[!IMPORTANT]
>
>구성 변수는 *`doPlugins`* 함수 위에 설정해야 합니다.

새로운 구현의 경우 다음 글로벌 구성 코드를 AppMeasurement.js의 앞에 붙여넣어 시작할 수 있습니다.

```js
//initialize AppMeasurement 
var s_account="INSERT-RSID-HERE" 
var s=s_gi(s_account) 
 
/******** VISITOR ID SERVICE CONFIG - REQUIRES VisitorAPI.js ********/ 
s.visitor=Visitor.getInstance("INSERT-MCORG-ID-HERE") 
 
/************************** CONFIG SECTION **************************/ 
/* You may add or alter any code config here. */ 
/* Link Tracking Config */ 
s.trackDownloadLinks=true 
s.trackExternalLinks=true 
s.trackInlineStats=true 
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,pdf,doc,docx,xls,xlsx,ppt,pptx" 
s.linkInternalFilters="javascript:" //optional: add your internal domain here 
s.linkLeaveQueryString=false 
s.linkTrackVars="None" 
s.linkTrackEvents="None" 
 
/* uncomment below to use doPlugins */ 
/* s.usePlugins=true 
function s_doPlugins(s) { 
 
// use implementation plug-ins that are defined below 
// in this section. For example, if you copied the append 
// list plug-in code below, you could call: 
// s.events=s.apl(s.events,"event1",",",1); 
 
} 
s.doPlugins=s_doPlugins */ 
 
/* WARNING: Changing any of the below variables will cause drastic 
changes to how your visitor data is collected.  Changes should only be 
made when instructed to do so by your account manager.*/ 
s.trackingServer="INSERT-TRACKING-SERVER-HERE" 
s.trackingServerSecure="INSERT-SECURE-TRACKING-SERVER-HERE" 
 
/************************** PLUGINS SECTION *************************/ 
 
// copy and paste implementation plug-ins here - See "Implementation Plug-ins" @ 
// https://marketing.adobe.com/resources/help/en_US/sc/implement/#Implementation_Plugins 
// Plug-ins can then be used in the s_doPlugins(s) function above  
 
/****************************** MODULES *****************************/ 
 
// copy and paste implementation modules (Media, Integrate) here 
// AppMeasurement_Module_Media.js - Media Module, included in AppMeasurement zip 
// AppMeasurement_Module_Integrate.js - Integrate Module, included in AppMeasurement zip 
 
/* ============== DO NOT ALTER ANYTHING BELOW THIS LINE ! ===============  
```

## 예제 페이지 코드 {#section_042412C29CC249E298F19B2BC2F43CE7}

새 구현에서 다음 페이지 코드를 추적할 페이지의 열기 <body> 태그 바로 다음에 붙여넣을 수 있습니다.

```js
<script language="JavaScript" type="text/javascript"><!-- 
/* You may give each page an identifying name, server, and channel on 
the next lines. */ 
s.pageName="" 
s.server="" 
s.channel="" 
s.pageType="" 
s.prop1="" 
s.prop2="" 
s.prop3="" 
s.prop4="" 
s.prop5="" 
/* Conversion Variables */ 
s.campaign="" 
s.state="" 
s.zip="" 
s.events="" 
s.products="" 
s.purchaseID="" 
s.eVar1="" 
s.eVar2="" 
s.eVar3="" 
s.eVar4="" 
s.eVar5="" 
var s_code=s.t();if(s_code)document.write(s_code)//--></script>
```

각 페이지의 `AppMeasurement.js` 및 `VisitorAPI.js`에도 참조를 포함해야 합니다. 지침에 대해서는 [JavaScript 구현](../../implement/js-implementation/javascript-implementation-overview.md)을 참조하십시오.
