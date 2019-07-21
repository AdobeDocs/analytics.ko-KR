---
description: APL(또는 appendList) 플러그인을 사용하면, 대/소문자를 구분하여 확인 또는 대/소문자를 구분하지 않고 확인 옵션을 사용하여 값이 목록에 있는지 확인함으로써 모든 구분된 목록에 값을 추가할 수 있습니다. APL 플러그인은 몇몇 표준 플러그인에서 참조되며 다양한 상황에서 직접 사용할 수도 있습니다.
keywords: Analytics 구현
seo-description: APL(또는 appendList) 플러그인을 사용하면, 대/소문자를 구분하여 확인 또는 대/소문자를 구분하지 않고 확인 옵션을 사용하여 값이 목록에 있는지 확인함으로써 모든 구분된 목록에 값을 추가할 수 있습니다. APL 플러그인은 몇몇 표준 플러그인에서 참조되며 다양한 상황에서 직접 사용할 수도 있습니다.
seo-title: appendList
solution: Analytics
subtopic: 플러그인
title: appendList
topic: 개발자 및 구현
uuid: e 923 c 86 c-eaa 6-4 e 17-a 3 a 4-0 e 08 af 886674
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# appendList

APL(또는 appendList) 플러그인을 사용하면, 대/소문자를 구분하여 확인 또는 대/소문자를 구분하지 않고 확인 옵션을 사용하여 값이 목록에 있는지 확인함으로써 모든 구분된 목록에 값을 추가할 수 있습니다. APL 플러그인은 몇몇 표준 플러그인에서 참조되며 다양한 상황에서 직접 사용할 수도 있습니다.

이 플러그인은 다음과 같은 경우에 유용합니다.

* 현재 이벤트 변수에 이벤트 추가
* 목록에 있는 값을 복제하지 않고 목록 변수에 값 추가
* 페이지 로직을 기반으로 현재 제품 변수에 제품 추가
* 다음 매개 변수에 값 추가: *`linkTrackVars`* and *`linkTrackEvents`*

**사용 사례 1**

<table id="table_5AAC1D9892CD4E5C9060E119EE4E7DC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>시나리오 </p> </td> 
   <td colname="col2"> <p>이벤트가 복제되지 않도록 하면서 현재 이벤트 변수에 <span class="term"> event 1 </span> 는 현재 이벤트 변수에 대해 중복되지 않습니다. </p> <p>s.events="scCheckout" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>코드 </p> </td> 
   <td colname="col2"> <p>s.events=s.apl(s.events,"event1",",",1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>결과 </p> </td> 
   <td colname="col2"> <p>s.events="scCheckout,event1" </p> </td> 
  </tr> 
 </tbody> 
</table>

**사용 사례 2**

<table id="table_C4356C9AB95948F3929A7B75E07AE9E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>시나리오 </p> </td> 
   <td colname="col2"> <p>값 <span class="term"> history </span> to the list variable <span class="varname"> prop 1 </span>, with <span class="term"> history </span> and <span class="term"> history </span> considered the same value. </p> <p>s.prop1="Science,History" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>코드 </p> </td> 
   <td colname="col2"> <p>s.prop1=s.apl(s.prop1,"history",",",2) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>결과 </p> </td> 
   <td colname="col2"> <p>s.prop1="Science,History" </p> <p> <span class="term"> 기록에 이미 내역이 </span> 있으므로 <span class="term"> 내역이 </span> 추가되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>다음 지침을 따르면 사이트에서 데이터 수집 코드를 수정해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 [!DNL Analytics] 사용 및 구현 경험이 풍부한 개발자가 수행해야만 합니다.

## 구현 {#section_F4C91CA2037F478C9F7B53F357E6A5F0}

다음 단계에 따라 APL 플러그인을 구현합니다.

1. 고객 지원 센터 또는 현재 담당 Adobe 컨설턴트에게 플러그인 코드를 요청합니다.
1. Add call(s) to the API function as needed within the *`s_doPlugins`* function

코드는 사이트에서 다음과 같이 표시됩니다.

```js
/* Plugin Config */ 
 
s.usePlugins=true 
 
function s_doPlugins(s) { 
 
/* Add calls to plugins here */ 
 
s.events=s.apl(s.events,"event1",",",1) 
 
} 
 
s.doPlugins=s_doPlugins
```

**지원되는 브라우저**

이 플러그인을 사용하려면 브라우저가 JavaScript 버전 1.0을 지원해야 합니다.

**플러그인 정보**

<table id="table_7B9EDD616C164D6B8B53558337DF12C2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 플러그인 정보 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>매개 변수 </p> </td> 
   <td colname="col2"> <p>apl((L,v,d,u) </p> <p>L = 소스 목록, 빈 목록 사용 가능 </p> <p> v = 추가할 값 </p> <p> d = 목록 구분 기호 </p> <p> u(선택 사항, 기본값은 0) 고유 값 확인. 0=고유 여부 확인 없이 항상 값을 추가합니다. 1=대/소문자를 구분하지 않고 확인하며 값이 목록에 없는 경우에만 추가합니다. 2=대/소문자를 구분하여 확인하며 값이 목록에 없는 경우에만 추가합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>반환 값 </p> </td> 
   <td colname="col2"> <p>원본 목록, 값이 추가된 경우 추가한 값 포함 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용 예 </p> </td> 
   <td colname="col2"> <p>s.events=s.apl(s.events,"event1",",",1); </p> </td> 
  </tr> 
 </tbody> 
</table>

소스 목록 L은 *`L=""`*. 반환된 값은 빈 목록 또는 값이 하나 있는 목록입니다.

**플러그인 코드**

```js
/******************************************************************** 
 * 
 * Main Plug-in code (should be in Plug-ins section) 
 * 
 *******************************************************************/ 
/* 
 * Plugin Utility: apl v1.1 
 */ 
s.apl=new Function("l","v","d","u","" 
+"var s=this,m=0;if(!l)l='';if(u){var i,n,a=s.split(l,d);for(i=0;i<a." 
+"length;i++){n=a[i];m=m||(u==1?(n==v):(n.toLowerCase()==v.toLowerCas" 
+"e()));}}if(!m)l=l?l+d+v:v;return l"); 
 
/******************************************************************** 
 * 
 * Commented example of how to use this is doPlugins function 
 * 
 *******************************************************************/ 
  
 Not Applicable - Utility function only 
 
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
  
 s.split
```

