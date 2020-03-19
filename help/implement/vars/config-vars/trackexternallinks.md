---
title: trackExternalLinks
description: 종료 링크에 대한 자동 링크 추적을 활성화하거나 비활성화합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# trackExternalLinks

Adobe는 각 종료 링크에 대한 [`tl()`](../functions/tl-method.md) 방법을 수동으로 설정하지 않고 아웃바운드 링크를 추적하는 기능을 제공합니다. 종료 링크에 자동 링크 추적을 사용하려면 이 변수를 활성화합니다.

활성화되면 AppMeasurement는 클릭한 링크 URL을 [`linkInternalFilters`](linkinternalfilters.md) [`linkExternalFilters`](linkexternalfilters.md)및 의 값과 비교합니다. 일치하는 항목이 있으면 종료 링크 추적 호출이 자동으로 실행됩니다.

## Adobe Experience Platform Launch에서 아웃바운드 링크 추적

아웃바운드 링크 추적은 Adobe Analytics 확장을 구성할 때 아코디언 아래의 [!UICONTROL Link Tracking] 확인란입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
4. 확인란을 표시하는 [!UICONTROL Link Tracking] 아코디언을 [!UICONTROL Track outbound links] 확장합니다.

자동 종료 링크 추적을 활성화하려면 이 확인란을 클릭합니다.

## s.trackExternalLinks in AppMeasurement and Launch 사용자 지정 코드 편집기

은 자동 종료 링크 추적을 활성화 또는 비활성화하는 `s.trackExternalLinks` 부울 값입니다. 아웃바운드 링크를 추적하지 않거나 종료 링크를 추적하기 위해 메서드를 수동으로 호출하려는 경우 이 변수를 로 `tl()` `false`설정합니다.

```js
s.trackDownloadLinks = true;
```
