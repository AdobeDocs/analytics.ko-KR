---
description: Analysis Workspace에서 사용할 수 있는 시각화를 사용하여 데이터를 시각적으로 표현하는 방법을 알아봅니다.
keywords: Analysis Workspace
title: 시각화 개요
feature: Visualizations
role: User, Admin
exl-id: b40aa942-4a08-4ff3-9895-e92f9a187b54
source-git-commit: 599fbea7cb22e9cd0193b56fc2fb3c506bc62949
workflow-type: tm+mt
source-wordcount: '1510'
ht-degree: 94%

---

# 시각화 개요

Workspace는 데이터를 시각적으로 나타내는 다양한 시각화를 생성할 수 있도록 해 줍니다. 막대 차트, 도넛 차트, 히스토그램, 선 차트, 맵, 산포도 등과 같은 데이터.

## 유형

Analysis Workspace에서 다음 시각화 유형을 사용할 수 있습니다.


| 아이콘 | 이름 | 설명 |
| :---: | --- | ---| 
| ![GraphArea](/help/assets/icons/GraphArea.svg) | [영역](/help/analyze/analysis-workspace/visualizations/area.md) | 영역 그래프 시각화. 선 그래프와 비슷하지만 선 아래에 색칠된 영역이 있습니다. 여러 개의 지표가 있고 두 개 이상 지표의 교차 지점으로 표시되는 영역을 시각화하려는 경우 영역 그래프를 사용하십시오. |
| ![GraphBarVertical](/help/assets/icons/GraphBarVertical.svg) | [막대](/help/analyze/analysis-workspace/visualizations/bar.md) | 하나 이상 지표에서 다양한 값을 나타내는 세로 막대의 막대 그래프 시각화. |
| ![GraphBarVertical](/help/assets/icons/GraphBarVerticalStacked.svg) | [스택 막대](/help/analyze/analysis-workspace/visualizations/bar.md) | 하나 이상 지표에서 다양한 값을 나타내는 세로 막대의 누적 막대 그래프 시각화. |
| ![GraphBullet](/help/assets/icons/GraphBullet.svg)</p> | [글머리 기호](/help/analyze/analysis-workspace/visualizations/bullet-graph.md) | 중요한 값이 다른 성능 범위(목표)에 대해 비교되거나 측정되는 방식을 표시하는 글머리 기호 그래프 시각화. |
| ![TextNumbered](/help/assets/icons/TextNumbered.svg) | [코호트 테이블](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) | 코호트 시각화는 지정된 기간 동안 공통적인 특성을 공유하는 사람들의 그룹입니다. 코호트 테이블은 유지, 이탈 또는 지연 시간 분석에 유용합니다. |
| ![콤보](/help/assets/icons/ComboChart.svg) | [콤보](combo-charts.md) | 콤보 차트를 사용하면 테이블을 먼저 만들지 않고도 빠르게 비교 시각화를 만들 수 있습니다. |
| ![GraphDonut](/help/assets/icons/GraphDonut.svg) | [도넛](/help/analyze/analysis-workspace/visualizations/donut.md) | 파이 차트와 유사하게 도넛 시각화는 데이터를 전체의 일부 또는 세그먼트로 표시합니다. |
| ![ConversionFunnel](/help/assets/icons/ConversionFunnel.svg) | [폴아웃](/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md) | 폴아웃 시각화는 방문자가 페이지의 사전 정의된 순서를 떠나고(폴아웃) 계속 따라가는(폴스루) 위치를 보여 줍니다. |
| ![GraphPathing](/help/assets/icons/GraphPathing.svg) | [플로우](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) | 플로우 시각화는 고객이 웹 사이트 및 앱을 통과하는 정확한 경로를 보여 줍니다. |
| ![ViewTable](/help/assets/icons/ViewTable.svg)</p> | [자유 형식 테이블](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) | 자유 형식 테이블 시각화는 대화형 시각화입니다. 자유 형식 테이블 시각화는 Workspace의 데이터 분석을 위한 기반입니다. |
| ![GraphHistogram](/help/assets/icons/Histogram.svg) | [히스토그램](/help/analyze/analysis-workspace/visualizations/histogram.md) | 히스토그램 시각화는 지표 볼륨을 기반으로 사람, 방문자 또는 이벤트를 버킷으로 버킷화합니다. |
| ![GraphBarHorizontal](/help/assets/icons/GraphBarHorizontal.svg) | [가로 막대](/help/analyze/analysis-workspace/visualizations/horizontal-bar.md) | 가로 막대 시각화는 하나 이상의 지표에서 다양한 값을 나타내는 가로 막대를 보여 줍니다. |
| ![GraphBarHorizontalStacked](/help/assets/icons/GraphBarHorizontalStacked.svg) | [스택 가로 막대](/help/analyze/analysis-workspace/visualizations/horizontal-bar.md) | 스택 가로 막대 시각화는 하나 이상의 지표에서 다양한 값을 나타내는 가로 막대를 보여 줍니다. |
| ![KeyMetrics](/help/assets/icons/KeyMetrics.svg) | [주요 지표 요약](/help/analyze/analysis-workspace/visualizations/key-metric.md) | 주요 지표 요약 시각화는 라인, 요약 변경 사항 및 요약 숫자 시각화를 결합합니다. |
| ![GraphTrend](/help/assets/icons/GraphTrend.svg) | [라인](/help/analyze/analysis-workspace/visualizations/line.md) | 라인 시각화는 일정 기간 동안 값이 어떻게 변하는지를 보여 주기 위해 라인을 사용하여 지표를 나타냅니다. 라인 차트는 x축을 따라 시간을 사용합니다. |
| ![지구](/help/assets/icons/Globe.svg) | [맵](/help/analyze/analysis-workspace/visualizations/map-visualization.md) | 모든 지표(계산된 지표 포함)의 시각적 맵을 작성할 수 있도록 해 줍니다 |
| ![GraphScatter](/help/assets/icons/GraphScatter.svg) | [산포도](/help/analyze/analysis-workspace/visualizations/scatterplot.md) | 산포도 시각화는 차원 항목과 최대 3개 지표 간의 관계를 표시합니다. |
| ![PageRule](/help/assets/icons/PageRule.svg) | [섹션 헤더](section-header.md) | 패널 내의 섹션을 식별하고 표현합니다. |
| ![MoveUpDown](/help/assets/icons/MoveUpDown.svg) | [요약 변경](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) | 요약 변경 시각화는 선택한 셀 간의 변경 사항을 하나의 큰 숫자나 백분율로 표시합니다. |
| ![123](/help/assets/icons/123.svg)</p> | [요약 숫자](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) | 요약 숫자 시각화는 선택한 셀을 하나의 큰 숫자로 표시합니다. |
| ![텍스트](/help/assets/icons/Text.svg) | [텍스트](/help/analyze/analysis-workspace/visualizations/text.md) | 텍스트 시각화는 사용자 정의 텍스트를 Workspace에 추가할 수 있게 합니다. 패널/시각화 설명을 활용하는 것 외에도 사용자의 분석 및 인사이트에 추가 컨텍스트를 추가하는 데 유용합니다. |
| ![ModernGridView](/help/assets/icons/ModernGridView.svg) | [트리맵](/help/analyze/analysis-workspace/visualizations/treemap.md)<p> | 트리맵 시각화는 계층형(트리 구조) 데이터를 중첩된 직사각형 세트로 표시합니다. |
| ![유형](/help/assets/icons/TwoDots.svg) | [벤](/help/analyze/analysis-workspace/visualizations/venn.md) | 벤 시각화는 원을 사용하여 최대 3개 세그먼트의 지표 겹침을 나타냅니다. |

<!--

| Name| Icon | Description |
| --- |:---: | ---|
| [Area](/help/analyze/analysis-workspace/visualizations/area.md)|![Area icon](assets/Smock_GraphArea_18_N.svg)</p> | Like a line graph, but with a colored area below the line. Use an area graph when you have multiple metrics and want to visualize the area expressed by the intersection of two or more metrics. |
| [Bar](/help/analyze/analysis-workspace/visualizations/bar.md)|![Bar icon](assets/Smock_GraphBarVertical_18_N.svg)</p> | Shows vertical bars representing various values across one or more metrics. |
| [Bullet graph](/help/analyze/analysis-workspace/visualizations/bullet-graph.md)|![Bullet icon](assets/Smock_GraphBullet_18_N.svg)</p> | Shows how a value you are interested in compares to or measures against other performance ranges (goals). |
| [Cohort table](/help/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis.md)|![Cohort table icon](assets/Smock_TextNumbered_18_N.svg)</p> | A *`cohort`* is a group of people sharing common characteristics over a specified period. Cohort Analysis is useful for retention, churn or latency analysis. |
| [Donut](/help/analyze/analysis-workspace/visualizations/donut.md) | ![Donut icon](assets/Smock_GraphDonut_18_N.svg)</p> | Similar to a pie chart, this visualization shows data as parts or segments of a whole. |
| [Fallout](/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md) | ![Fallout icon](assets/Smock_ConversionFunnel_18_N.svg)</p> | Fallout reports show where visitors left (fell out) and continued through (fell through) a predefined sequence of pages. Can be set to eventual or exact sequences |
| [Flow](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) | ![Flow icon](assets/flow-icon.png)</p> | Shows exact customer paths through your websites and apps. |
| [Freeform table](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) | ![Freeform table icon](assets/Smock_ViewTable_18_N.svg)</p> | A Freeform table is not merely a data table, but also an interactive visualization. It is the foundation for data analysis in Workspace.|
| [Histogram](/help/analyze/analysis-workspace/visualizations/histogram.md) | ![Histogram icon](assets/Smock_GraphHistogram_18_N.svg)</p> | A histogram buckets visitors, visits or hits into buckets based on a metric volume. |
| [Horizontal bar](/help/analyze/analysis-workspace/visualizations/horizontal-bar.md) | ![Horizontal bar icon](assets/Smock_GraphBarHorizontal_18_N.svg)</p> | Shows horizontal bars representing various values across one or more metrics. |
| [Key metric summary](/help/analyze/analysis-workspace/visualizations/key-metric.md) | ![Key metric icon](assets/key-metric-icon.png)</p> | Shows how a metric is trending within a single timeframe, or lets you compare metric performance across two timeframes. |
| [Line](/help/analyze/analysis-workspace/visualizations/line.md) | ![Line icon](assets/Smock_GraphTrend_18_N.svg)</p> | Represents metrics using a line in order to show how values change over a period of time. A line chart uses time along the x-axis. |
| [Map](/help/analyze/analysis-workspace/visualizations/map-visualization.md) | ![Map icon](assets/map-icon.png)</p> | Lets you build a visual map of any metric (including calculated metrics). |
| [Scatterplot](/help/analyze/analysis-workspace/visualizations/scatterplot.md) | ![Scatterplot icon](assets/Smock_GraphScatter_18_N.svg)</p> | Shows the relationship between dimension items and up to three metrics. |
| [Summary number](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) | ![Summary number icon](assets/summary-number-icon.png)</p> | Shows the selected cell as 1 large number. |
| [Summary change](/help/analyze/analysis-workspace/visualizations/summary-number-change.md) | ![Summary change icon](assets/summary-change-icon.png)</p> | Shows the change between the selected cells as 1 large number/percent. |
| [Text](/help/analyze/analysis-workspace/visualizations/text.md) | ![Text icon](assets/Smock_Text_18_N.svg)</p> | Lets you add user-defined text to your Workspace. Helpful for adding additional context to your analysis and insights, in addition to leveraging panel/visualization descriptions |
| [Treemap](/help/analyze/analysis-workspace/visualizations/treemap.md) | ![Treemap icon](assets/Smock_GraphTree_18_N.svg)</p> | Displays hierarchical (tree-structured) data as a set of nested rectangles. |
| [Venn](/help/analyze/analysis-workspace/visualizations/venn.md) | ![Venn icon](assets/venn-icon.png)</p> | Uses circles to depict the metric overlap of up to 3 segments. |

-->

## 패널 내에 시각화 추가

1. 시각화를 추가할 Analysis Workspace 프로젝트를 엽니다.

1. 다음 방법 중 하나를 사용하여 시각화를 추가합니다.

   ![시각화 추가](assets/add-visualization.png)

   * 왼쪽 패널에서 ![GraphBarVertical](/help/assets/icons/GraphBarVertical.svg) **시각화**&#x200B;를 선택한 다음 시각화를 추가하려는 패널로 시각화를 드래그합니다.

   * 시각화를 추가하려는 패널에서 ![AddCircle](/help/assets/icons/AddCircle.svg)을 선택한 다음 추가하려는 시각화 아이콘을 선택합니다. 각 시각화의 아이콘 위에 마우스를 올려 놓으면 이름을 확인할 수 있습니다.

   * [빈 패널](/help/analyze/analysis-workspace/c-panels/blank-panel.md)을 추가한 다음 추가하려는 시각화를 선택합니다.

   * Analysis Workspace 프로젝트의 기존 시각화의 컨텍스트 메뉴에서 **[!UICONTROL 시각화 복제]** 또는 **[!UICONTROL 시각화 복사]**&#x200B;를 선택합니다.

   * Workspace **[!UICONTROL 삽입]** 메뉴를 사용하여 시각화를 삽입합니다.

   * 자유 형식 테이블의 컨텍스트 메뉴에서 **[!UICONTROL 시각화]**&#x200B;를 선택합니다. 그런 다음 하위 메뉴에서 시각화를 선택합니다. 테이블의 현재 선택에 따라 Workspace는 제공할 시각화를 결정하고 요청된 시각화를 구축하기 위해 데이터를 해석합니다.

## 범례

시각화 범례를 사용하면 소스 테이블의 날짜를 시각화에 그려진 시리즈와 연결할 수 있습니다. 범례는 대화형입니다. 시각화에서 시리즈를 표시하거나 숨기려면 범례 항목을 선택할 수 있습니다. 이는 시각화 중인 데이터를 단순화하려는 경우 유용합니다.

또한 시각적 오브젝트를 보다 쉽게 사용할 수 있도록 범례 레이블의 이름을 바꿀 수 있습니다. 참고: 트리맵, 글머리 기호, 요약 변경 사항 또는 숫자, 텍스트, 자유 형식, 히스토그램, 코호트 또는 플로우 시각화에는 범례 편집이 적용되지 **않습니다**.

범례 레이블을 편집하려면 다음 작업을 수행하십시오.

1. 범례 레이블 중 하나를 마우스 오른쪽 버튼으로 클릭합니다.
1. **[!UICONTROL 레이블 편집을 클릭합니다]**.

   ![범례 레이블과 레이블 편집 옵션.](assets/edit-label.png)

1. 새 레이블 텍스트를 입력합니다.
1. **[!UICONTROL Enter]**&#x200B;를 눌러 저장합니다.



### 설정

사용 가능한 시각화 설정은 시각화에 따라 다릅니다. 아래 테이블은 가장 일반적인 설정을 요약한 것입니다. 일부 시각화에는 특정 설정이 있습니다. 자세한 내용은 개별 시각화 문서를 참조하십시오.

| 옵션 | 설명 |
| --- | --- |
| **[!UICONTROL 시각화 유형]** | 데이터를 시각화하는 데 사용되는 시각화 유형을 변경합니다. |
| **[!UICONTROL 세부 기간]** | 트렌드 시각화의 세부 기간을 변경합니다. 이 변경 사항은 데이터 소스 테이블에도 적용됩니다. |
| **[!UICONTROL 백분율]** | 값을 백분율로 표시합니다. |
| **[!UICONTROL 100% 스택]** | 차트를 100% 스택 시각화로 바꿉니다. 영역, 막대, 가로 막대로 구성된 스택 시각화에만 적용됩니다. |
| **[!UICONTROL 범례 표시]** | 범례 텍스트를 표시합니다. |
| **[!UICONTROL 최대 항목 수 제한]** | 시각화에 표시되는 항목 수를 제한합니다. 선택하면 최대 항목 수를 정의합니다. |
| **[!UICONTROL 주석 표시]** | 이 시각화를 위해 작성된 주석을 표시합니다. |
| **[!UICONTROL 제목 숨기기]** | 시각화의 제목을 숨깁니다. |
| **[!UICONTROL Y축을 0에 고정]** | Y축의 하단을 0으로 강제 적용합니다. 차트에 표시된 모든 값이 0보다 매우 큰 경우 차트 기본값에 따라 Y축의 하단이 0이 아닌 값으로 지정됩니다. 이 옵션을 활성화하면 Y축이 0으로 강제 설정되고 차트가 다시 그려집니다. |
| **[!UICONTROL 이중 축 표시]** | 두 가지 다른 지표에 대한 왼쪽 및 오른쪽 Y축을 표시합니다. 이 옵션은 두 개의 지표가 있는 경우에만 적용됩니다. 이중 축은 그려진 지표의 크기가 다른 경우에 유용합니다. |
| **[!UICONTROL X축 표시]** | 시각화에 X축을 표시합니다. |
| **[!UICONTROL Y축 표시]** | 시각화에 Y축을 표시합니다. |
| **[!UICONTROL 라인에 바벨 표시]** | 콤보 차트 시각화에서 라인 시각화에 바벨을 표시합니다. |
| **[!UICONTROL 표준화]** | 지표를 등분 비례에 강제 적용합니다. 그려진 지표의의 크기가 다를 때는 동일한 비율이 도움이 됩니다. |
| **[!UICONTROL 예외 항목 표시]** | 예외 항목 탐지를 표시하여 선 그래프 및 자유 형식 테이블을 향상시킵니다. 라인 시각화의 예외 항목 탐지에는 예상 값(파선)과 예상 범위(음영 처리된 띠)가 포함됩니다. |
| **[!UICONTROL 예측 표시]** | 예측 값을 표시하여 선 그래프와 자유 형식 테이블을 향상시킵니다. |
| **[!UICONTROL 최소 표시]** | 시각화에 최소값을 보여 줍니다. |
| **[!UICONTROL 최대 표시]** | 시각화에 최대값을 보여 줍니다. |
| **[!UICONTROL 트렌드 라인 표시]** | 시각화에 트렌드 라인을 표시합니다. 선택하면 드롭다운 메뉴에서 추세선 유형을 선택할 수 있습니다. |

생성한 모든 시각화에 대한 설정을 사용자 정의할 수 있습니다. 자세한 내용은 [사용자 환경 설정](/help/analyze/analysis-workspace/user-preferences.md)을 참조하십시오.


## 컨텍스트 메뉴 {#right-click}

시각화 헤더의 컨텍스트 메뉴(예: 마우스 사용 시 마우스 오른쪽 버튼 클릭 등 대체 선택을 통해 사용 가능)를 사용하여 시각화를 위한 추가 기능에 액세스합니다. 모든 시각화에 모든 옵션을 사용할 수 있는 것은 아닙니다.

![마우스 오른쪽 클릭 옵션이 표시된 추가 시각화 설정. 다음 섹션에서는 옵션을 설명합니다.](assets/right-click.png)

| 옵션 | 설명 |
| --- | --- |
| **[!UICONTROL 복사된 시각화 삽입]** | 복사한 시각화를 프로젝트 내의 다른 위치 또는 완전히 다른 프로젝트에 붙여넣기(삽입)할 수 있습니다. |
| **[!UICONTROL 클립보드에 데이터 복사]** | 시각화에서 클립보드로 [데이터를 복사](/help/analyze/analysis-workspace/curate-share/download-send.md#copy-to-clipboard)합니다. |
| **[!UICONTROL 클립보드에 선택 항목 복사]** | 시각화에서 클립보드로 [선택 항목을 복사](/help/analyze/analysis-workspace/curate-share/download-send.md#copy-to-clipboard)합니다. |
| **[!UICONTROL CSV로 항목 다운로드(*차원 이름*)]** | [로컬 장치에 시각화의 차원 항목을 다운로드](/help/analyze/analysis-workspace/curate-share/download-send.md#download-items-as-csv)(최대 50,000개)합니다. 선택한 차원에 최대 50,000개의 차원 항목. |
| **[!UICONTROL 시각화 복사]** | 시각화를 복사하여 프로젝트 내의 다른 위치 또는 완전히 다른 프로젝트에 삽입할 수 있습니다. |
| **[!UICONTROL 데이터 CSV 다운로드]** | 로컬 장치에 시각화의 [표시된 데이터를 다운로드합니다](/help/analyze/analysis-workspace/curate-share/download-send.md#download-as-csv). |
| **[!UICONTROL 시각화 복제]** | 시각화를 정확하게 복제합니다. |
| **[!UICONTROL 설명 편집]** | 시각화에 대한 텍스트 설명을 추가 (또는 편집)합니다. [텍스트](text.md)를 확인합니다. |
| **[!UICONTROL 시각화 링크 가져오기]** | 시각화에 대한 링크를 직접 복사하여 공유합니다. 링크 공유 대화 상자에 링크가 표시됩니다. 복사를 선택하면 링크를 클립보드에 복사할 수 있습니다. |
| **[!UICONTROL 시작]** | 현재 시각화에 대한 구성을 삭제하여 처음부터 다시 구성할 수 있습니다. |


## 구성

일부 시각화(코호트 테이블, 폴아웃, 플로우 등)에는 시각화를 구축하는 데 도움이 되는 구성 대화 상자가 있습니다. 시각화 상단의 ![편집](/help/assets/icons/Edit.svg)을 사용하여 구성에 액세스하고 이를 변경합니다.

![구성 창](assets/configuration.png)

## 시각화

어떤 시각화를 선택할지 확실하지 않은 경우, 자유 형식 테이블 행에서 ![GraphBarVerticalAdd](/help/assets/icons/GraphBarVerticalAdd.svg) **[!UICONTROL 시각화]**&#x200B;를 선택합니다(마우스를 올려 놓으면 사용 가능). 이 선택 방법은 시각화를 추가하는 가장 빠른 방법입니다. Analysis Workspace는 기존 학습을 토대로 사용자 데이터에 가장 적합한 시각화를 추정합니다. 예를 들어 1개의 행을 선택한 경우 트렌드 [선 그래프](line.md)가 생성됩니다. 3개의 필터 행을 선택한 경우 [벤](venn.md) 다이어그램이 생성됩니다.

![빠른 시각화](assets/quick-viz.png)


<!--
## Settings {#settings}

![](assets/settings.png)

| Setting | Description |
| --- | --- |
| Visualization Type | Change the type of visual used to depict the data. |
| Granularity | For trended visualizations, you can change the time granularity (day, week, month, etc.) from this drop-down list. This change also applies to the data source table. |
| Percentages | Displays values in percentages. |
| 100% Stacked | This setting on area stacked, bar stacked or horizontal bar stacked visualizations turns the chart into a "100% stacked" visualization. Example: ![Stacked 100%](assets/stacked_100_percent.png) |
| Legend Visible | Lets you hide the detailed legend text for the Summary Number/Summary Change visualization. |
| Limit Max Items | Lets you limit the number of items that a visualization displays. |
| Anchor Y Axis at Zero | If all the values plotted on the chart are considerably above zero, the chart default will make the bottom of the y-axis NON-ZERO. If you check this box, the y-axis will be forced to zero (and it will re-draw the chart). |
| Normalization | Forces metrics to equal proportions. This is helpful when plotted metrics are of very different magnitudes. |
| Display Dual Axis | Only applies if you have two metrics - you can have a y-axis on the left (for one metric) and on the right (for the other metric). This is helpful when plotted metrics are of very different magnitudes. |
| Show Anomalies | Enhances line graphs and freeform tables by displaying anomaly detection. Anomaly detection in line visualizations includes an expected value (dashed line) and an expected range (shaded band). |

## Legend {#legend}

A visualization legend helps you to relate date in a source table to plotted series in the visualization. The legend is interactive - you can click a legend item to show/hide a series in the visualization. This is helpful if you want to simplify the data being visualized. 

Additionally, you can rename legend labels to help you make visuals more consumable. Note: legend editing does **not** apply to: Treemap, Bullet, Summary Change/Number, Text, Freeform, Histogram, Cohort or Flow visualizations.

To edit a legend label:

1. Right-click one of the legend labels.
1. Click **[!UICONTROL Edit Label]**.

   ![](assets/edit-label.png)

1. Enter the new label text.
1. Press **[!UICONTROL Enter]** to save.

## Right-click menu {#right-click}

Additional functionality for a visualziation is available by right-clicking on the visualization header. Settings will vary by visualization. Some of the settings available are:

![](assets/right-click.png)

| Setting | Description |
| --- | --- |
| Insert Copied Panel/Visualization|Lets you paste ("insert") a copied panel or visualization to another place within the project, or into a completely different project. |
| Copy Visualization | Lets you right-click and copy a visualization, so that you can insert it to another place within the project, or into a completely different project. |
| [Download items as CSV](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/download-send.html?lang=ko&#download-items) | Download up to 50,000 dimension items for the selected dimension as a CSV. |
| [Download data as CSV](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/download-send.html?lang=ko&#download-data) | Download visualization data source as a CSV. |
| Duplicate Visualization | Makes an exact duplicate of the current visualization, which you can then modify. |
| Edit Description | Add (or edit) a text description for the visualization. |
| Get Visualization Link | Lets you direct someone to a specific visualization within a project. When the link is clicked, the recipient will be required to login before being directed to the exact visualization linked to. |
| Start Over | (Works for Flow, Venn, Histogram) Deletes the configuration for the current visualization so you can re-configure it from scratch. |

## Create Visual icon {#quick-viz}

If you are not sure which visualization to pick, click the **[!UICONTROL Create Visual]** icon in any table row (available on hover). This the the fastest way to add a visualization. Clicking it prompts Analysis Workspace to take an educated guess at which visualization would best fit your data. For example, if you have 1 row selected, it will create a trended line graph. If you have 3 segment rows selected, it will create a Venn diagram. 

![](assets/quick-viz.png)

## Change the scale axis on visualizations

Here is a video overview:

>[!VIDEO](https://video.tv.adobe.com/v/30859/?quality=12&captions=kor)

-->
