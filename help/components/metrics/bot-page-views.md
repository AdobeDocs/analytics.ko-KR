---
title: 봇 페이지 조회수
description: 보트 규칙과 일치하는 페이지 보기 수입니다.
feature: Metrics
exl-id: d6699880-3faa-4df9-ad49-c7998f6ce45b
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 11%

---

# 봇 페이지 조회수

&#39;보트 페이지 보기 수&#39; [지표](overview.md)은(는) [보트 규칙](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md)과(와) 일치하는 페이지 히트 수를 보여줍니다.

보트 보고는 보고서 세트의 나머지 데이터와 분리되므로 이 지표는 다음 차원에서만 작동합니다.

* [봇 이름](../dimensions/bot-name.md)
* [페이지](../dimensions/page.md)
* 시간 기반 차원(예: [일](../dimensions/day.md), [주](../dimensions/week.md) 또는 [월](../dimensions/month.md))

이 지표와 함께 다른 차원을 사용하면 데이터가 반환되지 않습니다.

## 이 지표의 계산 방법

Adobe은 모든 페이지 조회수를 확인하여 조직이 구성한 보트 규칙과 일치하는지 확인합니다. 주어진 히트가 보트 규칙과 일치하는 경우 페이지 히트는 보고에서 제외되며 이 지표는 1만큼 증가합니다. 이 지표에는 링크 추적 히트([`tl()`](/help/implement/vars/functions/tl-method.md))가 포함되지 않습니다.
