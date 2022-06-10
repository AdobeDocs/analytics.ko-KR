---
title: abort
description: abort 변수는 히트가 Adobe 데이터 수집 서버에 전송되지 않도록 하는 부울입니다.
feature: Variables
exl-id: e4e25a89-272b-4444-b52b-c7fe2478ff30
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 40%

---

# abort

`abort` 변수는 그 다음 추적 호출이 Adobe에 전송되지 않도록 하는 부울입니다. 웹 SDK에 유사한 기능이 있어서 `false` xdm 이벤트를 전송하기 전에.

## 웹 SDK 확장을 사용하여 이벤트 보내기 취소

를 사용하십시오 [!UICONTROL 이벤트 전송 전 시 콜백] 코드 편집기 및 반환 `false`.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 원하는 태그 속성을 클릭합니다.
1. 로 이동합니다. [!UICONTROL 확장] 탭을 클릭한 다음 **[!UICONTROL 구성]** 버튼 아래 [!UICONTROL Adobe Experience Platform Web SDK].
1. 아래 [!UICONTROL 데이터 수집]를 클릭하고 **[!UICONTROL 이벤트 전송 콜백 코드 전 편집]** 버튼을 클릭합니다.
1. 코드 편집기에서 Edge로 데이터 전송을 중단하려는 조건 아래에 다음 코드를 지정합니다.

```js
return false;
```

## 웹 SDK를 수동으로 구현하는 이벤트 보내기 취소

를 사용하십시오 `onBeforeEventSend` 콜백 및 반환 `false`. 자세한 내용은 [이벤트 전역 수정](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) 를 참조하십시오.

```js
alloy("configure"), {
    "onBeforeEventSend": function(content) {
        return false;
    }
}
```

## Adobe Analytics 확장에서 abort 변수 사용

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.abort

`s.abort` 변수는 부울입니다. 기본값은 `false`입니다.

* `true`로 설정하면 그 다음 추적 호출 ([`t()`](../functions/t-method.md) 또는 [`tl()`](../functions/tl-method.md))이 데이터를 Adobe에 전송하지 않습니다.
* `false`로 설정하거나 정의하지 않을 경우 이 변수는 아무 작업도 하지 않습니다.

```js
s.abort = true;
```

>[!NOTE]
>
>`abort` 변수는 모든 추적 호출 후 `false`로 재설정됩니다. 동일한 페이지에서 후속 추적 호출을 중지해야 하는 경우에는 `abort`을 다시 `true`로 설정하십시오.

예: `abort` 변수는 [`doPlugins()`](../functions/doplugins.md) Adobe으로 이미지 요청이 전송되기 전에 마지막으로 실행되는 함수입니다. 이 예는 와 유사하게 작동합니다 `onBeforeEventSend` callback using the Web SDK.

```js
s.doPlugins = function(s) {
    s.campaign = s.Util.getQueryParam("cid");
    if ((!s.campaign) && (!s.events)) {
        s.abort = true;
    }
};
```

일부 사용자 지정 링크 또는 디스플레이 광고의 외부 링크와 같이 추적하지 않으려는 활동을 식별하는 데 사용하는 논리에 집중할 수 있습니다.
