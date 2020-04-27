---
description: 지표 및 차원을 요청에 추가하는 절차.
title: 지표 및 차원 추가
topic: Report builder
uuid: 588ce96b-3a2d-42b7-8a8e-7e6f448a0115
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 지표 및 차원 추가

지표 및 차원을 요청에 추가하는 절차.

1. [에서 데이터 요청을](/help/analyze/report-builder/data-requests/data-requests.md) 만든 [!UICONTROL Request Wizard: Step 1]다음 을 클릭합니다 **[!UICONTROL Next]**.
1. On the [!UICONTROL Request Wizard: Step 2], double-click metrics, or drag them to the desired position.

   ![단계 정보](assets/adding_metrics.png)

   When you add metrics, they are not removed from the [!UICONTROL Metrics] tab, because you can display metrics multiple times within a request. 예를 들어, 각 값 이외에도 지표 소계를 표시할 수 있습니다. 하지만 사용할 수 있는 지표 목록은 차원을 추가 또는 제거할 때마다 달라집니다.

   You can add only metrics to the [!UICONTROL Metrics] layout section. 지표는 [!UICONTROL Column Label] 레이아웃에 a로 추가됩니다 [!UICONTROL Metric Header]. If you move a [!UICONTROL Metric Header] from [!UICONTROL Column Layout] to [!UICONTROL Row Layout], it is displayed there and is used as a metric as a breakdown.

   검색 창은 지표 목록 바로 위 지표 탭에 표시됩니다.

   ![](assets/search_bar_metric.png)

   다음 사항에 주의하십시오.

   * 검색어를 입력하면 목록이 자동으로 업데이트되어 레이블이 검색어와 일치하는 지표만 표시합니다.
   * 일치 항목은 대/소문자를 구분하지 않으며 검색어를 포함하는 값을 검색합니다.
   * 전체 단어 검색, 또는 다른 특수 검색 플래그(다음으로 시작, 다음으로 끝남, AND, OR 등)는 지원되지 않습니다.

      요청 마법사를 종료하거나(즉, [마침] 또는 [취소]를 클릭하면) 요청 마법사 1단계로 돌아가거나 또는 지표 카테고리를 변경하면 검색어가 지워집니다.

      다음의 경우에는 검색어가 지워지지 않습니다.

   * 목록에서 지표 항목 중 하나를 끌어다 놓아서(또는 두 번 클릭해서) [피벗 레이아웃/사용자 지정 레이아웃 지표] 패널에 추가하는 경우.
   * [피벗 레이아웃/사용자 지정 레이아웃 지표] 패널에서 지표 항목을 제거하는 경우.
   * [차원] 탭을 클릭한 다음 [지표] 탭으로 돌아오는 경우.
   * 종료 시 바로 요청 마법사 2단계로 돌아가는 다른 하위 양식(양식 또는 모드 없음)을 호출하는 경우. 이러한 양식의 예는 다음과 같습니다.

      * 차원 필터 양식
      * 날짜 범위 형식 양식
      * 형식 옵션 양식
      * 텍스트 앞에/뒤에 추가 양식
      * 출력 범위 위치 양식

1. (선택 사항) 지표별로 요청을 정렬하려면 지표 레이블을 클릭하면 됩니다.
1. 지표를 추가하는 것과 같은 방식으로 차원을 추가합니다.

On the [!UICONTROL Dimensions] tab, the system displays dimensions that break down or are a classification of any base report you select on Step 1, and on the configuration of the report suite. 차원을 레이아웃 격자에 놓으면 트리 보기에서 차원이 제거되고 사용할 수 있는 남은 차원의 목록이 다시 계산됩니다.

The [!UICONTROL Date] dimension is added automatically. Available date dimensions change depending on the selected granularity from the [!UICONTROL Request Wizard: Step 1]. (유효한 값:

    * 시간
    * 일
    * 주
    * 월
    * 년
    * 날짜 범위(세부기간이 지정되지 않은 경우)

1. [서식 선택 사항](/help/analyze/report-builder/layout/t-format-display-headers.md) 및 필터를 구성하여 지표 및 차원을 수정합니다.
1. 클릭 **[!UICONTROL Finish]**.
In the following example, dimensions relate to the [!UICONTROL Page] metric. 여기에서, [!UICONTROL Referring Domain] 차원은 [!UICONTROL Page] 및 [!UICONTROL Referring Domain]사이에 분류 보고서를 만듭니다. The [!UICONTROL Dimension] tab is updated with only dimensions that you can add to a breakdown report.

![](assets/page_pageview_02.png)
