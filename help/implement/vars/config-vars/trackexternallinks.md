---
title: trackExternalLinks
description: 종료 링크에 대한 자동 링크 추적을 활성화하거나 비활성화합니다.
translation-type: tm+mt
source-git-commit: 04b97e93a95691132680d4da197dc62eb2b9fdd1

---


# trackExternalLinks

Adobe는 각 종료 링크에 대한 `tl()` 함수를 수동으로 설정하지 않고 아웃바운드 링크를 추적하는 기능을 제공합니다. 종료 링크에 자동 링크 추적을 사용하려면 이 변수를 활성화합니다.

활성화되면 AppMeasurement는 클릭한 링크 URL을 `linkInternalFilters` `linkExternalFilters`및 의 값과 비교합니다. 일치하는 항목이 있으면 종료 링크 추적 호출이 자동으로 실행됩니다.

## Adobe Experience Platform Launch에서 아웃바운드 링크 추적

아웃바운드 링크 추적은 Adobe Analytics 확장을 구성할 [!UICONTROL 때 링크 추적] 아코디언 아래의 확인란입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 확장 [!UICONTROL 탭으로 이동한] 다음 Adobe [!UICONTROL Analytics에서 구성] 단추를 클릭합니다.
4. 아웃바운드 링크 [!UICONTROL 추적] 확인란을 표시하는 링크 추적 [!UICONTROL 아코디언을 확장합니다] .

자동 종료 링크 추적을 활성화하려면 이 확인란을 클릭합니다.

## s.trackExternalLinks in AppMeasurement and Launch 사용자 지정 코드 편집기

은 자동 종료 링크 추적을 활성화 또는 비활성화하는 `s.trackExternalLinks` 부울 값입니다. 아웃바운드 링크를 추적하지 않거나 종료 링크를 추적하는 `tl()` 함수를 수동으로 호출하려는 경우 이 변수를 로 `false`설정합니다.

```js
s.trackDownloadLinks = true;
```
