---
title: p_fo (첫 번째 페이지만)
description: 특정 루틴이 페이지당 한 번만 실행되도록 합니다.
feature: Variables
exl-id: e82d77f9-2ea9-4b1b-b645-b12879c344ec
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 100%

---

# Adobe 플러그인: p_fo (첫 번째 페이지만)

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`p_fo` 플러그인은 특정 JavaScript 개체가 있는지 확인하는 유틸리티입니다. 해당 개체가 없으면 플러그인이 개체를 만들고 `true`를 반환합니다. 페이지에 JavaScript 개체가 이미 있으면 `false`를 반환합니다. 이 플러그인은 페이지에서 코드를 정확히 한 번만 실행하는 데 유용합니다. 몇 가지 다른 플러그인은 이 코드를 사용하여 작동합니다. 페이지에서 코드가 몇 번 실행되는지 걱정되지 않거나 종속 플러그인을 사용하지 않는 경우에는 이 플러그인이 필요하지 않습니다.

## Adobe Experience Platform의 태그를 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해 주는 확장 기능을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [데이터 수집 UI](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그] 버튼을 클릭합니다.
1. [!UICONTROL 일반적인 Analytics 플러그인] 확장 기능을 설치 및 게시합니다.
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨 (페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: p_fo 초기화
1. 변경 사항을 저장하고 규칙에 퍼블리싱합니다.

## 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [데이터 수집 UI](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 [!UICONTROL 구성] 버튼을 클릭합니다.
1. [!UICONTROL 사용자 지정 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 버튼이 표시됩니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화 ([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v3.0 (Requires AppMeasurement) */
function p_fo(c){if("-v"===c)return{plugin:"p_fo",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c){a=b;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.p_fo="3.0");window.__fo||(window.__fo={});if(window.__fo[c])return!1;window.__fo[c]={};return!0};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`p_fo` 함수에서는 다음 인수를 사용합니다.

* **on** (필수, 문자열): 개체가 페이지에 아직 없을 경우 플러그인이 생성하는 JavaScript 개체의 이름입니다.

개체가 아직 없으면 이 함수는 `true`를 반환하고 개체를 만듭니다. 개체가 이미 있으면 이 함수는 `false`를 반환합니다.

## 호출 예

### 예 #1

다음 코드는 페이지 내에 &quot;myobject&quot; 개체가 있는지 확인합니다.  myobject 개체가 없으면 코드는 &quot;myobject&quot; 개체를 만들고 true 값을 반환합니다.  따라서 조건문 (즉, Console.log (&#39;hello&#39;);) 내의 코드가 실행됩니다.

반면에 p_fo 호출이 발생할 때 &quot;myobject&quot; 개체가 이미 있으면 p_fo 함수는 false 값을 반환하며, 따라서 조건문은 false로 간주됩니다.  이 경우 조건문 내의 코드는 실행되지 않습니다.

```js
if(p_fo("myobject"))
{
  console.log("hello");
}
```

**참고:** 새 페이지 개체/DOM이 로드되거나 현재 페이지가 다시 로드될 때마다 on 인수에 지정된 개체가 더 이상 존재하지 않으므로 페이지 로드가 완료된 후 처음 실행될 때 p_fo 플러그인은 다시 true를 반환합니다.

## 버전 내역

### 3.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 2.0

* 포인트 릴리스 (다시 컴파일됨, 더 작은 코드 크기).
* 반환 값 유형을 정수에서 부울로 변경했습니다.

### 1.0

* 초기 릴리스.
