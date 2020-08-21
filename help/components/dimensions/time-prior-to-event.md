---
title: 이벤트까지 남은 시간
description: 방문의 첫 번째 히트와 지표 사이의 시간입니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 78%

---


# 이벤트까지 남은 시간

이벤트까지 남은 시간 차원은 방문의 첫 번째 히트와 원하는 지표 사이에 경과된 시간을 보고합니다. 이 차원은 양식 제출이나 구매와 같은 성공 이벤트에 도달하는 데 걸리는 시간을 파악하는 데 유용합니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 기술적으로 즉시 작동하지만 사용자 지정 및 구매 이벤트에 가장 잘 작동합니다. 사이트에서는 사용자 지정 이벤트를 구현하는 것이 좋습니다. 사용자 지정 이벤트를 구현하는 경우 이 차원에 대해 추가적인 구현은 필요하지 않습니다.

## Dimension 항목

Dimension items include time-based buckets ranging from `"Less than 1 minute"` to `"More than 15 hours"`. For example, if it took a visitor 23 minutes from their first hit to a purchase, it would belong under the `"10 to 30 minutes"` dimension item.
