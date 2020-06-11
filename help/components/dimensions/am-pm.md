---
title: 오전/오후
description: 오전 또는 오후 시간 동안 히트가 발생했는지 여부를 결정합니다.
translation-type: tm+mt
source-git-commit: 05ea2778cd5cd324c660fd0f1d2ac02373829f0f
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---


# 오전/오후

&#39;AM/PM&#39; 차원은 AM 또는 PM 시간 동안 히트가 발생했는지 여부를 알려줍니다. The time of the hit is based on the [report suite&#39;s time zone](/help/admin/admin/general-acct-settings-admin.md).

## 데이터로 이 차원 채우기

이 치수는 완전히 정상이다. 변경할 설정이 없습니다. 유일한 종속성은 보고서 세트의 시간대입니다. 이 시간대에서는 오전 시간이고 PM을 결정합니다.

## 차원 값

이 차원은 항상 두 개의 차원 값을 포함합니다. `"AM"` 및 `"PM"`. 차원 값 `"AM"` 은 오전 12:00부터 오전 11:59까지 모든 히트에 적용되는 반면, 차원 값은 오후 12:00부터 오후 11:59까지 모든 히트에 `"PM"` 적용됩니다.
