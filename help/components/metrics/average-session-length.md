---
title: 평균 세션 길이 (모바일)
description: 모바일 디바이스의 평균 세션 길이입니다.
feature: Metrics
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
source-git-commit: 47d5a532505aff48d43972836c78620870bd8221
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 65%

---

# 평균 세션 길이 (모바일)

평균 세션 길이 (모바일) 지표는 주어진 차원 항목이 차원 항목마다 존재하는 평균 시간을 보여 줍니다. 비슷하지만 [방문당 체류 시간 [초]](https://experienceleague.adobe.com/docs/analytics/components/metrics/time-spent-per-visit.html) 이 지표를 제외하고 계산의 일부로서 모바일 SDK 관련 구성 요소를 사용합니다.

## 이 지표의 계산 방법

이 지표는 [모바일 지표](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html?lang=ko-KR) `'Total session length' / ('Launches' - 'First launches'`을 사용하여 계산됩니다.
