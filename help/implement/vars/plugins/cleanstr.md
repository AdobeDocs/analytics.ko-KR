---
title: cleanStr
description: 문자열에서 모든 불필요한 문자를 제거하거나 바꿉니다.
exl-id: d699dcd4-5e0a-40d3-b345-e5b1a077d393
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '529'
ht-degree: 100%

---

# Adobe 플러그인: cleanStr

>[!IMPORTANT]
>
>이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`cleanStr` 플러그인은 HTML 태그 문자, 추가 공백, 탭, 줄바꿈/캐리지 리턴 등 문자열에서 불필요한 모든 문자를 제거하거나 대체합니다. 또한 왼쪽/오른쪽 작은 따옴표 (`‘` 및 `’`)를 곧은 작은 따옴표 (`'`)로 바꿉니다. 변수 값에서 불필요한 문자를 제거하려 하는데 Launch의 &#39;텍스트 정리&#39; 기능이 구현 요구 사항을 충족하지 않는 경우 이 플러그인을 사용하는 것이 좋습니다.습니다. 수집된 데이터에 불필요한 문자가 포함되어 있지 않거나 Launch의 &#39;텍스트 정리&#39; 기능으로 충분한 경우 이 플러그인은 필요하지 않습니다.

## Adobe Experience Platform Launch 확장 기능을 사용하여 플러그인 설치

Adobe는 가장 일반적으로 사용되는 플러그인을 사용할 수 있도록 해 주는 확장 기능을 제공합니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, [!UICONTROL 카탈로그] 버튼을 클릭합니다.
1. [!UICONTROL 일반적인 Analytics 플러그인] 확장 기능을 설치 및 게시합니다.
1. 아직 없다면 다음 구성으로 &quot;플러그인 초기화&quot;라는 레이블이 지정된 규칙을 만듭니다.
   * 조건: 없음
   * 이벤트: 핵심 - 라이브러리가 로드됨 (페이지 상단)
1. 다음 구성으로 위의 규칙에 작업을 추가합니다.
   * 확장: 일반적인 Analytics 플러그인
   * 작업 유형: CleanStr 초기화
1. 변경 사항을 저장하고 규칙에 게시합니다.

## Launch 사용자 지정 코드 편집기를 사용하여 플러그인 설치

플러그인 확장 기능을 사용하지 않으려는 경우 사용자 지정 코드 편집기를 사용할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
1. 원하는 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 확장 아래의 [!UICONTROL 구성] 버튼을 클릭합니다.
1. [!UICONTROL 사용자 지정 코드를 사용하여 추적 구성] 아코디언을 확장합니다. 그러면 [!UICONTROL 편집기 열기] 버튼이 표시됩니다.
1. 사용자 지정 코드 편집기를 열고 아래에 제공된 플러그인 코드를 편집 창에 붙여넣습니다.
1. 변경 사항을 저장하고 Analytics 확장에 게시합니다.

## AppMeasurement를 사용하여 플러그인 설치

Analytics 추적 개체가 인스턴스화 ([`s_gi`](../functions/s-gi.md) 사용)된 후 AppMeasurement 파일의 아무 곳에나 다음 코드를 복사하여 붙여넣으십시오. 구현에서 코드의 주석 및 버전 번호를 보존하면 Adobe에서 잠재적인 문제를 해결하는 데 도움이 됩니다.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: cleanStr v2.0 (No Prerequisites Required) */
function cleanStr(str){var a=str;if("-v"===a)return{plugin:"cleanStr",version:"2.0"};a:{if("undefined"!==typeof window.s_c_il){var b=0;for(var c;b<window.s_c_il.length;b++)if(c=window.s_c_il[b],c._c&&"s_c"===c._c){b=c;break a}}b=void 0}"undefined"!==typeof b&&(b.contextData.cleanStr="2.0");if("string"===typeof a){a=a.replace(/<\/?[^>]+(>|$)/g,"");a=a.trim();a=a.replace(/[\u2018\u2019\u201A]/g,"'");a=a.replace(/\t+/g,"");for(a=a.replace(/[\n\r]/g," ");-1<a.indexOf("  ");)a=a.replace(/\s\s/g," ");return a}return""}
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`cleanStr` 메서드에서는 다음 인수를 사용합니다.

* **`str`**  (필수, 문자열): HTML 인코딩, 추가 공백, 탭 또는 기타 불필요한 문자를 정리할 값입니다.

이 메서드는 모든 불필요한 문자가 제거된 `str` 인수의 값을 반환합니다.

## 예

### 예 #1

다음과 같이 가정하십시오. 여기서 점은 공백을 나타내고 화살표는 탭 문자를 나타냅니다.

```js
s.eVar1 = "»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

다음 코드를 실행하면...

```js
s.eVar1 = cleanStr(s.eVar1)
```

...eVar1은 &quot;this is a messystring&quot;과 같게 됩니다 (모든 추가 공백 및 모든 탭 문자가 제거됨).

### 예 #2

...

```js
s.eVar1 = "»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

...이고, 다음 코드가 실행되면...

```js
cleanStr(s.eVar1)
```

...s.eVar1의 최종 값은 여전히 다음과 같습니다.

```js
"»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

반환 값을 변수에 지정하지 않고 플러그인을 실행해도 실제로 str 인수를 통해 전달된 변수가 &quot;재설정&quot;되지는 않습니다.

## 버전 내역

### 2.0 (2021년 3월 19일)

* 버전 번호를 컨텍스트 데이터로 추가했습니다.

### 1.0 (2018년 4월 15일)

* 초기 릴리스.
