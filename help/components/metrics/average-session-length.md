---
title: 평균 세션 길이 (모바일)
description: 모바일 디바이스의 평균 세션 길이입니다.
feature: Metrics
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
TQID: https://experienceleague.adobe.com/4TaQP7sH0pADpnwoQR-aqOpKqKvcuUXU1vmE3-ETOzM
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 36%

---

# 평균 세션 길이 (모바일)

&#39;평균 세션 길이(모바일)&#39; [지표](overview.md)은(는) 차원 항목당 주어진 차원 항목이 있는 평균 시간을 보여줍니다. 이 지표는 계산의 일부로 모바일 SDK 관련 구성 요소를 사용한다는 점을 제외하면 [[!UICONTROL 방문당 체류 시간(초)]](time-spent-per-visit.md) 지표와 유사합니다.

## 이 지표의 계산 방법

이 지표는 [라이프사이클 지표](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/) `'Total Session length' / ('Launches' - 'First launches'`을(를) 사용하여 계산됩니다.
