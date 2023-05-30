---
title: 보트 이름
description: 보트 규칙과 일치하는 보트의 이름입니다.
exl-id: 668c1dce-c603-477a-9df7-dacb649bbf63
source-git-commit: 5ba12c243a8013c52b487d048c54461ebdf7bd85
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 3%

---

# 보트 이름

보트 이름 차원은 다음을 사용하여 감지된 보트의 이름을 보여줍니다. [보트 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md). 이러한 규칙은 기본 IAB 규칙 또는 조직에서 구성하는 사용자 지정 보트 규칙일 수 있습니다. 이 메서드는 사이트를 방문하는 보트나 가장 많은 트래픽을 발생시키는 봇에 대해 자세히 알아보고자 하는 경우에 유용합니다.

일치하는 히트 수 [!UICONTROL 보트 규칙] 이 차원을 제외하고 모든 Analytics 보고에서 자동으로 필터링됩니다. [봇 발생 횟수](../metrics/bot-occurrences.md), 및 [보트 페이지 보기 수](../metrics/bot-page-views.md). 이 차원과 이 두 지표를 사용하여 나머지 보고서에서 제외되는 보트 데이터를 확인할 수 있습니다.

보트 보고는 보고서 세트의 나머지 데이터와 분리되어 있으므로 이 차원에서는 다음 차원 및 지표만 지원됩니다.

* [페이지](page.md)
* 시간 기반 차원 (예: [일](day.md), [주](week.md), 또는 [월](month.md))
* [봇 발생 횟수](../metrics/bot-occurrences.md)
* [보트 페이지 보기 수](../metrics/bot-page-views.md)

이 차원과 함께 다른 차원 또는 지표를 사용하면 데이터가 반환되지 않습니다.

## 이 차원을 데이터로 채우기

활성화한 경우 [보트 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md), 이 차원은 자동으로 데이터를 수집합니다. 아직 활성화하지 않은 경우 [!UICONTROL 보트 규칙], 이 차원은 Analysis Workspace에 표시되지 않습니다.

## 차원 항목

각 차원 항목에는 IAB 또는 사용자 지정 보트 규칙 기준과 일치하는 보트의 이름이 나열됩니다.
