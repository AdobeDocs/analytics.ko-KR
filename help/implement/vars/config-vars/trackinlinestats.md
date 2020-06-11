---
title: trackInlineStats
description: 구현에서 Activity Map을 활성화하거나 비활성화합니다.
keywords: disable activity map
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 100%

---


# trackInlineStats

Activity Map은 방문자가 클릭하는 위치와 클릭하는 내용에 대한 데이터를 수집하는 Adobe Analytics의 기능입니다. Analytics 보고서나 브라우저 확장 오버레이를 사용하여 이 데이터를 볼 수 있습니다. Activity Map 기능을 사용하려면 이 변수를 활성화하십시오.

활성화하면 AppMeasurement가 링크에 대한 정보를 수집하고 다음 이미지 요청에서 해당 데이터를 전송합니다. 각 클릭의 정보는 `s_sq`라는 레이블이 지정된 쿠키에 저장됩니다.

## Adobe Experience Platform Launch에서 ClickMap 활성화

[!UICONTROL ClickMap 활성화]는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 링크 추적] 아코디언 아래에 있는 확인란입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
4. [!UICONTROL 링크 추적] 아코디언을 확장합니다. 그러면 [!UICONTROL ClickMap 활성화] 확인란이 표시됩니다.

Activity Map 추적을 활성화하려면 확인란을 클릭하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.trackInlineStats

`s.trackInlineStats`는 Activity Map 추적을 활성화하거나 비활성화하는 부울입니다. 기본값은 `false`입니다. Activity Map 데이터 수집을 활성화하려면 이 값을 `true`로 설정하십시오.

```js
s.trackInlineStats = true;
```
