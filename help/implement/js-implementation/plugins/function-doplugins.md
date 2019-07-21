---
description: JavaScript 플러그인은 대개 붙여넣는 코드에서 t() 함수가 호출될 때 실행되는 doPlugins 함수에 의해 호출됩니다.
keywords: Analytics 구현
seo-description: JavaScript 플러그인은 대개 붙여넣는 코드에서 t() 함수가 호출될 때 실행되는 doPlugins 함수에 의해 호출됩니다.
seo-title: doPlugins 함수
solution: Analytics
subtopic: 플러그인
title: doPlugins 함수
topic: 개발자 및 구현
uuid: 367 D 5550-F 8 E 2-477 D -8681-18 AE 9665 D 699
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# doPlugins 함수

JavaScript 플러그인은 대개 붙여넣는 코드에서 t() 함수가 호출될 때 실행되는 doPlugins 함수에 의해 호출됩니다.

따라서 `doPlugins` 함수에 변수를 설정하면 HTML 페이지에 설정한 변수를 덮어쓸 수 있습니다. `doPlugins` 함수가 호출되지 않는 유일한 시간은 *`usePlugins`* 변수가 설정되어 `false`있을 때입니다.

**코드 예**

The `doPlugins` function is typically called `s_doPlugins`. 그러나 상황에 따라(단일 페이지에 두 개 이상의 [!DNL Analytics] 코드 버전이 나타날 수 있는 경우) `doPlugins` 함수의 이름을 변경할 수도 있습니다. 충돌을 방지하기 위해 표준 `doPlugins` 함수의 이름을 변경해야 하는 경우는 아래 예와 같이 `doPlugins`에 올바른 함수 이름을 지정하십시오.

```js
/* Plugin Config */ 
s_mc.usePlugins=true 
function  
<b>s_mc_doPlugins</b>(s_mc) { 
/* Add calls to plugins here */ 
} 
s_mc.doPlugins= 
<b>s_mc_doPlugins</b>
```

**doPlugins 사용**

이 함수를 사용하면 간단하게 변수에 기본값을 제공하거나 사이트의 페이지에 있는 쿼리 문자열 매개 변수에서 값을 가져올 수 있습니다. `doPlugins` 사용하면 한 파일만 업데이트할 수 있으므로 HTML 페이지에 값을 채우는 것보다 간편합니다. JavaScript 파일의 변경 사항이 항상 즉시 적용되는 것은 아닙니다. 사이트를 다시 방문하는 방문자는 캐시된 버전의 JavaScript 파일을 사용하는 경우가 많습니다. 즉, 변경한 후 한 달이 지날 때까지 파일 업데이트가 모든 방문자에게 적용되지 않을 수도 있습니다.

다음 예에서는 `doPlugins` 함수를 사용하여 변수에 기본값을 설정하고 쿼리 문자열에서 값을 가져오는 방법을 보여줍니다.

```js
/* Plugin Config */ 
s.usePlugins=true 
function s_doPlugins(s) { 
/* Add calls to plugins here */ 
// if prop1 doesn't have a value, set it to "Default Value" 
if(!s.prop1) 
s.prop1="Default Value" 
 
// if campaign doesn't have a value, get cid from the query string 
if(!s.campaign) 
s.campaign=getQueryParam('cid'); 
} 
s.doPlugins=s_doPlugins
```

**설치된 플러그인**

플러그인이 JavaScript 파일에 포함되어 있고 사용할 준비가 되었는지 확인하려면 JavaScript 파일의 [!UICONTROL Plugins Section]을 확인합니다. 다음 예에서는 `getQueryParam` 함수가 [!UICONTROL Plugins Section]에서 어떻게 표시되는지 보여줍니다.

```js
/************************** PLUGINS SECTION *************************/ 
 
/* You may insert any plugins you wish to use here. */ 
/* 
* Plugin: getQueryParam 1.3 - Return query string parameter values 
*/ 
s.getQueryParam=new Function("qp","d","" 
+"vars=this,v='',i,t;d=d?d:'';while(qp){i=qp.indexOf(',');i=i<0?qp.l" 
// 
// ... more code below ... 
// 
```

