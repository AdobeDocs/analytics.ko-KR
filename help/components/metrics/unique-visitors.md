---
title: 고유 방문자 수
description: 고유 방문자 ID의 수입니다.
feature: Metrics
exl-id: 56e7bad4-4802-49ac-a0f1-ae77441fc016
source-git-commit: f26f406848ab26092738089aac64ed9b4fc08019
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 83%

---

# 고유 방문자 수

“고유 방문자 수” [지표](overview.md)는 차원 항목에 대한 방문자 ID의 수를 보여 줍니다. 차원 항목의 인기도에 대한 높은 수준의 개요를 제공하므로 트래픽을 결정할 때 사용되는 가장 일반적인 지표 중 하나입니다. 예를 들어 방문자는 한 달 동안 매일 사이트를 방문할 수 있지만 여전히 하나의 고유 방문자로 계산됩니다.

[디바이스 간 분석](../cda/overview.md)을 사용하는 경우 지표는 [고유 디바이스](unique-devices.md) 지표로 대체됩니다.

## 일별, 주별, 월별, 분기별 및 연간 고유 방문자 수

Analysis Workspace는 보고서의 세부기간을 기준으로 고유 방문자를 처리합니다. 예를 들어 [일](../dimensions/day.md) 차원을 사용하는 경우 각 차원 항목에 대한 일별 고유 방문자 수를 보게 됩니다. 하지만 보고서 합계의 경우에는 자유 형식 테이블의 날짜 범위에 대해 중복이 제거된 고유 방문자 수입니다.

## 이 지표의 계산 방법

이 지표는 주어진 차원 항목에 대한 고유 방문자 ID의 수를 계산합니다. Adobe Analytics이 고유 방문자를 식별하는 방법에 대한 자세한 내용은 [방문자 식별 개요](/help/implement/id/overview.md)를 참조하십시오.
