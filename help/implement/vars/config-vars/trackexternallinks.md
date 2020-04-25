---
title: trackExternalLinks
description: 종료 링크에 대한 자동 링크 추적을 활성화하거나 비활성화합니다.
translation-type: tm+mt
source-git-commit: 94218548dc4e3efd57df95c992003e94640e4330

---


# trackExternalLinks

Adobe offers the ability to track outbound links without manually setting the [`tl()`](../functions/tl-method.md) method for each exit link. 종료 링크에 대한 자동 링크 추적을 사용하려면 이 변수를 활성화하십시오.

활성화되면 AppMeasurement는 클릭한 모든 링크 URL을 [`linkInternalFilters`](linkinternalfilters.md) 및 [`linkExternalFilters`](linkexternalfilters.md)의 값과 비교합니다. 일치하는 항목이 있으면 종료 링크 추적 호출이 자동으로 실행됩니다.

## Adobe Experience Platform Launch에서 아웃바운드 링크 추적

아웃바운드 링크 추적은 Adobe Analytics 확장을 구성할 때 [!UICONTROL 링크 추적] 아코디언 아래에 있는 확인란입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
4. [!UICONTROL 링크 추적] 아코디언을 확장합니다. 그러면 [!UICONTROL 아웃바운드 링크 추적] 확인란이 표시됩니다.

자동 종료 링크 추적을 활성화하려면 확인란을 클릭하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.trackExternalLinks

`s.trackExternalLinks`는 자동 종료 링크 추적을 활성화하거나 비활성화화하는 부울입니다. If you do not want to track outbound links, or would prefer to manually call the `tl()` method to track exit links, set this variable to `false`.

```js
s.trackExternalLinks = true;
```
