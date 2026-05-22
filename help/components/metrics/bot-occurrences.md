---
title: 봇 발생 횟수
description: 보트 규칙과 일치하는 히트의 수입니다.
feature: Metrics
exl-id: 94cbbee4-8455-48b1-b804-534ed8fccdc9
TQID: https://experienceleague.adobe.com/LH7eQC-Z6Y3nku1QzI9Yn0N3MRwGA--5R-93lfadT1c
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 9%

---

# 봇 발생 횟수

&#39;보트 발생 횟수&#39; [지표](overview.md)은(는) [보트 규칙](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md)과(와) 일치하는 히트의 수를 보여줍니다.

보트 보고는 보고서 세트의 나머지 데이터와 분리되므로 이 지표는 다음 차원에서만 작동합니다.

* [봇 이름](../dimensions/bot-name.md)
* [페이지](../dimensions/page.md)
* 시간 기반 차원(예: [일](../dimensions/day.md), [주](../dimensions/week.md) 또는 [월](../dimensions/month.md))

이 지표와 함께 다른 차원을 사용하면 데이터가 반환되지 않습니다.

## 이 지표의 계산 방법

Adobe은 모든 히트를 검사하여 조직이 구성한 보트 규칙과 일치하는지 확인합니다. 주어진 히트가 보트 규칙과 일치하는 경우 히트는 보고에서 제외되며 이 지표는 1만큼 증가합니다. 이 지표에는 페이지 보기 수([`t()`](/help/implement/vars/functions/t-method.md))와 링크 추적 히트 수([`tl()`](/help/implement/vars/functions/tl-method.md))가 모두 포함되지만, [보트 페이지 보기 수](bot-page-views.md)에는 링크 추적 히트가 포함되지 않습니다.
