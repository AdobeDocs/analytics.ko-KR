---
title: 오전/오후
description: 히트가 오전과 오후 중 언제 발생했는지를 확인합니다.
translation-type: ht
source-git-commit: cd2225ec00190af6b616f313b419935c4f8dfafd
workflow-type: ht
source-wordcount: '117'
ht-degree: 100%

---


# 오전/오후

오전/오후 차원은 히트가 오전과 오후 중 언제 발생했는지 알려줍니다. 히트 시간은 [보고서 세트의 시간대](/help/admin/admin/general-acct-settings-admin.md)를 기반으로 합니다.

## 이 차원을 데이터로 채우기

이 차원은 즉시 작동합니다. 변경할 설정이 없으며 유일한 종속성은 어느 시간이 오전이고 어느 시간이 오후인지 결정하는 보고서 세트의 시간대입니다.

## 차원 항목

이 차원은 항상 `"AM"`과 `"PM"`, 이렇게 두 개의 차원 항목을 포함합니다. 차원 항목 `"AM"`은 오전 12:00부터 오전 11:59까지의 모든 히트에 적용되는 반면, 차원 항목 `"PM"`는 오후 12:00부터 오후 11:59까지의 모든 히트에 적용됩니다.
