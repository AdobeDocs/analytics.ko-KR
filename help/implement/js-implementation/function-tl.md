---
description: JavaScript용 AppMeasurement 파일에 설정된 매개 변수를 기반으로 파일 다운로드 및 종료 링크를 자동으로 추적할 수 있습니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Link tracking
title: s.tl() 함수 - 링크 추적
topic: Developer and implementation
uuid: f28f071a-8820-4f74-89cd-fd2333a21f22
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.tl() 함수 - 링크 추적

조직에서 추적할 링크 및 동작을 제어하려면 수동 링크 추적을 사용하는 것이 좋습니다. 원하는 정확한 콘텐츠와 함께 링크 추적 이미지 요청을 수동으로 전송하려면 s.tl() 함수를 사용합니다. 기본 링크 추적만 필요한 경우에는 [구성 변수](c-variables/configuration-variables.md)의 `s.trackDownloadLinks` 및 `s.trackExternalLinks`를 참조하십시오. 사용자 지정 링크는 자동으로 추적할 수 없습니다.

> [!NOTE] 링크 추적 코드는 사이트 및 보고 요구에 따라 다릅니다. 구현 경험 전 또는 구현 컨설턴트가 비즈니스 요구에 따라 이 기능을 사용하는 방법을 파악하는 것이 좋습니다.

## 구문 및 예

기본 구문:

`s.tl(`**`this`**`,`**`linkType`**`,`**`linkName`**`,`**`variableOverrides`**`,`**`doneAction`**`);`

기본 예:

```HTML
<!-- Basic HTML link example-->
<a href="example.html" onClick="s.tl(this,'o','Example link');">Click here</a>
```

```JavaScript
// Basic JavaScript link example
s.tl(this,'o','Example Link');
```

### this/true(필수)

첫 번째 인수는 브라우저가 최대 500밀리초를 기다린 후에 페이지에서 나가는지 여부를 결정합니다. 이미지 요청이 500밀리초 이내로 전송되면 페이지가 클릭한 링크로 즉시 이동합니다.

* `this`: AppMeasurement에 이미지 요청을 전송할 시간을 제공하기 위해 최대 500밀리초를 대기합니다. 기본값.
* `true`: 기다리지 않습니다. 링크가 페이지에서 나가는 경우 이미지 요청이 전송되지 않을 수 있습니다.

링크가 페이지를 나가는 경우에만 지연이 필요합니다.

```JavaScript
// Include 500ms delay
s.tl(this,'o','Example link');

// Do not include 500ms delay
s.tl(true,'o','Example link');
```

### linkType(필수)

초 인수에는 캡처할 링크의 유형에 따라 세 가지 가능한 값이 있습니다. 이미지 요청이 채우는 Adobe Analytics의 차원을 결정합니다.

* `d`: 파일 다운로드
* `e`: 종료 링크
* `o`: 사용자 지정 링크

```JavaScript
// Populates the File Downloads dimension
s.tl(this,'d','Example link');

// Populates the Exit Links dimension
s.tl(this,'e','Example link');

// Populates the Custom Links dimension
s.tl(this,'o','Example link');
```

### linkName(필수)

이 인수는 최대 100바이트를 사용하는 어떤 사용자 지정 값도 될 수 있습니다. 보고에서 차원 값을 결정합니다.

```JavaScript
// Populates the Custom Link dimension with "Referral click to example.com"
s.tl(this,'o','Referral click to example.com');

// Populates the Download link dimension with "Last quarter performance PDF"
s.tl(this,'d','Last quarter performance PDF');
```

### variableOverrides(선택 사항)

단일 호출에 대한 변수 값을 변경할 수 있습니다. doneAction 인수를 사용하고 변수 재정의가 없는 경우 `null`을 사용합니다.

### doneAction(선택 사항)

추적 링크 호출이 완료된 후 실행할 탐색 동작을 지정합니다. `s.useForcedLinkTracking` 및 `s.forcedLinkTrackingTimeout`을 사용해야 합니다. doneAction 변수는 문자열 `navigate`가 될 수 있으며, 이로 인해 메서드가 `document.location`을 `linkObject`의 href 특성으로 설정합니다. 또한 doneAction 변수는 고급 사용자 지정을 허용하는 함수가 될 수 있습니다.

앵커 `onClick` 이벤트에 doneAction에 대한 값을 제공하는 경우, 기본 브라우저 탐색을 방지할 수 있도록 `false` 호출 후에 `s.tl`를 반환해야 합니다.
기본 동작을 미러링하고 href 특성에 의해 지정된 URL을 따르려면 `navigate`의 문자열을 doneAction으로 제공합니다. 선택 사항으로, doneAction으로 이 함수를 전달하여 탐색 이벤트를 처리하도록 자체 함수를 제공할 수 있습니다.

```JavaScript
s.tl(this,'e','Example link',null,'navigate');return false;
```

## 링크 추적에서 JavaScript 함수 사용

링크 추적 코드를 페이지 또는 연결된 JavaScript 파일에 정의된 자체 포함된 JavaScript 함수에 통합할 수 있습니다. 그런 다음 각 링크의 onClick 함수에서 호출을 지정할 수 있습니다.

```JavaScript
// Set in AppMeasurement file or page code
function trackClickInteraction(name){
    s.linkTrackVars='eVar16,eVar17';
    s.eVar16 = name;
    s.eVar17 = s.pageName;
    s.tl(true,'o',name);
}
```

```HTML
<!-- Use wherever you want to track links -->
<a href="example.html" onClick="trackClickInteraction('Example link');">Click here</a>
```

## 중복 링크 카운트 방지 {#section_9C3F73DE758F4727943439DED110543C}

링크가 자동 파일 다운로드나 종료 링크 추적에 의해 링크가 정상적으로 캡처되는 상황에서 링크가 두 번 카운트될 가능성이 있습니다. 예를 들어 PDF 다운로드를 자동으로 추적하는 경우 `s.tl` 호출로 인해 다운로드 카운트가 중복될 수 있습니다.

```JavaScript
function trackDownload(obj) {}
    s.tl(obj,'d','PDF Document');
}
```

링크를 두 번 카운트하지 않도록 다음과 같이 수정한 JavaScript 함수를 사용하십시오:

```JavaScript
function linkCode(obj) {
    var lt = obj.href != null ? s.lt(obj.href) : "";
    if (lt=="") {
        s.tl(obj,'d','PDF Document');
    }
}
```
