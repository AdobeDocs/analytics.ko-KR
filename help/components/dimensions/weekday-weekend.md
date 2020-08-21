---
title: 평일/주말
description: 히트가 평일과 주말 중 언제 발생했는지를 확인합니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 68%

---


# 평일/주말

평일/주말 차원은 히트가 평일(월요일 - 금요일)과 주말(토요일 - 일요일) 중 언제 발생했는지 알려줍니다. 히트 시간은 [보고서 세트의 시간대](/help/admin/admin/general-acct-settings-admin.md)를 기반으로 합니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## Dimension 항목

This dimension always contains exactly two dimension items: `"Weekday"` and `"Weekend"`. The dimension item `"Weekday"` applies to all hits Monday through Friday, while the dimension item `"Weekend"` applies to all hits on Saturday and Sunday.
