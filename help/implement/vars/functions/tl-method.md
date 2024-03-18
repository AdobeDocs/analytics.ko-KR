---
title: tl
description: Adobe에 링크 추적 호출을 보냅니다.
feature: Variables
exl-id: 470662b2-ce07-4432-b2d5-a670fbb77771
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 76%

---

# tl

`tl()` 메서드는 Adobe Analytics의 중요한 핵심 구성 요소입니다. 이 메서드는 페이지에 정의된 모든 Analytics 변수를 가져와 이미지 요청에 컴파일한 다음, 해당 데이터를 Adobe 데이터 수집 서버에 보냅니다. 이것은 [`t()`](t-method.md) 메서드와 유사하지만 페이지 보기 수를 증가시키지는 않습니다. 또한 이 메서드는 전체 페이지 로드로 간주되지 않는 링크 및 기타 요소를 추적하는 데 유용합니다.

[`trackDownloadLinks`](../config-vars/trackdownloadlinks.md) 또는 [`trackExternalLinks`](../config-vars/trackexternallinks.md)가 활성화되면 AppMeasurement가 다운로드 링크 및 종료 링크 추적 데이터를 보내는 `tl()` 메서드를 자동으로 호출합니다. 조직에서 추적할 링크와 그 동작을 보다 세밀하게 제어하는 것을 선호하는 경우 `tl()` 메서드를 수동으로 호출할 수 있습니다. 사용자 지정 링크는 수동으로만 추적할 수 있습니다.

## 웹 SDK를 사용한 링크 추적

웹 SDK는 페이지 보기 호출과 링크 추적 호출을 구분하지 않으며, 둘 다 `sendEvent` 명령입니다.

XDM 개체를 사용하고 Adobe Analytics이 주어진 이벤트를 링크 추적 호출로 계산하도록 하려는 경우 XDM 데이터에 다음이 포함되어 있는지 확인하십시오.

* 링크 이름: 매핑됨 `xdm.web.webInteraction.name`.
* 링크 URL:에 매핑됨 `xdm.web.webInteraction.URL`.
* 링크 유형: 매핑됨 `xdm.web.webInteraction.type`. 유효한 값에는 `other`(사용자 정의 링크), `download`(다운로드 링크) 및 `exit`(종료 링크)가 포함됩니다.

```js
alloy("sendEvent", {
  "xdm": {
    "web": {
      "webInteraction": {
        "name": "My Custom Link",
        "URL": "https://example.com",
        "type": "other"
      }
    }
  }
});
```

데이터 개체를 사용하고 Adobe Analytics에서 특정 이벤트를 링크 추적 호출로 계산하도록 하려면 데이터 개체에 다음이 포함되어 있는지 확인하십시오.

* 링크 이름: 매핑됨 `data.__adobe.analytics.linkName`.
* 링크 URL:에 매핑됨 `data.__adobe.analytics.linkURL`.
* 링크 유형: 매핑됨 `data.__adobe.analytics.linkType`. 유효한 값에는 `o`(사용자 정의 링크), `d`(다운로드 링크) 및 `e`(종료 링크)가 포함됩니다.

```js
alloy("sendEvent", {
  "data": {
    "__adobe": {
      "analytics": {
        "linkName": "My custom link",
        "linkURL": "https://example.com",
        "linkType": "o"
      }
    }
  }
});
```

## Adobe Analytics 확장을 사용한 링크 추적

Adobe Analytics 확장에는 링크 추적 호출을 설정할 수 있는 전용 위치가 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 규칙] 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
1. 아래 [!UICONTROL 작업]를 클릭하고 원하는 작업을 클릭하거나 **&#39;+&#39;** 아이콘 을 클릭하여 작업을 추가합니다.
1. 설정 [!UICONTROL 확장] 드롭다운 목록 **[!UICONTROL Adobe Analytics]**&#x200B;및 [!UICONTROL 작업 유형] 끝 **[!UICONTROL 비콘 보내기]**.
1. `s.tl()` 라디오 버튼을 클릭합니다.

Analytics 확장에서는 선택적 인수를 설정할 수 없습니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.tl() 메서드

추적 호출을 Adobe에 보내려면 `s.tl()` 메서드를 호출하십시오.

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

### 링크 개체 (필수)

링크 개체 인수는 브라우저가 최대 500밀리초를 기다린 후에 페이지에서 나가는지 여부를 결정합니다. 이미지 요청이 500밀리초 이내로 전송되면 페이지가 클릭한 링크로 즉시 이동합니다.

>[!NOTE]
>
>AppMeasurement는 종료 링크에 대해 [`useBeacon`](../config-vars/usebeacon.md) 변수를 자동으로 활성화하므로 최신 브라우저에서 이 인수가 더 이상 필요하지 않게 됩니다. 이 인수는 이전 버전의 AppMeasurement에서 더 일반적으로 사용되었습니다.

* `this`: AppMeasurement에 이미지 요청을 전송할 시간을 제공하기 위해 최대 500밀리초를 대기합니다. 기본값.
* `true`: 기다리지 않습니다.

```JavaScript
// Include a 500ms delay with an exit link
s.tl(this,"e","Example exit link");

// Do not include a 500ms delay with an exit link
s.tl(true,"e","Example exit link");
```

### 링크 유형(필수)

링크 유형 인수는 링크 추적 호출 유형을 결정하는 단일 문자 문자열로서, 3개의 유효한 값이 있습니다.

* `o`: 링크는 [사용자 지정 링크](/help/components/dimensions/custom-link.md)입니다.
* `d`: 링크는 [다운로드 링크](/help/components/dimensions/download-link.md)입니다.
* `e`: 링크는 [종료 링크](/help/components/dimensions/exit-link.md)입니다.

```js
// Send a custom link
s.tl(true,"o","Example custom link");

// Send a download link
s.tl(true,"d","Example download link");

// Send an exit link
s.tl(true,"e","Example exit link");
```

### 링크 이름 (권장)

링크 이름 인수는 링크 추적 차원 항목을 결정하는 문자열로서, 보고에서 [사용자 지정 링크](/help/components/dimensions/custom-link.md), [다운로드 링크](/help/components/dimensions/download-link.md) 또는 [종료 링크](/help/components/dimensions/exit-link.md) 차원을 사용할 때 이 문자열에는 차원 항목이 포함됩니다. 이 인수가 설정되어 있지 않으면 [linkURL](../config-vars/linkurl.md) 변수가 사용됩니다.

```js
// When using the Download link dimension, this method call increases the occurrences metric for "Sea turtle PDF report" by 1.
s.tl(true,"d","Sea turtle PDF report");
```

### 변수 무시 (선택 사항)

단일 호출에 대한 변수 값을 변경할 수 있습니다. 자세한 내용은 [변수 무시](../../js/overrides.md)를 참조하십시오.

```js
var y = new Object();
y.eVar1 = "Override value";
y.linkTrackVars = "eVar1";
s.tl(true,"o","Example custom link",y);
```

## 예제 및 사용 사례

HTML 링크 내에서 바로 기본 링크 추적 호출을 전송하십시오.

```HTML
<a href="example.html" onClick="s.tl(true,'o','Example link');">Click here</a>
```

메서드 인수를 사용하여 기본 링크 추적 호출을 만들도록 JavaScript를 사용합니다.

```JavaScript
s.tl(true,"o","Example link");
```

### 사용자 지정 함수 내에서 링크 추적 호출 만들기

링크 추적 코드를 페이지 또는 연결된 JavaScript 파일에 정의된 자체 포함된 JavaScript 함수에 통합할 수 있습니다. 그런 다음 각 링크의 onClick 함수에서 호출을 지정할 수 있습니다. JavaScript 파일에서 다음을 설정하십시오.

```JavaScript
function trackClickInteraction(name){
  s.linkTrackVars = "eVar1,eVar2";
  s.eVar1 = name;
  s.eVar2 = s.pageName;
  s.tl(true,"o",name);
}
```

그런 다음 주어진 링크를 추적하고 싶을 때마다 이 함수를 호출할 수 있습니다.

```HTML
<!-- Use wherever you want to track links -->
<a href="example.html" onClick="trackClickInteraction('Example link');">Click here</a>
```

### 중복 링크 추적 방지

`trackDownloadLinks` 또는 `trackExternalLinks`가 활성화되어 있으면 올바른 필터가 일치하는 경우 AppMeasurement가 자동으로 링크 추적 호출을 생성합니다. 이러한 링크 클릭에 대해 수동으로도 `s.tl()`을 호출하는 경우 중복 데이터를 Adobe에 보낼 수 있습니다. 중복 데이터는 보고서 수치들을 부풀려서 정확성을 떨어뜨립니다.

예를 들어 다음 함수는 동일한 링크 클릭에 대해 두 개의 링크 추적 호출 (수동 및 자동 다운로드 링크)을 보냅니다.

```JavaScript
function trackDownload(obj) {
  s.tl(obj,"d","Example PDF download");
}
```

다음의 수정된 함수를 사용하여 중복 링크 추적 호출을 방지할 수 있습니다. 이 함수는 먼저 링크 개체가 있는지 확인하고 링크 개체가 빈 문자열인 경우 수동 링크 추적 호출만 보냅니다.

```JavaScript
function linkCode(obj) {
  var lt = obj.href != null ? s.lt(obj.href) : "";
  if (lt=="") {
    s.tl(obj,"d","Example PDF download");
  }
}
```
