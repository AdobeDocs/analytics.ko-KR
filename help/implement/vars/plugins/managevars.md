---
title: manageVars
description: 한 번에 두 개 이상의 Analytics 변수 값을 변경합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe 플러그인: manageVars

>[!IMPORTANT] 이 플러그인은 Adobe Analytics를 최대한 활용할 수 있도록 Adobe Consulting에서 무료로 제공합니다. Adobe 고객 지원 팀에서는 설치 또는 문제 해결 등 이 플러그인에 대한 지원을 제공하지 않습니다. 이 플러그인에 대한 도움이 필요한 경우 조직의 계정 관리자에게 문의하십시오. 계정 관리자가 도와줄 컨설턴트와의 만남을 주선할 수 있습니다.

`manageVars` 플러그인을 사용하면 여러 Analytics 변수의 값을 한 번에 조작할 수 있습니다. 값을 소문자로 설정하거나 여러 변수 값에서 불필요한 문자를 동시에 제거할 수도 있습니다. 여러 변수의 값을 한 번에 정리하려면 이 플러그인을 사용하는 것이 좋습니다.

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
   * 작업 유형: manageVars 초기화
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
/* Adobe Consulting Plugin: manageVars v2.1 (Requires pt plug-in and other necessary callback plug-ins) */
s.manageVars=function(cb,l,il){var s=this;if(!s[cb])return!1;l=l||"";il=il||!0;var a,d="pageName,purchaseID,channel,server, pageType,campaign,state,zip,events,products,transactionID";for(a=1;76>a;a++)d+=",prop"+a;for(a=1;251>a;a++)d+=",eVar"+a;for(a=1;6>a;a++)d+=",hier"+a;for(a=1;4>a;a++)d+=",list"+a;for(a in s.contextData)d+=",contextData."+a;if(l){if(1==il)d=l.replace("['", ".").replace("']","");else if(0==il){l=l.split(",");il=d.split(",");d="";for(x in l)for(y in-1<l[x].indexOf("contextData")&& (l[x]="contextData."+l[x].split("'")[1]),il)l[x]===il[y]&&(il[y]="");for(y in il)d+=il[y]?","+il[y]:""}s.pt(d,",",cb,0);return!0} return""===l&&il?(s.pt(d,",",cb,0),!0):!1};

/* Adobe Consulting Plugin: lowerCaseVars for manageVars (Requires manageVars plug-in) */
s.lowerCaseVars=function(v){var s=this;s[v]&&("events"!==v&&-1===v.indexOf("contextData")?(s[v]=s[v].toString(),0!== s[v].indexOf("D=")&&(s[v]=s[v].toLowerCase())):-1<v.indexOf("contextData")&&(v=v.substring(v.indexOf(".")+1),s.contextData[v]&& (s.contextData[v]=s.contextData[v].toString().toLowerCase())))};

/* Adobe Consulting Plugin: cleanStr for manageVars (Requires manageVars and cleanStr plug-ins) */
s.cleanStr=function(v){var s=this;s[v]&&"function"!==typeof cleanStr&&(0>v.indexOf("contextData")?s[v]=cleanStr(s[v]): (v=v.substring(v.indexOf(".")+1),s.contextData[v]&&(s.contextData[v]=cleanStr(s.contextData[v].toString()))))};

/* Adobe Consulting Plugin: cleanStr v1.0 */
function cleanStr(str){if("string"===typeof str){str=str.replace(/<\/?[^>]+(>|$)/g,"").trim().replace(/[\u2018\u2019\u201A]/g, "'").replace(/\t+/g,"").replace(/[\n\r]/g," ");for(;-1<str.indexOf("  ");)str=str.replace(/\s\s/g," ");return str}return""};

/* Adobe Consulting Plugin: pt v2.01 */
s.pt=function(l,de,cf,fa){if(l&&this[cf]){l=l.split(de||",");de=l.length;for(var e,c=0;c<de;c++)if(e=this[cf](l[c],fa))return e}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## 플러그인 사용

`manageVars` 메서드에서는 다음 인수를 사용합니다.

* **`cb`** (필수, 문자열): 플러그인이 Analytics 변수를 조작하는 데 사용하는 콜백 함수의 이름입니다. `cleanStr`과 같은 Adobe 기능이나 사용자 지정 기능을 사용할 수 있습니다.
* **`l`** (선택 사항, 문자열): 조작하려는 Analytics 변수의 쉼표로 구분된 목록입니다. 설정하지 않으면 기본값은 다음을 포함한 모든 Adobe Analytics 변수로 설정됩니다.
   * `pageName`
   * `purchaseID`
   * `channel`
   * `server`
   * `pageType`
   * `campaign`
   * `state`
   * `zip`
   * `events`
   * `products`
   * `transactionID`
   * 모든 prop
   * 모든 eVar
   * 모든 계층 변수
   * 모든 목록 변수
   * 모든 컨텍스트 데이터 변수
* **`Il`** (선택 사항, 부울): `l` 인수에 선언된 변수 목록을 포함하지 않고 *제외*&#x200B;하려면 `false`로 설정하십시오. 기본값은 `true`입니다.

이 메서드를 호출하면 아무 것도 반환되지 않습니다. 대신 원하는 콜백 함수를 기반으로 Analytics 변수의 값을 변경합니다.

## 호출 예

### 예 #1

다음 코드...

```js
s.manageVars("lowerCaseVars");
```

...은(는) 위에서 설명한 모든 변수의 값을 소문자로 변경합니다.  일부 이벤트(예: scAdd, scCheckout 등)는 대/소문자를 구분하며 소문자를 사용하지 않아야 하므로 위 코드에 대한 유일한 예외는 events 변수입니다.

### 예 #2

다음 코드...

```js
s.manageVars("lowerCaseVars", "events", false);
```

...은(는) 기본적으로 events 변수가 소문자화되지 않으므로 첫 번째 예와 동일한 결과를 생성합니다.

### 예 #3

다음 코드...

```js
s.manageVars("lowerCaseVars", "eVar1,eVar2,eVar3,list2");
```

...은(는) eVar1, eVar2, eVar3 및 list2의 값만 변경합니다(예: 소문자).

### 예 #4

다음 코드...

```js
s.manageVars("lowerCaseVars", "eVar1,eVar2,eVar3,list2", false);
```

...은(는) eVar1, eVar2, eVar3 및 list2를 제외하고 위에 설명된 모든 변수의 값을 변경합니다(예: 소문자).

### 예 #5

다음 코드...

```js
s.manageVars("cleanStr");
```

...은(는) events 변수를 포함하여 위에 설명된 모든 변수의 값을 변경합니다. 특히 cleanStr 콜백 함수는 각 변수의 값에 대해 다음을 수행합니다.

* HTML 인코딩 제거
* 값의 시작과 끝에 있는 공백 제거
* 왼쪽/오른쪽 작은 따옴표(예: ’)를 곧은 작은따옴표(&#39;)로 바꾸기
* 탭 문자, 줄바꿈 문자 및 캐리지 리턴 문자를 공백으로 바꾸기
* 모든 이중(또는 삼중 등) 공백을 단일 공백으로 바꾸기

## 버전 기록

### 2.1(2019년 1월 14일)

* Internet Explorer 11 브라우저에 대한 버그 수정.
* `s.cleanStr`에 대한 변경 사항 - 이제 일반적인 `cleanStr` 함수를 사용합니다.

### 2.0(2018년 5월 7일)

* 포인트 릴리스(플러그인의 전체 재분석/다시 작성 포함)
* `cleanStr` 콜백 함수를 추가했습니다.
