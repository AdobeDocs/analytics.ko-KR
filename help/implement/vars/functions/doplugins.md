---
title: doPlugins
description: 히트가 컴파일되고 Adobe에 전송되기 바로 전에 논리를 구성합니다.
feature: Variables
exl-id: c5113be3-04b3-4dd2-8481-ba13149750ca
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 57%

---

# doPlugins

`doPlugins` 변수는 구현에서 값을 설정하는 &#39;마지막 호출&#39; 역할을 합니다. [`usePlugins`](../config-vars/useplugins.md)가 활성화된 경우 다음을 포함한 모든 유형의 이미지 요청이 컴파일되어 Adobe에 전송되기 바로 전에 자동으로 실행됩니다.

* 모든 페이지 보기 ([`t()`](t-method.md)) 호출
* 자동 다운로드 링크 및 종료 링크를 포함한 모든 링크 추적 ([`tl()`](tl-method.md)) 호출

이미지 요청이 컴파일되어 Adobe에 전송되기 바로 전에 `doPlugins` 변수를 사용하여 플러그인 코드를 호출하고 최종 변수 값을 설정하십시오.

## 웹 SDK 확장을 사용하여 이벤트 전 콜백 코드를 사용합니다

대신 `doPlugins`를 설정하는 것이 좋습니다 `onBeforeEventSend` 과 유사한 기능으로 바뀌었습니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 원하는 태그 속성을 클릭합니다.
1. 로 이동합니다. [!UICONTROL 확장] 탭을 클릭한 다음 **[!UICONTROL 구성]** 버튼 아래 [!UICONTROL Adobe Experience Platform Web SDK].
1. 아래 [!UICONTROL 데이터 수집]를 클릭하고 **[!UICONTROL 이벤트 전송 콜백 코드 전 편집]** 버튼을 클릭합니다.
1. 원하는 코드를 편집기에 넣습니다.

## 사용 `onBeforeEventSend` 웹 SDK 수동 구현

대신 `doPlugins`를 설정하는 것이 좋습니다 `onBeforeEventSend` 과 유사한 기능으로 바뀌었습니다. 자세한 내용은 [이벤트 전역 수정](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) 를 참조하십시오.

```js
// Set the trackingCode XDM field to "New value"
alloy("configure", {
  "onBeforeEventSend": function(content) {
    content.xdm.marketing.trackingCode = "New value";
  }
})
```

## Adobe Analytics 확장을 사용하는 플러그인

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 사용자 지정 코드의 s.doPlugins

`s.doPlugins` 변수를 원하는 코드를 포함하는 함수로 설정하십시오. 추적 호출을 수행하면 함수가 자동으로 실행됩니다.

```js
s.doPlugins = function() {/* Desired code */};
```

>[!IMPORTANT]
>
>함수를 구현에서 한 번만 `doPlugins` 변수로 설정하십시오. `doPlugins` 변수를 두 번 이상 설정하면 가장 최근 코드만 사용됩니다.

## 예

```js
// Set eVar1 to the web page's title
s.doPlugins = function() {
  s.eVar1 = window.document.title;
};

// Use the getPreviousValue plug-in (requires plug-in code outside the function)
s.doPlugins = function() {
  s.eVar1 = s.getPreviousValue(s.pageName,'gpv_pn');
}
```

>[!NOTE]
>
>이전 버전의 AppMeasurement에는 약간 다른 `doPlugins()` 코드가 있었습니다. 위의 형식을 우수 사례로 사용하는 것이 좋습니다.
