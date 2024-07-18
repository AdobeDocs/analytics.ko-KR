---
title: 평균 세션 길이 (모바일)
description: 모바일 디바이스의 평균 세션 길이입니다.
feature: Metrics
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 29%

---

# 평균 세션 길이 (모바일)

&#39;평균 세션 길이(모바일)&#39; [지표](overview.md)은(는) 차원 항목당 주어진 차원 항목이 있는 평균 시간을 보여줍니다. 이 지표는 계산의 일부로 모바일 SDK 관련 구성 요소를 사용한다는 점을 제외하면 [[!UICONTROL 방문당 체류 시간(초)]](time-spent-per-visit.md) 지표와 유사합니다.

## 이 지표의 계산 방법

이 지표는 [라이프사이클 지표](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/) `'Total Session length' / ('Launches' - 'First launches'`을(를) 사용하여 계산됩니다.
