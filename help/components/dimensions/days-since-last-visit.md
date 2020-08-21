---
title: 마지막 방문 이후의 일 수
description: 현재 히트와 마지막으로 방문한 시간 사이의 일 수입니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 74%

---


# 마지막 방문 이후의 일 수

마지막 방문 이후의 일 수 차원은 방문자의 현재 히트와 이전 방문(있는 경우) 사이에 경과된 시간의 크기를 측정합니다. 이 차원은 방문자가 사이트를 방문한 후 취하는 동작을 이해하는 데 도움이 됩니다. 해당 예는 다음과 같습니다.

* 사용자가 사이트를 얼마나 자주 다시 방문합니까?
* 반환 주기와 전환 사이에는 어떤 상관 관계가 있습니까? 반복 구매자들은 자주 방문하는 편입니까 가끔 방문하는 편입니까?
* 캠페인을 클릭하여 이동한 사용자가 자주 방문합니까?

처음 방문하는 사람은 이 차원에 포함되지 않습니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## Dimension 항목

Dimension 항목에는 방문자의 마지막 방문과 현재 히트 사이의 일 수가 포함됩니다. Each number of days is a separate dimension item, with `"Same day"` occurring where a visitor&#39;s last visit and the current hit happened on the same day.
