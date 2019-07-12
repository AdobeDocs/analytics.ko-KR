---
title: Adobe Analytics의 대상 보고서
description: 분석 작업 공간에서 고객 기반 보고서를 만드는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: 71899840dd5b401c6892b6ad5088d4a32fd07042

---


# 대상 보고서

대상자 보고서는 사이트를 방문하는 사람의 유형에 대한 정보를 보여줍니다.

이 페이지에서는 사용자가 분석 작업 공간 사용에 대한 기본적인 지식을 가지고 있다고 가정합니다. See [Create a basic report in Analysis Workspace for Google Analytics users](create-report.md) if you are not yet familiar with the tool in Adobe Analytics.

## 활성 사용자

활성 사용자는 이전 1, 7, 14 또는 28 일 동안 사이트에 누적 사용자 수를 표시합니다. Adobe에 Google Analytics에서 사용된 정확한 계산이 없지만, 지표 고유 방문자를 사용하여 선택한 날짜 범위를 기반으로 사이트에 대한 중복 제거된 사용자 수를 볼 수 있습니다.

고유 방문자의 라인 그래프를 획득하려면:

1. 왼쪽에 있는 시각화 아이콘을 클릭하고 선 시각화를 빈 자유 형식 테이블 위의 작업 영역으로 드래그합니다.
2. Click the Components icon on the left, then drag the **Unique Visitors** metric into the smaller space labeled &#39;Drop a Metric here&#39;.
3. If different granularity is desired, drag the desired date range (e.g. **Day**, **Week**, **Month**, etc.) 기존 날짜 차원 헤더 상단에서

See [Unique Visitors](../../../components/c-variables/c-metrics/metrics-unique-visitors.md) in the Components user guide for details on how Adobe calculates unique visitors.

## 라이프타임 값

라이프타임 값은 두 플랫폼에서 추가적으로 특수 구현이 필요한 기능입니다. 이 데이터를 얻으려면 구현 컨설턴트와 협력하는 것이 좋습니다.

## 집단 분석

집단 분석은 동일한 사용자가 사이트로 돌아오는 빈도를 보여줍니다.

집단 테이블을 만들려면:

1. 왼쪽에 있는 시각화 아이콘을 클릭하고 집단 테이블 시각화를 작업 영역으로 드래그합니다.
2. Click the Components icon on the left, then drag the **Visits** metric onto both the Inclusion Criteria and Return Criteria.
3. 작성을 클릭합니다.

See [Cohort Analysis](../../../analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) in the Analysis Workspace user guide for details on additional customizations to the cohort visualization.

## 대상자

Google Analytics의 대상자 보고서에는 대상 설정이 필요합니다. 또한 Adobe Audience Manager를 통해 Adobe의 구성을 구성해야 합니다. 자세한 내용은 Adobe Audience Manager 사용자 안내서를 참조하십시오.

## 사용자 탐색기

애널리스트는 사용자 탐색기 보고서를 사용하여 익명 식별자를 통해 개별 방문을 볼 수 있습니다. Adobe는 데이터의 히트 수준 원시 내보내기 인 데이터 피드 외부의 백엔드 식별자를 처리하지 않습니다.

* 분석 작업 공간에서 이 데이터를 원하는 경우 구현 컨설턴트와 협력하여 익명화된 고유 식별자 쿠키 값을 Evar에 전달할 수 있습니다. 이것은 월간 고유 방문자 1 백만 명 미만으로 구성된 소규모 구현에서만 작동합니다.
* If this data is desired within data feeds, the concatenated columns `visid_high` and `visid_low` are the most common way to identify unique visitors. Learn more about [Data Feeds](../../../export/analytics-data-feed/c-getstarted/data-feed-overview.md) in the Export user guide.

## 인구 통계 및 관심 보고서

인구 통계학적 및 관심사 데이터는 사이트 사용자의 연령, 성별 및 관심사에 대한 정보를 제공합니다. 이 데이터는 사이트 간 추적 기능을 통해 Google에 의해 수집됩니다.

인구 통계 및 관심 데이터는 Adobe에 의해 자동으로 수집되지 않습니다. 그러나 조직에서 이 데이터를 얻는 경우 Adobe Experience Cloud 플랫폼 내의 기능인 고객 속성을 사용할 수 있습니다. 속성별로 데이터의 구성을 완벽하게 제어할 수 있으며 인구 통계나 관심에만 국한되지 않습니다.

자세한 내용은 고객 속성 도움말을 참조하십시오.

## 지역 - 언어

지역 언어 보고서는 방문자의 브라우저에서 언어 설정에 따른 사이트 트래픽을 보여줍니다.

언어 보고서를 만들려면:

1. In the Components menu, locate the **Language** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Language](../../../components/c-variables/dimensionslist/reports-languages.md) dimension in the Components user guide for more information.

## 지역 - 위치

지리적 위치 보고서는 국가별 데이터를 분리하여 전세계 지도 보기를 제공합니다.

지리적 위치 보고서를 만들려면:

1. 왼쪽에 있는 시각화 아이콘을 클릭하고 맵 시각화를 빈 자유 형식 테이블 위의 작업 영역으로 드래그합니다.
2. Click the Components icon on the left, then drag the **Unique Visitors** metric into the space labeled &#39;Add Metric&#39;.
3. 작성을 클릭합니다.

지도 외에 표를 원하는 경우:

1. In the Components menu, locate the **Countries** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See [Geosegmentation](../../../components/c-variables/dimensionslist/reports-geosegmentation.md) dimensions in the Components user guide for more information.

## 비헤이비어 - 신규 및 재방문

새 보고서 및 돌아온 보고서는 첫 번째 세션 (새 방문 횟수) 와 후속 세션 (재방문) 의 간소화된 보기를 제공합니다.

새 방문 횟수 및 재방문 보고서를 만들려면:

1. In the components menu, locate the **First Time Visits** segment and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;. **첫 번째 방문은** 세그먼트이고 작업 영역은 일반적으로 차원을 사용하여 행을 나타냅니다.
2. **재방문 세그먼트를** 찾아 세그먼트 행 머리글의 상단에서 드래그합니다. 이렇게 하면 세그먼트를 처음 방문 시 차원과 같은 차원으로 추가하므로 간단한 비교를 할 수 있습니다.
3. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

라인 그래프도 필요한 경우:

1. 왼쪽의 시각화 아이콘을 클릭하고 선 시각화 기능을 자유 형식 테이블 위의 작업 영역으로 드래그합니다.
2. 자유 형식 테이블의 각 행에서 Ctrl 키 (Windows) 또는 Cmd 키 (Mac) 를 누른 상태에서 클릭하여 강조 표시합니다. 이렇게 하면 두 트렌드가 라인 시각화에 표시됩니다.
3. 라인 시각화의 왼쪽 위 모퉁이에 있는 작은 둥근 색상 점을 클릭한 다음 확인란 잠금 (Lock Selection) 를 클릭합니다.

## 동작 - 빈도 및 최근

The frequency &amp; recency report is approximately equal to the **Visit Number** dimension in Analysis Workspace.

1. In the components menu, locate the **Visit Number** dimension and drag it onto the large freeform table area labeled &#39;Drop a dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Visit Number](../../../components/c-variables/dimensionslist/reports-visitor-number.md) dimension in the Components user guide for more information.

## 행동 - 참여

The engagement report is approximately equal to the **Time Spent per Visit - Bucketed** dimension.

1. In the components menu, locate the **Time Spent per Visit - Bucketed** dimension and drag it onto the large freeform table area labeled &#39;Drop a dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Time Spent per Visit](../../../components/c-variables/dimensionslist/reports-time-spent-per-visit.md) dimension in the Components user guide for more information.

## 기술 - 브라우저 및 OS

브라우저 및 OS 보고서에는 여러 가지 기본 차원이 있습니다.

* **브라우저** 기본 차원은 분석 작업 공간에서 차원으로 사용할 수도 있습니다.
* **운영 체제** 기본 차원은 분석 작업 공간에서 차원으로 사용할 수도 있습니다.
* **화면 해상도** 기본 차원은 분석 작업 공간에서 **모니터 해상도** 차원으로 사용할 수 있습니다.
* **화면 색상** 기본 차원은 분석 작업 공간에서 **색상 깊이** 차원으로 사용할 수 있습니다.
* **Flash 버전** 기본 차원은 Adobe Analytics에서 사용할 수 없지만 필요한 경우 evar에 의해 데이터를 수집할 수 있습니다.

1. 구성 요소 메뉴에서 위에 언급된 원하는 차원을 찾아&#39;여기에서 차원 놓기&#39;레이블이 지정된 큰 자유형 테이블 영역으로 드래그합니다.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

해당 차원에 대한 자세한 내용은 구성 요소 사용자 안내서의 다음 페이지를 참조하십시오.

* [브라우저](../../../components/c-variables/dimensionslist/reports-browsers.md)
* [운영 체제](../../../components/c-variables/dimensionslist/reports-operating-system.md)
* [모니터 해상도](../../../components/c-variables/dimensionslist/reports-technology.md)
* [색상 깊이](../../../components/c-variables/dimensionslist/reports-color-depth.md)

## 기술 - 네트워크

The network report is approximately equal to the **Domain** dimension.

1. In the components menu, locate the **Domain** dimension and drag it onto the large freeform table area labeled &#39;Drop a dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Domain](../../../components/c-variables/dimensionslist/reports-domains.md) dimension in the Components user guide for more information.

## 모바일 - 개요

The mobile overview report is approximately equal to the **Mobile Device Type** dimension. &#39; 기타&#39;값은 데스크톱 트래픽과 같습니다.

1. In the components menu, locate the **Mobile Device Type** dimension and drag it onto the large freeform table area labeled &#39;Drop a dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Mobile Device Type](../../../components/c-variables/dimensionslist/reports-device-types.md) dimension in the Components user guide for more information.

## 모바일 - 장치

The mobile devices report is approximately equal to the **Mobile Device** dimension.

1. In the components menu, locate the **Mobile Device** dimension and drag it onto the large freeform table area labeled &#39;Drop a dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Mobile Device](../../../components/c-variables/dimensionslist/reports-devices.md) dimension in the Components user guide for more information.

## 사용자 지정

사용자 지정 보고서는 구현 기준으로 정의됩니다. 이 보고서를 해석하려면 조직의 Analytics 관리자 및/또는 구현 컨설턴트와 함께 작업합니다. Typically an organization maintains a [Solution Design Document](../../../implement/prepare/solution-design.md) to keep track of custom variable values and how they are populated.

## 벤치마크

벤치마크 보고서를 사용하면 데이터의 패싯이 업계 평균과 어떻게 비교되는지 확인할 수 있습니다. Adobe는 현재 고객 간의 벤치마크 데이터를 공유하지 않습니다.

## 사용자 흐름

흐름 보고서는 두 플랫폼에서 모두 사용할 수 있습니다. 흐름 보고서를 만들려면:

1. 왼쪽의 시각화 아이콘을 클릭하고 흐름 시각화 기능을 자유 형식 테이블 위의 작업 영역으로 드래그합니다.
2. **페이지** 차원을 찾은 다음 화살표 아이콘을 클릭하여 페이지 값을 표시합니다. 차원 값은 노란색으로 표시됩니다.
3. 원하는 페이지 값을 찾아 가운데에 있는&#39;차원 또는 항목&#39;레이블이 지정된 공간으로 드래그합니다.
4. 이 흐름 보고서는 대화형입니다. 다음 또는 이전 페이지로 흐름을 확장하려면 아무 값이나 클릭합니다. 마우스 오른쪽 단추를 클릭하여 열을 확장하거나 축소합니다. 동일한 흐름 보고서 내에서 다른 차원을 사용할 수도 있습니다.
