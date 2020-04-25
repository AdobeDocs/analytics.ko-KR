---
description: 'null'
title: 기여도 분석 실행
uuid: 5282a5f9-0771-4974-93cb-335204bde114
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 기여도 분석 실행

기여도 분석은 Adobe Analytics에서 관찰된 예외 항목에 기여한 사항을 드러내도록 설계된 집중 기계 학습 프로세스입니다. 이 프로세스의 목적은 사용자가 집중 영역이나 추가 분석 기회를 원래 가능한 것보다 훨씬 더 빨리 찾는 것을 돕는 것입니다. 

## 기여도 분석 실행 {#section_7D2C5E48A5664727941DF4C90976D9DC}

프로젝트에서 기여도 분석을 호출하는 데에는 두 가지 방법이 있습니다.

* In a freeform table with daily granularity, right-click any row and select **[!UICONTROL Run Contribution Analysis]**. 예외 항목을 표시하지 않는 행에서 실행할 수도 있습니다.

   >[!NOTE]
   >
   >현재 Adobe에서는 일별 세부기간만 사용하는 기여도 분석을 지원합니다.

   ![](assets/run_ca.png)

* 라인 차트에서는, 라인 차트의 예외 항목 데이터 포인트 위로 마우스를 가져갑니다. Click the **[!UICONTROL Analyze]** link that appears.

   ![](assets/contribution-analysis.png)

1. (Optional) After you have clicked **[!UICONTROL Run Contribution Analysis]** in either the line chart or a table, you can narrow the scope of (and thus speed up) the analysis by [excluding dimensions](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/run-contribution-analysis.md#section_F6932F4BF74544B5872164E7B1E0C6FC).

1. 기여도 분석이 로드되는 동안 기다려 주십시오. 이 작업은 보고서 세트의 크기와 차원의 수에 따라 상당한 시간이 걸릴 수 있습니다. 기여도 분석에서는 차원당 상위 50,000개의 항목을 분석합니다.
1. 그런 다음 Analysis Workspace에서는 이 프로젝트 내에서 바로 새 기여도 분석 패널을 로드합니다. 전에 Reports &amp; Analytics에서 기여도 분석을 사용한 적이 있다면 익숙한 패널이 많이 표시됩니다.

   * 해당 일의 **방문** 수를 보여 주는 시각화.
   * 컨텍스트에 대한 월별 **방문 횟수 꺾은 선형**.
   * 이 예외 항목에 기여하고, [기여도 점수](https://marketing.adobe.com/resources/help/ko_KR/analytics/contribution/ca_contribution_score.html)와 해당 지표, 고유 방문자 수 지표로 정렬되어 크기 조정 관점의 문맥에서 지표를 적용하기 위한 **상위 항목**.

   * [생성된 세그먼트](https://marketing.adobe.com/resources/help/ko_KR/analytics/contribution/ca_workflow_premium.html)(상위 항목 클러스터) 표는 기여도 점수, 예외 항목 발생 횟수 및 이상 지표에 기여하는 전체적인 비율을 기반으로 상위 항목의 연관성을 식별합니다. 그런 다음 대상 세그먼트로서 캡처됩니다(기여도 세그먼트 1, 기여도 세그먼트 2 등). &quot;i&quot;(정보) 단추를 클릭하면 세그먼트를 구성하는 상위 항목을 포함하여 각 자동 세그먼트의 정의가 표시됩니다. 

      ![](assets/auto_segment.png)

1. 이제 기여도 분석은 Analysis Workspace의 일부이므로 다음과 같이 표의 마우스 오른쪽 단추 클릭 메뉴에 있는 많은 기능을 사용하여 분석을 훨씬 더 의미 있게 할 수 있습니다. 

   * [각 차원 항목을 다른 차원으로 분석](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md)
   * [하나 이상의 행에 대한 트렌드 표시](/help/analyze/analysis-workspace/analysis-workspace-features.md#section_34930C967C104C2B9092BA8DCF2BF81A)
   * [새 시각화 추가](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)
   * [경고 만들기 ](/help/components/c-alerts/intellligent-alerts.md)
   * [세그먼트 만들기 또는 비교](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

>[!NOTE] 기여도 분석 내에서 파란색 점이 있는 분석되는 예외 항목과 이 항목에 연결된 지능형 경고 프로젝트를 강조 표시합니다. 이렇게 하면 분석되는 예외 항목이 더 명확히 표시됩니다.

## 기여도 분석에서 차원 제외 {#section_F6932F4BF74544B5872164E7B1E0C6FC}

기여도 분석에서 일부 차원을 제외하고자 하는 경우가 있을 수 있습니다. 예를 들어, 브라우저 또는 하드웨어와 관련된 차원을 전혀 고려하지 않을 수 있으며, 이를 제거하여 분석 속도를 높이고 싶을 수도 있습니다.

1. 라인 차트에서 **[!UICONTROL Run Contribution Analysis]** 또는 **[!UICONTROL Analyze]** 을 클릭하면 **[!UICONTROL Excluded Dimensions]** 패널이 표시됩니다.

1. 원하지 않는 크기를 **[!UICONTROL Excluded Dimensions]** 패널로 드래그한 다음 클릭하여 목록을 저장합니다 **[!UICONTROL Set as Default]**. Or, click **[!UICONTROL Clear All]** to start over with selecting dimensions to exclude.

   ![](assets/exclude_dimensions.png)

1. After you have added dimensions to exclude (or chosen not to), click **[!UICONTROL Run Contribution Analysis]** again.
1. 제외된 차원 목록을 수정해야 하는 경우, 차원을 두 번 클릭하면 제외된 차원 목록이 표시됩니다.

   ![](assets/excluded-dimensions.png)

1. Just delete any unwanted dimensions by clicking the x next to them, then save the list by clicking **[!UICONTROL Set as Default]**.

