---
title: trackInlineStats
description: 구현에서 Activity map 활성화 또는 비활성화
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# trackInlineStats

Activity Map은 방문자가 클릭하는 위치와 클릭하는 내용에 대한 데이터를 수집하는 Adobe Analytics의 기능입니다. Analytics 보고서나 브라우저 확장 오버레이를 사용하여 이 데이터를 볼 수 있습니다. Activity Map 기능을 사용하려면 이 변수를 활성화합니다.

활성화되면 AppMeasurement는 링크에 대한 정보를 수집하고 다음 이미지 요청에서 해당 데이터를 전송합니다. 각 클릭의 정보는 레이블이 지정된 쿠키에 저장됩니다 `s_sq`.

## Adobe Experience Platform Launch에서 Clickmap 활성화

[!UICONTROL Adobe Analytics] 확장을 구성할 때 [!UICONTROL 링크 추적] 아코디언 아래의 확인란은 Clickmap 활성화입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 확장 [!UICONTROL 탭으로 이동한] 다음 Adobe [!UICONTROL Analytics에서 구성] 단추를 클릭합니다.
4. Clickmap [!UICONTROL 사용] 확인란을 표시하는 링크 추적 [!UICONTROL 아코디언을 확장합니다] .

확인란을 클릭하여 Activity Map 추적을 활성화합니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.trackInlineStats

은 `s.trackInlineStats` Activity Map 추적을 활성화하거나 비활성화하는 부울입니다. Its default value is `false`. Activity Map 데이터 수집을 활성화하려는 `true` 경우 이 값을 설정합니다.

```js
s.trackInlineStats = true;
```
