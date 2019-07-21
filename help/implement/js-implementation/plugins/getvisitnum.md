---
description: getVisitNum 플러그인은 사용자의 사이트 방문 수를 결정하고 이 값을 Analytics 변수에 캡처합니다.
keywords: Analytics 구현
seo-description: getVisitNum 플러그인은 사용자의 사이트 방문 수를 결정하고 이 값을 Analytics 변수에 캡처합니다.
seo-title: getVisitNum
solution: Analytics
subtopic: 플러그인
title: getVisitNum
topic: 개발자 및 구현
uuid: 27 d 57 f 92-fffb -44 d 0-b 9 ca -9 da 93323 f 64 c
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getVisitNum

getVisitNum 플러그인은 사용자의 사이트 방문 수를 결정하고 이 값을 Analytics 변수에 캡처합니다.

## 플러그인 코드 및 구현 {#section_92E94A96A4764113B5588F1B83E3DE2C}

**CONFIG SECTION**: 이 섹션은 변경할 필요가 없습니다.

**플러그인 구성**

다음 코드를 *`s_doPlugins()`* 함수는 Plugin Config 라는 *`s_code.js`* 레이블의 영역에 *있습니다*. 방문 수 데이터를 캡처하는 데 사용할 사용자 지정 트래픽(s.prop) 변수 또는 사용자 지정 전환(s.eVar) 변수 하나를 선택합니다. 관리 콘솔을 사용하여 활성화했지만 현재 다른 목적으로 사용하고 있지는 않은 변수여야 합니다. 다음 예를 사용하여 요구 사항에 맞게 업데이트할 수 있습니다.

`s.prop1=s.getVisitNum();`

>[!NOTE]
>
>다음 지침을 따르면 사이트에서 데이터 수집 코드를 수정해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 [!DNL Analytics] 사용 및 구현 경험이 풍부한 개발자가 수행해야만 합니다.

**PLUGINS SECTION**: [!DNL s_code.js] 파일에서 PLUGINS SECTION이라는 레이블이 지정된 영역에 다음 코드를 추가합니다. 플러그인 코드의 이 부분은 어떤 방식으로도 변경하지 마십시오.

```js
/* 
* Plugin: getVisitNum - version 3.0 
*/ 
s.getVisitNum=new Function("tp","c","c2","" 
+"var s=this,e=new Date,cval,cvisit,ct=e.getTime(),d;if(!tp){tp='m';}" 
+"if(tp=='m'||tp=='w'||tp=='d'){eo=s.endof(tp),y=eo.getTime();e.setTi" 
+"me(y);}else {d=tp*86400000;e.setTime(ct+d);}if(!c){c='s_vnum';}if(!" 
+"c2){c2='s_invisit';}cval=s.c_r(c);if(cval){var i=cval.indexOf('&vn=" 
+"'),str=cval.substring(i+4,cval.length),k;}cvisit=s.c_r(c2);if(cvisi" 
+"t){if(str){e.setTime(ct+1800000);s.c_w(c2,'true',e);return str;}els" 
+"e {return 'unknown visit number';}}else {if(str){str++;k=cval.substri" 
+"ng(0,i);e.setTime(k);s.c_w(c,k+'&vn='+str,e);e.setTime(ct+1800000);" 
+"s.c_w(c2,'true',e);return str;}else {s.c_w(c,e.getTime()+'&vn=1',e)" 
+";e.setTime(ct+1800000);s.c_w(c2,'true',e);return 1;}}"); 
s.dimo=new Function("m","y","" 
+"var d=new Date(y,m+1,0);return d.getDate();"); 
s.endof=new Function("x","" 
+"var t=new Date;t.setHours(0);t.setMinutes(0);t.setSeconds(0);if(x==" 
+"'m'){d=s.dimo(t.getMonth(),t.getFullYear())-t.getDate()+1;}else if(" 
+"x=='w'){d=7-t.getDay();}else {d=1;}t.setDate(t.getDate()+d);return " 
+"t;");
```

**매개 변수**

* tp = (문자열, 선택 사항) 추적 기간. 일에 "d", 주에 "w", 월에 "m" 또는 사용자 지정 일 수에 번호를 사용합니다.

   * 일, 주 또는 월을 선택한 경우, 일/주/월이 끝날 때 방문 번호가 재설정됩니다.
   * 사용자 지정 일 수를 선택한 경우에는, 방문 번호가 해당 일 수 다음에 재설정됩니다.
   * 값을 제공하지 않으면 "m"이 사용됩니다.

* c = (문자열, 선택 사항) 영구적 쿠키 이름을 지정합니다. 기본값은 's_vnum'입니다.
* c2 = (문자열, 선택 사항) 세션 쿠키 이름을 지정합니다. 기본값은 's_invisit'입니다.

**반환**

* 방문의 방문 번호(1,2,3 등)를 반환합니다. 이 번호는 각 방문의 첫 번째 페이지에서만 증분 처리됩니다.
* 플러그인이 방문 번호를 식별할 수 없을 경우(쿠키가 차단됨) "알 수 없는 방문 번호"를 반환합니다.

**예**

```js
s.prop1=s.getVisitNum(365); //custom length, 365 days. Default cookie names 
s.prop1=s.getVisitNum('w'); //resets weekly 
s.prop1=s.getVisitNum('m','s_vmonthnum','s_monthinvisit'); //resets montly, custom cookie names 
s.prop1=s.getVisitNum('d'); //resets daily
```

**참고**

* 프로덕션 환경에 플러그인을 배포하기 전에 항상 플러그인 설치를 종합적으로 테스트하여 데이터 수집이 예상대로 수행되는지 확인하십시오.
* 이 플러그인은 사용자의 웹 브라우저에서 쿠키를 설정하는 능력을 이용합니다. 사용자가 쿠키를 승인하지 않은 경우는 모든 방문이 첫 번째 방문으로 나타납니다.

