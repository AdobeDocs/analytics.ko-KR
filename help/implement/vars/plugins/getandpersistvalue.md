---
title: getAndPersistValue
description: 언제든지 나중에 검색할 수 있는 값을 저장합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe 플러그인: getAndPersistValue

>[!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`getAndPersistValue` 플러그인을 사용하면 방문 중에 나중에 검색할 수 있는 쿠키에 값을 저장할 수 있습니다. It serves a similar role to the [!UICONTROL Storage duration] feature in Adobe Experience Platform Launch. 변수가 설정된 후 Analytics 변수를 후속 히트에서 동일한 값으로 자동으로 유지하려면 이 플러그인을 사용하는 것이 좋습니다. This plug-in is not necessary if Launch&#39;s [!UICONTROL Storage duration] feature is sufficient, or if you do not need to set and persist variables to the same value in subsequent hits. eVar 변수는 Adobe에 의해 서버측에서 지속되므로 이 변수의 기본적인 지속성에서는 이 플러그인을 사용할 필요가 없습니다.

## Adobe Experience Platform Launch 확장을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해주는 확장을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. 확장 [!UICONTROL Common Analytics Plugins] 프로그램 설치 및 게시
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨(페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: getAndPersistValue 초기화
1. 변경 사항을 저장하고 규칙에 게시합니다.

## Launch 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. Go to the [!UICONTROL Extensions] tab, then click the [!UICONTROL Configure] button under the Adobe Analytics extension.
1. 단추를 표시하는 [!UICONTROL Configure tracking using custom code] 아코디언을 [!UICONTROL Open Editor] 확장합니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여 넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여 넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getAndPersistValue v2.0 */
s.getAndPersistValue=function(vtp,cn,ex){var b=new Date;cn=cn?cn:"s_gapv";(ex=ex?ex:0)?b.setTime(b.getTime()+864E5*ex): b.setTime(b.getTime()+18E5);vtp||(vtp=this.c_r(cn));this.c_w(cn,vtp,b);return vtp};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`getAndPersist` 메서드에서는 다음 인수를 사용합니다.

* **`vtp`** (필수): 페이지에서 페이지로 유지할 값입니다.
* **`cn`** (선택 사항): 값을 저장할 쿠키의 이름입니다. 이 인수를 설정하지 않으면 쿠키의 이름이 `"s_gapv"`로 지정됩니다.
* **`ex`** (선택 사항): 쿠키가 만료될 때까지 남은 일 수입니다. 이 인수가 `0`이거나 설정되지 않으면 방문이 끝날 때(30분 동안 활동이 없음) 쿠키가 만료됩니다.

`vtp` 인수의 변수가 설정되면 플러그인은 쿠키를 설정한 후 쿠키 값을 반환합니다. `vtp` 인수의 변수가 설정되지 않으면 플러그인은 쿠키 값 반환만 수행합니다.

## 예

### 예 #1

다음 코드는 eVar21을 &quot;hello&quot;라는 값과 동일하게 설정합니다. 그러면 이 코드는 28일 후에 만료되고 eVar21의 값과 같은 ev21gapv 쿠키를 설정합니다(즉, &quot;hello&quot;). 그러면 코드는 eVar21을 ev21gapv 쿠키의 값과 동일하게 (재)설정합니다.

```js
s.eVar21 = "hello";
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### 예 #2

eVar21이 현재 페이지에 아직 설정되지 않았지만 지난 28일 내에 이전 페이지에서 &quot;hello&quot;로 설정되었다고 가정하십시오. 다음 코드는 eVar21만을 ev21gapv 쿠키의 값(즉, &quot;hello&quot;)과 동일하게 설정합니다. eVar21이 함수가 호출되기 전에 현재 페이지에서 설정되지 않았으므로 이 코드를 실행해도 ev21gapv 쿠키가 재설정되지는 않습니다.

```js
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### 예 #3

eVar21이 현재 페이지에 아직 설정되지 않았지만 지난 28일 내에 이전 페이지에서 &quot;hello&quot;로 설정되었다고 가정하십시오. 다음 코드는 prop35만을 ev21gapv 쿠키의 값(즉, &quot;hello&quot;)과 동일하게 설정합니다.  eVar21은 설정하지 않습니다.

```js
s.prop35 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### 예 #4

다음 코드는 eVar21을 &quot;howdy&quot;라는 값과 동일하게 설정합니다.  그러면 이 코드는  28일 후에 만료되고 eVar21의 값과 같은 ev21gapv 쿠키를 설정(또는 재설정)합니다(즉, &quot;howdy&quot;). 그런 다음 이 코드는 prop35를 ev21gapv 쿠키의 값(즉, &quot;howdy&quot;)과 동일하게 설정합니다.

```js
s.eVar21 = "howdy";
s.prop35 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### 예 #5

s.eVar21이 지난 28일 내에 어떤 페이지에서도 설정되지 않았다고 가정하십시오. 다음 코드는 ev21gapv 쿠키가 마지막으로 설정되고 28일 후 만료되었으므로 s.eVar21을 nothing과 동일하게 설정합니다.

```js
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### 예 #6

다음 코드는 eVar30을 &quot;shopping&quot;과 동일하게 설정합니다. 그런 다음, 브라우저 세션이 끝날 때 만료되는 s_gapv 쿠키를 s.eVar30의 값과 동일하게 설정합니다(즉, &quot;shopping&quot;). 그런 다음 s.eVar30을 s_gapv 쿠키의 값과 동일하게 설정합니다(즉, getAndPersistValue 호출은 s_gapv 쿠키의 값을 반환하며, 이 경우 그 값은 &quot;shopping&quot;).

```js
s.eVar30 = "shopping";
s.eVar30 = s.getAndPersistValue(s.eVar30);
```

s.eVar30이 세션 중에 표시되는 추가 페이지에 명시적 값으로 설정되어 있지 않지만 다음 코드를 통해 설정되는 경우(doPlugins에서)...

```js
s.eVar30 = s.getAndPersistValue(s.eVar30);
```

...s.eVar30은 &quot;shopping&quot;(즉, s_gapv 쿠키의 지속적인 값)으로 설정됩니다.

## 버전 기록

### 2.0(2018년 4월 16일)

* 포인트 릴리스(작은 코드 크기)
* 이제 0을 `ex` 인수에 전달하면 브라우저 세션이 끝날 때 만료되지 않고 30분 동안 아무 활동이 없으면 만료가 강제 적용됩니다.

### 1.0(2016년 1월 18일)

* 초기 릴리스.
