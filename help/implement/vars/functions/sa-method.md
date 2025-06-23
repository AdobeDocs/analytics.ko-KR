---
title: sa
description: 구현에서 언제든지 보고서 세트를 변경합니다.
feature: Appmeasurement Implementation
exl-id: 524857a7-c820-4985-86c7-fcf21a0809bd
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 42%

---

# sa

`sa()` 메서드를 사용하면 페이지에서 언제든지 보고서 세트를 동적으로 변경할 수 있습니다. 페이지를 다시 로드하지 않고 데이터를 다양한 보고서 세트에 보내려는 경우 이 메서드를 사용할 수 있습니다.

## 웹 SDK을 사용하여 보고서 세트 처리

웹 SDK은 데이터를 원하는 Analytics 보고서 세트로 전달하는 특정 데이터 스트림에 데이터를 전송하여 작동합니다. 단일 데이터 스트림은 데이터를 여러 보고서 세트로 전달할 수 있습니다. 이 섹션은 Web SDK 확장 및 Web SDK 수동 구현 모두에 적용됩니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 왼쪽의 **[!UICONTROL 데이터스트림]**&#x200B;을 클릭합니다.
1. 원하는 데이터 스트림을 클릭하거나 **[!UICONTROL 새 데이터 스트림]**&#x200B;을 클릭합니다.
1. **[!UICONTROL 서비스 추가]**&#x200B;를 클릭한 다음 **[!UICONTROL Adobe Analytics]**&#x200B;을(를) 선택합니다.
1. 원하는 보고서 세트 ID를 입력합니다. 동일한 데이터를 여러 보고서 세트로 보내려면 **[!UICONTROL 보고서 세트 추가]**&#x200B;를 클릭하십시오.
1. 원하는 보고서 세트를 모두 입력했으면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 웹 SDK 확장을 사용하여 원하는 데이터 스트림 설정

웹 SDK 확장은 각 환경에 대한 데이터 스트림 드롭다운 목록을 제공합니다. 또는 데이터 스트림 ID를 수동으로 입력할 수도 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음 [!UICONTROL Adobe Experience Platform Web SDK] 아래의 **[!UICONTROL 구성]** 단추를 클릭합니다.
1. [!UICONTROL 데이터스트림]에서 각 환경의 드롭다운 목록에서 원하는 데이터스트림을 선택합니다.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 웹 SDK을 수동으로 구현하여 원하는 데이터 스트림 설정

`datastreamId` 구성 변수를 데이터 스트림 ID로 설정합니다. 데이터 스트림 ID는 Adobe Experience Platform 데이터 수집에서 데이터 스트림을 볼 때 오른쪽에 있습니다.

```js
alloy("configure", {
  datastreamId: "example-a01f-4458-8cec-ef61de241c93",
  orgId: "ADB3LETTERSANDNUMBERS@AdobeOrg"
});
```

자세한 내용은 웹 SDK 설명서의 [웹 SDK 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR)을 참조하십시오.

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
