---
title: getNewRepeat
description: 신규 방문자와 반복 방문자의 활동을 추적합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:getNewRepeat

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `getNewRepeat` 플러그인을 사용하면 원하는 일 수 내에 사이트 방문자가 새 방문자인지 반복 방문자인지를 확인할 수 있습니다. 사용자 지정 일 수를 사용하여 방문자를 &quot;신규&quot;로 식별하려면 이 플러그인을 사용하는 것이 좋습니다. 분석 작업 공간의 새/반복 방문자 차원이 조직의 요구 사항에 맞는 경우 이 플러그인은 불필요합니다.

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
   * 작업 유형:getNewRepeat 초기화
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
/* Adobe Consulting Plugin: getNewRepeat v2.1 */
s.getNewRepeat=function(d){d=d?d:30;var s=this,p="s_nr"+d,b=new Date,e=s.c_r(p),f=e.split("-"),c=b.getTime();b.setTime(c+864E5*d); if(""===e||18E4>c-f[0]&&"New"===f[1])return s.c_w(p,c+"-New",b),"New";s.c_w(p,c+"-Repeat",b);return"Repeat"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `getNewRepeat` 메서드는 다음 인수를 사용합니다.

* **`d`** (정수, 선택 사항):방문자를 다시 로 재설정하는 방문 간 필요한 최소 일 `"New"`수입니다. 이 인수를 설정하지 않으면 기본값은 30일입니다.

이 메서드는 플러그인으로 설정된 쿠키가 없거나 만료된 `"New"` 경우 값을 반환합니다. 플러그인으로 설정된 쿠키가 존재하는지 `"Repeat"` 여부와 현재 히트 이후의 시간 및 쿠키에 설정된 시간이 30분 이상인 경우 값을 반환합니다. 이 메서드는 전체 방문에 대해 동일한 값을 반환합니다.

이 플러그인은 `"s_nr[LENGTH]"` 인수와 `[LENGTH]` 동일한 `d` 위치에 있는 쿠키를 사용합니다. 쿠키에는 현재 시간과 방문자의 현재 상태를 나타내는 Unix 타임스탬프가 포함되어`"New"` 있습니다(또는 `"Repeat"`).

## 호출 예

### 예 #1

다음 코드는 새 방문자에 대해 s.eVar1을 &quot;새로 만들기&quot;의 값과 동일하게 설정하고, 방문자의 사이트 방문 중 나머지 동안 &quot;새로 만들기&quot;(각 새 호출 사용)의 값과 같은 s.eVar1을 계속 설정합니다.

```js
s.eVar1=s.getNewRepeat();
```

### 예 #2

방문자가 마지막 s.getNewRepeat()가 호출된 이후 31분에서 30일 동안 언제든지 사이트로 돌아오는 경우, 다음 코드는 s.eVar1을 &quot;Repeat&quot;의 값과 동일하게 설정하고 방문자의 나머지 사이트 방문 동안 s.eVar1을 &quot;Repeat&quot;의 값과 동일하게 설정합니다(새로운 호출이 있을 경우).

```js
s.eVar1=s.getNewRepeat();
```

### 예 #3

방문자가 마지막으로 s.getNewRepeat()가 호출된 이후 최소 30일 동안 사이트에 있지 않은 경우, 다음 코드는 s.eVar1을 &quot;New&quot;의 값과 동일하게 설정하고 방문자의 나머지 사이트 방문 동안 s.eVar1을 &quot;New&quot;의 값과 동일하게 설정합니다(새로운 각 호출 사용).

```js
s.eVar1=s.getNewRepeat();
```

### 예 #4

방문자가 마지막 s.getNewRepeat()가 호출된 이후 31분에서 365일(즉, 1년)에 언제든지 사이트로 돌아오는 경우, 다음 코드는 s.eVar1을 &quot;Repeat&quot;의 값과 동일하게 설정하고 나머지 호출 동안 s.eVar1을 &quot;Repeat&quot;의 값과 동일하게 설정합니다. 방문자의 사이트 방문.

```js
s.eVar1=s.getNewRepeat(365);
```

### 예 #5

방문자가 마지막 s.getNewRepeat()가 호출된 이후 최소 365일(즉, 1년) 동안 사이트에 있지 않은 경우, 다음 코드는 s.eVar1을 &quot;New&quot;의 값과 동일하게 설정하고 나머지 방문자 전체에서 s.eVar1을 &quot;New&quot;의 값과 동일하게 설정합니다. 사이트를 방문합니다.

```js
s.eVar1=s.getNewRepeat(365);
```

## 버전 내역

### 2.1(2019년 9월 30일)

* 플러그인 크기를 줄이기 위한 JavaScript 로직의 재구성

### 2.0(2018년 4월 16일)

* 더 작은 코드 크기로 다시 컴파일
* 방문 정보를 저장할 쿠키의 이름을 지정하는 기능을 제거했습니다. 이제 플러그인은 `d` 인수로 전달된 값을 기준으로 쿠키의 이름을 동적으로 지정합니다.
