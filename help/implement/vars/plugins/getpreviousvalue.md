---
title: getPreviousValue
description: 변수에 전달된 마지막 값을 가져옵니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:getPreviousValue

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `getPreviousValue` 플러그인을 사용하면 변수를 이전 히트에 설정된 값으로 설정할 수 있습니다. 구현에 현재 히트에서 원하는 값이 모두 포함된 경우에는 이 플러그인이 필요하지 않습니다.

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
   * 작업 유형:getPreviousValue 초기화
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
/* Adobe Consulting Plugin: getPreviousValue v2.0 */
s.getPreviousValue=function(v,c){var s=this,d;c=c||"s_gpv";var b=new Date;b.setTime(b.getTime()+18E5);s.c_r(c)&&(d=s.c_r(c)); v?s.c_w(c,v,b):s.c_w(c,d,b);return d};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `getPreviousValue` 메서드는 다음 인수를 사용합니다.

* **`v`** (문자열, 필수):다음 이미지 요청으로 전달할 값이 있는 변수입니다. 일반적인 변수는 이전 페이지 값을 `s.pageName` 검색하는 데 사용됩니다.
* **`c`** (문자열, 선택 사항):값을 저장하는 쿠키의 이름입니다.  이 인수를 설정하지 않으면 기본값은 `"s_gpv"`입니다.

이 메서드를 호출하면 쿠키에 포함된 문자열 값이 반환됩니다. 그런 다음 플러그인은 쿠키 만료를 재설정하고 `v` 인수로부터 변수 값을 할당합니다. 쿠키는 활동이 없는 지 30분 후에 만료됩니다.

## 호출 예

### 예 #1

다음 코드...

```js
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
```

* 첫 번째 설정은 s.prop7을 이전 이미지 요청에서 s.pageName으로 전달된 값과 동일하게 설정합니다(즉, &quot;gpv_Page&quot; 쿠키에 저장된 값).
* 그러면 코드는 &quot;gpv_Page&quot; 쿠키를 재설정하여 s.pageName의 현재 값과 같게 합니다.
* 이 코드가 실행될 때 s.pageName이 설정되지 않은 경우 코드는 쿠키의 현재 값에 대한 만료를 재설정합니다

### 예 #2

다음 코드는 s.prop7을 s.pageName에 전달된 마지막 값과 같게 설정하지만, event1이 inList 플러그인을 통해 결정된 대로 s.events 내에 포함된 경우에만 호출이 발생할 때 됩니다.

```js
if(s.inList(s.events,"event1")) s.prop7=s.getPreviousValue(s.pageName,"gpv_Page");
```

### 예 #3

다음 코드는 s.prop7을 s.pageName으로 전달된 마지막 값과 같게 설정하지만 s.pageName이 현재 페이지에서 동시에 설정된 경우에만 해당됩니다.

```js
if(s.pageName) s.prop7=s.getPreviousValue(s.pageName,"gpv_Page");
```

### 예 #4

다음 코드는 s.eVar10을 이전 이미지 요청에서 s.eVar1로 전달된 값과 동일하게 설정합니다.   이전 eVar1 값은 &quot;s_gpv&quot; 쿠키에 포함되어 있었습니다.  그러면 코드는 &quot;s_gpv&quot; 쿠키를 s.eVar1의 현재 값과 동일하게 설정합니다.

```js
s.eVar10 = s.getPreviousValue(s.eVar1)
```

## 가능성 없는 퀴리스

v 인수와 연결된 변수가 새 값으로 설정되고 getPreviousValue 플러그인이 실행되지만 Analytics 서버 호출이 동시에 전송되지 않으면, 새 v 인수 값은 다음에 플러그인이 실행될 때 &quot;이전 값&quot;으로 간주됩니다.
예를 들어 다음 코드가 방문의 첫 페이지에서 실행된다고 가정합니다.

```js
s.pageName="home"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
s.t();
```

이 코드는 pageName 인수가 &quot;home&quot;이고 p7(prop7) 인수가 설정되지 않은 서버 호출을 생성합니다.  그러나 s.getPreviousValue에 대한 호출은 s.pageName(예:&quot;home&quot;)을 클릭합니다.
이제 같은 페이지에서 바로 다음 코드가 실행된다고 가정합니다.

```js
s.pageName="happy value"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
```

s.t() 함수가 이 코드 블록에서 실행되지 않으므로 다른 이미지 요청이 만들어지지 않습니다.  그러나, s.getPreviousValue() 함수 코드가 이 시간에 실행될 때 s.prop7은 s.pageName의 이전 값(예:&quot;home&quot;)을 선택한 다음 s.pageName(예:&quot;gpv_Page&quot; 쿠키의 &quot;happy value&quot;).
방문자가 다른 페이지로 이동하고 이 페이지에서 다음 코드가 실행된다고 가정합니다.

```js
s.pageName="page 2"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
s.t();
```

s.t() 호출 함수가 실행되면, s.pageName=&quot;page 2&quot; 및 s.prop7이 &quot;happy value&quot;인 이미지 요청을 만듭니다. 이 값은 getPreviousValue에 대한 마지막 호출이 수행될 때 s.pageName의 값입니다.   &quot;home&quot;이 s.pageName에 전달된 첫 번째 값이지만 &quot;home&quot;의 s.prop7 값은 실제 이미지 요청에 포함되지 않았습니다.

## 버전 내역

### v2.0(2019년 10월 7일)

* 포인트 릴리스(전체 논리 다시 작성).
