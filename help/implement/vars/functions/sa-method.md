---
title: sa
description: 구현에서 언제든지 보고서 세트를 변경합니다.
feature: Variables
exl-id: 524857a7-c820-4985-86c7-fcf21a0809bd
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 38%

---

# sa

`sa()` 메서드를 사용하면 페이지에서 언제든지 보고서 세트를 동적으로 변경할 수 있습니다. 페이지를 다시 로드하지 않고 데이터를 다양한 보고서 세트에 보내려는 경우 이 메서드를 사용할 수 있습니다.

## 웹 SDK를 사용하여 보고서 세트 처리

웹 SDK는 원하는 Analytics 보고서 세트에 데이터를 전달하는 특정 데이터 스트림에 데이터를 보내 작동합니다. 단일 데이터 스트림은 데이터를 여러 보고서 세트에 전달할 수 있습니다. 이 섹션은 웹 SDK 확장 프로그램 및 웹 SDK를 수동으로 구현하는 방법에 모두 적용됩니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 클릭 **[!UICONTROL 데이터 스트림]** 왼쪽에 있습니다.
1. 원하는 데이터 스트림을 클릭하거나 **[!UICONTROL 새 데이터 스트림]**.
1. 클릭 **[!UICONTROL 서비스 추가]**&#x200B;를 선택하고 을 선택합니다. **[!UICONTROL Adobe Analytics]**.
1. 원하는 보고서 세트 ID를 입력합니다. 동일한 데이터를 여러 보고서 세트로 보내려면 **[!UICONTROL 보고서 세트 추가]**.
1. 원하는 보고서 세트를 모두 입력하면 **[!UICONTROL 저장]**.

## 웹 SDK 확장을 사용하여 원하는 데이터 스트림 설정

웹 SDK 확장은 각 환경에 대한 데이터 스트림 드롭다운을 제공합니다. 또는 수동으로 데이터 스트림 ID를 입력할 수 있습니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 원하는 태그 속성을 클릭합니다.
1. 로 이동합니다. [!UICONTROL 확장] 탭을 클릭한 다음 **[!UICONTROL 구성]** 버튼 아래 [!UICONTROL Adobe Experience Platform Web SDK].
1. 아래 [!UICONTROL 데이터 스트림]를 눌러 각 환경에 대한 드롭다운에서 원하는 데이터 스트림을 선택합니다.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## Web SDK를 수동으로 구현하는 원하는 데이터 스트림을 설정합니다

설정 `edgeConfigId` 구성 변수를 데이터 스트림 ID에 추가합니다. 데이터 스트림 ID는 Adobe Experience Platform 데이터 수집에서 데이터 스트림을 볼 때 오른쪽에 있습니다.

```js
alloy("configure", {
  "edgeConfigId": "example-a01f-4458-8cec-ef61de241c93",
});
```

자세한 내용은 [웹 SDK 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR?lang=ko-KR) 를 참조하십시오.

## Adobe Analytics 확장을 사용하여 보고서 세트 변경

인터페이스에서 보고서 세트를 변경하는 유연한 방법은 없습니다. 보고서 세트는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 라이브러리 관리] 아코디언 아래에서 설정할 수 있습니다. 하지만 규칙을 사용하여 보고서 세트를 변경하거나 업데이트할 수는 없습니다. 보고서 세트 값을 설정한 후 업데이트하려면 AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.sa()

대상 보고서 세트를 변경하려면 `s.sa()` 메서드를 호출하십시오. 이 메서드의 유일한 인수는 하나의 보고서 세트 ID나 쉼표로 구분된 여러 보고서 세트 ID를 포함하는 문자열입니다. 보고서 세트 ID 인수는 필수입니다. 이 문자열 인수에는 공백을 사용하지 마십시오.

```js
s.sa("examplersid");
```

예를 들어 사용자가 사이트에서 특정 작업을 수행하는 경우 보고서 세트를 변경할 수 있습니다.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// If the visitor plays a video, you can add a video report suite
s.sa("examplersid,videorsid");

// Then send an image request
s.t();
```
