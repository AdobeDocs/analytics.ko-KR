---
description: 'null'
title: 기여도 분석 실행
uuid: 5282a5f9-0771-4974-93cb-335204bde114
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 기여도 분석 실행

기여도 분석은 Adobe Analytics에서 관찰된 예외 항목에 대한 기여자를 파악하기 위해 고안된 집중적인 기계 학습 프로세스입니다. 사용자가 집중된 영역이나 추가 분석 기회를 다른 경우보다 훨씬 빠르게 찾을 수 있도록 지원하기 위한 것입니다.

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

1. 기여도 분석이 로드되는 동안 기다립니다. 이 작업은 보고서 세트의 크기와 차원 수에 따라 상당한 시간이 걸릴 수 있습니다. 기여도 분석은 차원당 상위 50,000개 항목에 대한 분석을 수행합니다.
1. 그런 다음 분석 작업 공간이 이 프로젝트 내에서 직접 새 기여도 분석 패널을 로드합니다. 이전에 보고 및 분석에서 기여도 분석을 사용한 경우 익숙한 패널이 많이 표시됩니다.

   * 해당 날의 방문 수를 **보여주는** 시각화
   * 컨텍스트에 **대한 월별 방문 트렌드 라인** .
   * **이** 예외 항목에 기여한 상위 항목, [기여도 점수](https://marketing.adobe.com/resources/help/ko_KR/analytics/contribution/ca_contribution_score.html), 해당 지표 및 크기 조정 관점에서 지표를 컨텍스트에 넣는 고유 방문자 수 지표를 표시합니다.

   * 생성된 [세그먼트](https://marketing.adobe.com/resources/help/ko_KR/analytics/contribution/ca_workflow_premium.html) (상위 항목 클러스터) 테이블은 기여도 점수, 예외 항목 발생 및 예외 항목 지표에 기여하는 전체 비율을 기준으로 상위 항목의 연결을 식별합니다. 그러면 대상 세그먼트로 캡처됩니다(기여도 세그먼트 1, 기여도 세그먼트 2 등). &quot;i&quot;(정보) 단추를 클릭하면 각 자동 세그먼트의 정의를 볼 수 있습니다. 여기에는 자동 세그먼트가 구성하는 상위 항목이 포함됩니다.

      ![](assets/auto_segment.png)

1. 기여도 분석은 이제 분석 작업 공간의 일부이므로 표의 마우스 오른쪽 단추 클릭 메뉴에서 여러 기능을 활용하여 다음과 같이 보다 의미 있는 분석을 만들 수 있습니다.

   * [각 차원 항목을 다른 차원으로 분석](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md)
   * [하나 이상의 행에 대한 트렌드 표시](/help/analyze/analysis-workspace/analysis-workspace-features.md#section_34930C967C104C2B9092BA8DCF2BF81A)
   * [새 시각화 추가](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)
   * [경고 만들기 ](/help/components/c-alerts/intellligent-alerts.md)
   * [세그먼트 만들기 또는 비교](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

>[!NOTE] 기여도 분석 내에서 파란색 점이 있는 분석되는 예외 항목과 이 항목에 연결된 지능형 경고 프로젝트를 강조 표시합니다. 이렇게 하면 분석되는 예외 항목이 더 명확히 표시됩니다.

## 기여도 분석에서 차원 제외 {#section_F6932F4BF74544B5872164E7B1E0C6FC}

기여도 분석에서 일부 차원을 제외하려는 경우가 있을 수 있습니다. 예를 들어 브라우저 또는 하드웨어 관련 차원은 전혀 신경 쓰지 않을 수 있으며 이러한 차원을 제거하여 분석 속도를 높이고자 합니다.

1. 라인 차트에서 **[!UICONTROL Run Contribution Analysis]** 또는 **[!UICONTROL Analyze]** 을 클릭하면 **[!UICONTROL Excluded Dimensions]** 패널이 표시됩니다.

1. 원하지 않는 크기를 **[!UICONTROL Excluded Dimensions]** 패널로 드래그한 다음 클릭하여 목록을 저장합니다 **[!UICONTROL Set as Default]**. Or, click **[!UICONTROL Clear All]** to start over with selecting dimensions to exclude.

   ![](assets/exclude_dimensions.png)

1. After you have added dimensions to exclude (or chosen not to), click **[!UICONTROL Run Contribution Analysis]** again.
1. 제외된 차원 목록을 수정해야 하는 경우, 차원을 두 번 클릭하면 제외된 차원 목록이 표시됩니다.

   ![](assets/excluded-dimensions.png)

1. Just delete any unwanted dimensions by clicking the x next to them, then save the list by clicking **[!UICONTROL Set as Default]**.

