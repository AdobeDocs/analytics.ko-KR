---
title: 보트 이름
description: 보트 규칙과 일치하는 보트 이름입니다.
source-git-commit: d7d9bbf9bf43509eb756408f772be870c3854aa5
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 3%

---

# 보트 이름

보트 이름 차원은 다음을 사용하여 감지된 보트 이름을 표시합니다 [보트 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md). 이러한 규칙은 기본 IAB 규칙 또는 조직이 구성하는 사용자 지정 보트 규칙일 수 있습니다. 이 방법은 보트가 사이트를 방문하는 것이나 가장 많은 트래픽을 생성하는 보트가 있는지에 대해 자세히 알고 싶을 때 유용합니다.

일치하는 히트 [!UICONTROL 보트 규칙] 은 이 차원을 제외하고 모든 Analytics 보고에서 자동으로 필터링됩니다. [보트 발생 횟수](../metrics/bot-occurrences.md), 및 [보트 페이지 보기](../metrics/bot-page-views.md). 이 차원 및 이 두 지표를 사용하여 나머지 보고서에서 제외되는 보트 데이터를 확인할 수 있습니다.

보트 보고는 나머지 보고서 세트 데이터와 구분되므로 다음 차원 및 지표만 이 차원에서 지원됩니다.

* [페이지](page.md)
* 시간 기반 차원(예: [일](day.md), [주](week.md), 또는 [월](month.md))
* [보트 발생 횟수](../metrics/bot-occurrences.md)
* [보트 페이지 보기](../metrics/bot-page-views.md)

이 차원과 함께 다른 차원이나 지표를 사용하면 데이터가 반환되지 않습니다.

## 이 차원을 데이터로 채우기

활성화한 경우 [보트 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md)로 지정하는 경우 이 차원은 데이터를 자동으로 수집합니다. 아직 활성화되지 않은 경우 [!UICONTROL 보트 규칙]로 지정하는 경우 이 차원은 Analysis Workspace에 표시되지 않습니다.

## 차원 항목

각 차원 항목에는 IAB 또는 사용자 지정 보트 규칙 기준과 일치하는 보트의 이름이 나열됩니다.
