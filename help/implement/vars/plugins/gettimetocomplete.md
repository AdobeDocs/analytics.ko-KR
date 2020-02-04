---
title: getTimeToComplete
description: 작업을 완료하는 데 걸린 시간을 측정합니다.
translation-type: tm+mt
source-git-commit: 365944140bb1dfc9bc8669ae530c631e8ff1629b

---


# Adobe 플러그인:getTimeToComplete

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

플러그인은 사용자가 사이트에서 프로세스를 완료하는 데 걸리는 시간을 추적합니다. `getTimeToComplete` &quot;시계&quot;는 `start` 작업이 호출될 때 시작되고 `stop` 작업이 호출될 때 종료됩니다. 사이트에서 완료하는 데 시간이 걸리는 워크플로우가 있고 방문자가 완료하는 데 얼마나 많은 시간을 소요하는지 알고 싶은 경우 이 플러그인을 사용하는 것이 좋습니다. 세부기간이 전체 초로만 줄어들기 때문에 사이트의 워크플로우가 짧은 시간(3초 미만)에 걸리는 경우 이 플러그인을 사용할 필요가 없습니다.

## Adobe Experience Platform Launch 익스텐션을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있는 확장 기능을 제공합니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. 원하는 속성을 클릭합니다.
1. [확장] [!UICONTROL 탭으로] 이동한 다음 [카탈로그] [!UICONTROL 단추를 클릭합니다]
1. Common Analytics 플러그인 [!UICONTROL 확장 설치 및] 게시
1. 플러그인을 사용하려는 론치 규칙의 경우 다음 구성으로 작업을 추가합니다.
   * 확장:공통 Analytics 플러그인
   * 작업 유형:AddProductEvar 초기화
1. 규칙 변경 내용을 저장하고 규칙에 게시

## Launch 사용자 정의 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려면 사용자 정의 코드 편집기를 사용할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. 원하는 속성을 클릭합니다.
1. 확장 [!UICONTROL 탭으로 이동한] 다음 Adobe [!UICONTROL Analytics] 확장 프로그램 아래에 있는 구성 단추를 클릭합니다.
1. [편집기 [!UICONTROL 열기]] 단추를 표시하는 사용자 지정 코드 [!UICONTROL 아코디언을 사용하여 추적] 구성을확장합니다.
1. 사용자 정의 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여 넣습니다.
1. Analytics 확장 프로그램에 변경 사항을 저장하고 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣습니다(사용 `s_gi`). 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getTimeToComplete v3.1 (Requires formatTime and inList plug-ins) */
s.getTimeToComplete=function(sos,cn,exp){sos=sos?sos.toLowerCase():"start";if("stop"===sos||"start"===sos){cn=cn?cn:"s_gttc";exp=exp?exp:0;var s=this,d=s.c_r(cn),e=new Date;if("start"===sos&&!d)s.c_w(cn,e.getTime(),exp?new Date(e.getTime()+864E5*exp):0);else if("stop"===sos&&d)return sos=Math.round((e.getTime()-d)/1E3),s.c_w(cn,"",0),s.formatTime(sos)}};

/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0,ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `getTimeToComplete` 메서드는 다음 인수를 사용합니다.

* **`sos`**(선택 사항, 문자열):타이머를 시작할`"start"`시간으로 설정합니다. 타이머를 중지할`"stop"`시간으로 설정합니다. 기본값은`"start"`입니다.
* **`cn`**(선택 사항, 문자열):시작 시간을 저장할 쿠키의 이름입니다. 기본값은`"s_gttc"`입니다.
* **`exp`**(선택 사항, 정수):쿠키(및 타이머)가 만료되는 일 수입니다. 기본값은`0`로, 브라우저 세션의 끝을 나타냅니다.

이 메서드를 호출하면 일, 시간, 분 및/또는 `"start"` 작업과 `"stop"` 작업 사이에 걸린 시간(초)이 포함된 문자열이 반환됩니다.

## 호출 예

### 예 #1

이 호출을 사용하여 방문자가 체크아웃 프로세스를 시작하는 시점과 구매를 수행하는 시기 사이의 시간을 결정합니다.

방문자가 체크아웃을 시작할 때 타이머를 시작합니다.

```js
if(s.events.indexOf("scCheckout") > -1) s.getTimeToComplete("start");
```

방문자가 구매하면 타이머를 중지하고 prop1을 중지 및 시작 사이의 시간 차이로 설정합니다.

```js
if(s.events.indexOf("purchase") > -1) s.prop1 = s.getTimeToComplete("stop");
```

s.prop1은 구매 프로세스를 완료하는 데 필요한 시간을 캡처합니다.

### 예 #2

여러 개의 타이머 실행(다른 프로세스를 측정하기 위해)을 동시에 실행하려면, cn 쿠키 인수를 수동으로 설정해야 합니다.  예를 들어 구매를 완료하는 데 필요한 시간을 측정하려는 경우 다음 코드를 설정합니다.

```javascript
if(s.inList(s.events, "scCheckout")) s.getTimeToComplete("start", "gttcpurchase");
if(s.inList(s.events, "purchase")) s.prop1 = s.getTimeToComplete("start", "gttcpurchase");
```

...그러나 등록 양식을 작성하는 데 필요한 시간을 동시에 측정하려는 경우 다음 코드도 실행해야 합니다.

```js
if(s.inList(s.events, "event1")) s.getTimeToComplete("start", "gttcregister", 7);
if(s.inList(s.events, "event2")) s.prop2 = s.getTimeToComplete("stop", "gttcregister", 7);
```

두 번째 예에서는 event1이 완료되는 데 최대 7일이 걸릴 수 있는 등록 프로세스의 시작을 캡처하기 위한 것으로, event2는 등록 완료를 캡처하기 위한 것입니다.  s.prop2는 등록 프로세스를 완료하는 데 필요한 시간을 캡처합니다.

## 버전 내역

### 3.1(2019년 9월 30일)

* 첫 번째 인수에 &quot;start&quot; 또는 &quot;stop&quot;의 값이 필요한 논리를 추가했습니다.  전달된 다른 모든 값은 플러그인의 실행을 중지합니다.
* 플러그인을 `inList 2.0` 업데이트했습니다 `inList 2.1`.

### 3.0(2018년 8월 23일)

* 플러그인을 `formatTime v1.0` 업데이트했습니다 `formatTime v1.1`.

### 3.0(2018년 4월 17일)

* 포인트 릴리스(다시 컴파일되고 더 작은 코드 크기).
* 사소한 버그가 수정되었습니다.

### 2.0 2016년 6월 21일)

* 플러그인에 대한 종속성을 `p_fo` 제거했습니다.
* H-code 및 AppMeasurement와의 호환성을 추가했습니다.
* 콘솔 로깅을 추가했습니다.
