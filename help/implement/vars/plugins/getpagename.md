---
title: getPageName
description: 현재 웹 사이트 경로에서 읽기 쉬운 pageName을 만듭니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe 플러그인: getPageName

>[!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getPageName` 플러그인을 사용하면 현재 URL의 읽기 쉽고 친숙한 형식의 버전을 만들 수 있습니다. 보고 시 쉽게 설정하고 이해할 수 있는 [`pageName`](../page-vars/pagename.md) 값을 원하는 경우 이 플러그인을 사용하는 것이 좋습니다. 이 플러그인은 데이터 계층 사용과 같이 `pageName` 변수에 대한 이름 지정 구조를 이미 가지고 있는 경우에는 불필요하고, `pageName` 변수를 설정하는 다른 해결 방법이 없을 때 사용하는 것이 가장 좋습니다.

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
   * 작업 유형: getPageName 초기화
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
/* Adobe Consulting Plugin: getPageName v4.0 */
var getPageName=function(si,qv,hv,de){var c=location.hostname,f=location.pathname.substring(1).split("/"),h=f.length, g=location.search.substring(1).split("&"),l=g.length,k=location.hash.substring(1).split("&"),m=k.length;de=de?de:": ";si=si?si:c;qv= qv?qv:"";hv=hv?hv:"";if(1===h&&""===f[0])si=si+de+"home";else for(c=0;c<h;c++)si=si+de+decodeURIComponent(f[c]); if(qv&&(1!==l||""!== g[0]))for(f=qv.split(","),h=f.length,c=0;c<h;c++)for(qv=0;qv<l;qv++)if(f[c]===g[qv].split("=")[0]){si=si+de+decodeURIComponent(g[qv]);break}if(hv&&(1!==m||""!==k[0]))for(hv=hv.split(","),g=hv.length,c=0;c<g;c++)for(qv=0;qv<m;qv++)if(hv[c]===k[qv].split("=")[0]){si=si+de+decodeURIComponent(k[qv]);break}return si.substring(si.length-de.length)===de?si.substring(0,si.length-de.length):si};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getPageName` 메서드에서는 다음 인수를 사용합니다.

* **`si`** (선택 사항, 문자열): 사이트의 ID를 나타내는 문자열 시작 부분에 삽입되는 ID입니다. 이 값은 숫자 ID나 친숙한 이름일 수 있습니다. 설정하지 않으면 기본값이 현재 도메인으로 설정됩니다.
* **`qv`** (선택 사항, 문자열): 쿼리 문자열 매개 변수의 쉼표로 구분된 목록으로서, URL에 있는 경우에는 문자열에 추가됩니다.
* **`hv`** (선택 사항, 문자열): URL 해시에 있는 매개 변수의 쉼표로 구분된 목록으로서, URL에 있는 경우에는 문자열에 추가됩니다.
* **`de`** (선택 사항, 문자열): 문자열의 개별 부분을 분할하는 구분 기호입니다. 기본값은 파이프(`|`)입니다.

이 메서드는 URL의 친숙한 형식 버전을 포함하는 문자열을 반환합니다. 이 문자열은 일반적으로 `pageName` 변수에 지정되지만 다른 변수에서도 사용할 수 있습니다.

## 호출 예

### 예 #1

현재 URL이...

```js
https://mail.google.com/mail/u/0/#inbox
```

...이고, 다음 코드가 실행되면...

```js
s.pageName = getPageName()
```

...s.pageName의 최종 값은 다음과 같습니다.

```js
s.pageName = "mail.google.com|mail|u|0";
```

### 예 #2

현재 URL이...

```js
https://mail.google.com/mail/u/0/#inbox
```

...이고, 다음 코드가 실행되면...

```js
s.pageName = getPageName("gmail")
```

...s.pageName의 최종 값은 다음과 같습니다.

```js
s.pageName = "gmail|mail|u|0";
```

### 예 #3

현재 URL이...

```js
https://www.google.com/
```

...이고, 다음 코드가 실행되면...

```js
s.pageName = getPageName()
```

...s.pageName의 최종 값은 다음과 같습니다.

```js
s.pageName = "www.google.com|home"
```

**참고**: 경로를 포함하지 않는 URL에서 코드가 실행되면 반환 값의 끝에 항상 &quot;home&quot;이라는 값을 추가합니다.

### 예 #4

현재 URL이...

```js
https://www.google.com/
```

...이고, 다음 코드가 실행되면...

```js
s.pageName = getPageName("google","","","|")
```

...s.pageName의 최종 값은 다음과 같습니다.

```js
s.pageName = "google|home"
```

### 예 #5

현재 URL이...

```js
https://www.hotelrooms.com/en/booking/room-booking.html?cid=1235#/step2&arrive=2018-05-26&depart=2018-05-27&numGuests=2
```

...이고, 다음 코드가 실행되면...

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

getPageName 플러그인의 버전 4.0 이상은 실행할 Adobe Analytics의 AppMeasurement 개체(즉, &quot;s&quot; 개체)의 존재여부에 따라 달라지지 않습니다. 이 버전으로 업그레이드하려는 경우 반드시 호출에서 &quot;s&quot; 개체의 인스턴스를 제거하여 플러그인을 호출하는 코드를 변경하십시오.
예를 들어, 다음 내용을

```js
s.pageName = s.getPageName();
```

다음과 같이 변경하십시오.

```js
s.pageName = getPageName();
```

## 버전 기록

### 4.1(2019년 9월 17일)

* 기본 구분 기호 값을 파이프 문자(원래 콜론 + 공백이었음)로 변경했습니다.

### 4.0(2018년 5월 22일)

* 전체 플러그인 분석/다시 작성
