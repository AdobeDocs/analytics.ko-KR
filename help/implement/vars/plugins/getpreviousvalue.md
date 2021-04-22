---
title: getPreviousValue
description: 변수에 전달된 마지막 값을 가져옵니다.
exl-id: 235c504b-ba97-4399-a07b-b0bfc764f1ba
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '895'
ht-degree: 100%

---

# Adobe 플러그인: getPreviousValue

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getPreviousValue` 플러그인을 사용하면 변수를 이전 히트에 설정된 값으로 설정할 수 있습니다. 현재 히트에서 원하는 값이 구현에 모두 포함된 경우에는 이 플러그인이 필요하지 않습니다.

## Adobe Experience Platform Launch 확장 기능을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해 주는 확장 기능을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그] 버튼을 클릭합니다.
1. [!UICONTROL 일반적인 Analytics 플러그인] 확장 기능을 설치 및 게시합니다.
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨 (페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: getPreviousValue 초기화
1. 변경 사항을 저장하고 규칙에 게시합니다.

## Launch 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 [!UICONTROL 구성] 버튼을 클릭합니다.
1. [!UICONTROL 사용자 지정 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 버튼이 표시됩니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화 ([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/* Adobe Consulting Plugin: getPreviousValue v3.0 */
function getPreviousValue(v,c){var k=v,d=c;if("-v"===k)return{plugin:"getPreviousValue",version:"3.0"};var a=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof a&&(a.contextData.getPreviousValue="3.0");window.cookieWrite=window.cookieWrite||function(c,b,f){if("string"===typeof c){var h=window.location.hostname,a=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){a=2<a?a:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<a;)e=h.lastIndexOf(".",e-1),a--;e=0<e?h.substring(e):h}}g=e;b="undefined"!==typeof b?""+b:"";if(f||""===b)if(""===b&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};var l;d=d||"s_gpv";a=new Date;a.setTime(a.getTime()+18E5);window.cookieRead(d)&&(l=window.cookieRead(d));k?window.cookieWrite(d,k,a):window.cookieWrite(d,l,a);return l};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getPreviousValue` 메서드에서는 다음 인수를 사용합니다.

* **`v`**  (문자열, 필수): 다음 이미지 요청에 전달할 값이 있는 변수입니다. 사용되는 일반적인 변수는 이전 페이지 값을 검색하는 `s.pageName`입니다.
* **`c`**  (문자열, 선택 사항): 값을 저장하는 쿠키의 이름입니다. 이 인수를 설정하지 않으면 기본값이 `"s_gpv"`로 지정됩니다.

이 메서드를 호출하면 쿠키에 포함된 문자열 값이 반환됩니다. 그러면 플러그인이 쿠키 만료를 재설정하고 여기에 `v` 인수의 변수 값을 지정합니다. 쿠키는 30분 동안 활동이 없으면 만료됩니다.

## 호출 예

### 예 #1

다음 코드...

```js
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
```

* 먼저 s.prop7을 이전 이미지 요청의 s.pageName에 전달된 값과 동일하게 설정합니다 (즉, &quot;gpv_Page&quot; 쿠키에 저장된 값).
* 그러면 코드가 &quot;gpv_Page&quot; 쿠키를 재설정하여 s.pageName의 현재 값과 같게 만듭니다.
* 이 코드가 실행될 때 s.pageName이 설정되어 있지 않으면 코드가 쿠키의 현재 값에 대한 만료를 재설정합니다.

### 예 #2

다음 코드는 s.prop7을 s.pageName에 전달된 마지막 값과 동일하게 설정하지만, 호출이 발생할 때 inList 플러그인을 통해 결정된 대로 event1도 s.events 내에 포함된 경우에 한합니다.

```js
if(s.inList(s.events,"event1")) s.prop7=s.getPreviousValue(s.pageName,"gpv_Page");
```

### 예 #3

다음 코드는 s.prop7을 s.pageName에 전달된 마지막 값과 동일하게 설정하지만 s.pageName이 현재 해당 페이지에서 동시에 설정된 경우에 한합니다.

```js
if(s.pageName) s.prop7=s.getPreviousValue(s.pageName,"gpv_Page");
```

### 예 #4

다음 코드는 s.eVar10을 이전 이미지 요청의 s.eVar1에 전달된 값과 동일하게 설정합니다. 이전 eVar1 값은 &quot;s_gpv&quot; 쿠키에 포함되었을 것입니다. 그러면 코드는 &quot;s_gpv&quot; 쿠키를 s.eVar1의 현재 값과 동일하게 설정합니다.

```js
s.eVar10 = s.getPreviousValue(s.eVar1)
```

## 가능성 없는 일

v 인수와 연결된 변수가 새 값으로 설정되고 getPreviousValue 플러그인이 실행되지만 Analytics 서버 호출이 동시에 전송되지 않으면 새 v 인수 값은 다음에 플러그인이 실행될 때에도 여전히 &quot;이전 값&quot;으로 간주됩니다.
예를 들어 다음 코드가 방문의 첫 페이지에서 실행된다고 가정해 보십시오.

```js
s.pageName="home"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
s.t();
```

이 코드는 pageName 인수가 &quot;home&quot;이고 p7 (prop7) 인수가 설정되지 않은 경우 서버 호출을 생성합니다. 그러나 s.getPreviousValue를 호출하면 호출에 지정된 쿠키 (즉, &quot;gpv_Page&quot; 쿠키)에 s.pageName의 값 (즉, &quot;home&quot;)이 저장됩니다.
이제, 그 직후에 같은 페이지에서 다음 코드가 어떤 이유로든 실행된다고 가정하십시오.

```js
s.pageName="happy value"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
```

이 코드 블록에서는 s.t () 함수가 실행되지 않으므로 다른 이미지 요청은 만들어지지 않습니다. 그러나, 이 번에 s.getPreviousValue () 함수 코드가 실행되면 s.prop7이 s.pageName의 이전 값 (즉, &quot;home&quot;)과 동일하게 설정되고 s.pageName의 새 값 (즉, &quot;happy value&quot;)은 &quot;gpv_Page&quot; 쿠키에 저장됩니다.
방문자가 다른 페이지로 이동하고 이 페이지에서 다음 코드가 실행된다고 가정하십시오.

```js
s.pageName="page 2"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
s.t();
```

s.t () 호출 함수가 실행되면 s.pageName=&quot;page 2&quot;이고 s.prop7이 &quot;happy value&quot;인 이미지 요청이 만들어집니다. 이때 &quot;happy value&quot;는 getPreviousValue에 대한 마지막 호출이 수행되었을 때 s.pageName의 값이었습니다. s.pageName에 전달된 첫 번째 값이 &quot;home&quot;이지만 &quot;home&quot;이라는 s.prop7 값은 어떠한 실제 이미지 요청에도 포함되지 않았습니다.

## 버전 내역

### 3.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### v2.0 (2019년 10월 7일)

* 포인트 릴리스 (전체 논리 다시 작성).
