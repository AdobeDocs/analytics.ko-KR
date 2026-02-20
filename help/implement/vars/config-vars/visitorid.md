---
title: visitorID
description: 사용자 지정 방문자 ID를 사용합니다.
feature: Appmeasurement Implementation
exl-id: cb336042-01a1-4a66-a947-a221a7919c1b
role: Admin, Developer
source-git-commit: de98bf68c57f5453b6662f6e6e57312d8fd3e642
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 19%

---

# visitorID

Adobe에서는 여러 가지 방법을 사용하여 사이트에서 방문자를 [식별](../../id/overview.md)합니다. **`visitorID` 변수는 다른 모든 방문자 식별 메서드를 무시합니다.**

>[!IMPORTANT]
>
>이 변수는 사용하지 않는 것이 좋습니다. 대신 [Adobe Experience Cloud ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ko-KR)를 사용하십시오.

## Analytics에서 `visitorID`을(를) 사용하는 방법

이 변수는 다른 모든 유형의 방문자 식별을 대체하는 수동 방문자 ID 재정의입니다. 단일 방문자로 계산하려면 개인용 모든 히트에서 동일한 `visitorID` 값을 사용해야 합니다.

* `visitorID`을(를) 생략한 히트는 다른 방문자 식별 방법으로 대체되며 별도의 방문자로 처리됩니다.
* 두 개 이상의 `visitorID` 값을 사용하는 히트는 별도의 방문자로 처리됩니다.
* Adobe에서는 서로 다른 방문자 ID를 사용하는 히트를 결합하지 않습니다.

식별 우선 순위 및 식별자를 혼합하면 방문자 수가 부풀려지는 이유에 대한 자세한 내용은 [Adobe Analytics의 방문자 식별](../../id/overview.md)을 참조하십시오.

>[!WARNING]
>
>해당 사용자에 대한 모든 히트에 대해 설정되어 있고 값이 변경되지 않는다고 보장할 수 있는 경우에만 `visitorID`을(를) 설정하십시오. 일부 히트에서만 설정하거나, 방문 도중에 도입하거나(인증 시 등), 히트 간에 변경하면 단일 방문자의 활동이 여러 방문자로 분할됩니다.

>[!CAUTION]
>
>잘못된 사용자 지정 방문자 ID 값으로 인해 데이터가 올바르지 않고 보고 성능이 저하될 수 있습니다. 이 변수에 기본값 또는 자리 표시자 값(예: `"0"` 또는 `"NULL"`)이 포함되어 있으면 Adobe은 이러한 히트를 동일한 방문자인 것처럼 취급합니다. 이 경우 방문자 수가 인위적으로 적고 방문자 수준 세그먼트가 예상대로 작동하지 않아 잘못된 데이터가 발생합니다. 사용자 지정 방문자 ID를 잘못 구현하면 처리 서버에 부하가 발생하여 [지연](/help/technotes/latency.md)이 증가하고 보고서 성능이 저하될 수도 있습니다.

## Adobe Analytics 확장을 사용한 방문자 ID

[!UICONTROL 방문자 ID]는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 쿠키] 아코디언 아래의 필드입니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 선택합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음 Adobe Analytics 아래의 **[!UICONTROL 구성]** 단추를 선택합니다.
4. [!UICONTROL 쿠키] 아코디언을 확장합니다. 그러면 [!UICONTROL 방문자 ID] 필드가 표시됩니다.

이 필드를 사용자 지정 방문자 ID가 포함된 데이터 요소에 할당하십시오. **모든 방문자에 대해 이 필드를 단일 정적 값으로 설정하지 마십시오.** 방문자별로 확인되고 모든 히트에서 일정하게 유지되는 데이터 요소를 사용합니다.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.visitorID

`s.visitorID` 변수는 방문자에 대한 사용자 지정 고유 식별자를 포함하는 문자열입니다. 유효한 값에는 최대 100바이트의 영숫자 문자가 포함됩니다. 대시, 공백, 밑줄 또는 기호는 이 변수에서 사용하지 마십시오.

```js
s.visitorID = "abc123";
```

## 웹 SDK을 사용하는 방문자 ID

Adobe Experience Platform Edge Network을 사용하면 XDM의 [ID 맵](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/overview.html?lang=ko#using-identitymap)을 사용하여 여러 식별자를 제공할 수 있습니다. ID 맵의 각 ID에는 다른 네임스페이스가 있습니다. [데이터 스트림 구성](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=ko#analytics)의 일부로 방문자 ID에 사용할 네임스페이스를 지정할 수 있습니다. 이 필드가 구성되면 이 네임스페이스에 대해 지정된 값으로 이벤트를 보낼 때 Analytics에서 방문자 ID로 자동으로 사용됩니다.
