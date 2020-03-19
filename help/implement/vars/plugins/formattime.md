---
title: formatTime
description: 초 단위의 시간을 분, 시간 등으로 변환할 수 있습니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:formatTime

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `formatTime` 플러그인을 사용하면 원하는 벤치마크 값으로 반올림하여 단 몇 초 만에 버킷 형식으로 표시할 수 있습니다. 시간 값을 초 단위로 캡처하여 버킷 형식(예: 분, 일 또는 주)으로 변환하려는 경우 이 플러그인을 사용하는 것이 좋습니다. 두 번째 기반 값을 시간 반올림된 형식으로 버킷하지 않으려는 경우 이 플러그인은 불필요합니다.

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
   * 작업 유형:형식 초기화 시간
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
/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0, ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `formatTime` 메서드는 다음 인수를 사용합니다.

* **`ns`** (필수, 정수):변환 또는 서식을 지정할 시간(초)
* **`tf`** (선택 사항, 문자열):초를 반환하는 형식 유형;기본값(초)
   * 시간(일)을 원하는 `"d"` 경우(기본적으로 가장 가까운 1/4일 벤치마크로 반올림됨)
   * 시간 단위(기본적으로 가장 가까운 1/4시간 벤치마크로 반올림됨)를 원하는 `"h"` 경우 설정합니다.
   * 시간을 분 단위로 원하는 `"m"` 경우 설정(기본적으로 가장 가까운 1/2분 벤치마크로 반올림됨)
   * 시간을 초 단위로 원하는 `"s"` 경우(기본적으로 가장 가까운 5초 벤치마크로 반올림됨)
* **`bml`** (선택 사항, 숫자):라운딩 벤치마크 길이입니다. 인수에 나열된 벤치마크 기본값 `tf`

이 메서드는 `tf` 인수에 지정한 단위를 사용하여 형식이 지정된 초 수를 반환합니다. 인수가 설정되지 않은 `tf` 경우:

* 1분 미만의 모든 항목은 가장 가까운 5초 벤치마크로 반올림됩니다.
* 1분에서 1시간 사이의 모든 것은 가장 가까운 1/2분 벤치마크로 반올림됩니다
* 1시간 및 1일 사이의 모든 것은 가장 가까운 15분 벤치마크로 반올림됩니다
* 하루 이상 모든 것이 가장 가까운 일 벤치마크로 반올림됩니다.

## 예

### 예 #1

다음 코드...

```js
s.eVar1 = s.formatTime(38242);
```

...s.eVar1이 &quot;10.5시간&quot;으로 설정됩니다.

전달된 인수(38242초)는 10시간 37분 22초와 같습니다.  이 호출에서 tf 인수가 설정되지 않고 전달된 시간(초)이 1시간에서 하루 사이이기 때문에 플러그인은 가장 가까운 15분 벤치마크로 변환된 초 수를 반환합니다.

### 예 #2

다음 코드...

```js
s.eVar1 = s.formatTime(38250);
```

...s.eVar1을 &quot;10.75시간&quot;으로 설정합니다. 전달된 인수(38250초)는 10시간, 37분 및 30초와 같습니다.  이 경우 가장 가까운 4/4시간 벤치마크로 전달된 초 수를 반올림하면 최종 값이 10.75시간으로 설정됩니다

### 예 #3

다음 코드...

```js
s.eVar1 = s.formatTime(38242, "m");
```

...s.eVar1이 &quot;637.5분&quot;으로 설정됩니다.

이 경우, &quot;m&quot; 인수는 플러그인을 강제로 사용하여 초 단위를 가장 가까운 1/2분 벤치마크로 변환합니다

### 예 #4

다음 코드...

```js
s.eVar1 = s.formatTime(38242, "m", 20);
```

...s.eVar1이 &quot;640분&quot;으로 설정됩니다.

tf 인수 값(&quot;m&quot;)은 플러그인을 강제로 사용하여 초를 분으로 변환하지만 bml 인수 값(20)은 플러그인이 분초를 가장 가까운 20분 벤치마크로 변환하도록 합니다.

### 예 #5

다음 코드...

```js
s.eVar1 = s.formatTime(125, "s", 2);
```

...s.eVar1은 &quot;126초&quot;와 같게 설정되며, 이는 125초와 가장 가까운 2초 벤치마크입니다.

### 예 #6

다음 코드...

```js
s.eVar1 = s.formatTime(125, "m", 3);
```

...s.eVar1은 &quot;3분&quot;과 같게 설정되며, 이는 125초로 가장 가까운 3분 벤치마크입니다

### 예 #7

다음 코드...

```js
s.eVar1 = s.formatTime(145, "m", .4);
```

...는 s.eVar1을 &quot;2.4분&quot;과 같게 설정합니다. 이 시간은 가장 가까운 2/5분 벤치마크(예:.4 = 2/5) - 145초

## 버전 내역

### 1.1(2018년 5월 21일)

* 라운딩에 더 많은 유연성을 허용하도록 `bml` 인수를 추가했습니다.

### 1.0(2018년 4월 15일)

* 초기 릴리스.
