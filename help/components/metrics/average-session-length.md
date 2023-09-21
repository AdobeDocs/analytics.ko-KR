---
title: 평균 세션 길이 (모바일)
description: 모바일 디바이스의 평균 세션 길이입니다.
feature: Metrics
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 41%

---

# 평균 세션 길이 (모바일)

평균 세션 길이(모바일) [지표](overview.md) 주어진 차원 항목이 차원 항목마다 존재하는 평균 시간을 보여줍니다. 이는 과 유사합니다. [방문당 체류 시간[초]](https://experienceleague.adobe.com/docs/analytics/components/metrics/time-spent-per-visit.html) 이 지표를 제외한 다른 지표에서는 계산의 일부로서 모바일 SDK 관련 구성 요소를 사용합니다.

## 이 지표의 계산 방법

이 지표는 [모바일 지표](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html?lang=ko-KR) `'Total session length' / ('Launches' - 'First launches'`을 사용하여 계산됩니다.
