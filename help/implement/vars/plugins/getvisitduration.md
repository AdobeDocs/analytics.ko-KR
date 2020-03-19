---
title: getVisitDuration
description: 지금까지 방문자가 사이트에서 보낸 시간을 추적합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:getVisitDuration

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `getVisitDuration` 플러그인은 방문자가 해당 시점까지 사이트에 있었던 시간(분)을 추적합니다. 사이트에서 최대 해당 시점까지 누적 시간을 추적하거나 활동을 수행하는 데 소요되는 시간을 추적하려면 이 플러그인을 사용하는 것이 좋습니다. 이 플러그인은 이벤트 간의 시간을 추적하지 않습니다.이 기능을 원하는 경우 [`getTimeBetweenEvents`](gettimebetweenevents.md) 플러그인을 사용하십시오.

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
   * 작업 유형:getVisitDuration 초기화
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
/* Adobe Consulting Plugin: getVisitDuration v2.0 */
s.getVisitDuration=function(){var d=new Date,c=d.getTime(),b=this.c_r("s_dur");if(isNaN(b)||18E5<c-b)b=c;var a=c-b;d.setTime(c+18E5); this.c_w("s_dur",b+"",d);if(0===a)return"first hit of visit";a=Math.floor(a/6E4);return 0===a?"less than a minute":1===a?"1 minute": a+" minutes"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `getVisitDuration` 메서드는 인수를 사용하지 않습니다. 다음 값 중 하나를 반환합니다.

* `"first hit of visit"`
* `"less than a minute"`
* `"1 minute"`
* `"[x] minutes"` (여기서 `[x]` 방문자가 사이트에 도착한 후 경과된 시간(분)입니다.

이 플러그인은 방문자가 사이트에 랜딩한 이후 경과된 시간(밀리초)인 퍼스트 파티 쿠키를 만듭니다. `"s_dur"` 쿠키는 활동이 없는 지 30분 후에 만료됩니다.

## 호출 예

### 예 #1

다음 코드...

```js
s.eVar10 = s.getVisitDuration();
```

...은 항상 eVar10을 사이트에 방문한 후 경과된 시간과 같게 설정합니다

### 예 #2

다음 코드...

```js
if(s.inList(s.events, "purchase")) s.eVar10 = s.getVisitDuration();
```

...inList 플러그인을 사용하여 이벤트 변수에 구매 이벤트가 포함되어 있는지 확인합니다.  이 경우, eVar10은 방문자의 방문 시작과 구매 시간 사이의 분 수와 같게 설정됩니다.

### 예 #3

다음 코드...

```js
s.prop10 = s.getVisitDuration();
```

...는 방문자가 사이트에 도착한 이후 경과된 시간(분)과 항상 prop10을 설정합니다.  이 기능은 prop10에 경로 지정이 활성화되어 있는 경우에 유용합니다.  prop10 보고서에 &quot;종료&quot; 지표를 추가하면 방문자가 사이트를 떠나기 전에 몇 분 동안 방문이 소요되었는지에 대한 세부적인 &quot;산포도&quot; 보고서가 표시됩니다.

## 버전 내역

### 2.0(2018년 5월 2일)

* 포인트 릴리스(플러그인의 전체 재분석/다시 작성).
