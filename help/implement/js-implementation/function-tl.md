---
description: JavaScript용 AppMeasurement 파일에 설정된 매개 변수를 기반으로 파일 다운로드 및 종료 링크를 자동으로 추적할 수 있습니다.
keywords: Analytics 구현
seo-description: JavaScript용 AppMeasurement 파일에 설정된 매개 변수를 기반으로 파일 다운로드 및 종료 링크를 자동으로 추적할 수 있습니다.
seo-title: s.tl() 함수 - 링크 추적
solution: Analytics
subtopic: 링크 추적
title: s.tl() 함수 - 링크 추적
topic: 개발자 및 구현
uuid: f28f071a-8820-4f74-89cd-fd2333a21f22
translation-type: tm+mt
source-git-commit: 1ed1c6cd3fd6d29fa156cd4b2c4bdfe9120b3c61

---


# s.tl() 함수 - 링크 추적

조직에서 추적하기 위한 링크 및 동작을 보다 세밀하게 제어하려는 경우 수동 링크 추적이 권장됩니다. s.tl() 함수를 사용하여 원하는 정확한 컨텐츠와 함께 링크 추적 이미지 요청을 수동으로 보냅니다. 기본 링크 추적이 필요한 모든 경우 구성 변수 `s.trackDownloadLinks` 및 `s.trackExitLinks` 아래의 [링크를](c-variables/configuration-variables.md)참조하십시오. 사용자 지정 링크는 자동으로 추적할 수 없습니다.

> [!NOTE] 링크 추적 코드는 사이트 및 보고 요구 사항에 따라 매우 구체적입니다. Adobe에서는 비즈니스 요구 사항에 따라 이 기능을 사용하는 방법을 이해하려면 사전 구현 경험 또는 구현 컨설턴트를 권장합니다.

## 구문 및 예제

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

### this/true (필수)

첫 번째 인수는 브라우저가 페이지 밖으로 이동하기 전에 최대 500ms까지 대기하는지 여부를 결정합니다. 이미지 요청이 500ms보다 빨리 전송되면 페이지가 클릭한 링크로 즉시 이동합니다.

* `this`:AppMeasurement에서 이미지 요청을 보낼 시간을 최대 500ms까지 기다립니다. 기본값.
* `true`:기다리지 마십시오. 링크가 페이지에서 벗어나는 경우 이미지 요청이 전송되지 않을 수 있습니다.

지연은 링크가 페이지를 떠나는 경우에만 필요합니다.

```JavaScript
// Include 500ms delay
s.tl(this,'o','Example link');

// Do not include 500ms delay
s.tl(true,'o','Example link');
```

### linkType(필수)

두 번째 인수에는 캡처할 링크의 유형에 따라 세 개의 유효한 값이 있습니다. Adobe Analytics에서 이미지 요청이 채우는 차원을 결정합니다.

* `d`: 파일 다운로드
* `e`: 종료 링크
* `o`:사용자 지정 링크

```JavaScript
// Populates the File Downloads dimension
s.tl(this,'d','Example link');

// Populates the Exit Links dimension
s.tl(this,'e','Example link');

// Populates the Custom Links dimension
s.tl(this,'o','Example link');
```

### linkName(필수)

이 인수는 최대 100바이트의 사용자 지정 값일 수 있습니다. 이것은 보고에서 차원 값을 결정합니다.

```JavaScript
// Populates the Custom Link dimension with "Referral click to example.com"
s.tl(this,'o','Referral click to example.com');

// Populates the Download link dimension with "Last quarter performance PDF"
s.tl(this,'d','Last quarter performance PDF');
```

### variableOverrides(선택 사항)

단일 호출에 대한 변수 값을 변경할 수 있습니다. doneAction 인수를 사용하고 변수 오버라이드가 없는 경우 를 `null`사용합니다.

### doneAction(선택 사항)

추적 링크 호출이 완료된 후 실행할 탐색 동작을 지정합니다. 및 를 사용해야 `s.useForcedLinkTracking` 합니다 `s.forcedLinkTrackingTimeout`. The doneAction variable can be the string `navigate`, which causes the method to set `document.location` to the href attribute of `linkObject`. 또한 doneAction 변수는 고급 사용자 지정을 허용하는 함수가 될 수 있습니다.

앵커 `onClick` 이벤트에 doneAction에 대한 값을 제공하는 경우, 기본 브라우저 탐색을 방지할 수 있도록 `false` 호출 후에 `s.tl`를 반환해야 합니다.
To mirror the default behavior and follow the URL specified by the href attribute, provide a string of `navigate` as the doneAction. 선택 사항으로, doneAction으로 이 함수를 전달하여 탐색 이벤트를 처리하도록 자체 함수를 제공할 수 있습니다.

```JavaScript
s.tl(this,'e','Example link',null,'navigate');return false;
```

## 링크 추적에서 JavaScript 함수 사용

링크 추적 코드를 페이지 또는 연결된 JavaScript 파일에서 정의된 독립된 JavaScript 함수에 통합할 수 있습니다. 그런 다음 각 링크의 onClick 함수에서 호출을 수행할 수 있습니다.

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

링크가 자동 파일 다운로드 또는 종료 링크 추적에 의해 정상적으로 링크가 캡처되는 경우 링크가 두 번 카운트될 수 있습니다. For example, if you are tracking PDF downloads automatically, an `s.tl` call results in a duplicate download count:

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
