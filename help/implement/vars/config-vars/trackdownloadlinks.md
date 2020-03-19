---
title: trackDownloadLinks
description: 다운로드 링크에 대한 자동 링크 추적을 활성화하거나 비활성화합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# trackDownLoadLinks

Adobe는 각 다운로드 링크에 대한 [`tl()`](../functions/tl-method.md) 방법을 수동으로 설정하지 않고도 다운로드 링크를 추적하는 기능을 제공합니다. 다운로드 링크에 자동 링크 추적을 사용하려면 이 변수를 활성화합니다.

활성화되면 AppMeasurement는 클릭한 모든 링크 URL을 의 값과 비교합니다 [`linkDownloadFileTypes`](linkdownloadfiletypes.md). 일치하는 항목이 있으면 다운로드 링크 추적 호출이 자동으로 실행됩니다.

## Adobe Experience Platform Launch에서 다운로드 링크 추적

다운로드 링크 추적은 Adobe Analytics 확장 기능을 구성할 때 아코디언 아래의 [!UICONTROL Link Tracking] 확인란입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
4. 확인란을 표시하는 [!UICONTROL Link Tracking] 아코디언을 [!UICONTROL Track download links] 확장합니다.

확인란을 클릭하여 자동 다운로드 링크 추적을 활성화합니다.

## s.trackDownloadLinks in AppMeasurement and Launch custom code editor

은 자동 다운로드 링크 추적을 활성화 또는 비활성화하는 `s.trackDownloadLinks` 부울 값입니다. 다운로드 링크를 추적하지 않으려는 경우 또는 다운로드를 추적할 `tl()` 방법을 수동으로 호출하려는 경우 이 변수를 로 설정하십시오 `false`.

```js
s.trackDownloadLinks = true;
```
