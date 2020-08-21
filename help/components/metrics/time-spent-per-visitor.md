---
title: 방문자당 체류 시간(초)
description: null
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 54%

---


# 방문자당 체류 시간(초)

&#39;방문자당 체류 시간(초)&#39; 지표는 방문자의 전체 라이프타임 동안 방문자가 주어진 차원 항목과 상호 작용하는 평균 시간을 보여줍니다.

이 지표는 처리 아키텍처가 달라서 Data Warehouse에서는 사용할 수 없습니다.

## 이 지표의 계산 방법

이 지표는 공식 [`Total seconds spent`](total-seconds-spent.md) `divided by` [`Unique visitors`](unique-visitors.md)를 사용합니다.

## 100%를 넘는 백분율

이 지표에는 100%를 넘는 백분율이 자주 포함됩니다. 분모는 방문자당 전체 차원의 체류 시간이고 분자는 방문자당 체류 시간입니다. 방문자당 전체 차원의 체류 시간이 특정 차원 항목의 방문자당 체류 시간보다 낮은 경우 백분율이 100%를 넘는 것을 볼 수 있습니다. 이 지표로 등급 보고서를 정렬하면 예외적인 방문자당 체류 시간 값이 표시되는데, 이것은 일반적으로 중요하지 않습니다. Adobe에서는 등급 보고서에서 [방문 횟수](visits.md)와 같은 다른 지표로 정렬하는 것을 권장합니다.

체류 시간에 대한 일반적인 정보가 필요하면 [체류 시간 개요](time-spent.md)를 참조하십시오.
