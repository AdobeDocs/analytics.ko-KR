---
title: 평균 세션 길이 (모바일)
description: 모바일 디바이스의 평균 세션 길이입니다.
feature: Metrics
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 26%

---

# 평균 세션 길이 (모바일)

평균 세션 길이(모바일) [지표](overview.md) 주어진 차원 항목이 차원 항목마다 존재하는 평균 시간을 보여줍니다. 이는 과 유사합니다. [[!UICONTROL 방문당 체류 시간 (초)]](time-spent-per-visit.md) 이 지표를 제외한 다른 지표에서는 계산의 일부로서 모바일 SDK 관련 구성 요소를 사용합니다.

## 이 지표의 계산 방법

이 지표는 다음을 사용하여 계산됩니다. [라이프사이클 지표](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/) `'Total Session length' / ('Launches' - 'First launches'`.
