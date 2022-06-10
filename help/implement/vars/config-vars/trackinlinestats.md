---
title: trackInlineStats
description: 구현에서 Activity Map을 활성화하거나 비활성화합니다.
keywords: Activity Map 비활성화
feature: Variables
exl-id: a52adc1d-1be7-4002-b393-7ce66332b483
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 78%

---

# trackInlineStats

Activity Map은 방문자가 클릭하는 위치와 클릭하는 내용에 대한 데이터를 수집하는 Adobe Analytics의 기능입니다. Analytics 보고서나 브라우저 확장 오버레이를 사용하여 이 데이터를 볼 수 있습니다. Activity Map 기능을 사용하려면 이 변수를 활성화하십시오.

활성화하면 AppMeasurement가 링크에 대한 정보를 수집하고 다음 이미지 요청에서 해당 데이터를 전송합니다. 각 클릭의 정보는 `s_sq`라는 레이블이 지정된 쿠키에 저장됩니다.

## 웹 SDK를 사용하여 Activity Map

웹 SDK는 아직 Activity Map 데이터 수집을 지원하지 않습니다.

## Adobe Analytics 확장을 사용하여 Clickmap 활성화

[!UICONTROL ClickMap 활성화]는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 링크 추적] 아코디언 아래에 있는 확인란입니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
4. [!UICONTROL 링크 추적] 아코디언을 확장합니다. 그러면 [!UICONTROL ClickMap 활성화] 확인란이 표시됩니다.

Activity Map 추적을 활성화하려면 확인란을 클릭하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.trackInlineStats

`s.trackInlineStats`는 Activity Map 추적을 활성화하거나 비활성화하는 부울입니다. 기본값은 `false`입니다. Activity Map 데이터 수집을 활성화하려면 이 값을 `true`로 설정하십시오.

```js
s.trackInlineStats = true;
```
