---
title: visitorID
description: 사용자 지정 방문자 ID를 사용합니다.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# visitorID

Adobe는 여러 가지 방법을 사용하여 사이트에서 방문자를 식별합니다. 이 `visitorID` 변수는 방문자 식별의 다른 모든 방법을 무시합니다.

> [!IMPORTANT] Adobe는 이 변수를 사용하지 않도록 권장합니다. Adobe Experience [Cloud Identity Service를](https://docs.adobe.com/content/help/en/id-service/using/home.html) 대신 사용하십시오.

## Adobe Experience Platform 시작 방문자 ID

[!UICONTROL 방문자] ID는 Adobe Analytics [!UICONTROL 확장을 구성할 때 쿠키] 아코디언 아래에 있는 필드입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 확장 [!UICONTROL 탭으로 이동한] 다음 Adobe [!UICONTROL Analytics에서 구성] 단추를 클릭합니다.
4. 방문자 [!UICONTROL ID] 필드를 표시하는 쿠키 [!UICONTROL 아코디언을] 확장합니다.

이 필드를 사용자 지정 방문자 ID가 포함된 데이터 요소에 할당합니다. 이 필드를 정적 값으로 설정하지 마십시오.

## s.visitorID in AppMeasurement and Launch 사용자 지정 코드 편집기

이 `s.visitorID` 변수는 방문자에 대한 사용자 지정 고유 식별자를 포함하는 문자열입니다. 유효한 값에는 최대 100바이트의 영숫자 문자가 포함됩니다. 이 변수에서 대시, 공백, 밑줄 또는 심볼을 사용하지 마십시오.

> [!WARNING] 방문을 통해 `visitorID` 변수를 부분적으로 설정하면 데이터가 두 개의 개별 고유 방문자로 만들어집니다.

```js
s.visitorID = "abc123";
```
