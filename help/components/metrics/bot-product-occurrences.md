---
title: 봇 제품 발생 횟수
description: 보트 제품 발생 횟수 지표는 보트 규칙과 일치하고 Analytics 보고에서 제외된 제품 문자열 하위 히트 수를 보여줍니다.
feature: Metrics
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 3ba8d2cce29a1965c85789c3fd0543c23533e3a8
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 5%
---
# 봇 제품 발생 횟수

&#39;봇 제품 발생 횟수&#39; [지표](overview.md)은(는) [봇 규칙](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md)과(와) 일치하는 하위 히트의 수를 표시합니다.

보트 보고는 보고서 세트의 나머지 데이터와 분리되므로 이 지표는 다음 차원에서만 작동합니다.

* [봇 이름](../dimensions/bot-name.md)
* [제품](../dimensions/product.md)
* 시간 기반 차원(예: [일](../dimensions/day.md), [주](../dimensions/week.md) 또는 [월](../dimensions/month.md))

이 지표와 함께 다른 차원을 사용하면 데이터가 반환되지 않습니다.

## 이 지표의 계산 방법

Adobe은 [제품 문자열](/help/implement/vars/page-vars/products.md)이 포함된 모든 하위 히트를 확인하여 조직에서 구성한 보트 규칙과 일치하는지 확인합니다. 주어진 하위 히트가 보트 규칙과 일치하는 경우 하위 히트는 보고에서 제외되며 이 지표는 하나씩 증가합니다.
