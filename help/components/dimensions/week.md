---
title: 주
description: 지표가 발생한 주입니다.
translation-type: tm+mt
source-git-commit: a94b8e090b9a3c75a57fd396cac8486bba2e5d79
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 42%

---


# 주

주 차원은 주어진 지표가 발생한 주를 보고합니다. 첫 번째 차원 항목은 날짜 범위의 첫 번째 주이고 마지막 차원 항목은 날짜 범위의 마지막 주입니다. 이 차원은 시간에 따른 지표를 볼 수 있으므로 트렌드 보고서에 필수적입니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## Dimension 항목

Analysis Workspace에서 차원 항목에는 주의 첫째 날의 날짜(월, 일 및 연도)가 포함됩니다.

Data Warehouse에서 차원 항목에는 요청의 날짜 범위를 기반으로 번호가 매겨진 주일이 포함됩니다. 예를 들어 첫 번째 전체 주는 입니다 `"Week 1"`. 요청에 부분 주가 포함된 경우 데이터는 차원 항목으로 그룹화됩니다 `"Week 0"`.
