---
title: getTimeSinceLastVisit
description: 두 방문 사이의 경과 시간을 측정합니다.
translation-type: tm+mt
source-git-commit: 26f06adbef1608a6e01df3ab1d3ad4ba78abc28f

---


# Adobe 플러그인:getTimeSinceLastVisit

> [!IMPORTANT] Adobe Consulting에서 제공하는 이 플러그인은 Adobe Analytics를 사용하여 더 많은 가치를 창출할 수 있도록 도움을 줍니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `getTimeSinceLastVisit` 플러그인을 사용하면 방문자가 마지막 방문 후 사이트를 다시 방문하는 시간을 추적할 수 있습니다.

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
/* Adobe Consulting Plugin: getTimeSinceLastVisit v1.0 (Requires formatTime and inList plug-ins) */
s.getTimeSinceLastVisit=function(){var s=this,a=new Date,b=a.getTime(),c=s.c_r("s_tslv")||0,d=Math.round((b-c)/1E3);a.setTime(b+63072E6);s.c_w("s_tslv",b,a);return c?1800<d&&s.formatTime?s.formatTime(d):"":"New Visitor"};

/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0, ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
 /******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `getTimeSinceLastVisit` 메서드는 인수를 사용하지 않습니다. 방문자가 마지막으로 사이트를 방문한 이후 경과된 시간(다음 형식으로 버킷됨)을 반환합니다.

* 마지막 방문 이후 30분에서 1시간 사이의 시간이 가장 가까운 30분 벤치마크로 설정됩니다. 예, `"30.5 minutes"`, `"53 minutes"`
* 1시간과 1일 사이의 시간은 가장 가까운 15분 벤치마크로 반올림됩니다. 예, `"2.25 hours"`, `"7.5 hours"`
* 하루 이상의 시간은 가장 가까운 일 벤치마크로 반올림됩니다. 예, `"1 day"`, `"3 days"`, `"9 days"`, `"372 days"`
* 방문자가 이전에 방문한 적이 없거나 경과 시간이 2년 이상인 경우 이 값은 로 `"New Visitor"`설정됩니다.

> [!NOTE] 이 플러그인은 방문의 첫 번째 히트에 대한 값만 반환합니다.

이 플러그인은 현재 시간의 Unix 타임스탬프로 `"s_tslv"` 설정된 퍼스트 파티 쿠키를 만듭니다. 쿠키는 2년 동안 사용하지 않으면 만료됩니다.

## 호출 예

### 예 #1

새 방문자가 사이트를 방문하고 방문의 첫 페이지에서 다음 코드가 실행되는 경우...

```javascript
s.prop1 = s.getTimeSinceLastVisit();
s.linkTrackVars = s.apl(s.linkTrackVars, "prop1") //ensures that prop1 will be included on the first hit of the visit
```

...s.prop1의 값은 &quot;새 방문자&quot;로 설정됩니다.

35분 동안 활동이 없는 후 동일한 도메인에서 동일한 코드가 실행되는 경우 s.prop1의 값은 &quot;35분&quot;으로 설정됩니다.

추가로 사용하지 않는 지 4일 후 동일한 코드가 동일한 도메인에서 실행되는 경우 s.prop1의 값은 &quot;4일&quot;로 설정됩니다.

## 버전 내역

### 1.0(2018년 4월 16일)

* 포인트 릴리스(다시 컴파일된 코드 및 더 작은 크기).
* 플러그인에서 파생된 `getDaysSinceLastVisit` 코드(이제 더 이상 사용되지 않으며 이름이 변경됨).
* 이제 반환 값에 `formatTime` 및 `inList` 플러그인을 사용합니다.
