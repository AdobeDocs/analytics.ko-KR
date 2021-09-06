---
title: getResponsiveLayout
description: 현재 보고 있는 웹 사이트의 레이아웃을 파악합니다.
exl-id: 5b192d02-fc3c-4b82-acb4-42902202ab5f
source-git-commit: ab078c5da7e0e38ab9f0f941b407cad0b42dd4d1
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 87%

---

# Adobe 플러그인: getResponsiveLayout

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getResponsiveLayout` 플러그인을 사용하면 방문자가 현재 보고 있는 반응형 디자인 기반 웹 사이트의 버전을 추적할 수 있습니다. 사이트에서 반응형 디자인을 사용하고 방문자가 본 사이트의 버전을 추적하려는 경우 이 플러그인을 사용하는 것이 좋습니다. 사이트에서 반응형 디자인을 사용하지 않는 경우 이 플러그인은 불필요합니다.

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
   * 작업 유형: getResponsiveLayout 초기화
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
/* Adobe Consulting Plugin: getResponsiveLayout v1.1 (Requires AppMeasurement) */
var getResponsiveLayout=function(ppw,plw,tw){var c=ppw,b=plw,e=tw;if("-v"===c)return{plugin:"getResponsiveLayout",version:"1.1"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var d;a<window.s_c_il.length;a++)if(d=window.s_c_il[a],d._c&&"s_c"===d._c){a=d;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.getResponsiveLayout="1.1");if(!(isNaN(c)||isNaN(b)||isNaN(e)||b<c||e<b))return a=window.innerWidth||document.documentElement.clientWidth||document.body.clientWidth,(c<b&&a<=b?a<=c?"phone portrait layout":"phone landscape layout":a<=b?"phone layout":a<=e?"tablet layout":"desktop layout")+":"+a+"x"+(window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight)};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getResponsiveLayout` 함수는 다음 인수를 사용합니다.

* **`ppw`** (필수, 정수): 페이지가 휴대폰 세로 레이아웃에서 휴대폰 가로 기반 레이아웃으로 전환하기 전에 브라우저 창으로 사용할 수 있는 최대 픽셀 너비
* **`plw`** (필수, 정수): 페이지가 휴대폰 가로 레이아웃에서 태블릿 기반 레이아웃으로 전환하기 전에 브라우저 창으로 사용할 수 있는 최대 픽셀 너비
* **`tw`** (필수, 정수): 페이지가 태블릿 레이아웃에서 데스크탑 기반 레이아웃으로 전환하기 전에 브라우저 창으로 사용할 수 있는 최대 픽셀 너비

이 함수를 호출하면 콜론(`:`)으로 구분된 두 부분을 포함하는 문자열이 반환됩니다. 문자열의 첫 부분에는 브라우저의 너비와 위의 인수에 따라 다음 값 중 하나가 포함됩니다.

* `"phone portrait layout"`
* `"phone landscape layout"`
* `"phone layout"` (세로 및 가로 레이아웃이 모두 없는 사이트의 경우)
* `"tablet layout"`
* `"desktop layout"`

반환된 문자열의 두 번째 부분은 브라우저의 너비와 높이 차원입니다. (예: `"desktop layout:1243x700"`)

## 예

```js
// A visitor accesses your site on their laptop. The browser window is maximized.
// * Your site switches from phone portrait mode to phone landscape mode when the browser width is greater than 500 pixels
// * Your site switches from phone landscape mode to tablet mode when the browser width is greater than 700 pixels
// * Your site switches from tablet mode to desktop mode when the browser width is greater than 1000 pixels
// Sets eVar10 to "desktop layout:1920x937".
s.eVar10 = getResponsiveLayout(500, 700, 1000);

// A visitor accesses your site on their phone.
// * Your site has only a phone mode, a tablet mode, and a desktop mode
// * Your site switches from phone mode to tablet mode when the browser width is greater than 800 pixels
// * Your site switches from tablet mode to desktop mode when the browser width is greater than 1,100 pixels
// Sets eVar10 to "phone portrait layout:720x1280"
s.eVar10 = getResponsiveLayout(800, 800, 1100);
```

## 버전 내역

### 1.1 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 1.0 (2018년 5월 2일)

* 초기 릴리스.
