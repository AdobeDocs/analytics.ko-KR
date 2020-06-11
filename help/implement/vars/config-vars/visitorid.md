---
title: visitorID
description: 사용자 지정 방문자 ID를 사용합니다.
translation-type: tm+mt
source-git-commit: b9bb7a60398b8c392393a8d16b58292f91ab0ea7
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 71%

---


# visitorID

Adobe에서는 여러 메서드를 사용하여 사이트의 방문자를 식별합니다. `visitorID` 변수는 다른 모든 방문자 식별 메서드를 무시합니다.

>[!IMPORTANT] 이 변수는 사용하지 않는 것이 좋습니다. 대신 [Adobe Experience Cloud ID 서비스](https://docs.adobe.com/content/help/ko-KR/id-service/using/home.html)를 사용하십시오.

## Adobe Experience Platform Launch의 방문자 ID

[!UICONTROL 방문자 ID]는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 쿠키] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
4. [!UICONTROL 쿠키] 아코디언을 확장합니다. 그러면 [!UICONTROL 방문자 ID] 필드가 표시됩니다.

이 필드를 사용자 지정 방문자 ID가 포함된 데이터 요소에 할당하십시오. 이 필드를 정적 값으로 설정하지는 마십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.visitorID

`s.visitorID` 변수는 방문자에 대한 사용자 지정 고유 식별자를 포함하는 문자열입니다. 유효한 값에는 최대 100바이트의 영숫자 문자가 포함됩니다. 대시, 공백, 밑줄 또는 기호는 이 변수에서 사용하지 마십시오.

>[!WARNING] 방문 도중에 `visitorID` 변수를 설정하면 데이터가 두 개의 개별 고유 방문자가 됩니다.

```js
s.visitorID = "abc123";
```

>[!CAUTION] 사용자 지정 방문자 ID의 구현이 잘못되면 데이터가 잘못되고 보고 성능이 저하될 수 있습니다. 이 변수에 기본값(예: `"0"` 또는 `"NULL"`)이 포함된 경우 Adobe는 이러한 히트를 동일한 방문자로 취급합니다. 이 경우 방문자 수가 적고 방문자 수준 세그먼트가 예상대로 작동하지 않아 데이터가 잘못됩니다. 사용자 지정 방문자 ID를 잘못 구현하여 처리 서버에서 무거운 로드가 발생하고 [지연이](/help/technotes/latency.md) 증가하고 보고서 성능이 저하됩니다.
