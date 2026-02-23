---
description: 기존 지표에서 생성할 수 있는 계산된 지표에 대해 알아봅니다.
keywords: 계산된 지표
title: 계산된 지표 개요
feature: Calculated Metrics
exl-id: 9bf8239f-cf74-4feb-85e5-d47805e90afb
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 99%

---

# 계산된 지표 개요

기존 지표에서 생성할 수 있는 계산된 사용자 정의 지표입니다.

계산된 지표는 기존 지표에서 생성할 수 있는 사용자 정의 지표입니다. 계산된 지표에서는 구현을 변경하지 않고도 데이터를 분석할 수 있는 사용자 정의 지표를 작성하고, 관리하고, 조정하는 유연한 방법을 제공합니다.

계산된 지표는 각 [!DNL Analytics] 패키지에서 사용할 수 있지만 Experience Cloud용 Adobe Analytics Foundation Pack은 [포맷 유형(소수점, 시간, 백분율, 통화)](/help/components/calculated-metrics/workflow/c-build-metrics/cm-build-metrics.md), [할당 변경(기본값, 선형, 참여도 등)](/help/components/calculated-metrics/workflow/c-build-metrics/m-metric-type-alloc.md), [지표 유형(표준, 총계)](/help/components/calculated-metrics/workflow/c-build-metrics/m-metric-type-alloc.md) 및 [기본 연산자](workflow/c-build-metrics/cm-build-metrics.md#operators)(더하기, 빼기, 곱하기, 나누기)를 포함한 기본 계산된 지표로 제한됩니다.


자세한 정보는 [Adobe Analytics 제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-analytics.html)을 참조하십시오.

<!--
Here is a comparison of calculated metrics and advanced calculated metrics capabilities: 

| [Format types (decimal, time, percent, currency)](/help/components/calculated-metrics/workflow/c-build-metrics/cm-build-metrics.md)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  |
| [Attribution changes (default, linear, participation, etc.)](/help/components/calculated-metrics/workflow/c-build-metrics/m-metric-type-alloc.md)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  |
| [Metric types (standard, total)](/help/components/calculated-metrics/workflow/c-build-metrics/m-metric-type-alloc.md)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  |
|  Basic operators (add, subtract, multiply, divide)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  |
| [Apply segments](/help/components/calculated-metrics/workflow/c-build-metrics/metrics-with-segments.md)  | ![StopCircle](/help/assets/icons/StopCircle.svg)  | Yes  |
| [Basic functions (count, abs value, mean, etc)](/help/components/calculated-metrics/cm-reference/cm-functions.md)  | No  | Yes  |
| [Advanced functions (regression, if/then, t-score, etc)](/help/components/calculated-metrics/cm-reference/cm-adv-functions.md)  | No  | Yes  |

-->

## 기능 {#section_A0A5C275B68A4D628950BBB0B1EE631F}

다음과 같은 작업을 수행할 수 있습니다.

* [!UICONTROL Analysis Workspace], [!UICONTROL Report Builder], [!UICONTROL 예외 항목 탐지] 및 [!UICONTROL 기여도 분석]에서 [지표를 만들 수 있습니다](/help/components/calculated-metrics/workflow/cm-workflow.md).
* 구현을 변경하지 않고도 보고서 실행 시 파생된 [세그먼트화된 지표를 만들 수 있습니다](/help/components/calculated-metrics/workflow/c-build-metrics/metrics-with-segments.md). 예를 들어 첫 번째 세션에 참여한 사람의 수로, *새 방문자 수*&#x200B;에 대한 지표를 만들 수 있습니다.

* 보고서 세트 간에 [지표를 공유](/help/components/calculated-metrics/workflow/cm-sharing.md)할 수 있습니다. 이것은 새로 만들어진 모든 지표가 동일한 로그인 회사에 있는 모든 보고서 세트에 적용됨을 의미합니다.

* 데이터를 더 잘 설명하는 데 도움이 되도록 [통계 함수를 포함](/help/components/calculated-metrics/cm-reference/cm-adv-functions.md)시킬 수 있습니다. 예를 들어 보고서에 있는 항목의 수를 계산하거나 각 항목에 대한 표준 편차의 수를 추가할 수 있습니다.

## 제한 사항

다음과 같이 일부 [!DNL Analytics] 기능에서는 계산된 지표를 사용할 수 없습니다.

* Analysis Workspace의 폴아웃
* [!UICONTROL Analysis Workspace의 집단 분석]
* [!UICONTROL Data Warehouse]
* [!UICONTROL 세그먼트]
* [!DNL Analytics] for [!DNL Target]


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [계산된 지표](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/components/calculated-metrics/calculated-metrics-implementationless-metrics){target="_blank"}를 확인하십시오.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [세그먼트 내 세그먼트화된 계산된 지표](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/components/calculated-metrics/calculated-metrics-segmented-metrics){target="_blank"}를 확인하십시오.

>[!ENDSHADEBOX]

<!--

Here is a short overview of the [!UICONTROL Calculated metrics] tools: 

|Tool|Capabilities|
|--- |--- |
| [Calculated metric builder](workflow/c-build-metrics/cm-build-metrics.md)| The capabilities are: <ul><li>Create calculated and advanced calculated metrics using advancmd allocation models.</li><li>Add segments inline to metric formulas</li><li>Compare segments in the same report. For example, compare local visitors vs. international visitors.</li><li>Use statistical functions</li><li>Provide detailed metric descriptions (show what it does, where to use it, where NOT to use it)</li><li>Copy definitions into new metrics</li><li>Provide an inline metric preview</li><li>Set metric polarity, which indicates whether it's good or bad if a given custom event (metric) goes up</li><li>Tag metrics</li></ul>|
|Calculated Metric Manager|<ul><li>Share metrics with others</li<li>Approve and curate metrics</li><li>Organize (tag) your metrics so people can find them</li><li>Delete metrics</li><li>Rename metrics</li></ul>|
|Metric Selector rail|Lets you search for and add/apply metrics to the report. You can also change the  sort order (options are: alphabetical, recommended, frequently used, recently used.) In addition, you can filter on Report Suites to show only metrics created in a specific report suite.  To access this Metric Selector, click the Metrics icon  to the left of a report. |
|API for Calculated Metrics|Part of the Adobe Analytics 2.0 API set.|

-->

>[!MORELIKETHIS]
>
>[지표 만들기](/help/components/calculated-metrics/workflow/cm-workflow.md)
>[지표 빌드](/help/components/calculated-metrics/workflow/c-build-metrics/cm-build-metrics.md)
>[함수 사용](/help/components/calculated-metrics/workflow/c-build-metrics/cm-using-functions.md)
>
