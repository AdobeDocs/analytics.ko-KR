---
title: Analytics 플랫폼 간 처리 및 아키텍처 차이점
description: 일부 데이터가 수집되고 표시되는 방식이 Adobe Analytics 및 Google Analytics와 같은 플랫폼에 따라 어떻게 다른지 알아보십시오.
translation-type: tm+mt
source-git-commit: 3211598c2ff43493b329a9be4fb6877ae29cf08b
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 66%

---


# Analytics 플랫폼 간 처리 및 아키텍처 차이점

Adobe Analytics와 Google Analytics는 모두 Analytics 도구이지만 플랫폼마다 데이터를 수집하고 처리하는 방법은 전혀 다릅니다. 이 페이지에서는 특정 차원 및 지표를 수집하는 방식의 몇 가지 주요 차이점과 유사한 보고서에 숫자가 다르게 표시되는 이유를 알아봅니다.

## [!UICONTROL 바운스 비율]

[!UICONTROL 바운스 비율은 대부분의 분석 도구에서 랜딩 페이지의 효율성과 관련성을 측정하기 위해 사용하는 일반적인 KPI입니다. ] 일반적으로 웹 사이트로 들어오지만 다른 페이지를 클릭하지 않은 방문 횟수로 정의됩니다.

* In Adobe Analytics, [!UICONTROL Bounce Rate] is calculated using the formula **Bounces divided by Entries**.
* In Google Analytics, [!UICONTROL Bounce Rate] is calculated using the formula **Single-page sessions divided by Sessions**.

두 플랫폼 모두, 동일한 방문이나 세션에서 여러 개의 히트를 전송하는 경우에는 바운스로 간주되지 않습니다. Adobe Analytics에서 사용자 지정 링크를 사용할 수 있으며 일반적으로 많이 사용하는데, 한 번의 방문이 한 번의 바운스로 카운트되지 않게 하는 역할을 합니다. Google Analytics는 일반적으로 동일한 페이지에서 두 개 이상의 데이터 요청을 전송하지 않습니다.

To achieve better parity between reporting tools, use the [!UICONTROL Single Page Visits] metric in Adobe Analytics instead of [!UICONTROL Bounces] as part of a calculated metric. The [!UICONTROL Single Page Visits] metric includes the total number of visits that only included one-page view, or visits that enter the website but do not include a click to another page.

자세한 내용은 구성 요소 사용 안내서의 [바운스 비율](/help/components/c-variables/c-metrics/metrics-bounce-rate.md) 지표를 참조하십시오.

## [!UICONTROL 방문 횟수 및 세션]

[!UICONTROL 방문] (Google Analytics의 세션으로 알려져 있음)은 짧은 시간 내에 동일한 사용자가 만든 페이지 보기 그룹입니다. [!UICONTROL 두 플랫폼의 방문 횟수는 일반적으로 비활성 상태가 30분간 지속되면 만료됩니다. ] Both platforms allow customization on when a [!UICONTROL Visit] expires. 각 플랫폼에서 차이가 발생할 수 있는 여러 가지 시나리오가 있습니다.

* **하루의 끝:** Google Analytics의 모든 세션은 그날 오후 11시 59분 이후에 만료됩니다. 사용자가 오전 12시 이후에도 여전히 사이트에서 활성 상태인 경우 새 세션이 만들어집니다. Adobe Analytics는 그다음 날의 방문을 동일한 방문의 일부로 간주합니다.
* **다른 캠페인:** 사용자의 캠페인 소스가 변경되면 Google Analytics에서 새 세션이 시작됩니다. If a new [!UICONTROL Tracking Code] value is seen in Adobe Analytics, it is considered part of the same visit.
* **수동 세션 재정의:** `sessionControl`을 사용하여 세션을 수동으로 시작하거나 종료하는 경우 Google Analytics에 새 세션이 시작됩니다. [!UICONTROL Adobe Analytics에서는 방문을 수동으로 종료할 수 없습니다.]
* **Adobe Analytics의 이상치 방문 감지:** Adobe Analytics의 새로운 [!UICONTROL 방문] 기능은 사용자가 12시간 연속 활동, 2500회 히트 또는 100초 내에 히트 수가 도달하면 자동으로 시작됩니다. 이러한 각 탐지 기준은 일반적으로 보트 활동에 의해 트리거됩니다.

자세한 내용은 구성 요소 사용 안내서의 [방문 횟수](/help/components/c-variables/c-metrics/metrics-visit.md) 지표를 참조하십시오.
