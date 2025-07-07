---
description: Analysis Workspace 내에서 데이터 예외 항목을 보고 분석하는 방법을 이해합니다.
title: 예외 항목 보기
feature: Anomaly Detection
role: User, Admin
exl-id: 32edc7f4-c9b9-472a-b328-246ea5b54d07
source-git-commit: b4c1636bdc9d5be522b16f945a46beabf4f7a733
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 49%

---

# 예외 항목 보기

Analysis Workspace의 예외 항목을 표 또는 선 차트로 볼 수 있습니다.

## 테이블에서 예외 항목 보기 {#section_869A87B92B574A38B017A980ED8A29C5}

시계열 자유 형식 테이블에서 예외 항목을 볼 수 있습니다.

1. 열 헤더에서 ![설정](/help/assets/icons/Setting.svg)을 선택한 다음 옵션 목록에서 **[!UICONTROL 예외 항목]** 옵션이 선택되어 있는지 확인하십시오. 자세한 내용은 [열 설정](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)을 참조하십시오.

1. 예외 항목은 다음과 같이 테이블에 표시됩니다.

   ![예외 항목이 검색됨](assets/anomaly-detected.png)

   데이터 예외 항목이 감지된 각 행의 오른쪽 위 모서리에 ◥이(가) 나타납니다.

   각 행 **의**&#x200B;색 세로 선➋은(는) 예상 값을 나타냅니다. 각 행 **의**&#x200B;색 음영 영역➊은(는) 실제 값을 나타냅니다. 라인(예상 값)과 음영 처리 영역(실제 값)을 비교하여 예외 항목이 있는지 여부를 결정합니다. (관찰은 [예외 항목 탐지에 사용된 통계 기법](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md)에 설명된 고급 통계 기법을 기반으로 예외적인 것으로 간주됩니다.)

1. 예외 항목에 대한 세부 정보를 보려면 행의 오른쪽 상단 모서리에서 ◥을(를) 선택하십시오. 실제 값이 예상 값보다 위 또는 아래로 벗어나는 정도(백분율로)가 표시됩니다.
1. 기여도 분석을 시작하려면 [기여도 분석 열기](run-contribution-analysis.md)를 선택하십시오.

## 선 차트에서 예외 항목 보기

라인 차트는 예외 항목을 볼 수 있는 유일한 시각화입니다.

라인 차트에서 예외 항목을 보려는 경우:

1. 시각화 헤더에서 ![설정](/help/assets/icons/Setting.svg)을 선택한 다음 옵션 목록에서 [!UICONTROL **예외 항목 표시**] 옵션이 선택되어 있는지 확인하십시오. 자세한 내용은 [라인](/help/analyze/analysis-workspace/visualizations/line.md)을 참조하십시오.

1. (선택 사항) 신뢰 구간에서 차트의 크기를 조절하려면 시각화 헤더에서 ![설정](/help/assets/icons/Setting.svg)을 선택한 다음 **[!UICONTROL 예외 항목이 Y축의 크기 조절을 허용하도록]** 옵션을 선택합니다.

   때때로 차트를 읽기 어렵게 만들 수 있으므로 이 옵션은 기본적으로 선택하지 않습니다.

   예외 항목은 다음과 같이 라인 차트에 표시됩니다.

   ![예외 항목이 선 시각화를 검색함](assets/anomaly-detected-line.gif)

   데이터 예외 항목이 탐지될 때마다 **흰색 점**&#x200B;이 라인에 나타납니다. (관찰은 [예외 항목 탐지에 사용된 통계 기법](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md)에 설명된 고급 통계 기법을 기반으로 예외적인 것으로 간주됩니다.)

   **밝은 음영 처리 영역**&#x200B;은 값이 발생해야 하는 신뢰 대역 또는 예상 범위입니다. 이 예상 범위를 벗어나는 모든 값은 예외 항목입니다.

   라인 차트에 여러 개의 지표가 있을 경우에는 예외 항목만 표시되고, 사용자는 마우스를 각 예외 항목의 위에 놓아 해당 지표에 대한 신뢰 대역을 확인해야 합니다.

   **점선**&#x200B;은 정확한 예상 값입니다.

1. 예외 항목(흰색 점)을 선택하여 다음 정보를 확인합니다.

   * 예외 항목이 발생한 날짜입니다.

   * 예외 항목의 원시 값.

   * 녹색 선으로 표시되는 예상 값보다 위 또는 아래 값의 백분율 값

   * 기여도 분석을 시작하는 **[!UICONTROL 분석]** 링크






