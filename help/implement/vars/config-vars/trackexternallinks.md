---
title: trackExternalLinks
description: 종료 링크에 대한 자동 링크 추적을 활성화하거나 비활성화합니다.
exl-id: a34d4ffa-ff82-460e-af7d-1a4be85fc631
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: ht
source-wordcount: '189'
ht-degree: 100%

---

# trackExternalLinks

Adobe는 각 종료 링크에 대한 [`tl()`](../functions/tl-method.md) 메서드를 수동으로 설정하지 않고도 아웃바운드 링크를 추적하는 기능을 제공합니다. 종료 링크에 대한 자동 링크 추적을 사용하려면 이 변수를 활성화하십시오.

활성화되면 AppMeasurement는 클릭한 모든 링크 URL을 [`linkInternalFilters`](linkinternalfilters.md) 및 [`linkExternalFilters`](linkexternalfilters.md)의 값과 비교합니다. 일치하는 항목이 있으면 종료 링크 추적 호출이 자동으로 실행됩니다.

## Adobe Experience Platform의 태그를 사용하는 아웃바운드 링크 추적

아웃바운드 링크 추적은 Adobe Analytics 확장을 구성할 때 [!UICONTROL 링크 추적] 아코디언 아래에 있는 확인란입니다.

1. AdobeID 자격 증명을 사용하여 [데이터 수집 UI](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 버튼을 클릭합니다.
4. [!UICONTROL 링크 추적] 아코디언을 확장합니다. 그러면 [!UICONTROL 아웃바운드 링크 추적] 확인란이 표시됩니다.

자동 종료 링크 추적을 활성화하려면 확인란을 클릭하십시오.

## AppMeasurement 및 사용자 지정 코드 편집기의 s.trackExternalLinks

`s.trackExternalLinks`는 자동 종료 링크 추적을 활성화하거나 비활성화하는 부울입니다. 아웃바운드 링크를 추적하지 않으려는 경우 또는 `tl()` 메서드를 수동으로 호출하여 종료 링크를 추적하려는 경우 이 변수를 `false`로 설정하십시오.

```js
s.trackExternalLinks = true;
```
