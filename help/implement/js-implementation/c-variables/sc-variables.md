---
description: Analytics는 분석 데이터 수집을 위한 다양한 변수를 제공합니다. 예를 들어 pageName 변수의 값은 보고되는 웹 페이지의 이름입니다. 이 섹션은 AppMeasurement에서 지원되는 변수를 나열합니다.
keywords: Analytics 구현; Appmeasurement 변수
seo-description: Analytics는 분석 데이터 수집을 위한 다양한 변수를 제공합니다. 예를 들어 pageName 변수의 값은 보고되는 웹 페이지의 이름입니다. 이 섹션은 AppMeasurement에서 지원되는 변수를 나열합니다.
seo-title: 변수 개요
solution: Analytics
subtopic: 변수
title: 변수 개요
topic: 개발자 및 구현
uuid: 067 D 0135-572 A -4 A 44-AF 9 E -445 D 3 C 4 E 9271
translation-type: tm+mt
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# 변수 개요

Analytics는 분석 데이터 수집을 위한 다양한 변수를 제공합니다. 예를 들어 pageName 변수의 값은 보고되는 웹 페이지의 이름입니다. 이 섹션은 AppMeasurement에서 지원되는 변수를 나열합니다.

각 변수가 분석 보고서에 어떻게 표시되는지 보려면 [변수 - 보고서에서 변수의 쓰임](https://marketing.adobe.com/resources/help/en_US/reference/?f=variable_definitions)을 참조하십시오.

<!-- 

<p>The following is for a client issue reported by Gundy on 1/22/16 in an email "Documentation and JavaScript Update Request". This may be a KB issue. Awaiting word from Russ. - Blake </p>

 -->

## 변수를 설정하는 방법 {#section_E52CF9E8FDF74164A1511E0D9D31884D}

AppMeasurement requires that all configuration variables be set before the initial call to the track function, *`t()`*. If configuration variables are set after the call to *`t()`*, unexpected results may occur.

Configuration variables are set inside the *`doPlugins`* function, which is called during the execution of the track function. The specific configuration variable causing this issue is *`trackInlineStats`*, which enables ClickMap data collection. 이 변수는 ClickMap 모듈을 정확히 파악할 수 없는 상태로 두므로, "정의되지 않음"이라는 문자열을 Adobe Analytics 비콘에 추가하여 통화 코드에 영향을 주는 첫 번째 추적 호출이 발생합니다.

이 문제를 해결하려면 모든 구성 변수를 doPlugins 함수의 위로 이동하십시오.

```
/************************** CONFIG SECTION **************************/ 
/* Ensure these variables are correct before deploying */ 
var s_account="[INSERT-REPORT-SUITE-ID-HERE]" 
var s=s_gi(s_account) 
s.trackingServer="[INSERT-TRACKING-SERVER-HERE]" 
s.visitorNamespace="[INSERT-VISITOR-NAMESPACE-HERE]" 
s.charSet="ISO-8859-1" 
s.currencyCode="USD" 
s.trackDownloadLinks=true 
s.trackExternalLinks=true 
s.trackInlineStats=true 
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,doc,pdf,xls" 
s.linkInternalFilters="javascript:,three,two,one,dev16,.,nike" 
s.linkLeaveQueryString=false 
s.linkTrackVars="None" 
s.linkTrackEvents="None" 
s.debugTracking=true 
 
s.usePlugins=true; 
function s_doPlugins(s) { 
    //add your custom plugin code here 
} 
s.doPlugins=s_doPlugins; 
 
/* 
============== DO NOT ALTER ANYTHING BELOW THIS LINE ! =============== 
 
AppMeasurement for JavaScript version: 1.5.3 
Copyright 1996-2016 Adobe, Inc. All Rights Reserved 
More info available at https://www.omniture.com 
*/ 
function AppMeasurement(){var a=this;a.version="1.5.3";var k=window;k.s_c_in||(k.s_c_il=[],k.s_c_in=0);a._il=k.s_c_il;a._in=k.s_c_in;a._il[a._in]=a;k.s_c_in++;a._c="s_c";var q=k.AppMeasurement.zb;q||(q=null);var r=k,n,t;try{for(n=r.parent,t=r.location;n&&n.location&&t&&""+n.location!=""+t&&r.location&&""+n.location!=""+r.location&&n.location.host==t.host;)r=n,n=r.parent}catch(u){}a.ob=function(a){try{console.log(a)}catch(b){}};a.za=function(a){return""+parseInt(a)==""+a};a.replace=function(a,b,d){return!a|| 
0>a.indexOf(b)?a:a.split(b).join(d)};a.escape=function(c){var b,d;if(!c)return c;c=encodeURIComponent(c);for(b=0;7>b;b++)d="+~!*()'".substring(b,b+1),0<=c.indexOf(d)&&(c=a.replace(c,d,"%"+d.charCodeAt(0).toString(16).toUpperCase()));return c};a.unescape=function(c){if(!c)return c;c=0<=c.indexOf("+")?a.replace(c,"+"," "):c;try{return decodeURIComponent(c)}catch(b){}return unescape(c)};a.gb=function(){var c=k.location.hostname,b=a.fpCookieDomainPeriods,d;b||(b=a.cookieDomainPeriods);if(c&&!a.cookieDomain&& 
```

