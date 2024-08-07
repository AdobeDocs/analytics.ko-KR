---
title: 방문당 체류 시간 (차원)
description: 방문이 걸린 총 시간입니다.
feature: Dimensions
exl-id: f241eb2d-7e22-47ee-ade8-8aeb7b2b9694
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 92%

---

# 방문당 체류 시간

*이 도움말 페이지에서는 &#39;방문당 체류 시간&#39;이 각각의 [차원](overview.md)(으)로 작동하는 방식을 설명합니다. 자세한 내용은 [방문당 체류 시간](../metrics/time-spent-per-visit.md) 지표를 참조하십시오.*

방문당 체류 시간 차원은 방문자가 전체 방문에서 보낸 시간을 기록합니다. 다음 절차를 사용하여 계산을 측정합니다.

1. 방문의 첫 번째 히트에 대한 타임스탬프를 봅니다.
2. 이 히트를 방문의 마지막 히트의 타임스탬프와 비교합니다.
3. 이 두 히트 사이에 경과된 시간이 페이지에서 보낸 시간에 기여합니다.

이러한 차원은 일반적으로 방문자가 사이트와 상호 작용하는 시간을 파악하려는 경우 유용합니다.

>[!TIP]
>
>체류 시간은 시간을 측정하기 위해 방문에서 적어도 두 개의 히트를 필요로 합니다. 하나의 히트로 구성된 방문은 이 차원에 나타나지 않습니다.

이 차원은 방문을 기반으로 합니다. 이는 값이 방문 내의 모든 히트에 적용되며 변경되지 않음을 의미합니다. 이 차원을 히트 기반 차원인 [페이지에서 보낸 시간](time-spent-on-page.md)과 비교해 보십시오.

이 차원은 [사이트에서 보낸 평균 시간](../metrics/average-time-on-site.md) 및 [방문당 체류 시간](../metrics/time-spent-per-visit.md) 지표와 관련이 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## 차원 항목

방문당 체류 시간에 대해 여러 차원이 존재합니다.

* **방문당 체류 시간 - 그룹**: 시간이 버킷됩니다. 차원 항목의 범위는 `"Less than 1 minute"`부터 `"More than 15 hours"`까지 입니다. 일반적으로 방문은 12시간 이상 지속되지 않습니다. 하지만 타임스탬프가 지정된 히트나 데이터 소스를 사용하는 경우 방문이 12시간을 초과할 수 있습니다.
* **방문당 체류 시간 - 세부기간**: 각각의 초 수는 고유한 차원 항목입니다. 이 차원은 Data Warehouse에서 사용할 수 없습니다.

체류 시간에 대한 일반적인 정보가 필요하면 [체류 시간 개요](../metrics/time-spent.md)를 참조하십시오.
