---
title: Adobe Analytics의 획득 보고서
description: 분석 작업 공간을 사용하여 획득 기반 보고서를 만드는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: 71899840dd5b401c6892b6ad5088d4a32fd07042

---


# 획득 보고서

획득 보고서는 사이트 방문자를 얻는 방법을 보여줍니다.

In Adobe Analytics, these reports are known as **Marketing Channels**. 기본적인 초기 설정을 필요로 하지만 보다 사용자 정의된 채널 보기를 허용합니다.

> [!IMPORTANT]
>
> 마케팅 채널 처리 규칙을 설정하여 이러한 보고서를 사용합니다. See [Getting Started with Marketing Channels](../../../components/c-marketing-channels/c-getting-started-mchannel.md) for information on how to best configure Marketing Channels in your organization.

이 페이지에서는 사용자가 분석 작업 공간 사용에 대한 기본적인 지식을 가지고 있다고 가정합니다. See [Create a basic report in Analysis Workspace for Google Analytics users](create-report.md) if you are not yet familiar with the tool in Adobe Analytics.

## 모든 트래픽 - 채널

방문자가 사이트에 도달하기 위해 사용하는 모든 채널의 전체 보기를 보여줍니다.

1. In the Components menu, locate the **Marketing Channel** dimension and drag it onto the large freeform table area labeled 'Drop a Dimension here'.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

## 모든 트래픽 - 트리 맵

채널 트래픽의 트리맵을 표시합니다. 이 보고서는 모든 트래픽 - 채널과 비슷하지만 다른 방식으로 표시됩니다.

1. 왼쪽의 시각화 아이콘을 클릭하고 트리맵 시각화를 빈 자유 형식 테이블 위의 작업 영역으로 드래그합니다.
2. Click the Components icon on the left, then drag the **Marketing Channel** dimension onto the large freeform table area labeled 'Drop a dimension here'.
3. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.
4. 추가 지표는 추가 트리 맵을 만듭니다. 하나의 트리맵만 필요한 경우:
   1. 트리맵을 나타내려면 원하는 지표의 맨 위 셀을 클릭합니다.
   2. Shift 키를 누른 상태에서 동일한 지표 열의 마지막 셀을 클릭하여 파란색을 강조 표시합니다. 올바르게 완료되면 시각화에 하나의 트리맵이 있습니다.
   3. 트리 맵 시각화의 오른쪽 위 모서리에서 색상 점을 클릭한 다음 확인란'선택 잠금'을 클릭합니다.

트리 맵은 마케팅 채널뿐만 아니라 모든 차원에 적용할 수 있습니다.

## 모든 트래픽 - 소스/미디어

소스 및 중간 보고서에는 사이트로 트래픽을 유도한 도메인이 표시됩니다.

* **소스** 기본 차원은 **참조 도메인** 차원으로 분석 작업 공간에서 사용할 수 있습니다.
* **중간** 기본 차원은 **참조 유형** 차원으로 분석 작업 공간에서 사용할 수 있습니다.
* **키워드** 기본 차원은 분석 작업 공간에서 **검색 키워드** 차원으로 사용할 수 있습니다.

1. 구성 요소 메뉴에서 위에 언급된 원하는 차원을 찾아'여기에서 차원 놓기'레이블이 지정된 큰 자유형 테이블 영역으로 드래그합니다.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

해당 차원에 대한 자세한 내용은 구성 요소 사용자 안내서의 다음 페이지를 참조하십시오.

* [조회 도메인](../../../components/c-variables/dimensionslist/reports-referring-domains.md)
* [레퍼러 유형](../../../components/c-variables/dimensionslist/reports-ref-types.md)
* [검색 키워드](../../../components/c-variables/dimensionslist/reports-search-keywords.md)

## 모든 트래픽 - 참조

* **소스** 기본 차원은 **참조 도메인** 차원으로 분석 작업 공간에서 사용할 수 있습니다.
* **랜딩 페이지** 기본 차원은 시작 **페이지** 차원으로 분석 작업 공간에서 사용할 수 있습니다.

1. In the components menu, locate the **Referring Domain** or **Entry Page** dimension and drag it onto the large freeform table area labeled 'Drop a dimension here'.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

See the [Referring Domain](../../../components/c-variables/dimensionslist/reports-referring-domains.md) dimension in the Components user guide for more information.

## Google 광고 보고서 및 검색 콘솔 보고서

Adobe는 광고 분석이라고 하는 분석 작업 공간의 기능을 사용하여 Google를 비롯한 다양한 플랫폼에서 광고 및 검색 데이터를 가져옵니다.

광고 분석 기능을 사용하려면 데이터를 반환해야 합니다. See [Advertising Analytics Help](../../../integrate/c-advertising-analytics/overview.md) for details on how to enable these additional dimensions in Analysis Workspace.

## 소셜 보고서

소셜 보고서는 소셜 네트워크의 컨텍스트를 제외하고 해당 행동 보고서와 유사한 정보를 제공합니다. 이 데이터는 차원과 세그먼트를 결합하여 분석 작업 공간에서 사용할 수 있습니다.

때때로 방문자는 동일한 세션에서 여러 채널을 통해 사이트에 도달합니다. 예를 들어 방문자가 소셜 미디어 페이지를 클릭하면 몇 분 후에 사이트에 도달하기 위해 검색 엔진을 방문합니다. 이러한 경우 이 보고서에 비소셜 도메인이 나타날 수 있습니다. 소셜 도메인이 아닌 도메인을 제외하려면 방문별로 보고서를 정렬하거나 방문 횟수 대신 히트를 기반으로 할 세그먼트 사본을 만듭니다. See [Segmentation Containers](../../../components/c-segmentation/seg-overview.md) in the Components user guide for more information.

### 소셜 - 네트워크 참조

네트워크 참조 보고서는 사이트로 트래픽을 유도한 소셜 네트워크 도메인을 보여줍니다. This data is available in Analysis Workspace using the **Referring Domain** dimension and **Visits from Social Sites** segment.

1. In the Components menu, locate the **Referring Domain** dimension and drag it onto the large freeform table area labeled 'Drop a Dimension here'.
2. In the Components menu, locate the **Visits from Social Sites** segment and drag in onto the small area just above the freeform table labeled 'Drop a segment here'.
3. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

### 소셜 - 랜딩 페이지

랜딩 페이지 보고서는 방문자가 소셜 네트워크를 통해 링크를 클릭한 후 도착한 페이지를 보여줍니다. This data is available in Analysis Workspace using the **Entry Page** dimension and **Visits from Social Sites** segment.

1. In the Components menu, locate the **Entry Page** dimension and drag it onto the large freeform table area labeled 'Drop a Dimension here'.
2. In the Components menu, locate the **Visits from Social Sites** segment and drag in onto the small area just above the freeform table labeled 'Drop a segment here'.
3. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

### 소셜 - 전환

전환 보고서는 소셜 네트워크 컨텍스트에서 전자 상거래 데이터를 보여줍니다. 두 플랫폼에서 이러한 보고서를 사용하려면 추가적인 구현이 필요합니다. 분석 작업 공간에 대해 이 데이터가 올바르게 구성되도록 구현 컨설턴트와 함께 작업하는 것이 좋습니다.

### 소셜 - 플러그인

Plugins 보고서는 방문자가 사이트에 포함된 소셜 미디어 플러그인과 상호 작용하는 방식을 보여줍니다. 분석 작업 공간에서 사용하려면 추가적인 구현이 필요합니다. Adobe는 구현 컨설턴트와 함께 이 데이터가 정확하게 수집되도록 할 것을 권장합니다.

### 소셜 - 사용자 흐름

사용자 흐름 보고서는 소셜 네트워크를 통해 도착하는 방문자의 컨텍스트에서 경로 데이터를 보여줍니다.

1. 왼쪽의 시각화 아이콘을 클릭하고 흐름 시각화 기능을 자유 형식 테이블 위의 작업 영역으로 드래그합니다.
2. Click the Components icon on the left, then drag the **Visits from Social Sites** segment onto the small area just above the flow visualization labeled 'Drop a Segment here'.
3. **페이지** 차원을 찾은 다음 화살표 아이콘을 클릭하여 페이지 값을 표시합니다. 차원 값은 노란색으로 표시됩니다.
4. 원하는 페이지 값을 찾아 가운데에 있는'차원 또는 항목'레이블이 지정된 공간으로 드래그합니다.
5. 이 흐름 보고서는 대화형입니다. 다음 또는 이전 페이지로 흐름을 확장하려면 아무 값이나 클릭합니다. 마우스 오른쪽 단추를 클릭하여 열을 확장하거나 축소합니다. 동일한 흐름 보고서 내에서 다른 차원을 사용할 수도 있습니다.

## 캠페인 - 모두

The campaigns report is available in Analysis Workspace using the **Tracking Code** dimension. 추적 코드 차원을 사용하려면 데이터를 수집하려면 추가 구현이 필요합니다.

사용자 지정 변수 (Evar) 를 사용하여 Adobe Analytics에서 utm 매개 변수를 수집할 수 있습니다. Adobe 에서는 구현 컨설턴트와 협력하여 추적 코드 값이 Adobe Analytics에서 정확하게 수집되도록 할 것을 권장합니다.

1. In the Components menu, locate the **Tracking Code** dimension and drag it onto the large freeform table area labeled 'Drop a Dimension here'.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

## 캠페인 - 유료 키워드

유료 키워드 보고서는 방문자가 검색 엔진에서 유료 검색 링크를 클릭한 후 각 키워드가 수행하는 방식을 보여줍니다. **검색 키워드 - 유료** 차원은 분석 작업 공간에서 사용할 수 있지만 데이터를 수집하려면 1 회 유료 검색 감지 설정이 필요합니다. See [Paid Search Detection](../../../admin/admin/paid-search-detection/paid-search-detection.md) in the Admin user guide for setup details.

1. In the Components menu, locate the **Search Keyword - Paid** dimension and drag it onto the large freeform table area labeled 'Drop a Dimension here'.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

## 캠페인 - 유기 키워드

유기 키워드 보고서는 방문자가 검색 엔진에서 유기적 검색 링크를 클릭한 후 각 키워드가 수행하는 방식을 보여줍니다. **검색 키워드 - 자연어 차원은** 분석 작업 공간에서 사용할 수 있습니다. 유료 검색 탐지가 설정되지 않은 경우 이 차원은 유료 키워드와 자연어 키워드를 모두 수집합니다.

1. In the Components menu, locate the **Search Keyword - Natural** dimension and drag it onto the large freeform table area labeled 'Drop a Dimension here'.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

## 비용 분석

이 보고서는 유료 마케팅 채널에 대한 방문, 비용 및 매출 성과 데이터를 보여줍니다. Adobe는 Adobe Advertising Cloud 라는 인사이트를 제공하는 전용 제품을 제공합니다. 조직에서 이 제품을 사용하려면 조직의 계정 관리자에게 문의하십시오.
