---
title: getTimeSinceLastVisit
description: 두 방문 사이의 경과 시간을 측정합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe 플러그인: getTimeSinceLastVisit

>[!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getTimeSinceLastVisit` 플러그인을 사용하면 방문자가 마지막 방문 후 사이트를 다시 방문하는 시간을 추적할 수 있습니다.

## Adobe Experience Platform Launch 확장을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해주는 확장을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. 확장 [!UICONTROL Common Analytics Plugins] 프로그램 설치 및 게시
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨(페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: getTimeSinceLastVisit 초기화
1. 변경 사항을 저장하고 규칙에 게시합니다.

## Launch 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. Go to the [!UICONTROL Extensions] tab, then click the [!UICONTROL Configure] button under the Adobe Analytics extension.
1. 단추를 표시하는 [!UICONTROL Configure tracking using custom code] 아코디언을 [!UICONTROL Open Editor] 확장합니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여 넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여 넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getTimeSinceLastVisit v1.0 (Requires formatTime and inList plug-ins) */
s.getTimeSinceLastVisit=function(){var s=this,a=new Date,b=a.getTime(),c=s.c_r("s_tslv")||0,d=Math.round((b-c)/1E3);a.setTime(b+63072E6);s.c_w("s_tslv",b,a);return c?1800<d&&s.formatTime?s.formatTime(d):"":"New Visitor"};

/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0, ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
 /******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getTimeSinceLastVisit` 메서드는 인수를 사용하지 않습니다. 이 메서드는 방문자가 마지막으로 사이트를 방문한 이후 경과된 시간을 반환합니다(다음 형식으로 변환됨).

* 마지막 방문 이후 30분에서 1시간 사이의 시간이 가장 가까운 0.5분 벤치마크로 설정됩니다. 예, `"30.5 minutes"`, `"53 minutes"`
* 1시간과 1일 사이의 시간은 가장 가까운 1/4시간 벤치마크로 반올림됩니다. 예, `"2.25 hours"`, `"7.5 hours"`
* 하루보다 큰 시간은 가장 가까운 일 벤치마크로 반올림됩니다. 예, `"1 day"`, `"3 days"`, `"9 days"`, `"372 days"`
* 방문자가 전에 방문한 적이 없거나 경과 시간이 2년을 넘는 경우 이 값은 `"New Visitor"`로 설정됩니다.

>[!NOTE] 이 플러그인은 방문의 첫 번째 히트에 대한 값만 반환합니다.

이 플러그인은 현재 시간의 Unix 타임스탬프로 설정된 `"s_tslv"`라는 자사 쿠키를 만듭니다. 이 쿠키는 2년 동안 활동이 없으면 만료됩니다.

## 호출 예

### 예 #1

완전히 새로운 방문자가 사이트를 방문하고 방문의 첫 페이지에서 다음 코드가 실행되는 경우...

```javascript
s.prop1 = s.getTimeSinceLastVisit();
s.linkTrackVars = s.apl(s.linkTrackVars, "prop1") //ensures that prop1 will be included on the first hit of the visit
```

...s.prop1의 값은 &quot;새 방문자&quot;와 동일하게 설정됩니다.

35분 동안 활동이 없었다가 그후 동일한 도메인에서 동일한 코드가 실행되는 경우 s.prop1의 값은 &quot;35분&quot;과 동일하게 설정됩니다.

4일 동안 더 활동이 없었다가 그후 동일한 도메인에서 동일한 코드가 실행되는 경우 s.prop1의 값은 &quot;4일&quot;과 동일하게 설정됩니다.

## 버전 기록

### 1.0(2018년 4월 16일)

* 포인트 릴리스(다시 컴파일된 코드 및 더 작은 크기).
* `getDaysSinceLastVisit` 플러그인에서 파생된 코드(이제 더 이상 사용되지 않으며 이름이 변경됨).
* 이제 반환 값에 `formatTime` 및 `inList` 플러그인을 사용합니다.
