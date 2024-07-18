---
title: Analytics 플랫폼 간 처리 및 아키텍처 차이점
description: 일부 데이터가 수집되고 표시되는 방식이 Adobe Analytics 및 Google Analytics와 같은 플랫폼에 따라 어떻게 다른지 알아보십시오.
feature: Third-party Integration
exl-id: 3e457915-3c2d-49f7-9b77-df18c04d49cd
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 100%

---

# Analytics 플랫폼 간 처리 및 아키텍처 차이점

Adobe Analytics와 Google Analytics는 모두 Analytics 도구이지만 플랫폼마다 데이터를 수집하고 처리하는 방법은 전혀 다릅니다. 이 페이지에서는 특정 차원 및 지표를 수집하는 방식의 몇 가지 주요 차이점과 유사한 보고서에 숫자가 다르게 표시되는 이유를 알아봅니다.

## [!UICONTROL 바운스 비율]

[!UICONTROL 바운스 비율은 대부분의 분석 도구에서 랜딩 페이지의 효율성과 관련성을 측정하기 위해 사용하는 일반적인 KPI입니다. ] 일반적으로 웹 사이트로 들어오지만 다른 페이지를 클릭하지 않은 방문 횟수로 정의됩니다.

* Adobe Analytics에서 [!UICONTROL 바운스 비율]은 **진입 횟수로 나눈 바운스 수** 공식을 사용하여 계산됩니다.
* Google Analytics에서 [!UICONTROL 바운스 비율]은 **세션 수로 나눈 단일 페이지 세션 수** 공식을 사용하여 계산됩니다.

두 플랫폼 모두, 동일한 방문이나 세션에서 여러 개의 히트를 전송하는 경우에는 바운스로 간주되지 않습니다. Adobe Analytics에서 사용자 지정 링크를 사용할 수 있으며 일반적으로 많이 사용하는데, 한 번의 방문이 한 번의 바운스로 카운트되지 않게 하는 역할을 합니다. Google Analytics는 일반적으로 동일한 페이지에서 두 개 이상의 데이터 요청을 전송하지 않습니다.

보고 도구 간의 패리티를 향상하기 위해 Adobe Analytics의 [!UICONTROL 단일 페이지 방문 횟수] 지표를 [!UICONTROL 바운스 수] 대신 계산된 지표의 일부로 사용합니다. [!UICONTROL  단일 페이지 방문 횟수] 지표에는 한 페이지 보기만 포함된 총 방문 횟수 또는 웹 사이트에 들어왔지만 다른 페이지를 클릭하지 않은 방문 횟수가 포함됩니다.

자세한 내용은 구성 요소 사용 안내서의 [바운스 비율](/help/components/metrics/bounce-rate.md) 지표를 참조하십시오.

## [!UICONTROL 방문 횟수 및 세션]

[!UICONTROL 방문 횟수] (Google Analytics에서는 세션이라고 함)는 짧은 시간에 동일한 사용자가 만든 페이지 보기 수 그룹입니다. [!UICONTROL 두 플랫폼의 방문 횟수는 일반적으로 비활성 상태가 30분간 지속되면 만료됩니다. ] 두 플랫폼 모두 [!UICONTROL 방문]이 만료되면 사용자 지정이 가능합니다. 각 플랫폼에서 차이가 발생할 수 있는 여러 가지 시나리오가 있습니다.

* **하루의 끝:** Google Analytics의 모든 세션은 그날 오후 11시 59분 이후에 만료됩니다. 사용자가 오전 12시 이후에도 여전히 사이트에서 활성 상태인 경우 새 세션이 만들어집니다. Adobe Analytics는 그다음 날의 방문을 동일한 방문의 일부로 간주합니다.
* **다른 캠페인:** 사용자의 캠페인 소스가 변경되면 Google Analytics에서 새 세션이 시작됩니다. 새 [!UICONTROL 추적 코드] 값이 Adobe Analytics에 표시되면 동일한 방문의 일부로 간주됩니다.
* **수동 세션 재정의:** `sessionControl`을 사용하여 세션을 수동으로 시작하거나 종료하는 경우 Google Analytics에 새 세션이 시작됩니다. [!UICONTROL Adobe Analytics에서는 방문을 수동으로 종료할 수 없습니다.]
* **Adobe Analytics의 이상치 방문 감지:** 사용자가 12시간 동안 지속적으로 활동하거나, 2500개 히트 또는 100초 이내에 100개 히트 수에 도달하면 Adobe Analytics에서 새 [!UICONTROL 방문]이 자동으로 시작됩니다. 이러한 각 탐지 기준은 일반적으로 보트 활동에 의해 트리거됩니다.

자세한 내용은 구성 요소 사용 안내서의 [방문 횟수](/help/components/metrics/visits.md) 지표를 참조하십시오.
