---
description: 지정한 쿼리 문자열 매개 변수가 현재 페이지 URL에 있는 경우 그 값을 반환합니다. 페이지의 쿼리 문자열에서 중요한 데이터(캠페인 추적 코드, 내부 검색 키워드 등)를 사용할 수 있기 때문에 getQueryParam은 Analytics 변수에서 데이터를 캡처하는 데 유용합니다.
keywords: Analytics 구현
seo-description: 지정한 쿼리 문자열 매개 변수가 현재 페이지 URL에 있는 경우 그 값을 반환합니다. 페이지의 쿼리 문자열에서 중요한 데이터(캠페인 추적 코드, 내부 검색 키워드 등)를 사용할 수 있기 때문에 getQueryParam은 Analytics 변수에서 데이터를 캡처하는 데 유용합니다.
seo-title: getQueryParam
solution: Analytics
subtopic: 플러그인
title: getQueryParam
topic: 개발자 및 구현
uuid: BA 202756-C 728-4 EBC -8 FD 9-5 BC 29 A 9 F 673 B
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getQueryParam

지정한 쿼리 문자열 매개 변수가 현재 페이지 URL에 있는 경우 그 값을 반환합니다. 페이지의 쿼리 문자열에서 중요한 데이터(캠페인 추적 코드, 내부 검색 키워드 등)를 사용할 수 있기 때문에 getQueryParam은 Analytics 변수에서 데이터를 캡처하는 데 유용합니다.

>[!IMPORTANT]
>
>이 플러그인은 H 코드에서만 사용됩니다. [JavaScript](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8) 용 appmeasurement는 기본적으로 util. getqueryparam를 사용하여 [이 기능을 제공합니다](../../../implement/js-implementation/util-getqueryparam.md#concept_763AD2621BB44A3990204BE72D3C9FA5).

Once installed in your [!DNL AppMeasurement] for JavaScript code, the plug-in is configured by selecting a [!DNL Analytics] variable to populate using data found in the query string, and specifying which query string values to capture. 플러그인은 지정한 쿼리 문자열이 있는 경우 검색하고 선택한 변수에 값을 채웁니다. 해당 값을 가진 쿼리 문자열 매개 변수가 없으면 빈 문자열이 반환됩니다. If a query string parameter exists but does not have a value (such as param1 in `?param1&param2=value`), the word *`true`* is returned.

>[!NOTE]
>
>The base code for the plug-in must be installed in your [!DNL AppMeasurement] for JavaScript code before the examples below will work.

If you wanted to use *`s.campaign`* to capture campaign tracking codes available as values of the *`cid`* query parameter, you would enter the following in the *`doPlugins()`* function in your [!DNL AppMeasurement] for JavaScript code:

`s.campaign=s.getQueryParam('cid')`

In this example, if the user arrived at a landing page on your site where the URL was [!DNL https://www.yoursite.com/index.html?cid=123456], then *`s.campaign`* would receive a value of *123456*. 이 점은 [!DNL DigitalPulse] 디버거를 사용하여 확인할 수 있습니다. 디버거에서는 이미지 요청의 일부로 *v0=123456*&#x200B;이 표시됩니다.

>[!NOTE]
>
>The parameter *`cid`* and others are used here as examples. 원하는 경우 사이트에 있는 임의의 쿼리 문자열 매개 변수로 바꿀 수 있습니다.

플러그인 *`getQueryParam`*&#x200B;에는 Analytics 변수로 데이터를 캡처하는 데 사용되는 두 개의 추가 인수(옵션)가 있습니다.

```js
s.getQueryParam('p','d','u') 
 
where: 
p = comma-separated list of query parameters to locate (can also be a single value with no comma) 
d = delimiter for list of values (in case more than one specified parameter is found) 
u = where to search for value (e.g., document.referrer); set to current page URL by default
```

*p*&#x200B;가 쿼리 문자열 매개 변수의 목록이고 URL에 쿼리 문자열 매개 변수가 두 개 이상 있는 경우는 목록에서 반환되는 모든 값이 구분 기호 *d*&#x200B;로 구분됩니다. 구분 기호로는 단일 문자나 " : "와 같은 문자열(공백-콜론-공백)을 사용할 수 있습니다. *d*&#x200B;를 생략하면 값 사이에 구분 기호를 사용하지 않습니다. 한 쿼리 문자열 매개 변수의 우선 순위가 다른 매개 변수보다 높은데 둘 모두가 사용된 경우는 아래와 같이 *if*&#x200B;문을 사용합니다.

```js
// cid takes precedence over iid if both exist in the query string 
s.campaign=s.getQueryParam('cid'); 
 if(!s.campaign) 
 s.campaign=s.getQueryParam('iid'); 
```

버전 *`getQueryParam`* v2.0 이상에서 플러그인은 쿼리 문자열 매개 변수를 추출할 URL을 지정하는 세 번째 인수 *u*&#x200B;를 선택 사항으로 승인할 수 있습니다. 기본적으로(즉, 세 번째 인수를 생략하거나 비워 둔 경우), 플러그인은 페이지 URL을 사용합니다. 예를 들어, 참조로부터 쿼리 문자열을 추출하려는 경우는 다음 코드를 사용할 수 있습니다.

```js
// take the query string from the referrer 
 s.eVar1=s.getQueryParam('pid','',document.referrer); 
```

필요한 쿼리 문자열 매개 변수가 현재 프레임의 URL이 아닌 주소 표시줄에 있는 경우 프레임에서 이 세 번째 인수에는 플래그 "f"를 사용해야 합니다.

```js
// take the query string from the parent frame 
 s.eVar1=s.getQueryParam('pid','',f); 
```

프레임과 *f* 매개 변수를 사용하는 경우는 각 페이지 보기마다 캠페인 추적 코드가 전송되지 않도록 *`getValOnce`* 플러그인을 사용해야 합니다.

>[!NOTE]
>
>다음 지침을 따르면 사이트에서 데이터 수집 코드를 수정해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 [!DNL Analytics] 사용 및 구현 경험이 풍부한 개발자가 수행해야만 합니다.

**플러그인 코드**

```js
/******************************************************************** 
 * 
 * Main Plug-in code (should be in Plug-ins section) 
 * 
 *******************************************************************/ 
/* 
 * Plugin: getQueryParam 2.3 
 */ 
s.getQueryParam=new Function("p","d","u","" 
+"var s=this,v='',i,t;d=d?d:'';u=u?u:(s.pageURL?s.pageURL:s.wd.locati" 
+"on);if(u=='f')u=s.gtfs().location;while(p){i=p.indexOf(',');i=i<0?p" 
+".length:i;t=s.p_gpv(p.substring(0,i),u+'');if(t){t=t.indexOf('#')>-" 
+"1?t.substring(0,t.indexOf('#')):t;}if(t)v+=v?d+t:t;p=p.substring(i=" 
+"=p.length?i:i+1)}return v"); 
s.p_gpv=new Function("k","u","" 
+"var s=this,v='',i=u.indexOf('?'),q;if(k&&i>-1){q=u.substring(i+1);v" 
+"=s.pt(q,'&','p_gvf',k)}return v"); 
s.p_gvf=new Function("t","k","" 
+"if(t){var s=this,i=t.indexOf('='),p=i<0?t:t.substring(0,i),v=i<0?'T" 
+"rue':t.substring(i+1);if(p.toLowerCase()==k.toLowerCase())return s." 
+"epa(v)}return ''"); 
 
/******************************************************************** 
 * 
 * Commented example of how to use this is doPlugins function 
 * 
 *******************************************************************/ 
 /* Plugin Example: getQueryParam 2.3 
 //single parameter 
 s.campaign=s.getQueryParam('cid'); 
 
 //multiple parameters 
 s.campaign=s.getQueryParam('cid,sid',':'); 
 
 //non-page URL example 
 s.campaign=s.getQueryParam('cid','',document.referrer); 
 
 //parent frame example 
 s.campaign=s.getQueryParam('cid','','f'); 
 
 */ 
 
/******************************************************************** 
 * 
 * Config variables (should be above doPlugins section) 
 * 
 *******************************************************************/ 
 
 None 
 
/******************************************************************** 
 * 
 * Utility functions that may be shared between plug-ins (name only) 
 * 
 *******************************************************************/ 
  
 None
```

