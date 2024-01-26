---
title: getValOnce
description: Analytics 변수가 한 행에서 동일한 값으로 두 번 설정되지 않도록 합니다.
feature: Variables
exl-id: 23bc5750-43a2-4693-8fe4-d6b31bc34154
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 74%

---

# Adobe 플러그인: getValOnce

{{plug-in}}

`getValOnce` 플러그인을 사용하면 변수가 동일한 값에 두 번 이상 설정되지 않습니다. 방문자가 페이지를 새로 고치거나 지정된 페이지를 여러 번 방문하는 경우 발생 수를 중복 제거하려면 이 플러그인을 사용하는 것이 좋습니다. Analysis Workspace에서 &#39;발생 수&#39; 지표가 걱정되지 않는 경우에는 이 플러그인은 필요하지 않습니다.

## Web SDK 확장을 사용하여 플러그인 설치

Adobe은 Web SDK에서 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해 주는 확장을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 클릭 **[!UICONTROL 태그]** 왼쪽에서 원하는 태그 속성을 클릭합니다.
1. 클릭 **[!UICONTROL 확장]** 왼쪽에서 을(를) 클릭한 다음 **[!UICONTROL 카탈로그]** 탭
1. 을(를) 찾아 설치합니다. **[!UICONTROL 일반 웹 SDK 플러그인]** 확장명.
1. 클릭 **[!UICONTROL 데이터 요소]** 왼쪽에서 원하는 데이터 요소를 클릭합니다.
1. 다음 구성으로 원하는 데이터 요소 이름을 설정합니다.
   * 확장: 일반적인 웹 SDK 플러그인
   * 데이터 요소: `getValOnce`
1. 오른쪽에서 원하는 매개 변수를 설정합니다.
1. 변경 사항을 저장하고 데이터 요소에 게시합니다.

## 웹 SDK를 수동으로 구현하여 플러그인 설치

이 플러그인은 아직 웹 SDK의 수동 구현 내에서 사용할 수 없습니다.

## Adobe Analytics 확장을 사용하여 플러그인 설치

Adobe은 Adobe Analytics에서 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해 주는 확장을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그] 버튼을 클릭합니다.
1. [!UICONTROL 일반적인 Analytics 플러그인] 확장 기능을 설치 및 게시합니다.
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨 (페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: getValOnce 초기화
1. 변경 사항을 저장하고 규칙에 퍼블리싱합니다.

## 사용자 지정 코드 편집기를 사용하여 플러그인 설치

일반 Analytics 플러그인 확장 프로그램을 사용하지 않으려면 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
1. [!UICONTROL 사용자 정의 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 버튼이 표시됩니다.
1. 사용자 정의 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 오브젝트가 인스턴스화 ([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣으십시오. 구현에서 코드의 댓글 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getValOnce v3.1 */
function getValOnce(vtc,cn,et,ep){var e=vtc,i=cn,t=et,n=ep;  if(arguments&&"-v"===arguments[0])return{plugin:"getValOnce",version:"3.1"};var o=function(){if(void 0!==window.s_c_il){for(var e,i=0;i<window.s_c_il.length;i++)if((e=window.s_c_il[i])._c&&"s_c"===e._c)return e}}();if(void 0!==o&&(o.contextData.getValOnce="3.1"),window.cookieWrite=window.cookieWrite||function(e,i,t){if("string"==typeof e){var n=window.location.hostname,o=window.location.hostname.split(".").length-1;if(n&&!/^[0-9.]+$/.test(n)){o=2<o?o:2;var r=n.lastIndexOf(".");if(0<=r){for(;0<=r&&1<o;)r=n.lastIndexOf(".",r-1),o--;r=0<r?n.substring(r):n}}if(g=r,i=void 0!==i?""+i:"",t||""===i){if(""===i&&(t=-60),"number"==typeof t){var f=new Date;f.setTime(f.getTime()+6e4*t)}else f=t}return!!e&&(document.cookie=encodeURIComponent(e)+"="+encodeURIComponent(i)+"; path=/;"+(t?" expires="+f.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!=typeof cookieRead)&&cookieRead(e)===i}},window.cookieRead=window.cookieRead||function(e){if("string"!=typeof e)return"";e=encodeURIComponent(e);var i=" "+document.cookie,t=i.indexOf(" "+e+"="),n=0>t?t:i.indexOf(";",t);return(e=0>t?"":decodeURIComponent(i.substring(t+2+e.length,0>n?i.length:n)))?e:""},e){var i=i||"s_gvo",t=t||0,n="m"===n?6e4:864e5;if(e!==cookieRead(i)){var r=new Date;return r.setTime(r.getTime()+t*n),cookieWrite(i,e,0===t?0:r),e}}return""}
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getValOnce` 함수에서는 다음 인수를 사용합니다.

* **`vtc`** (필수, 문자열): 변수가 이전에 동일한 값으로 설정되었는지 확인하는 변수입니다.
* **`cn`** (선택 사항, 문자열): 확인할 값이 들어 있는 쿠키의 이름입니다. 기본값은 `"s_gvo"`입니다.
* **`et`** (선택 사항, 정수): 쿠키의 만료 기간(`ep` 인수에 따라 일 또는 분 단위)입니다. 기본값은 `0`이고, 이 값은 브라우저 세션 종료 시 만료됩니다.
* **`ep`** (선택 사항, 문자열): `et` 인수도 설정되는 경우에만 이 인수를 설정하십시오. `et` 인수가 일 대신 분 단위로 만료되도록 하려면 이 인수를 `"m"`으로 설정하십시오. 기본값은 `"d"`이고, 이 값은 `et` 인수를 일 단위로 설정합니다.

`vtc` 인수와 쿠키 값이 일치하는 경우 이 함수는 빈 문자열을 반환합니다. `vtc` 인수와 쿠키 값이 일치하지 않으면 이 함수는 `vtc` 인수를 문자열로 반환합니다.

## 예

```js
// Prevent the same value from being passed in to the campaign variable more than once in a row for next 30 days
s.campaign = getValOnce(s.campaign,"s_campaign",30);

// Prevent the same value from being passed in to eVar2 more than once in a row for the browser session
s.eVar2 = getValOnce(s.eVar2,"s_ev2");

// Prevent the same value from being passed in to eVar8 more than once in a row for 10 minutes
s.eVar8 = getValOnce(s.eVar8,"s_ev8",10,"m");
```

## 버전 내역

### 3.1 (2022년 9월 22일)

* 만료에 대한 버그가 수정됨

### 3.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 2.01

* 쿠키 쓰기 문제를 수정했습니다.

### 2.0

* 포인트 릴리스 (다시 컴파일됨, 더 작은 코드 크기).

### 1.1

* `t` 매개 변수를 통해 만료에 대한 분 또는 일을 선택하는 옵션을 추가했습니다.
* 플러그인으로만 제한하는 데 사용되는 `k` 변수의 범위를 수정했습니다. 이 변경 사항으로 페이지의 다른 코드에 대한 간섭이 방지됩니다.
