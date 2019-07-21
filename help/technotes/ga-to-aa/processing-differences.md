---
title: 분석 플랫폼 간의 처리 및 아키텍처 차이점
description: Adobe Analytics 및 Google Analytics와 같은 플랫폼 간에 다른 데이터가 수집 및 표시되는 방식을 알아봅니다.
translation-type: tm+mt
source-git-commit: a5f612ba5e8446a56bc2bd252a8781e8ab1de403

---


# 분석 플랫폼 간의 처리 및 아키텍처 차이점

Adobe Analytics와 Google Analytics는 모두 분석 도구이지만 플랫폼 간에 데이터를 수집 및 처리하는 방식은 매우 다릅니다. 이 페이지에서는 특정 차원 및 지표가 수집되는 방식과 유사한 보고서에서 다른 수치를 표시하는 이유에 대한 주요 차이점을 이해할 수 있습니다.

## 바운스 비율

바운스 비율은 대부분의 Analytics 도구에서 랜딩 페이지의 효과 및 연관성을 측정하는 데 사용되는 일반적인 KPI 입니다. 이것은 일반적으로 웹 사이트를 시작하지만 다른 페이지에 클릭을 포함하지 않는 방문으로 정의됩니다.

* In Adobe Analytics, Bounce Rate is calculated using the formula **Bounces divided by Entries**.
* In Google Analytics, Bounce Rate is calculated using the formula **Single-page sessions divided by Sessions**.

두 플랫폼 모두에서 같은 방문 또는 세션에서 여러 히트가 전송되는 경우 바운스로 간주되지 않습니다. Adobe Analytics 에서는 사용자 지정 링크를 사용할 수 있고 매우 일반적이어서 방문이 바운스로 카운트되지 않습니다. Google Analytics는 일반적으로 동일한 페이지에서 두 개 이상의 데이터 요청을 전송하지 않습니다.

보고 도구 간에 더 나은 패리티를 얻으려면, 계산된 지표의 일부로서 바운스 대신 Adobe Analytics의 단일 페이지 방문 횟수 지표를 사용하십시오. 단일 페이지 방문 횟수 지표에는 한 페이지 보기만 포함된 총 방문 횟수 또는 다른 페이지에 대한 클릭 수를 포함하지 않는 방문 횟수가 포함됩니다.

See the [Bounce Rate](../../components/c-variables/c-metrics/metrics-bounce-rate.md) metric in the Components user guide for more information.

## 방문 및 세션

방문 (Google Analytics의 세션으로 알려져 있음) 는 짧은 시간에 동일한 사용자가 만든 페이지 보기 그룹입니다. 두 플랫폼의 방문은 일반적으로 비활동 상태로 30 분 후에 만료됩니다. 두 플랫폼 모두 방문이 만료되는 시기를 사용자 정의할 수 있습니다. 각 플랫폼에서 차이가 발생할 수 있는 여러 가지 시나리오가 있습니다.

* **하루 중 종료:** Google Analytics의 모든 세션은 지정된 날짜에 오후 11 시 59 분 이후에 만료됩니다. 사용자가 오전 12 시 이후에도 사이트에서 계속 활성 상태인 경우 새 세션이 만들어집니다. Adobe Analytics는 동일한 방문의 일부로 다음 날 방문 횟수를 계속합니다.
* **다양한 캠페인:** Google Analytics의 새 세션은 사용자의 캠페인 소스가 변경되면 시작됩니다. Adobe Analytics에 새로운 추적 코드 값이 표시되는 경우 동일한 방문의 일부로 간주됩니다.
* **수동 세션 재정의:** 세션을 수동으로 시작하거나 종료할 `sessionControl` 때 Google Analytics의 새 세션이 시작됩니다. Adobe Analytics에서 방문을 수동으로 종료할 수 없습니다.
* **Adobe Analytics의 이상값 방문 감지:** 사용자가 12 시간 동안 연속 활동, 2500 개의 히트 또는 100 초 내에 100 개의 히트까지 도달할 경우 Adobe Analytics의 새로운 방문이 자동으로 시작됩니다. 이러한 탐지 기준은 일반적으로 보트 활동에 의해 트리거됩니다.

See the [Visits](../../components/c-variables/c-metrics/metrics-visit.md) metric in the Components user guide for more information.
