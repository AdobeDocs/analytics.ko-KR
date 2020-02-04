---
title: tl
description: Adobe에 링크 추적 호출을 보냅니다.
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# tl

이 `tl` 메서드는 Adobe Analytics의 중요한 핵심 구성 요소입니다. 페이지에 정의된 모든 Analytics 변수를 가져와 이미지 요청으로 컴파일한 다음 해당 데이터를 Adobe 데이터 수집 서버로 보냅니다. 이 방법은 `t` 메서드와 유사하지만 페이지 보기를 증가시키지 않습니다. 전체 페이지 로드로 간주되지 않는 링크 및 기타 요소를 추적하는 데 유용합니다.

AppMeasurement가 `trackDownloadLinks` 또는 `trackExternalLinks` `tl` 활성화되면 다운로드 링크 및 종료 링크 추적 데이터를 보내는 방법을 자동으로 호출합니다. 조직에서 추적하기 위한 링크 및 동작을 보다 세밀하게 제어하려는 경우 해당 `tl` 메서드를 수동으로 호출할 수 있습니다. 사용자 지정 링크는 수동으로 추적할 수만 있습니다.

## Adobe Experience Platform Launch의 링크 추적 호출

Launch에는 링크 추적 호출을 설정하는 전용 위치가 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 규칙 [!UICONTROL 탭으로 이동한] 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. 작업 [!UICONTROL 아래에서]&#39;+&#39; 아이콘을 클릭합니다
5. 확장 [!UICONTROL 프로그램 드롭다운을 Adobe] Analytics로 설정하고 작업 [!UICONTROL 유형을] 비콘 전송으로 설정합니다.
6. Click the `s.tl()` radio button.

Launch에서는 선택적 인수를 설정할 수 없습니다.

## s.tl() 메서드(AppMeasurement 및 Launch 사용자 지정 코드 편집기)

Adobe에 추적 호출을 전송하려면 이 `s.tl()` 메서드를 호출합니다.

```js
s.tl();
```

선택적으로 이 메서드는 다음과 같은 여러 인수를 수락합니다.

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

### 링크 개체

링크 개체 인수는 브라우저가 페이지 밖으로 이동하기 전에 최대 500ms까지 대기하는지를 결정합니다. 이미지 요청이 500밀리초 이내로 전송되면 페이지가 클릭한 링크로 즉시 이동합니다.

> [!NOTE] AppMeasurement는 종료 링크에 대한 `useBeacon` 변수를 자동으로 활성화하므로 최신 브라우저에서 이 인수가 더 이상 필요하지 않습니다. 이 인수는 이전 버전의 AppMeasurement에서 더 일반적으로 사용되었습니다.

* `this`: AppMeasurement에 이미지 요청을 전송할 시간을 제공하기 위해 최대 500밀리초를 대기합니다. 기본값.
* `true`: 기다리지 않습니다.

```JavaScript
// Include a 500ms delay
s.tl(this);

// Do not include a 500ms delay
s.tl(true);
```

### 링크 유형

링크 유형 인수는 링크 추적 호출 유형을 결정하는 단일 문자 문자열입니다. 이것은 `linkType` 변수를 설정하는 것과 같습니다.

```js
// Send a custom link
s.tl(true,"o");

// Send a download link
s.tl(true,"d");

// Send an exit link
s.tl(true,"e");
```

### 링크 이름

링크 이름 인수는 링크 추적 차원 값을 결정하는 문자열입니다. 이것은 `linkName` 변수를 설정하는 것과 같습니다.

```js
s.tl(true,"d","Example download link");
```

### 변수 무시

단일 호출에 대한 변수 값을 변경할 수 있습니다. 자세한 내용은 [변수 대체를](../../js/overrides.md) 참조하십시오.

```js
var y = new Object();
y.eVar1 = "Override value";
y.linkTrackVars = "eVar1";
s.tl(true,"o","Example custom link",y);
```

## 예제 및 사용 사례

HTML 링크 내에서 바로 기본 링크 추적 호출을 전송합니다.

```HTML
<a href="example.html" onClick="s.tl(true,'o','Example link');">Click here</a>
```

JavaScript를 사용하여 기본 링크 추적 호출을 만듭니다.

```JavaScript
s.tl(true,"o","Example Link");
```

### 사용자 지정 함수 내에서 링크 추적 호출 만들기

링크 추적 코드를 페이지 또는 연결된 JavaScript 파일에 정의된 자체 포함된 JavaScript 함수에 통합할 수 있습니다. 그런 다음 각 링크의 onClick 함수에서 호출을 지정할 수 있습니다. JavaScript 파일에서 다음을 설정합니다.

```JavaScript
function trackClickInteraction(name){
  s.linkTrackVars = "eVar1,eVar2";
  s.eVar1 = name;
  s.eVar2 = s.pageName;
  s.tl(true,"o",name);
}
```

그런 다음 주어진 링크를 추적하려는 경우 언제든지 함수를 호출할 수 있습니다.

```HTML
<!-- Use wherever you want to track links -->
<a href="example.html" onClick="trackClickInteraction('Example link');">Click here</a>
```

### 중복 링크 추적 방지

또는 `trackDownloadLinks` `trackExternalLinks` 활성화된 경우 올바른 필터가 일치하는 경우 AppMeasurement가 자동으로 링크 추적 호출을 만듭니다. 이러한 링크 클릭에 `s.tl()` 대해 수동으로 전화하는 경우 중복 데이터를 Adobe에 전송할 수 있습니다. 중복 데이터는 보고서 번호를 부풀리고 정확도를 낮춥니다.

예를 들어, 다음 함수는 동일한 링크 클릭(수동 및 자동 다운로드 링크)에 대해 두 개의 링크 추적 호출을 보냅니다.

```JavaScript
function trackDownload(obj) {
  s.tl(obj,"d","Example PDF download");
}
```

다음의 수정된 함수를 사용하여 중복 링크 추적 호출을 방지할 수 있습니다. 먼저 링크 객체가 있는지 확인하고 링크 객체가 빈 문자열인 경우 수동 링크 추적 호출만 보냅니다.

```JavaScript
function linkCode(obj) {
  var lt = obj.href != null ? s.lt(obj.href) : "";
  if (lt=="") {
    s.tl(obj,"d","Example PDF download");
  }
}
```
