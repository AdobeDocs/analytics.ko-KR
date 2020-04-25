---
title: getGeoCoordinates
description: 방문자의 geoLocation을 추적합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe 플러그인: getGeoCoordinates

>[!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getGeoCoordinates` 플러그인을 사용하면 방문자 장치의 위도와 경도를 캡처할 수 있습니다. Analytics 변수에서 지리적 위치 데이터를 캡처하려면 이 플러그인을 사용하는 것이 좋습니다.

## Adobe Experience Platform Launch 확장을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해주는 확장을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그] 단추를 클릭합니다.
1. [!UICONTROL 일반적인 Analytics 플러그인] 확장을 설치 및 게시합니다.
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨(페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: getGeoCoordinates 초기화
1. 변경 사항을 저장하고 규칙에 게시합니다.

## Launch 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
1. [!UICONTROL 사용자 지정 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 단추가 표시됩니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여 넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여 넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getGeoCoordinates v1.0 */
s.getGeoCoordinates=function(){var d=this,b="",a=d.c_r("s_ggc").split("|"),e={timeout:5E3,maximumAge:0},f=function(c){c=c.coords;var a=new Date;a.setTime(a.getTime()+18E5);d.c_w("s_ggc",parseFloat(c.latitude.toFixed(4))+"|"+parseFloat(c.longitude.toFixed(4)),a); b="latitude="+parseFloat(c.latitude.toFixed(4))+" | longitude="+parseFloat(c.longitude.toFixed(4))},g=function(a){b="error retrieving geo coordinates"};1<a.length&&(b="latitude="+a[0]+" | longitude="+a[1]);navigator.geolocation&& navigator.geolocation.getCurrentPosition(f,g,e);""===b&&(b="geo coordinates not available");return b};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getGeoCoordinates` 메서드는 인수를 사용하지 않으며 다음 값 중 하나를 반환합니다.

* `"geo coordinates not available"`: 플러그인이 실행되는 시점에 사용할 수 있는 지리적 위치 데이터가 없는 장치의 경우. 이 값은 방문의 첫 번째 히트에서 일반적입니다. 특히 방문자가 위치 추적에 대해 먼저 동의해야 할 때 사용됩니다.
* `"error retrieving geo coordinates"`: 장치의 위치를 검색하려고 할 때 플러그인에 오류가 발생하는 경우.
* `"latitude=[LATITUDE] | longtitude=[LONGITUDE]"`: 여기서 [LATITUDE]/[LONGITUDE]는 각각 위도와 경도입니다.

>[!NOTE] 좌표 값은 가장 가까운 소수 넷째 자리로 반올림됩니다. 예를 들어 `"40.438635333"`이라는 값은 캡처할 고유 값들의 개수를 제한하기 위해 `"40.4386"`으로 반올림됩니다. 이러한 값은 약 20피트 내에서 장치의 정확한 위치를 찾아낼 수 있을 만큼 가깝습니다.

이 플러그인은 필요한 경우 `"s_ggc"`라는 쿠키를 사용하여 히트 간 좌표를 저장합니다.

## 호출 예

### 예 #1

다음 코드...

```js
s.eVar1 = s.getGeoCoordinates();
```

...은(는) 방문자의 장치 상태에 따라 eVar1을 위의 반환 값 중 하나와 동일하게 설정합니다.

### 예 #2

다음 코드는 위도와 경도를 다른 코드/애플리케이션에서 사용할 수 있도록 finalLatitude와 finalLongitude라는 자체 변수에 추출합니다.

```js
var coordinates = s.getGeoCoordinates();
if(coordinates.indexOf("latitude") > -1)
{
  var finalLatitude = Number(coordinates.split("|")[0].trim().split("=")[1]),
  finalLongitude = Number(coordinates.split("|")[1].trim().split("=")[1]);
}
```

여기에서 방문자가 특정 위치(예: 자유의 여신상)에 있는지 여부를 확인할 수 있습니다.

```js
if(finalLatitude >= 40.6891 && finalLatitude <= 40.6893 && finalLongtude >= -74.0446 && finalLongitude <= -74.0444)
  var visitorAtStatueOfLiberty = true;
else
  var visitorAtStatueOfLiberty = false;
```

## 버전 기록

### 1.0(2015년 5월 25일)

* 초기 릴리스.
