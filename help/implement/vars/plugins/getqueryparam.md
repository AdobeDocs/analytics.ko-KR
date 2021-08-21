---
title: getQueryParam
description: URL의 쿼리 문자열 매개 변수의 값을 추출합니다.
exl-id: d2d542d1-3a18-43d9-a50d-c06d8bd473b8
source-git-commit: ab078c5da7e0e38ab9f0f941b407cad0b42dd4d1
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 86%

---

# Adobe 플러그인: getQueryParam

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getQueryParam` 플러그인을 사용하면 URL에 포함된 모든 쿼리 문자열 매개 변수의 값을 추출할 수 있습니다. 이 플러그인은 랜딩 페이지 URL에서 내부와 외부의 캠페인 코드를 모두 추출하는 데 유용하며, 검색어 또는 기타 쿼리 문자열 매개 변수를 추출할 때에도 유용합니다.

이 플러그인은 여러 쿼리 문자열 매개 변수를 포함하는 해시 및 URL을 포함하여 복잡한 URL을 구문 분석하는 데 강력한 기능을 제공합니다. 간단한 쿼리 문자열 매개 변수만 필요한 경우에는 Adobe Experience Platform의 태그를 사용하는 URL 매개 변수 기능이나 AppMeasurement에 포함된 [`Util.getQueryParam()`](../functions/util-getqueryparam.md) 메서드를 사용하는 것이 좋습니다.

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
   * 작업 유형: getQueryParam 초기화
1. 변경 사항을 저장하고 규칙에 퍼블리싱합니다.

## 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [데이터 수집 UI](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 [!UICONTROL 구성] 버튼을 클릭합니다.
1. [!UICONTROL 사용자 지정 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 버튼이 표시됩니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getQueryParam v4.0.1  */
function getQueryParam(a,d,f){function n(g,c){c=c.split("?").join("&");c=c.split("#").join("&");var e=c.indexOf("&");if(g&&(-1<e||c.indexOf("=")>e)){e=c.substring(e+1);e=e.split("&");for(var h=0,p=e.length;h<p;h++){var l=e[h].split("="),q=l[1];if(l[0].toLowerCase()===g.toLowerCase())return decodeURIComponent(q||!0)}}return""}if("-v"===a)return{plugin:"getQueryParam",version:"4.0.1"};var b=function(){if("undefined"!==typeof window.s_c_il)for(var g=0,c;g<window.s_c_il.length;g++)if(c=window.s_c_il[g],c._c&&"s_c"===c._c)return c}();"undefined"!==typeof b&&(b.contextData.getQueryParam="4.0");if(a){d=d||"";f=(f||"undefined"!==typeof b&&b.pageURL||location.href)+"";(4<d.length||-1<d.indexOf("="))&&f&&4>f.length&&(b=d,d=f,f=b);b="";for(var m=a.split(","),r=m.length,k=0;k<r;k++)a=n(m[k],f),"string"===typeof a?(a=-1<a.indexOf("#")?a.substring(0,a.indexOf("#")):a,b+=b?d+a:a):b=""===b?a:b+(d+a);return b}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getQueryParam` 함수는 다음 인수를 사용합니다.

* **`qsp`**  (필수): URL 내에서 찾을 쿼리 문자열 매개 변수의 쉼표로 구분된 목록입니다. 대/소문자를 구분하지 않습니다.
* **`de`**  (선택 사항): 여러 쿼리 문자열 매개 변수가 일치하는 경우 사용할 구분 기호입니다. 기본값은 빈 문자열입니다.
* **`url`**  (선택 사항): 쿼리 문자열 매개 변수 값을 추출할 사용자 지정 URL, 문자열 또는 변수입니다. 기본값은 `window.location`입니다.

이 함수를 호출하면 위의 인수 및 URL에 따라 값이 반환됩니다.

* 일치하는 쿼리 문자열 매개 변수를 찾을 수 없으면 이 함수는 빈 문자열을 반환합니다.
* 일치하는 쿼리 문자열 매개 변수를 찾으면 이 함수는 쿼리 문자열 매개 변수 값을 반환합니다.
* 일치하는 쿼리 문자열 매개 변수를 찾았지만 값이 비어 있으면 이 함수는 `true`을 반환합니다.
* 일치하는 쿼리 문자열 매개 변수를 여러 개 찾으면 이 함수는 `de` 인수의 문자열로 각 매개 변수 값이 구분된 문자열을 반환합니다.

## 예

```js
// Given the URL https://example.com/?cid=trackingcode
// Sets the campaign variable to "trackingcode"
s.campaign = getQueryParam('cid');

// Given the URL https://example.com/?cid=trackingcode&ecid=123
// Sets the campaign variable to "trackingcode:123"
s.campaign = getQueryParam('cid,ecid',':');

// Given the URL https://example.com/?cid=trackingcode&ecid=123
// Sets the campaign variable to "trackingcode123"
s.campaign = getQueryParam('cid,ecid');

// Given the URL https://example.com/?cid=trackingcode&ecid=123#location
// Sets the campaign variable to "123"
s.campaign = getQueryParam('ecid');

// Given the URL https://example.com/#location&cid=trackingcode&ecid=123
// Sets the campaign variable to "123"
// The plug-in replaces the URL's hash character with a question mark if a question mark doesn't exist.
s.campaign = getQueryParam('ecid');

// Given the URL https://example.com
// Does not set the campaign variable to a value.
s.pageURL = "https://example.com/?cid=trackingcode";
s.campaign = getQueryParam('cid');

// Given the URL https://example.com
// Sets the campaign variable to "trackingcode"
s.pageURL = "https://example.com/?cid=trackingcode";
s.campaign = getQueryParam('cid','',s.pageURL);

// Given the URL https://example.com
// Sets eVar2 to "123|trackingcode|true|300"
s.eVar1 = "https://example.com/?cid=trackingcode&ecid=123#location&pos=300";
s.eVar2 = getQueryParam('ecid,cid,location,pos','|',s.eVar1);
```

## 버전 내역

### 4.0.1(2021년 3월 26일)

* 쿼리 문자열에 쿼리 매개 변수가 없을 때 “” 대신 정의되지 않음이 반환되는 문제가 업데이트되었습니다.

### 4.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.
* pt 플러그인에 대한 종속성이 제거되었습니다.

### 3.3 (2019년 9월 24일)

* 코드 크기를 줄이기 위해 불필요한 논리를 무시했습니다.

### 3.2 (2018년 5월 15일)

* `findParameterValue` 및 `getParameterValue` 함수를 `getQueryParam` 함수로 이동했습니다.

### 3.1 (2018년 5월 10일)

* 값이 없는 쿼리 문자열 매개 변수 캡처와 관련한 문제를 해결했습니다.

### 3.0 (2018년 4월 16일)

* 포인트 릴리스 (다시 컴파일됨, 더 작은 코드 크기).
* 가독성을 위해 도우미 함수를 `findParameterValue` 및 `getParameterValue`로 이름을 변경했습니다.
* URL 해시에 포함된 매개 변수를 찾기 위해 인수를 추가할 필요가 없어졌습니다.

### 2.5 (2016년 1월 8일)

* H-코드 및 AppMeasurement 모두와 호환합니다 (AppMeasurement에는 `s.pt` 필요).

### 2.4

* 코드가 해시 (`#`) 문자 뒤에 있는 쿼리 문자열 매개 변수를 찾을 수 있도록 해 주는 `h` 매개 변수를 추가했습니다.

### 2.3

* 추적 코드 다음에 해시가 있을 때만 플러그인이 작동했던 회귀 문제를 해결했습니다.

### 2.2

* 이제 반환 값에서 해시 문자 (및 그 이후의 모든 항목)를 제거합니다.

### 2.1

* H.10 코드와 호환
