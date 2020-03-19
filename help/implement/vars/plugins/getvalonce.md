---
title: getValOnce
description: Analytics 변수가 한 행에서 동일한 값으로 두 번 설정되지 않도록 합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:getValOnce

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

플러그인을 `getValOnce` 사용하면 변수가 동일한 값과 같은 값을 두 번 이상 설정할 수 없습니다. 방문자가 페이지를 새로 고치거나 지정된 페이지를 여러 번 방문하는 경우의 중복 제거를 원할 경우 이 플러그인을 사용하는 것이 좋습니다. 분석 작업 공간에서 &#39;발생&#39; 지표가 걱정되지 않는 경우 이 플러그인은 불필요합니다.

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
   * 작업 유형:getValOnce 초기화
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
/* Adobe Consulting Plugin: getValOnce v2.0 */
s.getValOnce=function(vtc,cn,et,ep){if(vtc&&(cn=cn||"s_gvo",et=et||0,ep="m"===ep?6E4:864E5,vtc!==this.c_r(cn))){var e=new Date;e.setTime(e.getTime()+et*ep);this.c_w(cn,vtc,0===et?0:ep);return vtc}return""};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `getValOnce` 메서드는 다음 인수를 사용합니다.

* **`vtc`** (필수, 문자열):변수가 이전에 동일한 값으로 설정되었는지 확인하고 확인하는 변수
* **`cn`** (선택 사항, 문자열):확인할 값이 들어 있는 쿠키의 이름입니다. 기본값은 `"s_gvo"`
* **`et`** (선택 사항, 정수):쿠키의 만료 기간(일 단위 또는 `ep` 인수에 따라 분)입니다. 기본값은 `0`로, 브라우저 세션이 끝날 때 만료됩니다.
* **`ep`** (선택 사항, 문자열):인수가 설정되는 경우에만 이 `et` 인수를 설정합니다. 인수가 일 대신 분 내에 만료되도록 하려면 이 인수를 `"m"` 설정합니다 `et` . 기본값은 `"d"`로, 일 단위로 `et` 인수를 설정합니다.

인수와 쿠키 값이 일치하는 경우 이 메서드는 빈 문자열을 반환합니다. `vtc` 인수와 쿠키 값이 일치하지 않으면 이 메서드는 `vtc` `vtc` 인수를 문자열로 반환합니다.

## 호출 예

### 예 #1

다음 30일 동안 동일한 값이 s.campaign에 두 번 이상 전달되지 않도록 하려면 이 호출을 사용하십시오.

```js
s.campaign=s.getValOnce(s.campaign,"s_campaign",30);
```

위의 호출에서 플러그인은 먼저 s_campaign 쿠키에 이미 포함된 값을 현재 s.campaign 변수에서 나오는 값과 비교합니다.   일치하는 항목이 없으면 플러그인은 s_campaign 쿠키를 s.campaign에서 오는 새 값과 동일하게 설정한 다음 새 값을 반환합니다.   이 비교는 앞으로 30일 동안 있을 것이다

### 예 #2

세션 전체에서 동일한 값이 설정되지 않도록 하려면 이 호출을 사용하십시오.

```js
s.eVar2=s.getValOnce(s.eVar2,"s_ev2",0,"m");
```

이 코드는 사용자 세션 전체에서 한 행에 동일한 값이 두 번 이상 s.eVar2로 전달되지 않도록 합니다.  또한 만료 시간이 0으로 설정되므로(호출 종료 시) 양식에서 &quot;m&quot; 값을 무시합니다.   또한 코드는 s_ev2 쿠키에 비교 값을 저장합니다.

## 버전 내역

### 2.0

* 포인트 릴리스(다시 컴파일되고 더 작은 코드 크기).

### 1.1

* 매개 변수를 통해 만료 시 분 또는 일을 선택하는 옵션이 `t` 추가되었습니다.
* 플러그인으로 제한하는 데 사용되는 `k` 변수의 범위를 수정했습니다. 이 변경 사항은 페이지의 다른 코드에 대한 간섭을 방지합니다.
