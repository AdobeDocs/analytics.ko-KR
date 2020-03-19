---
title: getQueryParam
description: URL의 쿼리 문자열 매개 변수 값을 추출합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:getQueryParam

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `getQueryParam` 플러그인을 사용하면 URL에 포함된 모든 쿼리 문자열 매개 변수의 값을 추출할 수 있습니다. 랜딩 페이지 URL에서 내부 및 외부 캠페인 코드를 추출하는 데 유용합니다. 검색어 또는 다른 쿼리 문자열 매개 변수를 추출할 때도 유용합니다.

이 플러그인은 여러 쿼리 문자열 매개 변수를 포함하는 해시 및 URL을 포함하여 복잡한 URL을 구문 분석하는 데 강력한 기능을 제공합니다. 단순 쿼리 문자열 매개 변수만 필요한 경우 Launch에서 URL 매개 변수 기능 또는 AppMeasurement에 포함된 [`Util.getQueryParam()`](../functions/util-getqueryparam.md) 메서드를 사용하는 것이 좋습니다.

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
   * 작업 유형:getQueryParam 초기화
1. 변경 내용을 저장하고 규칙에 게시합니다.

## Launch 사용자 정의 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려면 사용자 정의 코드 편집기를 사용할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. 원하는 속성을 클릭합니다.
1. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 확장 프로그램 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
1. 단추를 표시하는 [!UICONTROL Configure tracking using custom code] 아코디언을 [!UICONTROL Open Editor] 확장합니다.
1. 사용자 정의 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여 넣습니다.
1. Analytics 확장 프로그램에 변경 사항을 저장하고 게시합니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getQueryParam v3.3 (Requires pt plug-in) */
s.getQueryParam=function(qsp,de,url){var g=this,e="",k=function(b,de){de=de.split("?").join("&");de=de.split("#").join("&");var d=de.indexOf("&"),url="";b&&(-1<d||de.indexOf("=")>d)&&(d=de.substring(d+1),url=g.pt(d,"&","gpval",b));return url};qsp=qsp.split(",");var l=qsp.length;g.gpval=function(de,b){if(de){var d=de.split("="),url=d[0];d=d[1]?d[1]:!0;if(b.toLowerCase() ==url.toLowerCase())return"boolean"===typeof d?d:this.unescape(d)}return""};de=de?de:"";url=(url?url:g.pageURL?g.pageURL: location.href)+"";if((4<de.length||-1<de.indexOf("="))&&url&&4>url.length){var b=de;de=url;url=b}for(var h=0;h<l;h++)b=k(qsp[h],url) ,"string"===typeof b?(b=-1<b.indexOf("#")?b.substring(0,b.indexOf("#")):b,e+=e?de+b:b):e=""===e?b:e+(de+b);return e};

/* Adobe Consulting Plugin: pt v2.01 */ 
s.pt=function(l,de,cf,fa){if(l&&this[cf]){l=l.split(de||",");de=l.length;for(var e,c=0;c<de;c++)if(e=this[cf](l[c],fa))return e}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `getQueryParam` 메서드는 다음 인수를 사용합니다.

* **`qsp`** (필수):URL 내에서 찾을 쿼리 문자열 매개 변수의 쉼표로 구분된 목록입니다. 대/소문자를 구분하지 않습니다.
* **`de`** (선택 사항):여러 쿼리 문자열 매개 변수가 일치하는 경우 사용할 구분 기호입니다. 기본값은 빈 문자열입니다.
* **`url`** (선택 사항):쿼리 문자열 매개 변수 값을 추출하기 위한 사용자 지정 URL, 문자열 또는 변수. 기본값은 `window.location`입니다.

이 메서드를 호출하면 위의 인수 및 URL에 따라 값이 반환됩니다.

* 일치하는 쿼리 문자열 매개 변수를 찾을 수 없으면 이 메서드는 빈 문자열을 반환합니다.
* 일치하는 쿼리 문자열 매개 변수가 있으면 이 메서드는 쿼리 문자열 매개 변수 값을 반환합니다.
* 일치하는 쿼리 문자열 매개 변수가 있지만 값이 비어 있으면 메서드가 `true`반환됩니다.
* 일치하는 쿼리 문자열 매개 변수가 여러 개 있으면 이 메서드는 `de` 인수의 문자열로 구분된 각 매개 변수 값이 있는 문자열을 반환합니다.

## 호출 예

### 예 #1

현재 URL이 다음과 같은 경우:

```js
http://www.abc123.com/?cid=trackingcode1
```

다음 코드는 s.campaign을 &quot;trackingcode1&quot;과 동일하게 설정합니다.

```js
s.campaign=s.getQueryParam('cid');
```

### 예 #2

현재 URL이 다음과 같은 경우:

```js
http://www.abc123.com/?cid=trackingcode1&ecid=123456
```

다음 코드는 s.campaign을 &quot;trackingcode1:123456&quot;과 동일하게 설정합니다.

```js
s.campaign=s.getQueryParam('cid,ecid',':');
```

### 예 #3

현재 URL이 다음과 같은 경우:

```js
http://www.abc123.com/?cid=trackingcode1&ecid=123456
```

다음 코드는 s.campaign을 &quot;trackingcode1123456&quot;과 동일하게 설정합니다.

```js
s.campaign=s.getQueryParam('cid,ecid');
```

### 예 #4

현재 URL이 다음과 같은 경우:

```js
http://www.abc123.com/?cid=trackingcode1&ecid=123456#location
```

다음 코드는 s.campaign을 &quot;123456&quot;과 동일하게 설정합니다.

```js
s.campaign=s.getQueryParam('ecid');
```

### 예 #5

현재 URL이 다음과 같은 경우:

```js
http://www.abc123.com/#location&cid=trackingcode1&ecid=123456
```

다음 코드는 s.campaign을 &quot;123456&quot;과 동일하게 설정합니다.

```js
s.campaign=s.getQueryParam('ecid');
```

**참고:** 이 플러그인은 물음표가 없는 경우 Check의 해시 문자에 대한 URL을 물음표로 바꿉니다.  URL에 해시 문자 앞에 오는 물음표가 포함되어 있으면 플러그인은 URL을 Check의 해시 문자로 바꿉니다.

### 예 #6

현재 URL이 다음과 같은 경우...

```js
http://www.abc123.com/
```

...s.testURL 변수가 다음과 같이 설정된 경우:

```js
s.testURL="http://www.abc123.com/?cid=trackingcode1&ecid=123456#location&pos=300";
```

다음 코드는 s.campaign을 전혀 설정하지 않습니다.

```js
s.campaign=s.getQueryParam('cid');
```

하지만 다음 코드는 s.campaign을 &quot;trackingcode1&quot;과 동일하게 설정합니다.

```js
s.campaign=s.getQueryParam('cid','',s.testURL);
```

**참고:** 세 번째 매개 변수는

다음 코드는 s.eVar2를 &quot;123456|trackingcode1|true|300&quot;과 동일하게 설정합니다.

```js
s.eVar2=s.getQueryParam('ecid,cid,location,pos','|',s.testURL);
```

* 123456의 값은 s.testURL 변수의 ecid 매개 변수에서 가져옵니다
* trackingcode1의 값은 s.testURL 변수의 cid 매개 변수에서 가져옵니다
* true의 값은 s.testURL 변수의 해시 문자 뒤에 위치 매개 변수가 존재함(값이 아님)에서 옵니다

300의 값은 s.testURL 변수의 pos 매개 변수 값에서 가져옵니다

## 버전 내역

### 3.3(2019년 9월 24일)

* 불필요한 로직을 무시하여 코드 크기 축소

### 3.2(2018년 5월 15일)

* 함수로 `findParameterValue` 이동 및 `getParameterValue` 함수 `getQueryParam` 이동

### 3.1(2018년 5월 10일)

* 값이 없는 쿼리 문자열 매개 변수를 캡처하는 문제를 해결했습니다.

### 3.0(2018년 4월 16일)

* 포인트 릴리스(다시 컴파일되고 더 작은 코드 크기).
* 도우미 함수를 가독성을 위해 `findParameterValue` 및 `getParameterValue` 으로 변경했습니다.
* URL 해시에 포함된 매개 변수를 찾기 위해 인수를 추가할 필요가 제거되었습니다.

### 2.5(2016년 1월 8일)

* H-code 및 AppMeasurement와 호환(AppMeasurement와 `s.pt` 함께 필요)

### 2.4

* 코드가 해시( `h``#`) 문자 뒤에 있는 쿼리 문자열 매개 변수를 찾을 수 있도록 하는 매개 변수를 추가했습니다.

### 2.3

* 추적 코드 다음에 해시가 있을 때만 플러그인이 작동하는 회귀 문제를 해결했습니다.

### 2.2

* 이제 반환 값에서 해시 문자(및 이후 모든 항목)를 제거합니다.

### 2.1

* H.10 코드와 호환
