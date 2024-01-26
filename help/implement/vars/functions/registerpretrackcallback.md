---
title: registerPreTrackCallback
description: Adobe에 히트를 보내기 전 콜백 함수를 만듭니다.
feature: Variables
exl-id: 11c960d7-ded4-441a-822f-463d3a137d2d
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 55%

---

# registerPreTrackCallback

`registerPreTrackCallback` 변수를 사용하면 이미지 요청 URL이 컴파일된 후 전송되기 전에 조직에서 JavaScript 함수를 후크할 수 있습니다. 이 변수를 사용하여 AppMeasurement에서 수집한 데이터를 파트너 또는 사내 인프라에 보낼 수 있습니다.

>[!WARNING]
>
>다음과 같은 추적 호출을 하지 마십시오. [`t()`](t-method.md) 또는 [`tl()`](tl-method.md) 의 내부 `registerPreTrackCallback` 변수를 채우는 방법에 따라 페이지를 순서대로 표시합니다. 이 변수에서 추적 호출을 설정하면 이미지 요청의 무한 루프가 발생합니다.

`registerPreTrackCallback` 변수를 호출할 때마다 이미지 요청 URL이 컴파일될 때 해당 함수를 실행하도록 후크합니다. 동일한 페이지 로드에서 동일한 함수를 여러 번 등록하지 마십시오.

>[!NOTE]
>
>`registerPreTrackCallback`과 `registerPostTrackCallback` 사이에 실행된 함수의 타이밍과 순서는 보장되지 않습니다. 이 두 함수 간에 종속성이 생기지 않도록 하십시오.

## Web SDK 확장을 사용한 사전 추적 콜백

데이터가 컴파일된 후 Adobe으로 전송되기 전에 Web SDK에서 함수를 후크할 수 없습니다. 그러나 다음을 사용할 수 있습니다. `onBeforeEventSend` 데이터를 보내기 바로 전에 실행할 함수를 등록합니다.

1. 에 로그인합니다 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) AdobeID 자격 증명을 사용하는 UI.
1. 원하는 태그 속성을 클릭합니다.
1. 로 이동 [!UICONTROL 확장] 탭을 클릭한 다음 **[!UICONTROL 구성]** 아래에 있는 단추 [!UICONTROL Adobe Experience Platform 웹 SDK].
1. 아래 [!UICONTROL 데이터 수집]를 클릭하고 **[!UICONTROL 이벤트 전송 전 콜백 코드 편집]** 단추를 클릭합니다.
1. 편집기에 원하는 코드를 넣습니다.

## 웹 SDK를 수동으로 구현하는 사전 추적 콜백

데이터가 컴파일된 후 Adobe으로 전송되기 전에 Web SDK에서 함수를 후크할 수 없습니다. 그러나 다음을 사용할 수 있습니다. `onBeforeEventSend` 데이터가 전송되기 바로 전에 실행할 함수를 등록하려면 다음과 같이 하십시오. `doPlugins`. 다음을 참조하십시오 [전체적으로 이벤트 수정](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) 자세한 내용은 Web SDK 설명서 를 참조하십시오.

```js
// Set the trackingCode XDM field to "New value"
alloy("configure", {
  "onBeforeEventSend": function(content) {
    content.xdm.marketing.trackingCode = "New value";
  }
})
```

## Adobe Analytics 확장을 사용한 사전 추적 콜백

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.registerPreTrackCallback

`s.registerPreTrackCallback`은 함수를 유일한 인수로 사용하는 함수입니다. 중첩 함수는 이미지 요청이 전송되기 바로 전에 실행됩니다.

```js
s.registerPreTrackCallback(function(){/* Desired code */});
```

코드에서 이미지 요청 URL을 사용하려면 중첩 함수 내에서 `requestUrl` 문자열 인수를 참조하십시오. 원하는 용도로 `requestUrl` 변수를 구문 분석할 수 있습니다. 이 변수를 조정해도 데이터 수집에는 영향을 주지 않습니다.

```js
s.registerPreTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

`s.registerPreTrackCallback` 함수에서 추가 인수를 포함할 수 있으며 이 인수는 중첩 함수에서 사용할 수 있습니다.

```js
s.registerPreTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

>[!NOTE]
>
>페이지 변수를 설정하거나 이 함수 내에서 `requestUrl` 문자열을 변경해도 이 함수 호출 직후 전송된 이미지 요청에는 영향을 주지 **않습니다**. [`doPlugins()`](doplugins.md) 변수를 대신 사용하십시오.
