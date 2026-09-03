---
title: 방문자당 체류 시간 (초)
description: 방문자당 체류 시간 (초) 지표는 방문자가 방문자의 전체 라이프타임 동안 주어진 차원 항목과 상호 작용하는 평균 시간을 보여 줍니다.
feature: Metrics
exl-id: 80f38bab-2ee1-4d0d-ba53-9b2c7c85e481
TQID: https://experienceleague.adobe.com/NFmA2Q80h2WOTRwoJ882aFMG60y2HKngR0Ew0qnxb8o
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 182
ht-degree: 85%

---

# 방문자당 체류 시간 (초)

[!UICONTROL 방문자당 체류 시간(초)] [지표](overview.md)은 방문자가 방문자의 전체 라이프타임 동안 주어진 차원 항목과 상호 작용하는 평균 시간을 보여 줍니다.

이 지표는 처리 아키텍처가 달라서 Data Warehouse에서는 사용할 수 없습니다.

## 이 지표의 계산 방법

이 지표는 공식 [`Total seconds spent`](total-seconds-spent.md) `divided by` [`Unique visitors`](unique-visitors.md)를 사용합니다.

## 100%를 넘는 백분율

이 지표에는 100%를 넘는 백분율이 자주 포함됩니다. 분모는 전체 차원의 방문자당 체류 시간이고 분자는 차원 항목의 방문자당 체류 시간입니다. 전체 차원의 방문자당 체류 시간이 주어진 차원 항목의 방문자당 체류 시간보다 낮은 경우 백분율이 100%보다 높게 표시됩니다. 이 지표로 등급 보고서를 정렬하면 예외적인 방문자당 체류 시간 값이 표시되는데, 이것은 일반적으로 중요하지 않습니다. Adobe에서는 등급 보고서에서 [방문 횟수](visits.md)와 같은 다른 지표로 정렬하는 것을 권장합니다.

체류 시간에 대한 일반적인 정보가 필요하면 [체류 시간 개요](time-spent.md)를 참조하십시오.
