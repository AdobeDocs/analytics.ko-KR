---
title: getTimeBetweenEvents
description: 두 이벤트 사이의 시간을 측정합니다.
feature: Variables
exl-id: 15887796-4fe4-4b3a-9a65-a4672c5ecb34
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 91%

---

# Adobe 플러그인: getTimeBetweenEvents

{{plug-in}}

`getTimeBetweenEvents` 플러그인을 사용하면 장바구니 및 사용자 지정 이벤트를 포함하여 두 Analytics 이벤트 간의 시간을 추적할 수 있습니다. 이 플러그인은 체크아웃 프로세스가 완료되는 데 걸리는 시간이나 시간을 측정하려는 기타 프로세스를 추적하는 데 유용하며, 소요 시간을 측정하려는 변환 프로세스가 없는 경우에는 필요하지 않습니다.

## Web SDK 또는 Web SDK 확장을 사용하여 플러그인 설치

이 플러그인은 아직 웹 SDK에서 사용할 수 없습니다.

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
   * 작업 유형: getTimeBetweenEvents 초기화
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
/* Adobe Consulting Plugin: getTimeBetweenEvents v3.0 (AppMeasurement highly recommended) */
function getTimeBetweenEvents(ste,rt,stp,res,cn,etd,fmt,bml,rte){var v=ste,B=rt,x=stp,C=res,k=cn,m=etd,E=fmt,F=bml,p=rte;if("-v"===v)return{plugin:"getTimeBetweenEvents",version:"3.0"};var q=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();if("undefined"!==typeof q&&(q.contextData.getTimeBetweenEvents="3.0",window.cookieWrite=window.cookieWrite||function(c,b,d){if("string"===typeof c){var n=window.location.hostname,f=window.location.hostname.split(".").length-1;if(n&&!/^[0-9.]+$/.test(n)){f=2<f?f:2;var l=n.lastIndexOf(".");if(0<=l){for(;0<=l&&1<f;)l=n.lastIndexOf(".",l-1),f--;l=0<l?n.substring(l):n}}g=l;b="undefined"!==typeof b?""+b:"";if(d||""===b)if(""===b&&(d=-60),"number"===typeof d){var e=new Date;e.setTime(e.getTime()+6E4*d)}else e=d;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(d?" expires="+e.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof window.cookieRead)?window.cookieRead(c)===b:!1}},window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,d=b.indexOf(" "+c+"="),e=0>d?d:b.indexOf(";",d);return(c=0>d?"":decodeURIComponent(b.substring(d+2+c.length,0>e?b.length:e)))?c:""},window.formatTime=window.formatTime||function(c,b,d){function e(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(!("undefined"===typeof c||isNaN(c)||0>Number(c))){var f="";"string"===typeof b&&"d"===b||("string"!==typeof b||!e("h,m,s",b))&&86400<=c?(b=86400,f="days",d=isNaN(d)?1:b/(d*b)):"string"===typeof b&&"h"===b||("string"!==typeof b||!e("m,s",b))&&3600<=c?(b=3600,f="hours",d=isNaN(d)?4:b/(d*b)):"string"===typeof b&&"m"===b||("string"!==typeof b||!e("s",b))&&60<=c?(b=60,f="minutes",d=isNaN(d)?2:b/(d*b)):(b=1,f="seconds",d=isNaN(d)?.2:b/d);f=Math.round(c*d/b)/d+" "+f;0===f.indexOf("1 ")&&(f=f.substring(0,f.length-1));return f}},window.inList=window.inList||function(c,b,d,e){if("string"!==typeof b)return!1;if("string"===typeof c)c=c.split(d||",");else if("object"!==typeof c)return!1;d=0;for(a=c.length;d<a;d++)if(1==e&&b===c[d]||b.toLowerCase()===c[d].toLowerCase())return!0;return!1},"string"===typeof v&&"undefined"!==typeof B&&"string"===typeof x&&"undefined"!==typeof C)){k=k?k:"s_tbe";m=isNaN(m)?1:Number(m);var r=!1,t=!1,y=v.split(","),z=x.split(",");p=p?p.split(","):[];for(var u=window.cookieRead(k),w,D=new Date,A=D.getTime(),h=new Date,e=0;e<p.length;++e)if(window.inList(q.events,p[e])){h.setDate(h.getDate()-1);window.cookieWrite(k,"",h);return}h.setTime(h.getTime()+864E5*m);for(e=0;e<y.length&&!r&&(r=window.inList(q.events,y[e]),!0!==r);++e);for(e=0;e<z.length&&!t&&(t=window.inList(q.events,z[e]),!0!==t);++e);1===y.length&&1===z.length&&v===x&&r&&t?(u&&(w=(A-u)/1E3),window.cookieWrite(k,A,m?h:0)):(!r||1!=B&&u||window.cookieWrite(k,A,m?h:0),t&&u&&(w=(D.getTime()-u)/1E3,!0===C&&(h.setDate(h.getDate()-1),window.cookieWrite(k,"",h))));return w?window.formatTime(w,E,F):""}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getTimeBetweenEvents` 함수에서는 다음 인수를 사용합니다.

* **`ste`** (필수, 문자열): 타이머 시작 이벤트. 타이머를 시작할 Analytics 이벤트들을 쉼표로 구분한 문자열입니다.
* **`rt`** (필수, 부울): 타이머 다시 시작 옵션. `events` 변수에 타이머 시작 이벤트가 포함될 때마다 타이머를 다시 시작하려는 경우 `true`로 설정하십시오. 타이머 시작 이벤트가 표시될 때 타이머가 다시 시작되지 않도록 하려면 `false`로 설정하십시오.
* **`stp`** (필수, 문자열): 타이머 중지 이벤트. 타이머를 중지하는 Analytics 이벤트들을 쉼표로 구분한 문자열입니다.
* **`res`** (필수, 부울): 타이머 재설정 옵션. 타이머가 시작된 이후의 시간을 기록하고 타이머가 중지된 후에 재설정하려면 `true`로 설정하십시오. 시간을 기록하되 타이머를 중지하지 않으려면 `false`로 설정하십시오. `false`로 설정하면 이벤트 변수가 중지 이벤트를 기록한 후에도 타이머가 계속 실행됩니다.

  >[!TIP]
  >
  >이 인수를 `false`로 설정하면 아래의 `rte` 인수를 설정하는 것이 좋습니다.
* **`cn`** (선택 사항, 문자열): 첫 번째 이벤트의 시간이 저장되는 쿠키 이름입니다. 기본값은 `"s_tbe"`입니다.
* **`etd`** (선택 사항, 정수): 일 단위의 쿠키 만료 시간입니다. 브라우저 세션이 끝날 때 만료되도록 하려면 `0`으로 설정하십시오. 설정하지 않으면 기본값이 1일로 설정됩니다.
* **`fmt`** (선택 사항, 문자열): 초 수가 반환되는 시간 형식(기본값은 nothing)입니다.
   * `"s"` - 초
   * `"m"` - 분
   * `"h"` - 시간
   * `"d"` - 일
   * 설정하지 않으면 반환 값의 형식은 다음 규칙을 기반으로 합니다.
      * 1분 미만의 시간은 가장 가까운 5초 벤치마크로 반올림됩니다. 예를 들어 10초, 15초.
      * 1분과 1시간 사이의 모든 시간은 가장 가까운 1/2분 벤치마크로 반올림됩니다. 예를 들어 30.5분, 31분.
      * 1시간과 1일 사이의 모든 시간은 가장 가까운 1/4시간 벤치마크로 반올림됩니다. 예를 들어 2.25시간, 3.5시간
      * 하루보다 큰 모든 시간은 가장 가까운 일 벤치마크로 반올림됩니다. 예를 들어 1일, 3일, 9일
* **`bml`** (선택 사항, 숫자): `fmt` 인수의 형식에 따른 반올림 벤치마크의 길이입니다. 예를 들어 `fmt` 인수가 `"s"`이고 이 인수가 `2`인 경우 반환 값은 가장 가까운 2초 벤치마크로 반올림됩니다. `fmt` 인수가 `"m"`이고 이 인수가 `0.5`인 경우 반환 값은 가장 가까운 1/2분 벤치마크로 반올림됩니다.
* **`rte`** (선택 사항, 문자열): 타이머를 제거하거나 삭제하는 Analytics 이벤트들을 쉼표로 구분한 문자열입니다. 기본값은 nothing입니다.

이 함수를 호출하면 타이머 시작 이벤트와 타이머 중지 이벤트 사이의 시간을 나타내는 정수가 원하는 형식으로 반환됩니다.

## 호출 예

```js
// The timer starts or restarts when the events variable contains event1
// The timer stops and resets when the events variable contains event2
// The timer resets when the events variable contains event3 or the visitor closes their browser
// Sets eVar1 to the number of seconds between event1 and event2, rounded to the nearest 2-second benchmark
s.eVar1 = getTimeBetweenEvents("event1", true, "event2", true, "", 0, "s", 2, "event3");

// The timer starts when the events variable contains event1. It does NOT restart with subsequent hits that also contain event1
// The timer records a "lap" when the events variable contains event2. It does not stop the timer.
// The timer resets when the events variable contains event3 or if more than 20 days pass since the timer started
// The timer is stored in a cookie labeled "s_20"
// Sets eVar4 to the number of hours between event1 and event2, rounded to the nearest 90-minute benchmark
s.eVar4 = getTimeBetweenEvents("event1", false, "event2", false, "s_20", 20, "h", 1.5, "event3");

// Similar to the above timer in eVar4, except the return value is returned in seconds/minutes/hours/days depending on the timer length.
// The timer expires after 1 day.
s.eVar4 = getTimeBetweenEvents("event1", true, "event2", true);
```

## 버전 내역

### 3.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 2.1 (2018년 5월 26일)

* 새로운 버전의 `formatTime` 플러그인에 대한 변경 사항을 수용합니다.

### 2.0 (2018년 4월 6일)

* 플러그인의 전체 재작성/재분석.
