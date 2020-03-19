---
title: getPageName
description: 현재 웹 사이트 경로에서 읽기 쉬운 pageName을 만듭니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:getPageName

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `getPageName` 플러그인을 사용하면 현재 URL의 읽기 쉽고 친숙한 형식 버전을 만들 수 있습니다. 보고 시 손쉽게 설정하고 이해할 수 있는 [`pageName`](../page-vars/pagename.md) 값을 원하는 경우 이 플러그인을 사용하는 것이 좋습니다. 이 플러그인은 이미 데이터 레이어를 통해 하는 것과 같이 `pageName` 변수에 대한 이름 지정 구조를 가지고 있는 경우 불필요합니다. 다른 해결 방법이 없을 때 `pageName` 변수를 설정하는 것이 가장 좋습니다.

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
   * 작업 유형:getPageName 초기화
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
/* Adobe Consulting Plugin: getPageName v4.0 */
var getPageName=function(si,qv,hv,de){var c=location.hostname,f=location.pathname.substring(1).split("/"),h=f.length, g=location.search.substring(1).split("&"),l=g.length,k=location.hash.substring(1).split("&"),m=k.length;de=de?de:": ";si=si?si:c;qv= qv?qv:"";hv=hv?hv:"";if(1===h&&""===f[0])si=si+de+"home";else for(c=0;c<h;c++)si=si+de+decodeURIComponent(f[c]); if(qv&&(1!==l||""!== g[0]))for(f=qv.split(","),h=f.length,c=0;c<h;c++)for(qv=0;qv<l;qv++)if(f[c]===g[qv].split("=")[0]){si=si+de+decodeURIComponent(g[qv]);break}if(hv&&(1!==m||""!==k[0]))for(hv=hv.split(","),g=hv.length,c=0;c<g;c++)for(qv=0;qv<m;qv++)if(hv[c]===k[qv].split("=")[0]){si=si+de+decodeURIComponent(k[qv]);break}return si.substring(si.length-de.length)===de?si.substring(0,si.length-de.length):si};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `getPageName` 메서드는 다음 인수를 사용합니다.

* **`si`** (선택 사항, 문자열):사이트의 ID를 나타내는 문자열 시작 부분에 삽입된 ID입니다. 이 값은 숫자 ID 또는 친숙한 이름일 수 있습니다. 설정하지 않으면 기본적으로 현재 도메인으로 설정됩니다.
* **`qv`** (선택 사항, 문자열):URL에 있는 경우 문자열에 추가되는 쿼리 문자열 매개 변수의 쉼표로 구분된 목록
* **`hv`** (선택 사항, 문자열):URL 해시에 있는 쉼표로 구분된 매개 변수 목록(URL에 있는 경우 문자열에 추가)
* **`de`** (선택 사항, 문자열):문자열의 개별 부분을 분할하는 구분 기호. 기본값은 파이프(`|`)입니다.

이 메서드는 친숙한 형식의 URL 버전을 포함하는 문자열을 반환합니다. 이 문자열은 일반적으로 `pageName` 변수에 지정되지만 다른 변수도 사용할 수 있습니다.

## 호출 예

### 예 #1

현재 URL이

```js
https://mail.google.com/mail/u/0/#inbox
```

...다음 코드가 실행됩니다.

```js
s.pageName = getPageName()
```

...s.pageName의 최종 값은 다음과 같습니다.

```js
s.pageName = "mail.google.com|mail|u|0";
```

### 예 #2

현재 URL이

```js
https://mail.google.com/mail/u/0/#inbox
```

...다음 코드가 실행됩니다.

```js
s.pageName = getPageName("gmail")
```

...s.pageName의 최종 값은 다음과 같습니다.

```js
s.pageName = "gmail|mail|u|0";
```

### 예 #3

현재 URL이

```js
https://www.google.com/
```

...다음 코드가 실행됩니다.

```js
s.pageName = getPageName()
```

...s.pageName의 최종 값은 다음과 같습니다.

```js
s.pageName = "www.google.com|home"
```

**참고**:경로가 없는 URL에서 코드가 실행되면 반환 값의 끝에 항상 &quot;home&quot;의 값을 추가합니다

### 예 #4

현재 URL이

```js
https://www.google.com/
```

...다음 코드가 실행됩니다.

```js
s.pageName = getPageName("google","","","|")
```

...s.pageName의 최종 값은 다음과 같습니다.

```js
s.pageName = "google|home"
```

### 예 #5

현재 URL이

```js
https://www.hotelrooms.com/en/booking/room-booking.html?cid=1235#/step2&arrive=2018-05-26&depart=2018-05-27&numGuests=2
```

...다음 코드가 실행됩니다.

```js
s.pageName = getPageName()
```

...s.pageName의 최종 값은 다음과 같습니다.

```js
s.pageName = "www.hotelrooms.com|en|booking|room-booking.html"
```

그러나 다음 코드가 대신 실행되면...

```js
s.pageName = getPageName("hotelrooms","cid","arrive,numGuests",": ")
```

...s.pageName의 최종 값은 다음과 같습니다.

```js
s.pageName = "hotelrooms: en: booking: room-booking.html: cid=1235: arrive=2018-05-26: numGuests=2"
```

## 이전 버전에서 업그레이드

getPageName 플러그인의 버전 4.0+는 실행할 Adobe Analytics의 AppMeasurement 개체(즉, &quot;s&quot; 개체)의 존재에 종속되지 않습니다.  이 버전으로 업그레이드하려는 경우 호출에서 &quot;s&quot; 개체의 인스턴스를 제거하여 플러그인을 호출하는 코드를 변경해야 합니다.
예를 들어 다음을 변경합니다.

```js
s.pageName = s.getPageName();
```

...to this:

```js
s.pageName = getPageName();
```

## 버전 내역

### 4.1(2019년 9월 17일)

* 기본 구분 기호 값을 파이프 문자(콜론 + 공백)로 변경했습니다.

### 4.0(2018년 5월 22일)

* 전체 플러그인 분석/다시 작성
