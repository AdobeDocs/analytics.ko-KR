---
title: useBeacon
description: useBeacon을 사용하면 AppMeasurement에서 브라우저 sendBeacon API를 사용하도록 할 수 있습니다.
feature: Variables
exl-id: a3c4174a-711d-4a35-9f36-9b1049c7db54
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 54%

---

# useBeacon

대부분의 최신 브라우저에는 기본 메서드 `navigator.sendBeacon()`이 포함되어 있습니다. 이 메서드는 HTTP를 통해 적은 양의 데이터를 웹 서버에 비동기적으로 전송합니다. `useBeacon` 변수가 활성화되어 있으면 AppMeasurement가 `navigator.sendBeacon()` 메서드를 사용할 수 있습니다. 이 방법은 페이지를 언로드하기 전에 정보를 전송하려는 종료 링크 및 기타 상황에 유용합니다.

`useBeacon`이 활성화되어 있으면 Adobe에 전송된 다음 히트는 표준 `GET` 이미지 요청 대신 브라우저의 `navigator.sendBeacon()` 메서드를 사용합니다. 이 변수는 [`s.t()`](../functions/t-method.md) 및 [`s.tl()`](../functions/tl-method.md) 이미지 요청 모두에 적용됩니다. 이렇게 하려면 AppMeasurement 2.17.0 이상이 필요합니다.

>[!TIP]
>
>AppMeasurement는 종료 링크 이미지 요청에 대해 `useBeacon`을 자동으로 활성화합니다.

방문자가 `useBeacon`을 지원하지 않는 브라우저를 사용하면 `navigator.sendBeacon()` 변수는 무시됩니다. 이 변수를 사용하려면 AppMeasurement 2.16.0 이상이 필요합니다.

## 웹 SDK 확장을 사용하여 sendBeacon API 사용

다음 **[!UICONTROL 문서가 언로드됨]** 작업 구성 내의 확인란은 Adobe으로 전송된 데이터가 sendBeacon API를 사용하는지 여부를 결정합니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 원하는 태그 속성을 클릭합니다.
1. 로 이동합니다. [!UICONTROL 규칙] 탭을 클릭한 다음 원하는 규칙을 클릭합니다.
1. 아래 [!UICONTROL 작업]를 클릭하고 원하는 작업을 클릭하거나 **&#39;+&#39;** 아이콘을 클릭하여 새 작업을 추가합니다.
1. 확장 드롭다운을 로 설정합니다. **[!UICONTROL Adobe Experience Platform Web SDK]** 그리고 [!UICONTROL 작업 유형] to **[!UICONTROL 이벤트 보내기]**
1. 확인란을 클릭합니다 **[!UICONTROL 문서가 언로드됨]** 오른쪽에 있습니다.

이 확인란을 선택하면 sendBeacon API를 사용하여 데이터가 Adobe으로 전송됩니다. 기본적으로 선택되어 있지 않습니다.

## 웹 SDK를 수동으로 구현하는 sendBeacon API 사용

설정 `documentUnloading` to `true` 이벤트 보내기 설정하지 않으면 기본값은 입니다 `false`.

```json
alloy("sendEvent", {
  "documentUnloading": true,
  "xdm": {}
});
```

자세한 내용은 [sendBeacon API 사용](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#using-the-sendbeacon-api) 를 참조하십시오.

## Adobe Analytics 확장을 사용하여 비콘 사용

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.useBeacon

`s.useBeacon` 변수는 AppMeasurement가 브라우저의 `navigator.sendBeacon()` 메서드를 사용하는지 여부를 결정하는 부울입니다. 기본값은 `false`입니다. `navigator.sendBeacon()`의 비동기적 특성을 사용하려면 추적 함수를 호출하기 전에 이 변수를 `true`로 설정하십시오.

```js
s.useBeacon = true;
```

>[!NOTE]
>
>추적 호출이 실행된 후 이 변수는 `false`로 재설정됩니다. 구현이 동일한 페이지 로드에서 여러 이미지 요청을 전송하는 경우 (예: 단일 페이지 애플리케이션) 각 추적 호출 전에 이 변수를 `true`로 설정하십시오.
