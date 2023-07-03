---
title: 보트 페이지 보기 수
description: 보트 규칙과 일치하는 페이지 보기 수입니다.
feature: Metrics
exl-id: 9b1efcb1-10ca-40fb-8f20-e6da105366d9
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---

# 보트 페이지 보기 수

보트 페이지 보기 수 지표는 일치하는 페이지 히트의 수를 보여줍니다 [보트 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md).

보트 보고는 보고서 세트의 나머지 데이터와 분리되므로 이 지표는 다음 차원에서만 작동합니다.

* [보트 이름](../dimensions/bot-name.md)
* [페이지](../dimensions/page.md)
* 시간 기반 차원 (예: [일](../dimensions/day.md), [주](../dimensions/week.md), 또는 [월](../dimensions/month.md))

이 지표와 함께 다른 차원을 사용하면 데이터가 반환되지 않습니다.

## 이 지표의 계산 방법

Adobe은 모든 페이지 히트를 확인하여 조직이 구성한 보트 규칙과 일치하는지 확인합니다. 주어진 히트가 보트 규칙과 일치하는 경우 페이지 히트는 보고에서 제외되며 이 지표는 1만큼 증가합니다. 이 지표에는 링크 추적 히트( )가 포함되지 않습니다.[`tl()`](/help/implement/vars/functions/tl-method.md)).
