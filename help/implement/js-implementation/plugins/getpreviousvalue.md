---
description: 다음 페이지 보기의 Analytics 변수 값을 캡처합니다. 예를 들어, 플러그인을 사용하여 이전 페이지 보기에서 s.pageName 값을 사용자 지정 트래픽 변수로 캡처할 수 있습니다. 여기에는 지정된 성공 이벤트가 설정된 경우에만 이전 값을 캡처하는 옵션도 있습니다.
keywords: Analytics 구현
seo-description: 다음 페이지 보기의 Analytics 변수 값을 캡처합니다. 예를 들어, 플러그인을 사용하여 이전 페이지 보기에서 s.pageName 값을 사용자 지정 트래픽 변수로 캡처할 수 있습니다. 여기에는 지정된 성공 이벤트가 설정된 경우에만 이전 값을 캡처하는 옵션도 있습니다.
seo-title: getPreviousValue
solution: Analytics
subtopic: 플러그인
title: getPreviousValue
topic: 개발자 및 구현
uuid: 20 DA 7 B 4 A -9820-4690-A 1 CC-D 10 B 6 DD 627 A 7
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getPreviousValue

다음 페이지 보기의 Analytics 변수 값을 캡처합니다. 예를 들어, 플러그인을 사용하여 이전 페이지 보기에서 s.pageName 값을 사용자 지정 트래픽 변수로 캡처할 수 있습니다. 여기에는 지정된 성공 이벤트가 설정된 경우에만 이전 값을 캡처하는 옵션도 있습니다.

>[!NOTE]
>
>다음 지침을 따르면 사이트에서 데이터 수집 코드를 수정해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 [!DNL Analytics] 사용 및 구현 경험이 풍부한 개발자가 수행해야만 합니다.

## 플러그인 코드 및 구현 {#section_92E94A96A4764113B5588F1B83E3DE2C}

**CONFIG SECTION**: 이 섹션은 변경할 필요가 없습니다.

**플러그인 구성**

다음 코드를 *`s_doPlugins()`* 함수는 Plugin Config 라는 *`s_code.js`* 레이블의 영역에 *있습니다*. 지속되는 값 데이터를 캡처하는 데 사용할 사용자 지정 트래픽(s.prop) 변수 또는 사용자 지정 전환(s.eVar) 변수 하나를 선택합니다. 관리 콘솔을 사용하여 활성화했지만 현재 다른 목적으로 사용하고 있지는 않은 변수여야 합니다. 다음 예를 사용하여 요구 사항에 맞게 업데이트할 수 있습니다.

`s.prop1=s.getPreviousValue(s.pageName,'gpv_pn','event1');`

*`s.getPreviousValue`*&#x200B;에는 세 개의 인수가 있습니다.

1. The variable to be captured from the previous page ( *`s.pageName`* above).
1. The cookie name for use in storing the value for retrieval ( *`gpv_pn`* above).
1. The events that must be set on the page view in order to trigger the retrieval of the previous value ( *`event1`* above). 비워 두거나 생략하면 플러그인은 모든 페이지 보기에서 이전 값을 캡처합니다.

**PLUGINS SECTION**: [!DNL s_code.js] 파일에서 PLUGINS SECTION이라는 레이블이 지정된 영역에 다음 코드를 추가합니다. 플러그인 코드의 이 부분은 어떤 방식으로도 변경하지 마십시오.

```js
/* 
 * Plugin: getPreviousValue_v1.0 - return previous value of designated 
 * variable (requires split utility) 
 */ 
s.getPreviousValue=new Function("v","c","el","" 
+"var s=this,t=new Date,i,j,r='';t.setTime(t.getTime()+1800000);if(el" 
+"){if(s.events){i=s.split(el,',');j=s.split(s.events,',');for(x in i" 
+"){for(y in j){if(i[x]==j[y]){if(s.c_r(c)) r=s.c_r(c);v?s.c_w(c,v,t)" 
+":s.c_w(c,'no value',t);return r}}}}}else{if(s.c_r(c)) r=s.c_r(c);v?" 
+"s.c_w(c,v,t):s.c_w(c,'no value',t);return r}"); 
/* 
 * Utility Function: split v1.5 - split a string (JS 1.0 compatible) 
 */ 
s.split=new Function("l","d","" 
+"var i,x=0,a=new Array;while(l){i=l.indexOf(d);i=i>-1?i:l.length;a[x" 
+"++]=l.substring(0,i);l=l.substring(i+d.length);}return a"); 
```

**참고**

* 프로덕션 환경에 플러그인을 배포하기 전에 항상 플러그인 설치를 종합적으로 테스트하여 데이터 수집이 예상대로 수행되는지 확인하십시오.
* 주어진 페이지의 선택된 변수에 값이 없는 경우는 쿠키에 *no value*&#x200B;라는 텍스트가 설정됩니다.
* 이제 각 쿠키에 대해 30분으로 고정된 쿠키 만료 시간이 설정되며 페이지를 로드할 때마다 갱신됩니다. 플러그인은 방문이 지속되는 동안 작동합니다.
* 함수가 코드 플러그인 섹션의 일부로 호출되어야 하기 때문에 *`s.t()`**`s.tl()`* 또는 호출됩니다.

* 선택한 변수에는 *`s.getPreviousValue`*. *`s_doPlugins()`* 이 함수는 페이지의 변수가 채워지는 후에 실행되므로 이 문제는 거의 발생하지 않습니다. It should only be a matter of concern if the variable used with this plug-in is populated within the *`s_doPlugins()`* function and after the call to *`s.getPreviousValue`*.

