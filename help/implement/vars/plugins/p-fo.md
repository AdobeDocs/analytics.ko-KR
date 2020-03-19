---
title: p_fo(페이지 첫 번째 전용)
description: 특정 루틴이 페이지당 한 번만 실행되는지 확인합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:p_fo(페이지 첫 번째 전용)

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `p_fo` 플러그인은 특정 JavaScript 개체가 있는지 확인하는 유틸리티입니다. 객체가 없으면 플러그인이 객체를 만들어 반환합니다. `true` 페이지에 JavaScript 객체가 이미 있으면 이 객체가 반환됩니다 `false`. 이 플러그인은 페이지에서 코드를 정확히 한 번만 실행하는 데 유용합니다. 다른 여러 플러그인은 이 코드를 사용하여 작동합니다. 페이지에서 코드가 몇 번 실행되는지 걱정하지 않거나 종속 플러그인을 사용하지 않는 경우 이 플러그인은 불필요합니다.

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
   * 작업 유형:p_fo 초기화
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
/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v2.0 */
s.p_fo=function(on){var s=this;s.__fo||(s.__fo={});if(s.__fo[on])return!1;s.__fo[on]={};return!0};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `p_fo` 메서드는 다음 인수를 사용합니다.

* **설정** (필수, 문자열):객체가 페이지에 아직 없을 경우 플러그인이 생성하는 JavaScript 객체의 이름입니다.

객체가 아직 없으면 이 메서드는 객체를 반환하고 `true` 만듭니다. 객체가 이미 존재하는 경우 이 메서드는 반환됩니다 `false`.

## 호출 예

### 예 #1

다음 코드에서는 페이지 내에 &quot;핵심&quot; 개체가 있는지 확인합니다.  &quot;myobject&quot; 객체가 없는 경우 코드는 &quot;myobject&quot; 객체를 만들고 true 값을 반환합니다.  따라서 조건문(즉, Console.log(&#39;hello&#39;);) 내의 코드가 실행됩니다.

반면에 p_fo 호출이 발생할 때 &quot;myobject&quot; 개체가 이미 존재하는 경우 p_fo 함수는 false 값을 반환하므로 조건문은 false로 간주됩니다.  이 경우 조건문 내의 코드는 실행되지 않습니다.

```javascript
if(s.p_fo("myobject"))
{
  console.log("hello");
}
```

**참고:** 새 페이지 개체/DOM이 로드되거나 현재 페이지가 다시 로드될 때마다 on 인수에 지정된 개체가 더 이상 존재하지 않으므로 p_fo 플러그인은 페이지 로드가 완료된 후 처음 실행될 때 다시 true를 반환합니다.

## 버전 내역

### 2.0

* 포인트 릴리스(다시 컴파일되고 더 작은 코드 크기).
* 반환 값 유형을 정수에서 부울로 변경했습니다.

### 1.0

* 초기 릴리스.
