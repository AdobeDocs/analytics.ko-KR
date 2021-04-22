---
title: iframe과 함께 AppMeasurement 사용
description: iframe에 있는 동안 iframe 또는 상위 페이지 내에서 Adobe Analytics 변수에 액세스합니다.
exl-id: 59b9cd4f-8599-41ee-8b54-a6a556198ecd
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '327'
ht-degree: 100%

---

# iframe과 함께 AppMeasurement 사용

하위 및 상위 iframe 모두에서 AppMeasurement 변수를 참조할 수 있습니다. AppMeasurement 라이브러리가 존재하는 동일한 위치에 모든 변수를 정의해야 합니다. 다음 예에서는 iframe 내부 및 외부에서 기본 AppMeasurement 변수 및 메서드를 설정하는 방법을 설명합니다.

Adobe Experience Platform Launch를 사용하는 경우 추적기 개체에 전역적으로 액세스할 수 있는지 확인하십시오. Launch 사용 안내서의 [Adobe Analytics 확장 개요](https://docs.adobe.com/content/help/ko-KR/launch/using/extensions-ref/adobe-extension/analytics-extension/overview.html)를 참조하십시오.

>[!CAUTION]
>상위 페이지와 iframe 모두에 AppMeasurement 라이브러리를 포함하지 마십시오. 이렇게 하면 여러 이미지 요청을 전송하고 보고서를 부풀리며 청구 가능한 서버 호출이 증가하는 위험이 발생합니다.

## iframe에 있는 AppMeasurement에 액세스

iframe 개체를 통해 AppMeasurement 변수에 액세스할 수 있습니다. 이 예제는 [pageName](../vars/page-vars/pagename.md) 를 설정하고 iframe 객체를 참조하는 두 가지 다른 방법을 사용하여 [t () method](../vars/functions/t-method.md)를 호출합니다.

```js
// Reference AppMeasurement code that resides within an iframe and send an image request
document.getElementById('targetFrame').contentWindow.s.pageName="Page name within iframe";
document.getElementById('targetFrame').contentWindow.s.t();

// An alternate method to the above if there's only one iframe on the page
window.frames[0].contentWindow.s.pageName = "Page name within iframe";
window.frames[0].contentWindow.s.t();
```

## iframe 내부에서 AppMeasurement에 액세스

iframe 내에서 상위 페이지의 AppMeasurement 변수에 액세스할 수 있습니다. 이 예제는 [pageName](../vars/page-vars/pagename.md)를 설정하고 [t () method](../vars/functions/t-method.md)를 [`parent`](https://www.w3schools.com/jsref/prop_win_parent.asp) 속성을 사용하여 호출합니다.

```js
// Reference AppMeasurement code on a parent page from within an iframe and send an image request
parent.s.pageName = "Page Name on Hosted Window";
parent.s.t();
```

## `postMessage` 및 이벤트 리스너 사용

또는 `postMessage` 및 이벤트 리스너를 사용하여 변수를 설정할 수 있습니다. 이 메서드는 iframe에 대한 직접 참조가 필요하지 않습니다.

```js
// Place this code in your parent window
function listenMessage(e) {
    if(e.data == "Example page view call") {
        s.pageName = "Page name using postMessage";
        s.t();
    }
}
window.addEventListener("message", listenMessage, false);

// Place this code in the iframe
window.top.postMessage("Example page view call","https://example.com");
```

## 제한 사항

* 다른 JavaScript 코드와 마찬가지로 iframe은 도메인과 프로토콜이 일치할 때만 통신할 수 있습니다. 이 예제는 iframe 콘텐츠가 상위 도메인과 다른 도메인에 있는 경우 작동하지 않습니다.
* AppMeasurement가 iframe에 있는 경우 [`referrer`](../vars/page-vars/referrer.md) 변수는 실제 참조 URL이 아닌 상위 URL로 설정됩니다. `referrer` 변수를 수동으로 설정하여 이 문제를 해결할 수 있습니다.
* [Adobe Experience Cloud Debugger](https://docs.adobe.com/content/help/ko-KR/debugger/using/experience-cloud-debugger.html)는 iframe 내에서 트리거된 이미지 요청을 인식하지 않습니다.
* Activity Map은 iframe 내에서 클릭된 링크 위에 히트맵을 표시하지 않습니다. 대신 전체 iframe이 강조 표시됩니다.
