---
description: 'null'
seo-description: 'null'
seo-title: 샘플 구현 코드
solution: Analytics
title: 샘플 구현 코드
topic: Activity Map
uuid: 73879252-5 CE 1-42 A 5-AD 0 E-DCEE 73244 B 28
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Sample implementation code{#sample-implementation-code}

## Sample AppMeasurement.js file {#section_CD6E603EB41141E587B71E138FE99F52}

다음은 AppMeasurement 라이브러리 및 Activity Map 모듈이 어떻게 [!DNL AppMeasurement.js] 파일에서 결합되는지에 대한 예입니다.

이 Activity Map 구성에 적절한 코드 섹션은 **굵게** 표시되어 있습니다.

```
<b>// Initialize AppMeasurement 
 var s_account="INSERT-RSID-HERE" 
 var s=s_gi(s_account)</b> 
  
/******** VISITOR ID SERVICE CONFIG - REQUIRES VisitorAPI.js ********/ 
s.visitor=Visitor.getInstance("INSERT-MCORG-ID-HERE") 
  
/************************** CONFIG SECTION **************************/ 
/* You may add or alter any code config here. */ 
/* Link Tracking Config */ 
s.trackDownloadLinks=true 
s.trackExternalLinks=true 
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
changes to how your visitor data is collected. Changes should only be 
made when instructed to do so by your account manager.*/ 
s.trackingServer="INSERT-TRACKING-SERVER-HERE" 
s.trackingServerSecure="INSERT-SECURE-TRACKING-SERVER-HERE" 
  
/************************** PLUGINS SECTION *************************/ 
// copy and paste implementation plug-ins here - See "Implementation Plug-ins" @ 
// https://marketing.adobe.com/resources/help/en_US/sc/implement/impl_plugins.html 
// Plug-ins can then be used in the s_doPlugins(s) function above

<b>/****************************** START Activity Map MODULE *****************************/ 
 //The following module enables ActivityMap tracking in Adobe Analytics. ActivityMap 
  allows you to view data overlays on your links and content to understand how 
  users engage with your web site. If you do not intend to use ActivityMap, you 
  can remove the following block of code from your AppMeasurement.js file. 
  Additional documentation on how to configure Activity Map is available at: 
  https://marketing.adobe.com/resources/help/en_US/analytics/activitymap/getting-started-admins.html 
 */ 
 function AppMeasurement_Module_Activity Map(g){func 
 ... 
 /* END Activity Map MODULE */ 
 </b> 
/* 
 ============== DO NOT ALTER ANYTHING BELOW THIS LINE ! =============== 
 
AppMeasurement for JavaScript version: 1.6 
Copyright 1996-2016 Adobe, Inc. All Rights Reserved 
More info available at https://www.adobe.com/marketing-cloud.html 
*/ 
function AppMeasurement(){var a=this;a.version= 
...
```

