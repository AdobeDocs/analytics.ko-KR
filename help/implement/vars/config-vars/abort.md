---
title: abort
description: abort 변수는 히트가 Adobe 데이터 수집 서버에 전송되지 않도록 하는 부울입니다.
feature: Appmeasurement Implementation
exl-id: e4e25a89-272b-4444-b52b-c7fe2478ff30
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 39%

---

# abort

`abort` 변수는 그 다음 추적 호출이 Adobe으로 전송되지 않도록 하는 부울입니다. XDM 이벤트가 전송되기 전에 `false`을(를) 반환할 수 있는 유사한 기능이 웹 SDK에 있습니다.

## 웹 SDK 확장을 사용하여 이벤트 보내기 취소

이벤트 전송 콜백 전 [!UICONTROL On] 코드 편집기를 사용하고 `false`을(를) 반환합니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음 **[!UICONTROL Adobe Experience Platform Web SDK]** 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
1. [!UICONTROL 데이터 수집]에서 **[!UICONTROL 이벤트 전송 전 편집 콜백 코드]** 단추를 클릭합니다.
1. 코드 편집기에서 Edge에 데이터 전송을 중단하려는 조건에 따라 다음 코드를 넣습니다.

```js
return false;
```

## 웹 SDK을 수동으로 구현하여 이벤트 보내기 취소

`onBeforeEventSend` 콜백을 사용하고 `false`을(를) 반환합니다. 자세한 내용은 웹 SDK 설명서에서 [전역 이벤트 수정](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally)을 참조하십시오.

```js
alloy("configure"), {
    "onBeforeEventSend": function(content) {
        return false;
    }
}
```

## Adobe Analytics 확장에서 abort 변수 사용

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.abort

`s.abort` 변수는 부울입니다. 기본값은 `false`입니다.

* `true`로 설정하면 그 다음 추적 호출 ([`t()`](../functions/t-method.md) 또는 [`tl()`](../functions/tl-method.md))이 데이터를 Adobe에 전송하지 않습니다.
* `false`로 설정하거나 정의하지 않을 경우 이 변수는 아무 작업도 하지 않습니다.

```js
s.abort = true;
```

>[!NOTE]
>
>`abort` 변수는 모든 추적 호출 후 `false`로 재설정됩니다. 동일한 페이지에서 후속 추적 호출을 중단하려면 `abort`을(를) `true`(으)로 다시 설정하십시오.

`abort` 변수는 [`doPlugins()`](../functions/doplugins.md) 함수에서 설정할 수 있습니다. 이 함수는 이미지 요청이 Adobe으로 전송되기 전에 마지막으로 실행되는 함수입니다. 이 예제는 웹 SDK을 사용하는 `onBeforeEventSend` 콜백과 유사하게 작동합니다.

```js
s.doPlugins = function(s) {
    s.campaign = s.Util.getQueryParam("cid");
    if ((!s.campaign) && (!s.events)) {
        s.abort = true;
    }
};
```

일부 사용자 지정 링크 또는 디스플레이 광고의 외부 링크와 같이 추적하지 않으려는 활동을 식별하는 데 사용하는 논리에 집중할 수 있습니다.
