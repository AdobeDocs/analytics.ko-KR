---
title: cleanStr
description: 문자열에서 불필요한 모든 문자를 제거하거나 바꿉니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe 플러그인:cleanStr

> [!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 제공합니다. Adobe 고객 지원 센터에서는 설치 또는 문제 해결을 포함하여 이 플러그인을 지원하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 그들은 도움을 받기 위해 컨설턴트와 회의를 예약할 수 있다.

이 `cleanStr` 플러그인은 HTML 태그 문자, 추가 공백, 탭, 줄바꿈/캐리지 리턴 등 문자열에서 불필요한 모든 문자를 제거하거나 대체합니다. 또한 왼쪽/오른쪽 작은 따옴표(`‘` 및 `’`)를 곧은 작은 따옴표(`'`)로 바꿉니다. 변수 값에서 불필요한 문자를 제거하려면 이 플러그인을 사용하는 것이 좋습니다. Launch의 &#39;텍스트 정리&#39; 기능은 구현 요구 사항을 충족하지 않습니다. 수집된 데이터에 불필요한 문자가 포함되어 있지 않거나 Launch의 &#39;텍스트 정리&#39; 기능이 충분한 경우 이 플러그인은 필요하지 않습니다.

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
   * 작업 유형:CleanStr 초기화
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
/* Adobe Consulting Plugin: cleanStr v1.0 */
function cleanStr(str){if("string"===typeof str){str=str.replace(/<\/?[^>]+(>|$)/g,"");str=str.trim(); str=str.replace(/[\u2018\u2019\u201A]/g,"'");str=str.replace(/\t+/g,"");for(str=str.replace(/[\n\r]/g," ");-1<str.indexOf("  ");)str=str.replace(/\s\s/g," ");return str}return""};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

이 `cleanStr` 메서드는 다음 인수를 사용합니다.

* **`str`** (필수, 문자열):HTML 인코딩, 추가 공백, 탭 또는 기타 불필요한 문자를 정리할 값입니다.

이 메서드는 불필요한 모든 문자가 제거된 `str` 인수의 값을 반환합니다.

## 예

### 예 #1

다음과 같이 가정합니다. 여기서 점들은 공백을 나타내고 화살표는 탭 문자를 나타냅니다.

```js
s.eVar1 = "»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

다음 코드를 실행할 때...

```js
s.eVar1 = cleanStr(s.eVar1)
```

...eVar1은 &quot;this is a messystring&quot;으로 설정됩니다(모든 추가 공백 및 모든 탭 문자 제거).

### 예 #2

...

```js
s.eVar1 = "»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

...다음 코드가 실행됩니다.

```js
cleanStr(s.eVar1)
```

...s.eVar1의 최종 값은 여전히 다음과 같습니다.

```js
"»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

반환 값을 변수에 지정하지 않고 플러그인을 모두 실행해도 실제로는 str 인수를 통해 전달된 변수가 &quot;재설정&quot;되지 않습니다.

## 버전 내역

### 1.0(2018년 4월 15일)

* 초기 릴리스.
