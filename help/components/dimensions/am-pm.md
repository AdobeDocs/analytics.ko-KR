---
title: 오전/오후
description: 히트가 오전과 오후 중 언제 발생했는지를 확인합니다.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 70%

---


# 오전/오후

오전/오후 차원은 히트가 오전과 오후 중 언제 발생했는지 알려줍니다. 히트 시간은 [보고서 세트의 시간대](/help/admin/admin/general-acct-settings-admin.md)를 기반으로 합니다.

## 이 차원을 데이터로 채우기

이 차원은 즉시 작동합니다. 변경할 설정이 없으며 유일한 종속성은 어느 시간이 오전이고 어느 시간이 오후인지 결정하는 보고서 세트의 시간대입니다.

## Dimension 항목

This dimension always contains exactly two dimension items: `"AM"` and `"PM"`. The dimension item `"AM"` applies to all hits from 12:00 AM to 11:59 AM, while the dimension item `"PM"` applies to all hits from 12:00 PM to 11:59 PM.
