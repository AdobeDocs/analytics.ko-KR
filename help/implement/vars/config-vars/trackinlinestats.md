---
title: trackInlineStats
description: 구현에서 ClickMap을 활성화하거나 비활성화합니다.
keywords: clickmap 비활성화
feature: Variables
exl-id: a52adc1d-1be7-4002-b393-7ce66332b483
source-git-commit: 4af73d19afd8844f814aafd45153cc638aa535d6
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 31%

---

# trackInlineStats

>[!IMPORTANT]
>
>이 변수는 사용이 중단되었습니다. 다음을 참조하십시오 [Activity Map 활성화](/help/analyze/activity-map/activitymap-getting-started/activitymap-enable.md) 대신,

ClickMap은 방문자가 클릭하는 위치와 클릭하는 내용에 대한 데이터를 수집하는 Adobe Analytics의 폐기된 기능입니다. 기능이 (으)로 대체되었습니다. [Activity Map](/help/analyze/activity-map/activity-map.md).

활성화하면 AppMeasurement가 링크에 대한 정보를 수집하고 다음 이미지 요청에서 해당 데이터를 전송합니다. 각 클릭의 정보는 라는 쿠키에 저장됩니다 `s_sq`.

## Adobe Analytics 확장을 사용하여 ClickMap 활성화

[!UICONTROL ClickMap 활성화] 은(는) 아래에 있는 확인란입니다. [!UICONTROL 링크 추적] Adobe Analytics 확장을 구성할 때 아코디언

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3.  [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
4. 확장 [!UICONTROL 링크 추적] 아코디언 - [!UICONTROL ClickMap 활성화] 확인란.

>[!NOTE]
>
>이 확인란은 와 다릅니다. [!UICONTROL Activity Map 사용] 확인란: 아래에 있음 [!UICONTROL 라이브러리 관리] 아코디언

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.trackInlineStats

다음 `s.trackInlineStats` 는 ClickMap 추적을 활성화하거나 비활성화하는 부울입니다. Adobe 기능이 중단되었으므로 이 변수를 설정하지 않는 것이 좋습니다. 기본값은 `false`입니다.

```js
s.trackInlineStats = false;
```
