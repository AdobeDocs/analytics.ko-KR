---
title: 평일/주말
description: 히트가 평일과 주말 중 언제 발생했는지를 확인합니다.
feature: Dimensions
exl-id: c3111cdc-a5f9-4244-a725-b1bb1e72fcff
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 80%

---

# 평일/주말

평일/주말 [차원](overview.md) 히트가 평일(월요일 - 금요일)과 주말(토요일 - 일요일) 중 언제 발생했는지 알려줍니다. 히트 시간은 [보고서 세트의 시간대](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md)를 기반으로 합니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## 차원 항목

이 차원은 항상 `"Weekday"`과 `"Weekend"`, 이렇게 두 개의 차원 항목을 포함합니다. 차원 항목 `"Weekday"`은 월요일부터 금요일까지 모든 히트에 적용되고, 차원 항목 `"Weekend"`은 토요일과 일요일의 모든 히트에 적용됩니다.
