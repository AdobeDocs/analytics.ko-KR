---
description: 계산된 지표 및 고급 계산된 지표는 기존의 지표에서 만들 수 있는 사용자 정의 지표입니다.
keywords: 계산된 지표;고급 계산된 지표
title: 계산된 지표 및 고급 계산된 지표
feature: Calculated Metrics
exl-id: 9bf8239f-cf74-4feb-85e5-d47805e90afb
source-git-commit: 9714863374052e257e1d6349c442fc74182a0a2f
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 100%

---

# 계산된 지표 및 고급 계산된 지표

계산된 지표 및 고급 계산된 지표는 기존의 지표에서 만들 수 있는 사용자 정의 지표입니다.

Adobe의 계산된 지표 도구에서는 지표를 작성하고, 관리하고, 조정하는 유연한 방법을 제공합니다. 이 도구를 사용하는 마케터, 제품 관리자 및 분석가는 [!DNL Analytics] 구현을 변경하지 않아도 데이터에 대해 질문할 수 있습니다. 각 [!DNL Analytics] 패키지에서 사용할 수 있는 사용자 정의 지표는 다음과 같습니다.

* Adobe [!DNL Analytics] Foundation: 계산된 지표
* [Adobe Analytics Select](https://www.adobe.com/kr/data-analytics-cloud/analytics/select.html): 계산된 + 고급 계산된 지표
* [Adobe Analytics Prime](https://www.adobe.com/kr/data-analytics-cloud/analytics/prime.html): 계산된 + 고급 계산된 지표
* [Adobe Analytics Ultimate](https://www.adobe.com/kr/data-analytics-cloud/analytics/ultimate.html): 계산된 + 고급 계산된 지표

다음은 계산된 지표와 고급 계산된 지표 기능을 비교한 것입니다.

| Builder 옵션 | 계산된 지표 | 고급 계산된 지표 |
|---|---|---|
| [형식 유형 (십진수, 시간, 퍼센트, 통화)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) | 예 | 예 |
| [기여도 분석 변경 (기본값, 선형, 기여도 등)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | 예 | 예 |
| [지표 유형 (표준, 전체)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | 예 | 예 |
| 기본 연산자 (더하기, 빼기, 곱하기, 나누기) | 예 | 예 |
| [세그먼트 적용](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md) | 아니요 | 예 |
| [기본 함수 (수, 절대값, 평균 등)](/help/components/c-calcmetrics/cm-reference/cm-functions.md) | 아니요 | 예 |
| [고급 함수 (회귀, if/then, T 스코어 등)](/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md) | 아니요 | 예 |

## 기능 {#section_A0A5C275B68A4D628950BBB0B1EE631F}

다음과 같은 작업을 수행할 수 있습니다.

* [!UICONTROL Analysis Workspace], [!UICONTROL Report Builder], [!UICONTROL 예외 항목 탐지] 및 [!UICONTROL 기여도 분석]에서 지표를 만들 수 있습니다.
* 구현을 변경하지 않고도 보고서 실행 시 파생된 세그먼트화된 지표를 만들 수 있습니다. 이러한 지표는 세그먼트를 기반으로 하므로 기록에서 볼 수 있습니다.

>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [계산된 지표](https://video.tv.adobe.com/v/25407?quality=12&learn=on){target="_blank"}를 확인하십시오.

>[!ENDSHADEBOX]

* 보고서 세트 간에 지표를 공유할 수 있습니다. 이것은 새로 만들어진 모든 지표가 동일한 로그인 회사에 있는 모든 보고서 세트에 적용됨을 의미합니다.
* (고급 계산된 지표만 해당) 지표의 세그먼트. 예를 들어 첫 번째 세션에 참여한 사람의 수로, “새 방문자 수”에 대한 지표를 만들 수 있습니다.

* (고급 계산된 지표만 해당) 통계 함수를 통합하여 데이터를 더욱 효율적으로 설명할 수 있습니다. 예를 들어 보고서에 있는 항목의 수를 계산하거나 각 항목에 대한 표준 편차의 수를 추가할 수 있습니다.


## 제한 사항

일부 [!DNL Analytics] 기능은 이벤트를 사용할 수 있지만 계산된 지표는 사용할 수 없습니다.

* Analysis Workspace의 폴아웃
* [!UICONTROL Analysis Workspace의 집단 분석]
* [!UICONTROL Data Warehouse]
* [!UICONTROL 세그먼트]
* [!DNL Analytics] for [!DNL Target]


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [계산된 지표](https://video.tv.adobe.com/v/25407?quality=12&learn=on){target="_blank"}를 확인하십시오.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [세그먼트 내 세그먼트화된 계산된 지표](https://video.tv.adobe.com/v/25409?quality=12&learn=on){target="_blank"}를 확인하십시오.

>[!ENDSHADEBOX]

<!--

Here is a short overview of the [!UICONTROL Calculated metrics] tools: 

|Tool|Capabilities|
|--- |--- |
| [Calculated metric builder](c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md)| The capabilities are: <ul><li>Create calculated and advanced calculated metrics using advancmd allocation models.</li><li>Add segments inline to metric formulas</li><li>Compare segments in the same report. For example, compare local visitors vs. international visitors.</li><li>Use statistical functions</li><li>Provide detailed metric descriptions (show what it does, where to use it, where NOT to use it)</li><li>Copy definitions into new metrics</li><li>Provide an inline metric preview</li><li>Set metric polarity, which indicates whether it's good or bad if a given custom event (metric) goes up</li><li>Tag metrics</li></ul>|
|Calculated Metric Manager|<ul><li>Share metrics with others</li<li>Approve and curate metrics</li><li>Organize (tag) your metrics so people can find them</li><li>Delete metrics</li><li>Rename metrics</li></ul>|
|Metric Selector rail|Lets you search for and add/apply metrics to the report. You can also change the  sort order (options are: alphabetical, recommended, frequently used, recently used.) In addition, you can filter on Report Suites to show only metrics created in a specific report suite.  To access this Metric Selector, click the Metrics icon  to the left of a report. |
|API for Calculated Metrics|Part of the Adobe Analytics 2.0 API set.|

-->