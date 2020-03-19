---
title: addProductEvent
description: 제품 및 이벤트 변수에 사용자 지정 이벤트를 추가합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:addProductEvent

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `addProductEvent` 플러그인은 숫자 또는 통화 이벤트를 [`products`](../page-vars/products.md) 변수에 추가합니다. 제품 문자열 형식에 대한 걱정 없이 숫자 또는 통화 이벤트를 `products` 변수에 추가하려면 이 플러그인을 사용하는 것이 좋습니다. 이 플러그인은 `products` 변수에 숫자 또는 통화 이벤트를 사용하지 않는 경우 필요하지 않습니다.

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
   * 작업 유형:AddProductEvent 초기화
1. 변경 내용을 저장하고 규칙에 게시합니다.

## Launch 사용자 정의 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려면 사용자 정의 코드 편집기를 사용할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. 원하는 속성을 클릭합니다.
1. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 확장 프로그램 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
1. 단추를 표시하는 [!UICONTROL Configure tracking using custom code] 아코디언을 [!UICONTROL Open Editor] 확장합니다.
1. 사용자 정의 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여 넣습니다.
1. Analytics 확장 프로그램에 변경 사항을 저장하고 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣습니다(사용 [`s_gi`](../functions/s-gi.md)). 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: addProductEvent v1.0 (Requires apl v3.1 and inList v2.0+ plug-ins) */
s.addProductEvent=function(en,ev,ap){var s=this;if("string"===typeof en)if(ev=isNaN(ev)?"1":String(ev),ap=ap||!1,s.events= s.apl(s.events,en),s.products){var e=s.products.split(",");ap=ap?0:e.length-1;for(var a;ap<e.length;ap++)a=e[ap].split(";") ,a[4]&&a[4].includes("event")?a[4]=a[4]+"|"+en+"="+ev:a[5]?a[4]=en+"="+ev:a[4]||(a[3]||(a[3]=""),a[2]||(a[2]=""),a[1]||(a[1]=""),a[4]=en+"="+ev),e[ap]=a.join(";");s.products=e.join(",")}else s.products=";;;;"+en+"="+ev};

/* Adobe Consulting Plugin: apl (appendToList) v3.2 (Requires inList v2.0 or higher) */
s.apl=function(lv,vta,d1,d2,cc){if(!lv||"string"===typeof lv){if("undefined"===typeof this.inList||"string"!==typeof vta||""===vta)return lv;d1=d1||",";d2=d2||d1;1==d2&&(d2=d1,cc||(cc=1));2==d2&&1!=cc&&(d2=d1);vta=vta.split(",");for(var g=vta.length,e=0;e<g;e++)this.inList(lv,vta[e],d1,cc)||(lv=lv?lv+d2+vta[e]:vta[e])}return lv};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `addProductEvent` 메서드는 다음 인수를 사용합니다.

* **`en`** (필수, 문자열):변수의 마지막 항목에 추가할 `products` 이벤트입니다. 변수가 비어 있으면 이벤트(및 해당 값)가 첨부된 &quot;빈&quot; 제품 항목이 만들어집니다. `products`
* **`ev`** (필수, 문자열):인수의 숫자 또는 통화 이벤트에 할당된 `en` 값입니다.  설정되지 않은 경우 기본값이 로 `1` 설정됩니다.
* **`ap`** (선택 사항, 부울):products 변수에 현재 둘 이상의 제품 항목이 포함되어 있는 경우 `true` (또는 `1`) 값이 모든 제품 항목에 이벤트를 추가합니다.  설정되지 않은 경우 기본값이 로 `false` 설정됩니다.

반환되는 `addProductEvent` 값이 없습니다. 대신 이벤트와 해당 값을 `products` 변수에 추가합니다. 또한 이 플러그인은 이 [`events`](../page-vars/events/events-overview.md) 변수에서 필수이므로 이 변수를 자동으로 추가합니다.

## 쿠키

addProductEvent 플러그인은 쿠키를 만들거나 사용하지 않습니다

## 호출 예

### 예 #1

다음 코드는 `s.products` 변수를 로 설정합니다 `";product1;3;300,;product2;2;122,;product3;1;25;event35=25"`.

```js
s.products=";product1;3;300,;product2;2;122,;product3;1;25"
s.events="purchase";
s.addProductEvent("event35", "25");
```

위의 코드에서는 변수를 `s.events``"purchase,event35"`

### 예 #2

다음 코드는 변수를 `s.products``";product1;3;300;event35=25,;product2;2;122;event35=25,;product3;1;25;event35=25"`

```js
s.products=";product1;3;300,;product2;2;122,;product3;1;25";
s.addProductEvent("event35", 25, 1);
```

호출의 세 번째 인수가 `addProductEvent` (또는 `true` `1`)이면 각 제품 항목에는 호출에 지정된 이벤트가 해당 값에 추가됩니다.

### 예 #3

다음 코드는 변수를 `s.products``";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25;event33= 12|event34=10|event35=15"`

```js
s.products=";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25";
s.events="purchase,event2";
s.addProductEvent("event33", "12");
s.addProductEvent("event34", "10");
s.addProductEvent("event35", "15");
```

위의 코드에서는 변수를 `s.events``"purchase,event2,event33,event34,event35"`

### 예 #4

다음 코드는 변수를 `s.products``";product1;3;300;event2=10|event33=12|event34=10|event35=15;eVar33=large|eVar34=men|eVar35=blue, ;product2;2;122;event33=12|event34=10|event35=15,;product3;1;25;event33=12|event34=10|event35=15"`

```js
s.products=";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25"
s.events="purchase,event2"
s.addProductEvent("event33", "12", 1);
s.addProductEvent("event34", 10, 1);
s.addProductEvent("event35", "15", 1);
```

위 코드에서도 `s.events` 변수를 로 설정합니다 `"purchase,event2,event33,event34,event35"`.

> [!NOTE] 호출의 두 번째 인수는 정수 **또는** 정수/숫자를 나타내는 문자열일 수 있습니다

### 예 #5

아직 설정되지 `s.products` 않은 경우 다음 코드는 `";;;;event35=25"`

```js
s.addProductEvent("event35", "25");
```

위 코드는 `"event35"` 또는 `s.events` , 아직 설정되지 않은 경우 위 코드가 **로 설정됩니다**`s.events` `s.events` . `"event35"`

## 버전 내역

### 1.0(2019년 10월 7일)

* 초기 릴리스.
