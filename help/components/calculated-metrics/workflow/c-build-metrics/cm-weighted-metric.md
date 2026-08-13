---
description: 필터 및 가중치가 적용된 지표의 예에 대해 알아봅니다.
title: 필터 및 가중치가 적용된 지표
feature: Calculated Metrics
exl-id: bea46e03-7d05-44c8-b654-c61b1e32becc
TQID: https://experienceleague.adobe.com/Euk3sI0-AYtfmpEbL-8gfWU4HcFE6kGO6QGgctZbvig
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 9%

---

# 필터 및 가중치가 적용된 지표

이 문서에서는 필터 및 가중치가 적용된 지표의 예를 보여줍니다.

## 필터링된 바운스 비율

이 간단한 필터 지표는 방문이 100개를 초과하는 페이지에 대한 바운스 비율만 표시합니다.

![필터링된 바운스 비율](assets/filtered-bounce-rate.png){zoomable="yes"}

이 공식은 일관된 시간 범위에 따라 다르다는 점을 명심하십시오. 하루 동안 보고서를 실행하는 경우 방문이 20개가 넘는 페이지는 모두 살펴볼 가치가 있습니다. 한 달 동안 실행하는 경우 필터에 더 많은 방문을 포함할 수 있습니다.

## 백분위수로 필터링된 바운스 비율

이 필터는 방문 횟수로 정렬할 때 페이지의 상위 30%에 대한 바운스 비율을 표시합니다.

![백분위수로 필터링된 바운스 비율](assets/filtered-bounce-rate-with-percentile.png){zoomable="yes"}

## 가중치가 적용된 바운스 비율

일반적으로 바운스 비율을 기준으로 정렬하려고 하지만 방문 횟수가 더 많은 페이지가 목록에서 더 높아야 한다고 가정합니다. 다음과 같은 모습의 가중치가 적용된 바운스 비율을 만들 수 있습니다.

![](assets/weighted-bounce-rate.png)
