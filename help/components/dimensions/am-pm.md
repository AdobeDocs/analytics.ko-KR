---
title: 오전/오후
description: 히트가 오전과 오후 중 언제 발생했는지를 확인합니다.
feature: Dimensions
exl-id: 93fcdb9f-2ba3-402c-a389-b02ed8c990d2
TQID: https://experienceleague.adobe.com/R1syrJ7ylIe2ywH1isX4sjR2O84-8eL-jooYhjUdKhI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 64%

---

# 오전/오후

오전/오후 [차원](overview.md)은(는) 히트가 오전 또는 오후 시간 동안 발생했는지 여부에 대한 insight을 제공합니다. 히트 시간은 [보고서 세트의 시간대](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)를 기반으로 합니다.

## 이 차원을 데이터로 채우기

이 차원은 즉시 작동합니다. 변경할 설정이 없으며 유일한 종속성은 어느 시간이 오전이고 어느 시간이 오후인지 결정하는 보고서 세트의 시간대입니다.

## 차원 항목

이 차원은 항상 `"AM"`과 `"PM"`, 이렇게 두 개의 차원 항목을 포함합니다. 차원 항목 `"AM"`은(는) 오전 12:00부터 오전 11:59까지의 모든 히트에 적용되는 반면, 차원 항목 `"PM"`은(는) 오후 12:00부터 오후 11:59까지의 모든 히트에 적용됩니다.
