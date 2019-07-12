---
title: Adobe Analytics의 동작 보고서
description: Adobe Analytics에서 행동 보고서를 만드는 방법 학습
translation-type: tm+mt
source-git-commit: 71899840dd5b401c6892b6ad5088d4a32fd07042

---


# 동작 보고서

행동 보고서는 사용자가 사이트와 상호 작용하는 방법에 대한 정보를 보여줍니다.

이 페이지에서는 사용자가 분석 작업 공간 사용에 대한 기본적인 지식을 가지고 있다고 가정합니다. See [Create a basic report in Analysis Workspace for Google Analytics users](create-report.md) if you are not yet familiar with the tool in Adobe Analytics.

## 동작 흐름

흐름 시각화 기능을 사용하여 행동 흐름 보고서를 다시 만들 수 있습니다.

1. 왼쪽의 시각화 아이콘을 클릭하고 흐름 시각화 기능을 자유 형식 테이블 위의 작업 영역으로 드래그합니다.
2. **페이지** 차원을 찾은 다음 화살표 아이콘을 클릭하여 페이지 값을 표시합니다. 차원 값은 노란색으로 표시됩니다.
3. 원하는 페이지 값을 찾아 가운데에 있는&#39;차원 또는 항목&#39;레이블이 지정된 공간으로 드래그합니다.
4. 이 흐름 보고서는 대화형입니다. 다음 또는 이전 페이지로 흐름을 확장하려면 아무 값이나 클릭합니다. 마우스 오른쪽 단추를 클릭하여 열을 확장하거나 축소합니다. 동일한 흐름 보고서 내에서 다른 차원을 사용할 수도 있습니다.

![흐름 보고서](../assets/flow.png)

## 사이트 컨텐츠 - 모든 페이지

페이지 보고서는 사이트에 있는 개별 페이지의 성과를 보여줍니다.

1. In the Components menu, locate the **Pages** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

대안으로서, Adobe는 템플릿이라는 미리 만들어진 몇 가지 작업 영역을 제공합니다. 컨텐츠 소비 (웹) 템플릿은 모든 페이지 보고서와 유사한 값을 제공합니다.

1. *[!UICONTROL 프로젝트] &gt; [!UICONTROL 새로 만들기를]*클릭하여 프로젝트 옵션이 있는 모달 창을 엽니다.
2. 컨텐츠 소비 (웹) 템플릿을 클릭한 다음 만들기를 클릭합니다.

## 사이트 컨텐츠 - 컨텐츠 드릴다운

컨텐츠 드릴다운 보고서를 사용하면 URL 구조별 페이지 트래픽을 확인할 수 있습니다. 분석 작업 공간에서 사용하려면 추가적인 구현이 필요합니다. Adobe는 구현 컨설턴트와 함께 이 데이터가 정확하게 수집되도록 할 것을 권장합니다.

## 사이트 컨텐츠 - 랜딩 페이지

랜딩 페이지 보고서는 사이트의 상위 랜딩 페이지를 보여줍니다. Landing pages are available in Analysis Workspace as the **Entry Page** dimension.

1. In the Components menu, locate the **Entry Page** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

Adobe recommends using the **Visits** metric for this dimension.

## 사이트 컨텐츠 - 종료 페이지

종료 페이지 보고서는 개별 방문의 마지막 페이지가 된 상위 페이지를 보여줍니다. 동일한 이름의 분석 작업 공간에서 사용할 수 있습니다.

1. In the Components menu, locate the **Exit Page** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

Adobe recommends using the **Visits** metric for this dimension.

## 사이트 속도 보고서

사이트 속도 보고서는 페이지 로드 시간을 단축하여 페이지 로드 시간을 늘릴 수 있는 기회를 보여줍니다.

이 기능을 사용하려면 두 플랫폼에서 추가 구현이 필요합니다. 분석 작업 공간에 대해 이 데이터가 올바르게 구성되도록 구현 컨설턴트와 함께 작업하는 것이 좋습니다. [성능 시간 초과 플러그인은](../../../implement/js-implementation/plugins/performancetiming.md) 일반적으로 Adobe Analytics에서 성능 데이터를 얻을 수 있도록 evar에 할당됩니다.

## 사이트 검색 보고서

사이트 검색 보고서는 방문자가 사이트의 내부 검색 기능을 사용하는 방법에 대한 통찰력을 제공합니다.

이 기능을 사용하려면 두 플랫폼에서 추가 구현이 필요합니다. 분석 작업 공간에 대해 이 데이터가 올바르게 구성되도록 구현 컨설턴트와 함께 작업하는 것이 좋습니다. 일반적으로 내부 검색어는 쿼리 문자열 매개 변수에서 가져와서 보고를 위해 Evar에 배치됩니다.

## 이벤트 보고서

이벤트는 Google와 Adobe Analytics 간의 몇 가지 주요 구조적 차이점이 있습니다. 두 가지 모두 해당 플랫폼에서 제대로 작동하려면 추가적인 구현이 변경되었습니다.

* Google Analytics에서 이벤트는 구현에서 텍스트로 정의됩니다. 이벤트에는 카테고리, 작업 및 레이블이 있습니다.
* Adobe Analytics에서 이벤트는 식별자가 지정되는 관리 콘솔에 먼저 설정됩니다. 이 식별자는 구현 코드에서 사용됩니다. 예:
   1. 관리 콘솔에서 event 1 을&#39;registration&#39;으로 설정할 수 있습니다.
   2. 구현에서는 등록 확인 페이지의 이벤트 변수에 event 1를 포함하게 됩니다. 등록 확인 페이지가 표시될 때마다 event 1 이 증가합니다.
   3. 분석 작업 공간에서&#39;등록&#39;은 보고서에서 사용할 지표로 나타납니다.

이 기능은 구현 변경을 필요로 하기 때문에 분석 작업 공간에 대해 데이터가 올바르게 구성되도록 구현 컨설턴트와 함께 작업하는 것이 좋습니다.

## 게시자 보고서

Google의 Google 광고 관리자와 Google의 연결이 필요한 방식과 마찬가지로 Adobe는 Adobe Advertising Cloud 라는 인사이트를 제공하는 전용 제품을 제공합니다. 조직에서 이 제품을 사용하려면 조직의 계정 관리자에게 문의하십시오.
