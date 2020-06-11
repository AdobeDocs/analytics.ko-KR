---
title: 방문자당 체류 시간(초)
description: null
translation-type: tm+mt
source-git-commit: 5282ad3f6fdd2853979cbfb2707cc07a698f63a7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 6%

---


# 방문자당 체류 시간(초)

&#39;방문자당 체류 시간(초)&#39; 지표는 방문자 전체 라이프타임 동안 방문자가 주어진 차원 값과 상호 작용하는 평균 시간을 보여줍니다.

이 지표는 처리 아키텍처로 인해 데이터 웨어하우스에서 사용할 수 없습니다.

## 이 지표의 계산 방법

이 지표는 공식을 사용합니다 [`Total seconds spent`](total-seconds-spent.md)`divided by` [`Unique visitors`](unique-visitors.md).

## 백분율이 100%를 초과합니다.

이 지표에는 100%보다 높은 백분율이 자주 포함됩니다. 분모는 방문자당 전체 차원의 체류 시간이고 분자는 방문자당 체류 시간입니다. 방문자당 전체 차원의 체류 시간이 주어진 차원 값의 방문자당 체류 시간보다 낮은 경우 백분율이 100%보다 높은 것으로 표시됩니다. 이 지표로 등급 보고서를 정렬하면 일반적으로 가치가 없는 방문자당 예외 항목 체류 시간이 표시됩니다. Adobe에서는 등급 보고서에서 방문 횟수 [와](visits.md)같은 다른 지표별로 정렬하는 것이 좋습니다.

체류 [시간에 대한 일반적인 정보는 체류 시간 개요를](time-spent.md) 참조하십시오.
