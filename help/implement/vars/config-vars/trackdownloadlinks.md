---
title: trackDownloadLinks
description: 다운로드 링크에 대한 자동 링크 추적을 활성화하거나 비활성화합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# trackDownLoadLinks

Adobe offers the ability to track download links without manually setting the [`tl()`](../functions/tl-method.md) method for each download link. 다운로드 링크에 대한 자동 링크 추적을 사용하려면 이 변수를 활성화하십시오.

활성화되면 AppMeasurement는 클릭한 모든 링크 URL을 [`linkDownloadFileTypes`](linkdownloadfiletypes.md)의 값과 비교합니다. 일치하는 항목이 있으면 다운로드 링크 추적 호출이 자동으로 실행됩니다.

## Adobe Experience Platform Launch에서 다운로드 링크 추적

다운로드 링크 추적은 Adobe Analytics 확장을 구성할 때 [!UICONTROL 링크 추적] 아코디언 아래에 있는 확인란입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
4. [!UICONTROL 링크 추적] 아코디언을 확장합니다. 그러면 [!UICONTROL 다운로드 링크 추적] 확인란이 표시됩니다.

자동 다운로드 링크 추적을 활성화하려면 확인란을 클릭하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.trackDownloadLinks

`s.trackDownloadLinks`는 자동 다운로드 링크 추적을 활성화하거나 비활성화하는 부울입니다. If you do not want to track download links, or would prefer to manually call the `tl()` method to track downloads, set this variable to `false`.

```js
s.trackDownloadLinks = true;
```
