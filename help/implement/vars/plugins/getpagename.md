---
title: getPageName
description: 현재 웹 사이트 경로에서 읽기 쉬운 pageName을 만듭니다.
feature: Variables
exl-id: a3aaeb5d-65cd-45c1-88bb-f3c0efaff110
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: ht
source-wordcount: '596'
ht-degree: 100%

---

# Adobe 플러그인: getPageName

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getPageName` 플러그인을 사용하면 현재 URL의 읽기 쉽고 친숙한 형식의 버전을 만들 수 있습니다. 보고 시 쉽게 설정하고 이해할 수 있는 [`pageName`](../page-vars/pagename.md) 값을 원하는 경우 이 플러그인을 사용하는 것이 좋습니다. 이 플러그인은 데이터 계층 사용과 같이 `pageName` 변수에 대한 이름 지정 구조를 이미 가지고 있는 경우에는 불필요하고, `pageName` 변수를 설정하는 다른 해결 방법이 없을 때 사용하는 것이 가장 좋습니다.

## Adobe Experience Platform의 태그를 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해 주는 확장 기능을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [데이터 수집 UI](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그] 버튼을 클릭합니다.
1. [!UICONTROL 일반적인 Analytics 플러그인] 확장 기능을 설치 및 게시합니다.
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨 (페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: getPageName 초기화
1. 변경 사항을 저장하고 규칙에 퍼블리싱합니다.

## 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [데이터 수집 UI](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 [!UICONTROL 구성] 버튼을 클릭합니다.
1. [!UICONTROL 사용자 지정 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 버튼이 표시됩니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화 ([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getPageName v4.2 */
var getPageName=function(si,qv,hv,de){var a=si,b=qv,f=hv,e=de;if("-v"===a)return{plugin:"getPageName",version:"4.2"};a:{if("undefined"!==typeof window.s_c_il){var d=0;for(var g;d<window.s_c_il.length;d++)if(g=window.s_c_il[d],g._c&&"s_c"===g._c){d=g;break a}}d=void 0}"undefined"!==typeof d&&(d.contextData.getPageName="4.2");var c=location.hostname,h=location.pathname.substring(1).split("/"),l=h.length,k=location.search.substring(1).split("&"),m=k.length;d=location.hash.substring(1).split("&");g=d.length;e=e?e:"|";a=a?a:c;b=b?b:"";f=f?f:"";if(1===l&&""===h[0])a=a+e+"home";else for(c=0;c<l;c++)a=a+e+decodeURIComponent(h[c]);if(b&&(1!==m||""!==k[0]))for(h=b.split(","),l=h.length,c=0;c<l;c++)for(b=0;b<m;b++)if(h[c]===k[b].split("=")[0]){a=a+e+decodeURIComponent(k[b]);break}if(f&&(1!==g||""!==d[0]))for(f=f.split(","),k=f.length,c=0;c<k;c++)for(b=0;b<g;b++)if(f[c]===d[b].split("=")[0]){a=a+e+decodeURIComponent(d[b]);break}return a.substring(a.length-e.length)===e?a.substring(0,a.length-e.length):a};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getPageName` 함수에서는 다음 인수를 사용합니다.

* **`si`** (선택 사항, 문자열): 사이트의 ID를 나타내는 문자열 시작 부분에 삽입되는 ID입니다. 이 값은 숫자 ID나 친숙한 이름일 수 있습니다. 설정하지 않으면 기본값이 현재 도메인으로 설정됩니다.
* **`qv`** (선택 사항, 문자열): 쿼리 문자열 매개 변수의 쉼표로 구분된 목록으로서, URL에 있는 경우에는 문자열에 추가됩니다.
* **`hv`** (선택 사항, 문자열): URL 해시에 있는 매개 변수의 쉼표로 구분된 목록으로서, URL에 있는 경우에는 문자열에 추가됩니다.
* **`de`** (선택 사항, 문자열): 문자열의 개별 부분을 분할하는 구분 기호입니다. 기본값은 파이프(`|`)입니다.

이 함수는 URL의 친숙한 형식 버전을 포함하는 문자열을 반환합니다. 이 문자열은 일반적으로 `pageName` 변수에 지정되지만 다른 변수에서도 사용할 수 있습니다.

## 예

```js
// Given the URL https://mail.example.com/mail/u/0/#inbox, sets the page variable to "mail.example.com|mail|u|0".
s.pageName = getPageName();

// Given the URL https://mail.example.com/mail/u/0/#inbox, sets the page variable to "example|mail|u|0".
s.pageName = getPageName("example");

// Given the URL https://www.example.com/, sets the page variable to "www.example.com|home".
// When the code runs on a URL that does not contain a path, it always adds the value of "home" to the end of the return value.
s.pageName = getPageName();

// Given the URL https://www.example.com/, sets the page variable to "example|home".
s.pageName = getPageName("example","","","|");

// Given the URL https://www.example.com/en/booking/room-booking.html?cid=1235#/step2&arrive=05-26&depart=05-27&numGuests=2
// Sets the page variable to "www.example.com|en|booking|room-booking.html".
s.pageName = getPageName();

// Given the URL https://www.example.com/en/booking/room-booking.html?cid=1235#/step2&arrive=05-26&depart=05-27&numGuests=2
// Sets the page variable to "example: en: booking: room-booking.html: cid=1235: arrive=05-26: numGuests=2"
s.pageName = getPageName("example","cid","arrive,numGuests",": ");
```

## 이전 버전에서 업그레이드

`getPageName` 플러그인의 버전 4.0 이상은 실행할 Adobe Analytics의 AppMeasurement 개체(즉, `s` 개체)의 존재여부에 따라 달라지지 않습니다. 이 버전으로 업그레이드하려는 경우 반드시 호출에서 `s` 개체의 인스턴스를 제거하여 플러그인을 호출하는 코드를 변경하십시오. 예를 들어 `s.getPageName();`을 `getPageName();`으로 변경합니다.

## 버전 내역

### 4.2 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 4.1 (2019년 9월 17일)

* 기본 구분 기호 값을 파이프 문자 (원래 콜론 + 공백이었음)로 변경했습니다.

### 4.0 (2018년 5월 22일)

* 전체 플러그인 분석/다시 작성
