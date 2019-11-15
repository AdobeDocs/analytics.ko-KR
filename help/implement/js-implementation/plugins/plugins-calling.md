---
description: JavaScript 플러그인은 대개 붙여넣는 코드에서 t() 함수가 호출될 때 실행되는 doPlugins 함수에 의해 호출됩니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Plug-ins
title: doPlugins 함수를 사용하여 플러그인 호출
topic: Developer and implementation
uuid: 95dd01de-8136-4ec9-aac9-4a3d5371b839
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# doPlugins 함수를 사용하여 플러그인 호출

JavaScript 플러그인은 대개 붙여넣는 코드에서 t() 함수가 호출될 때 실행되는 doPlugins 함수에 의해 호출됩니다.

따라서 *`doPlugins`* 함수에 변수를 설정하면 HTML 페이지에 설정한 변수를 덮어쓸 수 있습니다. *`doPlugins`* 함수는 [!UICONTROL usePlugins] 변수가 'false'로 설정된 경우 호출되지 않습니다.

## 코드 예 {#section_6940FD16F2E94753A1C39694D0CF5FBA}

아래 코드 예는 JavaScript 파일에서 *`doPlugins`* 함수가 어떻게 표시되는지 보여 줍니다.

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

> [!NOTE]H 코드 및 이전 버전은 다양한 구문을 사용하여 아주 오래된 일부 브라우저(IE 4 및 5 등)를 지원합니다.

## doPlugins 함수 이름 바꾸기 {#section_70B7D58E057B48058E25907AB3726725}

일반적으로 *`doPlugins`* 함수를 *`s_doPlugins`*&#x200B;라고 합니다. 상황에 따라(보통 단일 페이지에 두 개 이상의 코드 버전이 표시될 수 있는 경우) *`doPlugins`* 함수 이름이 변경될 수 있습니다. 충돌을 방지하기 위해 표준 *`doPlugins`* 함수 이름을 변경해야 하는 경우 아래 예에 표시된 대로 *`doPlugins`*&#x200B;에 올바른 함수 이름이 지정되는지 확인합니다.

```js
/* Plugin Config */ 
s_mc.usePlugins=true 
function s_mc_doPlugins(s_mc) { 
 /* Add calls to plugins here */ 
} 
s_mc.doPlugins=s_mc_doPlugins 
```

## doPlugins 사용 {#section_FA5D901CC5214D54BCD08AB77BED7925}

*`doPlugins`* 함수를 사용하면 간단하게 변수에 기본값을 제공하거나 사이트의 페이지에 있는 [!UICONTROL 쿼리 문자열 매개 변수]에서 값을 가져올 수 있습니다. *`doPlugins`*&#x200B;를 사용하면 한 파일만 업데이트해야 하므로 종종 HTML 페이지에 값을 채우는 것보다 간편합니다. JavaScript 파일의 변경이 항상 즉각적인 것은 아닙니다. 사이트를 다시 방문하는 방문자는 캐시된 버전의 JavaScript 파일을 사용하는 경우가 많습니다. 즉, 변경한 후 한 달이 지날 때까지 파일 업데이트가 모든 방문자에게 적용되지 않을 수도 있습니다.

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

