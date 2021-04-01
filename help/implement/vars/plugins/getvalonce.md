---
title: getValOnce
description: Analytics 변수가 한 행에서 동일한 값으로 두 번 설정되지 않도록 합니다.
translation-type: ht
source-git-commit: 5a81754ca6137d7bc1e790fe537acbb4bbdb8efb
workflow-type: ht
source-wordcount: '729'
ht-degree: 100%

---


# Adobe 플러그인: getValOnce

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getValOnce` 플러그인을 사용하면 변수가 동일한 값에 두 번 이상 설정되지 않습니다. 방문자가 페이지를 새로 고치거나 지정된 페이지를 여러 번 방문하는 경우 발생 수를 중복 제거하려면 이 플러그인을 사용하는 것이 좋습니다. Analysis Workspace에서 &#39;발생 수&#39; 지표가 걱정되지 않는 경우에는 이 플러그인은 필요하지 않습니다.

## Adobe Experience Platform Launch 확장 기능을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해 주는 확장 기능을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그] 버튼을 클릭합니다.
1. [!UICONTROL 일반적인 Analytics 플러그인] 확장 기능을 설치 및 게시합니다.
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨(페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: getValOnce 초기화
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

Analytics 추적 개체가 인스턴스화([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getValOnce v3.0 (Requires AppMeasurement) */
function getValOnce(vtc,cn,et,ep){var e=vtc,k=cn,l=et,m=ep;if(arguments&&"-v"===arguments[0])return{plugin:"getValOnce",version:"3.0"};var c=function(){if("undefined"!==typeof window.s_c_il)for(var b=0,a;b<window.s_c_il.length;b++)if(a=window.s_c_il[b],a._c&&"s_c"===a._c)return a}();"undefined"!==typeof c&&(c.contextData.getValOnce="3.0");window.cookieWrite=window.cookieWrite||function(b,a,d){if("string"===typeof b){var h=window.location.hostname,c=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){c=2<c?
c:2;var f=h.lastIndexOf(".");if(0<=f){for(;0<=f&&1<c;)f=h.lastIndexOf(".",f-1),c--;f=0<f?h.substring(f):h}}g=f;a="undefined"!==typeof a?""+a:"";if(d||""===a)if(""===a&&(d=-60),"number"===typeof d){var e=new Date;e.setTime(e.getTime()+6E4*d)}else e=d;return b&&(document.cookie=encodeURIComponent(b)+"="+encodeURIComponent(a)+"; path=/;"+(d?" expires="+e.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(b)===a:!1}};window.cookieRead=window.cookieRead||function(b){if("string"===
typeof b)b=encodeURIComponent(b);else return"";var a=" "+document.cookie,d=a.indexOf(" "+b+"="),c=0>d?d:a.indexOf(";",d);return(b=0>d?"":decodeURIComponent(a.substring(d+2+b.length,0>c?a.length:c)))?b:""};return e&&(k=k||"s_gvo",l=l||0,m="m"===m?6E4:864E5,e!==this.c_r(k))?(c=new Date,c.setTime(c.getTime()+l*m),cookieWrite(k,e,0===l?0:m),e):""};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getValOnce` 메서드에서는 다음 인수를 사용합니다.

* **`vtc`** (필수, 문자열): 변수가 이전에 동일한 값으로 설정되었는지 확인하는 변수입니다.
* **`cn`** (선택 사항, 문자열): 확인할 값이 들어 있는 쿠키의 이름입니다. 기본값은 `"s_gvo"`입니다.
* **`et`** (선택 사항, 정수): 쿠키의 만료 기간(`ep` 인수에 따라 일 또는 분 단위)입니다. 기본값은 `0`이고, 이 값은 브라우저 세션 종료 시 만료됩니다.
* **`ep`** (선택 사항, 문자열): `et` 인수도 설정되는 경우에만 이 인수를 설정하십시오. `et` 인수가 일 대신 분 단위로 만료되도록 하려면 이 인수를 `"m"`으로 설정하십시오. 기본값은 `"d"`이고, 이 값은 `et` 인수를 일 단위로 설정합니다.

`vtc` 인수와 쿠키 값이 일치하는 경우 이 메서드는 빈 문자열을 반환합니다. `vtc` 인수와 쿠키 값이 일치하지 않으면 이 메서드는 `vtc` 인수를 문자열로 반환합니다.

## 호출 예

### 예 #1

다음 30일 동안 동일한 값이 s.campaign에 두 번 이상 연달아 전달되지 않도록 하려면 이 호출을 사용하십시오.

```js
s.campaign=s.getValOnce(s.campaign,"s_campaign",30);
```

위의 호출에서 플러그인은 먼저 s_campaign 쿠키에 이미 포함된 값을 현재 s.campaign 변수에서 나오는 값과 비교합니다. 일치하는 항목이 없으면 플러그인은 s_campaign 쿠키를 s.campaign에서 나오는 새 값과 동일하게 설정한 후 새 값을 반환합니다. 이 비교는 다음 30일 동안 있을 수행됩니다.

### 예 #2

세션 전체에서 동일한 값이 설정되지 않도록 하려면 이 호출을 사용하십시오.

```js
s.eVar2=s.getValOnce(s.eVar2,"s_ev2",0,"m");
```

이 코드는 사용자 세션 전체에서 동일한 값이 연달아 두 번 이상 s.eVar2로 전달되지 않도록 합니다. 또한 만료 시간이 0으로 설정되므로 이 코드는 ep 인수의 &quot;m&quot; 값도 무시합니다(호출 종료 시). 또한 이 코드는 s_ev2 쿠키에 비교 값을 저장합니다.

## 버전 내역

### 3.0(2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 2.01

* 쿠키 쓰기 문제를 수정했습니다.

### 2.0

* 포인트 릴리스(다시 컴파일됨, 더 작은 코드 크기).

### 1.1

* `t` 매개 변수를 통해 만료에 대한 분 또는 일을 선택하는 옵션을 추가했습니다.
* 플러그인으로만 제한하는 데 사용되는 `k` 변수의 범위를 수정했습니다. 이 변경 사항으로 페이지의 다른 코드에 대한 간섭이 방지됩니다.
