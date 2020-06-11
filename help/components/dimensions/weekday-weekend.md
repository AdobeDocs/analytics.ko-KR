---
title: 평일/주말
description: 히트가 평일 또는 주말 동안 발생했는지 여부를 결정합니다.
translation-type: tm+mt
source-git-commit: 05ea2778cd5cd324c660fd0f1d2ac02373829f0f
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 3%

---


# 평일/주말

&#39;평일/주말&#39; 차원은 평일(월요일 - 금요일) 또는 주말(토요일 - 일요일) 중에 히트가 발생했는지 여부를 알려줍니다. The time of the hit is based on the [report suite&#39;s time zone](/help/admin/admin/general-acct-settings-admin.md).

## 데이터로 이 차원 채우기

이 차원은 모든 구현에서 기본적으로 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## 차원 값

이 차원은 항상 두 개의 차원 값을 포함합니다. `"Weekday"` 및 `"Weekend"`. 차원 값 `"Weekday"` 은 월요일부터 금요일까지 모든 히트에 적용되는 반면 차원 값은 토요일과 일요일의 모든 히트에 `"Weekend"` 적용됩니다.
