---
description: 사용자 페이지가 브라우저 내에서 활성 탭으로 있던 시간(초)을 기록하고 다음 페이지 보기에서 지표에 그 값을 전달합니다.
keywords: Analytics 구현
seo-description: 사용자 페이지가 브라우저 내에서 활성 탭으로 있던 시간(초)을 기록하고 다음 페이지 보기에서 지표에 그 값을 전달합니다.
seo-title: getPageVisibility
solution: Analytics
title: getPageVisibility
topic: 개발자 및 구현
uuid: 3891 E 2 AA-D 5 C 1-4 A 2 B -8522-EB 2 BAE 39 EA 2 E
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getPageVisibility

사용자 페이지가 브라우저 내에서 활성 탭으로 있던 시간(초)을 기록하고 다음 페이지 보기에서 지표에 그 값을 전달합니다.

>[!NOTE]
>
>이 버전은 플러그인의 베타 버전이며 향후 업데이트될 예정입니다.

This plug-in requires [getVisitStart](../../../implement/js-implementation/plugins/getvisitstart.md#concept_1C3CD25A87094A498A1D8A455963FBD8).

이 플러그인은 브라우저 내에 해당 페이지가 표시되었던 총 초(활성 및 수동 보기 시간 모두)도 기록합니다. 페이지 가시성 이벤트와 연관된 이전 페이지 이름을 추적하려면 getPreviousValue 플러그인을 사용해야 합니다. 이러한 값을 추적하면 사용자 사이트에서 방문자 참여를 더 잘 이해하고 방문자 행동을 더 정확히 추적하는 데 유용합니다.

페이지 가시성 이벤트와 연관된 이전 페이지 이름을 추적하려면 getPreviousValue 플러그인을 사용해야 합니다. 이러한 값을 추적하면 사용자 사이트에서 방문자 참여를 더 잘 이해하고 방문자 행동을 더 정확히 추적하는 데 유용합니다.

>[!NOTE]
>
>다음 지침을 따르면 사이트에서 데이터 수집 코드를 수정해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 Analytics 사용 및 구현 경험이 풍부한 개발자만 수행해야 합니다. This plug-in is compatible only with [!DNL AppMeasurement] tracking libraries.

## 필요한 플러그인 지원 {#section_0CA7624F4A7B4B5F851A4300937887AD}

* appendList
* getPreviousValue
* getVisitStart

## 플러그인 코드 및 구현 {#section_543ABD8B3E6A48A5AFD86CFEDE144696}

**구성 섹션**

`s.pvel` 변수는 사용하려는 다음 이벤트 3개를 포함해야 합니다.

| 이벤트 | 정의 |
|---|---|
| 총 페이지 가시성 초(숫자) | 브라우저 내에서 페이지가 활성 상태였던 시간 |
| 총 페이지 초(숫자) | 가시성 상태와 관계없이 페이지가 브라우저에 로딩된 시간 |
| 총 페이지 가시성 인스턴스(카운터) | 이전 이벤트 2개에 대해 값이 기록된 횟수 |

**샘플 호출**

```
//Page Visibility Event List (total page visibility seconds, total page seconds, total page visibility instances) 
s.pvel='event7,event8,event9' 
```

**doPlugins Section**

플러그인을 초기화하려면 가급적 `doPlugins` 변수를 지정한 후에 s_code의 `s.pageName` 섹션에 두 라인의 코드가 필요합니다.

**샘플 호출**

```
/* Page Visibility */ 
s.eVar9 = s.getPreviousValue(s.pageName,'gpv_v9','');  //Record the previous page name in the designated eVar of your choice 
s.getPageVisibility(); 
```

**플러그인 섹션**

```
/* Page Visibility Plugin 0.1 (BETA) */ 
s.getPageVisibility=new Function("","" 
+"var s=this;if(s.getVisitStart()){s.Util.cookieWrite('s_pvs','');s.U" 
+"til.cookieWrite('s_tps','');}if(s.Util.cookieRead('s_pvs')&&s.pvt<1" 
+"){if(parseInt(s.Util.cookieRead('s_pvs'))<=parseInt(s.Util.cookieRe" 
+"ad('s_tps'))){s.pve=s.pvel.split(',');s.events=s.apl(s.events,s.pve" 
+"[0]+'='+(parseInt(s.Util.cookieRead('s_pvs'))),',',2);s.Util.cookie" 
+"Write('s_pvs','');s.events=s.apl(s.events,s.pve[1]+'='+(parseInt(s." 
+"Util.cookieRead('s_tps'))),',',2);s.Util.cookieWrite('s_tps','');s." 
+"events=s.apl(s.events,s.pve[2],',',2);}}s.pvi=setInterval(s.pvx,100" 
+"0);s.wpvi=setInterval(s.wpvc,5000);"); 
s.gbp=new Function("","" 
+"if('hidden'in document){return null;}var bp=['moz','ms','o','webkit" 
+"'];for(var i=0;i<bp.length;i++){var p=bp[i]+'Hidden';if(p in docume" 
+"nt){return bp[i];}}return null;"); 
s.hp=new Function("p","" 
+"if(p){return p+'Hidden';}else{return'hidden';}"); 
s.vs=new Function("p","" 
+"if(p){return p+'VisibilityState';}else{return'visibilityState';}"); 
s.ve=new Function("p","" 
+"if(p){return p+'visibilitychange';}else{return'visibilitychange';}"); 
s.pvx=new Function("","" 
+"s.pvt+=1;"); 
s.wpvc = function(){var tempDate = Date.now();s.Util.cookieWrite('s_tps', 
Math.ceil((tempDate - s.totalTime)/1000));s.Util.cookieWrite('s_pvs', s.pvt)} 
document.addEventListener('visibilitychange',function(event){if(document.hidden){s.visibility = false;clearTimeout(s.pvi);}else{s.visibility=true;s.pvi=setInterval(s.pvx,1000);}});s.totalTime=new Date();s.pvt=0;s.prefix=s.gbp;s.hidden=s.hp(s.prefix);s.visibility=true;s.visibilityState=s.vs(s.prefix);s.visibilityEvent=s.ve(s.prefix); 
```

## 참고 {#section_47964BB9D0A24BFEB4B2498A41D8B017}

* 프로덕션 환경에 배포하기 전에 항상 플러그인 설치를 테스트하여 데이터 수집이 예상대로 수행되는지 확인하십시오.
* 플러그인은 이전 페이지와 연결되어 페이지 가시성 초 및 총 초를 전달하기 때문에 방문 마지막 페이지 보기에 대한 데이터를 수집하지 않습니다.
* 이 플러그인은 사용자의 웹 브라우저에서 쿠키를 설정하는 기능을 이용합니다. 사용자가 자사 쿠키를 승인하지 않으면 플러그인은 Analytics에 데이터를 전달하지 않습니다.
* The plug-in creates its own first-party cookies named `s_tps` and `s_pvs`.

* 매우 적은 비율의 사용자가 브라우저 한계로 인해 보여진 페이지 비율 데이터를 전달하지 않는데 그 결과 데이터가 왜곡되지 않도록 하기 위해 플러그인 내에 논리가 포함됩니다. 하지만 이 플러그인은 IE, Firefox, Chrome 및 Safari에서 성공적으로 테스트되었습니다.
* 플러그인이 총 초를 측정하고 이전 페이지 이름과 그 값을 연관시키는 방법으로 인해 페이지에서 보낸 기본 시간 지표와 총 초 지표 사이에 차이가 생깁니다.
* [!UICONTROL 계산된 지표를] 만들어 이러한 지표와 연관된 방문자 행동을 요약 및 이해하는 데 도움이 됩니다.

   * ** 페이지 가시성** (총 페이지 가시성 초/총 페이지 초)
   * ** 총 숨겨진 초** (총 페이지 초 - 총 페이지 가시성 초)
   * ** 평균 페이지 가시성 초** (총 페이지 가시성 초/총 페이지 가시성 인스턴스)
   * **평균 페이지 숨겨진 초**((총 페이지 초 - 총 페이지 가시성 초)/총 페이지 가시성 인스턴스)

* 플러그인이 초를 반올림하는 방법으로 인해 총 페이지 가시성 초와 총 초 사이에 1~2초의 차이가 나면서 총 초가 더 높아질 수 있습니다. (향후 업데이트로 해결될 예정).
* getVisitStart 플러그인을 사용하면 30분 이상의 비활성 시간 후 새 방문을 시작하는 방문자를 설명할 수 있습니다. 처음부터 이렇게 작동하도록 설계된 것은 아닙니다. 하지만 플러그인의 향후 반복에서 "총 활성 초"를 포함할 때 문제 해결방법이 될 수도 있습니다.

## FAQ {#section_1ED9391D3BAA4208817F0DF69ABBB25E}

** 이 플러그인은 추가 서버 호출을 제공합니까? **

이 플러그인은 연속된 페이지 보기 서버 호출에 페이지 보기 값만 기록합니다. 결합되어 사용되는 추가 서버 호출은 없습니다.

**총 페이지 초 또는 총 페이지 가시성 인스턴스를 캡처하지 않으려면 이벤트 리스트에서 제거할 수 있습니까? **

예. 총 페이지 초 및 총 가시성 인스턴스는 선택적 이벤트로 원한다면 목록에서 제거할 수 있습니다.

** 이전 페이지 이름 이외의 보고서에서 캡처한 이벤트는 의미가 있습니까? **

이 플러그인이 연속된 이미지 요청 값을 기록하기 때문에 '이전 페이지' 컨텍스트에 캡처된 다른 eVar, 즉 '이전 페이지 URL'만 적용될 수 있습니다.

**플러그인이 s.tl() 호출에 또는 s.t() 호출에만 가시성 시간을 전송합니까?**

가시성 시간은 s.t() 호출로만 기록됩니다.
