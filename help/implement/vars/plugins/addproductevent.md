---
title: addProductEvent
description: products 및 events 변수에 사용자 지정 이벤트를 추가합니다.
feature: Appmeasurement Implementation
exl-id: 74f4cb93-714a-4d2b-88f3-408d032f6811
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 86%

---

# Adobe 플러그인: addProductEvent

{{plug-in}}

`addProductEvent` 플러그인은 숫자 또는 통화 이벤트를 [`products`](../page-vars/products.md) 변수에 추가합니다. 제품 문자열 형식에 대한 걱정 없이 숫자 또는 통화 이벤트를 `products` 변수에 추가하려면 이 플러그인을 사용하는 것이 좋습니다. 이 플러그인은 `products` 변수에서 숫자 또는 통화 이벤트를 사용하지 않는 경우 필요하지 않습니다.

## Web SDK 또는 Web SDK 확장을 사용하여 플러그인 설치

이 플러그인은 아직 웹 SDK 내에서 사용할 수 없습니다.

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
   * 작업 유형: addProductEvent 초기화
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
/* Adobe Consulting Plugin: addProductEvent v2.0 */
function addProductEvent(en,ev,ap){var f=en,g=ev,c=ap;if("-v"===f)return{plugin:"addProductEvent",version:"2.0"};var d=function(){if("undefined"!==typeof window.s_c_il)for(var b=0,e;b<window.s_c_il.length;b++)if(e=window.s_c_il[b],e._c&&"s_c"===e._c)return e}();if("undefined"!==typeof d&&(d.contextData.addProductEvent="2.0",window.apl=window.apl||function(b,e,c,d,f){function g(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(!b||"string"===typeof b){if("string"!==typeof e||""===e)return b;c=c||",";d=d||c;1==d&&(d=c,f||(f=1));2==d&&1!=f&&(d=c);e=e.split(",");k=e.length;for(var h=0;h<k;h++)g(b,e[h],c,f)||(b=b?b+d+e[h]:e[h])}return b},"string"===typeof f))if(g=isNaN(g)?"1":String(g),c=c||!1,d.events=window.apl(d.events,f),d.products){var l=d.products.split(","),m=l.length;c=c?0:m-1;for(var b;c<m;c++)b=l[c].split(";"),b[4]&&-1<b[4].indexOf("event")?b[4]=b[4]+"|"+f+"="+g:b[5]?b[4]=f+"="+g:b[4]||(b[3]||(b[3]=""),b[2]||(b[2]=""),b[1]||(b[1]=""),b[4]=f+"="+g),l[c]=b.join(";");d.products=l.join(",")}else d.products=";;;;"+f+"="+g};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`addProductEvent` 함수에서는 다음 인수를 사용합니다.

* **`en`** (필수, 문자열): `products` 변수의 마지막 항목에 추가할 이벤트입니다. `products` 변수가 비어 있으면 이벤트 (및 그 값)가 첨부된 &quot;빈&quot; 제품 항목이 만들어집니다.
* **`ev`** (필수, 문자열): `en` 인수의 숫자 또는 통화 이벤트에 지정된 값입니다.  설정하지 않으면 기본값이 `1`로 설정됩니다. 문자열 따옴표에 포함되지 않은 숫자도 유효합니다.
* **`ap`** (선택 사항, 부울): products 변수에 현재 둘 이상의 제품 항목이 포함되어 있는 경우, 값이 `true` (또는 `1`)이면 모든 제품 항목에 이벤트가 추가됩니다.  설정하지 않으면 기본값이 `false`로 설정됩니다.

`addProductEvent`는 아무 것도 반환하지 않습니다. 대신 이벤트와 그 값을 `products` 변수에 추가합니다. 또한 이 플러그인은 [`events`](../page-vars/events/events-overview.md) 변수에서 필수이므로 이 변수에 이벤트를 자동으로 추가합니다.

## 쿠키

`addProductEvent` 기능은 쿠키를 만들거나 사용하지 않습니다.

## 예

```js
// Sets the products variable to ";product1;3;300,;product2;2;122,;product3;1;25;event35=25".
// Also sets the events variable to "purchase,event35".
s.products = ";product1;3;300,;product2;2;122,;product3;1;25";
s.events = "purchase";
addProductEvent("event35", "25");

// Sets the products variable to ";product1;3;300;event35=25,;product2;2;122;event35=25,;product3;1;25;event35=25".
s.products = ";product1;3;300,;product2;2;122,;product3;1;25";
addProductEvent("event35", 25, true);

// Sets the products variable to ";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25;event33= 12|event34=10|event35=15"
// Also sets the s.events variable to "purchase,event2,event33,event34,event35".
s.products=";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25";
s.events="purchase,event2";
addProductEvent("event33", "12");
addProductEvent("event34", "10");
addProductEvent("event35", "15");

// Sets the products variable to ";product1;3;300;event2=10|event33=12|event34=10|event35=15;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122;event33=12|event34=10|event35=15,;product3;1;25;event33=12|event34=10|event35=15".
// Also sets the events variable to "purchase,event2,event33,event34,event35".
s.products=";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25"
s.events="purchase,event2"
addProductEvent("event33", "12", 1);
addProductEvent("event34", 10, 1);
addProductEvent("event35", "15", 1);

// If the products variable isn't already set, sets it to ";;;;event35=25".
// Also appends event35 to the events variable.
addProductEvent("event35", "25");
```

## 버전 내역

### 2.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 1.0 (2019년 10월 7일)

* 초기 릴리스.
