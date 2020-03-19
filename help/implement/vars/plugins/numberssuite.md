---
title: 숫자 세트
description: 다른 JavaScript 변수에서 사용할 숫자를 만들고 조작합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:숫자 세트

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

숫자 세트는 일련의 JavaScript 함수입니다. 여기에는 다음 플러그인이 포함되어 있습니다.

* **`zeroPad`**:숫자의 시작 부분에 특정 0을 추가합니다. 이 플러그인은 JavaScript 날짜 개체를 사용하여 작업하고 한 자리 숫자가 아닌 두 자리 숫자로 날짜 및 일의 서식을 지정하려는 경우와 같이 변수에 특정 자릿수가 필요한 경우에 유용합니다. 예를 들어, `01/09/2020` 대신 `1/9/2020`.
* **`randomNumber`**:특정 수의 숫자를 사용하여 무작위 숫자를 생성합니다. 이 플러그인은 타사 태그를 배포하고 캐시 버스트 임의 번호를 원하는 경우에 유용합니다.
* **`twoDecimals`**:100분의 1로 숫자를 돌리세요. 이 플러그인은 통화 용도의 경우 유용하므로 숫자를 유효한 통화 값으로 반올림할 수 있습니다.

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
   * 작업 유형:숫자 세트 초기화
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
/* Adobe Consulting Plugin: zeroPad v1.0 */
function zeroPad(num,nod){num=parseInt(num);nod=parseInt(nod);if(isNaN(num)||isNaN(nod))return"";var c=nod-num.toString().length+ 1;return Array(+(0<c&&c)).join("0")+num};

/* Adobe Consulting Plugin: randomNumber v2.0 (zeroPad plug-in optional)*/
function randomNumber(nod){nod="number"===typeof nod?17>Math.abs(nod)?Math.round(Math.abs(nod)):17:10;for(var a="1",c=0;c<nod;c++) a+="0";a=Number(a);a=Math.floor(Math.random().toFixed(nod)*a)+"";a.length!==nod&&"undefined"!==typeof zeroPad&&(a=zeroPad(a,nod)); return a};

/* Adobe Consulting Plugin: twoDecimals v1.0 */
function twoDecimals(v){return"undefined"===typeof v||void 0===v||isNaN(v)?0:Number(Number(v).toFixed(2))};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `zeroPad` 메서드는 다음 인수를 사용합니다.

* **num** (필수, 정수):패드할 번호입니다. 이 인수에 소수 자릿수가 포함된 경우 이 인수의 값을 반올림합니다.
* **nod** (필수, 정수):최종 반환 값의 숫자. 패드할 숫자의 자릿수가 패드할 자릿수보다 적은 경우 플러그인은 `num` 인수의 시작 부분에 0을 추가합니다.

이 `randomNumber` 메서드는 다음 인수를 사용합니다.

* **nod** (선택 사항, 정수):생성할 난수의 숫자 수입니다. 최대값은 17자리입니다. 기본값은 10자리입니다.

이 `twoDecimals` 메서드는 다음 인수를 사용합니다.

* **val** (필수, 숫자):가장 가까운 100번째 값으로 반올림할 숫자(문자열 또는 숫자 개체 중 하나로 표시됨)

## 반환

* 0Pad **** 메서드는 `num` 인수와 같은 문자열을 반환하지만, 값의 시작 부분에 특정 0의 수가 추가되어 반환 값의 정확한 수를 보장합니다.
* randomNumber **** 메서드는 원하는 자릿수의 난수와 같은 문자열을 반환합니다.
* 2 **Decimals** 메서드는 가장 가까운 100분의 1로 반올림된 숫자 개체를 반환합니다.

## 호출 예

### zeroPad 예제

```js
s.eVar25 = zeroPad(25.5562, 5) //sets eVar25 equal to "00025"

s.prop1 = zeroPad(25, 1) //sets prop1 equal to "25"

s.prop1 = zeroPad(232425235,23) //sets prop1 equal to "00000000000000232425235"
```

### randomNumber 예제

```js
s.eVar65 = randomNumber(15) //sets eVar65 equal to "721759731750342" or some other random 15-digit number

randomNumber() //returns a random 10-digit number but is useless since this isn't used in an expression

var j = randomNumber(35) //sets a variable named j equal to "15476068651810060" or another random 17-digit number
```

### 2Decimals 예제

```js
s.events = "event10=" + twoDecimals("85.4827128694") //sets s.events="event10=85.48"

var fivehundredthirtytwo = twoDecimals(532.000000001) //sets the variable fivehundredthirtytwo equal to 532

s.eVar65 = twoDecimals("672132.9699736457") //sets s.eVar65 equal to 672132.97
```

## 버전 내역

### 1.0(2019년 5월 25일)

* 초기 릴리스.
