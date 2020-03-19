---
title: getTimeBetweenEvents
description: 두 이벤트 사이의 시간을 측정합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:getTimeBetweenEvents

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `getTimeBetweenEvents` 플러그인을 사용하면 장바구니 및 사용자 지정 이벤트를 포함하여 두 Analytics 이벤트 간의 시간을 추적할 수 있습니다. 체크아웃 프로세스가 완료되는 데 걸리는 시간 또는 시간을 측정하려는 기타 프로세스를 추적하는 데 유용합니다. 이 플러그인의 소요 시간을 측정하려는 변환 프로세스가 없는 경우 이 플러그인은 불필요합니다.

## Adobe Experience Platform Launch 익스텐션을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있는 확장 기능을 제공합니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. 원하는 속성을 클릭합니다.
1. 탭으로 이동한 다음 [!UICONTROL Extensions] [!UICONTROL Catalog] 단추를 클릭합니다.
1. 확장 [!UICONTROL Common Analytics Plugins] 프로그램 설치 및 게시
1. 아직 설정하지 않은 경우, &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 다음 구성으로 만듭니다.
   * 조건:없음
   * 이벤트:코어 - 라이브러리가 로드됨(페이지 상단)
1. 다음 구성으로 위 규칙에 작업을 추가합니다.
   * 확장:공통 Analytics 플러그인
   * 작업 유형:getTimeBetweenEvents 초기화
1. 변경 내용을 저장하고 규칙에 게시합니다.

## Launch 사용자 정의 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려면 사용자 정의 코드 편집기를 사용할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. 원하는 속성을 클릭합니다.
1. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 확장 프로그램 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
1. 단추를 표시하는 [!UICONTROL Configure tracking using custom code] 아코디언을 [!UICONTROL Open Editor] 확장합니다.
1. 사용자 정의 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여 넣습니다.
1. Analytics 확장 프로그램에 변경 사항을 저장하고 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣습니다(사용 [`s_gi`](../functions/s-gi.md)). 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getTimeBetweenEvents v2.1 (Requires formatTime and inList plug-ins) */
s.getTimeBetweenEvents=function(ste,rt,stp,res,cn,etd,fmt,bml,rte){var s=this;if("string"===typeof ste&&"undefined"!==typeof rt&&"string"===typeof stp&&"undefined"!==typeof res){cn=cn?cn:"s_tbe";etd=isNaN(etd)?1:Number(etd);var f=!1,g=!1,n=!1, p=ste.split(","),q=stp.split(",");rte=rte?rte.split(","):[];for(var h=s.c_r(cn),k,v=new Date,r=v.getTime(),c=new Date,a=0; a<rte.length;++a)s.inList(s.events,rte[a])&&(n=!0);c.setTime(c.getTime()+864E5*etd);for(a=0;a<p.length&&!f&&(f=s.inList(s.events,p[a]),!0!==f);++a);for(a=0;a<q.length&&!g&&(g=s.inList(s.events,q[a]),!0!==g);++a);1===p.length&&1===q.length&&ste===stp&&f&&g?(h&&(k=(r-h)/1E3),s.c_w(cn,r,etd?c:0)):(!f||1!=rt&&h||s.c_w(cn,r,etd?c:0),g&&h&&(k=(v.getTime()-h)/1E3,!0===res&&(n=!0)));!0===n&&(c.setDate( c.getDate()-1),s.c_w(cn,"",c));return k?s.formatTime(k,fmt,bml):""}};

/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0,ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `getTimeBetweenEvents` 메서드는 다음 인수를 사용합니다.

* **`ste`** (필수, 문자열):타이머 이벤트를 시작합니다. &quot;타이머 시작&quot;을 위한 쉼표로 구분된 Analytics 이벤트 문자열.
* **`rt`** (필수, 부울):타이머 다시 시작 옵션. 변수에 시작 타이머 이벤트가 포함될 때마다 타이머를 다시 시작하려는 `true` 경우 으로 `events` 설정합니다. 시작 타이머 이벤트가 표시될 때 타이머가 다시 시작되지 않도록 `false` 설정합니다.
* **`stp`** (필수, 문자열):타이머 이벤트를 중지합니다. &quot;타이머 중지&quot;를 나타내는 쉼표로 구분된 Analytics 이벤트 문자열.
* **`res`** (필수, 부울):타이머 재설정 옵션을 참조하십시오. 타이머가 시작된 이후의 시간을 기록하고 일시 중지 후 타이머를 재설정하려면 `true` 설정합니다. 시간을 기록하되 타이머를 중지하지 않으려면 `false` 설정합니다. 로 설정된 `false`경우 이벤트 변수가 stop 이벤트를 기록한 후에도 타이머가 계속 실행됩니다.
   > [!TIP] 이 인수를 로 설정하면 `false`아래 `rte` 인수를 설정하는 것이 좋습니다.
* **`cn`** (선택 사항, 문자열):첫 번째 이벤트가 저장되는 쿠키 이름입니다. 기본값은 `"s_tbe"`입니다.
* **`etd`** (선택 사항, 정수):쿠키의 만료 시간(일)입니다. 브라우저 세션이 끝날 때 만료되도록 `0` 설정합니다. 설정되지 않은 경우 기본값은 1일입니다.
* **`fmt`** (선택 사항, 문자열):초 수가 반환되는 시간 형식(기본값은 nothing)입니다.
   * `"s"` 초
   * `"m"` 분
   * `"h"` 시간
   * `"d"` 일 수
   * 설정하지 않으면 반환 값의 형식은 다음 규칙을 기반으로 합니다.
      * 1분 미만의 모든 항목은 가장 가까운 5초 벤치마크로 반올림됩니다. 예: 10초, 15초
      * 1분에서 1시간 사이의 모든 것은 가장 가까운 1/2분 벤치마크로 반올림됩니다. 예: 30.5분, 31분
      * 1시간 및 1일 사이의 모든 것은 가장 가까운 15분 벤치마크로 반올림됩니다. 예: 2.25시간, 3.5시간
      * 하루 이상의 모든 것이 가장 가까운 일 벤치마크로 반올림됩니다. 예: 1일, 3일, 9일
* **`bml`** (선택 사항, 숫자):인수 형식에 따른 반올림 벤치마크 `fmt` 길이입니다. 예를 들어 `fmt` 인수가 `"s"` 이고 이 인수가 `2`인 경우 반환 값은 가장 가까운 2초 벤치마크로 반올림됩니다. 인수가 `fmt` 이고 이 인수가 `"m"` `0.5`인 경우 반환 값은 가장 가까운 30분 벤치마크로 반올림됩니다.
* **`rte`** (선택 사항, 문자열):타이머를 제거하거나 삭제하는 Analytics 이벤트의 쉼표로 구분된 문자열. 기본값은 nothing입니다.

이 메서드를 호출하면 시작 타이머 이벤트와 중지 타이머 이벤트 사이의 시간을 원하는 형식으로 나타내는 정수가 반환됩니다.

## 호출 예

### 예 #1

다음 코드...

```js
s.eVar1 = s.getTimeBetweenEvents("event1", true, "event2", true, "", 0, "s", 2, "event3");
```

...는 다음과 같이 동작하도록 구성되어 있습니다.

* s.events에 event1이 들어 있으면 타이머가 시작됩니다.
* s.events에 event1이 포함될 때마다 타이머가 다시 시작됩니다.
* s.events에 event2가 들어 있으면 타이머가 중지됩니다.
* s.events에 event2가 포함될 때마다 타이머가 재설정됩니다(즉, 0초로 이동).
* s.events에 event3 OR 방문자가 브라우저를 닫을 때도 타이머가 재설정됩니다
* event1과 event2 사이의 실제 시간이 기록되면 플러그인은 eVar1을 가장 가까운 2초 벤치마크(예: 0초, 2초, 4초, 10초, 184초 등)로 반올림하는 두 이벤트 사이의 시간(초)과 동일하게 설정합니다.
* 타이머가 시작되기 전에 s.events에 event2가 포함되어 있으면 eVar1은 전혀 설정되지 않습니다.

### 예 #2

다음 코드...

```js
s.eVar1 = s.getTimeBetweenEvents("event1", false, "event2", false, "s_20", 20, "h", 1.5, "event3");
```

...는 다음과 같이 동작하도록 구성되어 있습니다.

* s.events에 event1이 들어 있으면 타이머가 시작됩니다.
* s.events에 event1이 포함될 때마다 타이머가 다시 시작되지 않고 원래 타이머가 계속 실행됩니다
* s.events에 event2가 포함되어 있으면 타이머가 중지되지 않지만, 플러그인은 원래 event1 설정이 기록된 이후의 시간을 기록합니다
* 타이머는 &quot;s_20&quot;이라는 쿠키에 저장됩니다.
* 타이머는 s.events에 event3 OR이 들어 있거나 타이머가 시작된 후 20일이 지난 경우에만 재설정됩니다
* (원래) event1과 event2 사이의 시간이 기록되면 플러그인은 eVar1을 설정하며, 가장 가까운 1/2시간 벤치마크(예: 0 시간, 1.5 시간, 3 시간, 7.5 시간, 478.5 시간 등)로 반올림됩니다.

### 예 #3

다음 코드...

```js
s.eVar1 = s.getTimeBetweenEvents("event1", true, "event2", true);
```

...는 위의 첫 번째 예와 유사한 결과를 생성합니다.그러나 타이머의 최종 길이에 따라 eVar1의 값이 초, 분, 시간 또는 일 단위로 반환됩니다.  또한 타이머는 방문자가 브라우저를 닫을 시간이 아니라 처음 설정된 후 1일 후에 만료됩니다.

## 버전 내역

### 2.1(2018년 5월 26일)

* 새로운 버전의 `formatTime` 플러그인에 대한 변경 사항을 수용합니다.

### 2.0(2018년 4월 6일)

* 플러그인의 전체 재작성/재분석
