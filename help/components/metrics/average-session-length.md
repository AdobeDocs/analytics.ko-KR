---
title: 평균 세션 길이 (모바일)
description: 모바일 디바이스의 평균 세션 길이입니다.
feature: Metrics
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
source-git-commit: 7966c7d9add0011831c97fbe0dfcca2acd8afb58
workflow-type: ht
source-wordcount: '81'
ht-degree: 100%

---

# 평균 세션 길이 (모바일)

평균 세션 길이 (모바일) 지표는 주어진 차원 항목이 차원 항목마다 존재하는 평균 시간을 보여 줍니다. 이 지표는 계산의 일부로서 모바일 SDK 관련 구성 요소를 사용한다는 점을 제외하면 [사이트의 평균 시간](average-time-on-site.md)과 유사합니다.

## 이 지표의 계산 방법

이 지표는 [모바일 지표](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html?lang=ko-KR) `'Total session length' / ('Launches' - 'First launches'`을 사용하여 계산됩니다.
