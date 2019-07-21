---
description: JavaScript 플러그인은 대개 붙여넣는 코드에서 t() 함수가 호출될 때 실행되는 doPlugins 함수에 의해 호출됩니다.
keywords: Analytics 구현
seo-description: JavaScript 플러그인은 대개 붙여넣는 코드에서 t() 함수가 호출될 때 실행되는 doPlugins 함수에 의해 호출됩니다.
seo-title: Doplugins 함수로 플러그인 호출
solution: Analytics
subtopic: 플러그인
title: Doplugins 함수로 플러그인 호출
topic: 개발자 및 구현
uuid: 95 DD 01 DE -8136-4 EC 9-AAC 9-4 A 3 D 5371 B 839
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# Doplugins 함수로 플러그인 호출

JavaScript 플러그인은 대개 붙여넣는 코드에서 t() 함수가 호출될 때 실행되는 doPlugins 함수에 의해 호출됩니다.

Consequently, if you set a variable in the *`doPlugins`* function, you can overwrite a variable you set on the HTML page. *`doPlugins`* 함수가 호출되지 않는 유일한 시간은 [!UICONTROL Useplugins] 변수가'false'로 설정된 경우입니다.

## 코드 예 {#section_6940FD16F2E94753A1C39694D0CF5FBA}

The code example below is what the *`doPlugins`* function looks like in your JavaScript file:

JavaScript용 AppMeasurement:

```js
/* Plugin Config */ 
s.usePlugins=true 
s.doPlugins=function(s) { 
 /* Add calls to plugins here */ 
}
```

H 코드:

```js
/* Plugin Config */ 
s.usePlugins=true 
function s_doPlugins(s) { 
 /* Add calls to plugins here */ 
} 
s.doPlugins=s_doPlugins
```

>[!NOTE]
>
>H 코드 및 이전 버전은 다른 구문을 사용하여 아주 오래된 브라우저 (예: IE 4 및 5) 를 지원합니다.

## Renaming the doPlugins Function {#section_70B7D58E057B48058E25907AB3726725}

The *`doPlugins`* function is typically called *`s_doPlugins`*. In certain circumstances, (usually when more than one version of code may appear on a single page) the *`doPlugins`* function name may be changed. If the standard *`doPlugins`* function needs to be renamed to avoid conflicts, ensure that *`doPlugins`* is assigned the correct function name, as shown in the example below.

```js
/* Plugin Config */ 
s_mc.usePlugins=true 
function s_mc_doPlugins(s_mc) { 
 /* Add calls to plugins here */ 
} 
s_mc.doPlugins=s_mc_doPlugins 
```

## doPlugins 사용 {#section_FA5D901CC5214D54BCD08AB77BED7925}

*`doPlugins`* 이 함수를 사용하면 간단하게 변수에 기본값을 제공하거나 사이트의 페이지에서 [!UICONTROL 쿼리 문자열 매개 변수의] 값을 가져올 수 있습니다. Using *`doPlugins`* is often easier than populating the values in the HTML page because only one file must be updated. JavaScript 파일의 변경이 항상 즉각적인 것은 아닙니다. 사이트를 다시 방문하는 방문자는 캐시된 버전의 JavaScript 파일을 사용하는 경우가 많습니다. 즉, 변경한 후 한 달이 지날 때까지 파일 업데이트가 모든 방문자에게 적용되지 않을 수도 있습니다.

다음 예는 *`doPlugins`* 함수를 사용하여 변수에 대한 기본값을 설정하고 쿼리 문자열의 값을 가져올 수 있는 방법을 보여 줍니다.

```js
/* Plugin Config */ 
s.usePlugins=true 
s.doPlugins=function(s) { 
 /* Add calls to plugins here */ 
 // if prop1 doesn't have a value, set it to "Default Value" 
 if(!s.prop1) 
s.prop1="Default Value" 
 
 // if campaign doesn't have a value, get cid from the query string 
 if(!s.campaign) 
s.campaign=s.getQueryParam('cid'); 
 
// Note: The code to read query parameters is different for  
// Appmeasurement for JavaScript since a plug-in is not required: 
// s.campaign=s.Util.getQueryParam('cid'); 
} 
```

## 설치된 플러그인 {#section_C5494347D85940A78670032199787CD0}

플러그인이 JavaScript 파일에 포함되어 있고 사용할 준비가 되었는지 확인하려면 JavaScript 파일의 [!UICONTROL Plugins Section]을 확인합니다. 다음 예는 [!UICONTROL getQueryParam] 함수를 보여 줍니다.

```js
/************************** PLUGINS SECTION *************************/ 
/* You may insert any plugins you wish to use here.                 */ 
/* 
 * Plugin: getQueryParam 1.3 - Return query string parameter values 
 */ 
s.getQueryParam=new Function("qp","d","" 
+"var s=this,v='',i,t;d=d?d:'';while(qp){i=qp.indexOf(',');i=i<0?qp.l" 
// 
// ... more code below ... 
// 
```

