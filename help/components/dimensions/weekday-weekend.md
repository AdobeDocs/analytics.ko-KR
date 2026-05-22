---
title: 평일/주말
description: 히트가 평일과 주말 중 언제 발생했는지를 확인합니다.
feature: Dimensions
exl-id: c3111cdc-a5f9-4244-a725-b1bb1e72fcff
TQID: https://experienceleague.adobe.com/9TJv-49ub1zHsgEGtBeoJVoHhsBktlOr7QhmgLdLRSo
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 105
ht-degree: 80%

---

# 평일/주말

평일/주말&#39; [차원](overview.md)은(는) 히트가 평일(월요일 - 금요일)과 주말(토요일 - 일요일) 중 언제 발생했는지 insight을 제공합니다. 히트 시간은 [보고서 세트의 시간대](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)를 기반으로 합니다.

## 이 차원을 데이터로 채우기

이 차원은 모든 구현에 대해 즉시 작동합니다. 보고서 세트에 데이터가 포함되어 있으면 이 차원이 작동합니다.

## 차원 항목

이 차원은 항상 `"Weekday"`과 `"Weekend"`, 이렇게 두 개의 차원 항목을 포함합니다. 차원 항목 `"Weekday"`은 월요일부터 금요일까지 모든 히트에 적용되고, 차원 항목 `"Weekend"`은 토요일과 일요일의 모든 히트에 적용됩니다.
