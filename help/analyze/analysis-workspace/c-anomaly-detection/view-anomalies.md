---
description: 표 또는 라인 차트에서 예외 항목을 볼 수 있습니다.
title: Analysis Workspace에서 예외 항목 보기
feature: Anomaly Detection
role: User, Admin
exl-id: 32edc7f4-c9b9-472a-b328-246ea5b54d07
source-git-commit: 984406d00e5a5ae966fff60ec9fcfcb000958696
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 97%

---

# Analysis Workspace에서 예외 항목 보기

표 또는 라인 차트에서 예외 항목을 볼 수 있습니다.

## 표에서 예외 항목 보기 {#section_869A87B92B574A38B017A980ED8A29C5}

시계열 자유 형식 테이블에서 예외 항목을 볼 수 있습니다.

1. 열 머리글에서 열 설정 아이콘을 선택한 다음 옵션 목록에서 [!UICONTROL **예외 항목**] 옵션이 선택되었는지 확인합니다. 자세한 내용은 [열 설정](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)을 참조하십시오.

1. 업데이트된 테이블을 보려면 설정 메뉴 밖을 클릭합니다.

   ![](assets/anomaly_detected.png)

1. 예외 항목은 다음과 같이 테이블에 표시됩니다.

   데이터 예외 항목이 탐지되는 각 행의 오른쪽 상단에 **어두운 회색 삼각형**&#x200B;이 나타냅니다.

   각 행에 색상이 지정된 **수직선**&#x200B;은 예상 값을 가리킵니다. 각 행에 색상이 지정된 **음영 처리 영역**&#x200B;은 실제 값을 가리킵니다. 라인(예상 값)과 음영 처리 영역(실제 값)을 비교하여 예외 항목이 있는지 여부를 결정합니다. ([예외 항목 탐지에 사용되는 통계 기법](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md)에 설명된 대로 고급 통계 기법을 기준으로 관찰 내용을 예외적인 것으로 간주합니다.)

1. 예외 항목에 대한 세부 정보를 보려면 행의 오른쪽 상단에 있는 회색 삼각형을 선택합니다. 실제 값이 예상 값보다 위 또는 아래로 벗어나는 정도(백분율로)가 표시됩니다.

## 선 차트에서 예외 항목 보기 {#section_7C1192AFDB4345A8A2CCFB3AE0C47D82}

라인 차트는 예외 항목을 볼 수 있는 유일한 시각화입니다.

라인 차트에서 예외 항목을 보려는 경우:

1. 시각화 머리글에서 열 설정 아이콘을 선택한 다음 옵션 목록에서 [!UICONTROL **예외 항목 표시**] 옵션이 선택되었는지 확인합니다. 자세한 내용은 [라인](/help/analyze/analysis-workspace/visualizations/line.md)을 참조하십시오.

1. (선택 사항) 신뢰 구간에서 차트의 크기를 조절하려면 시각화 머리글에서 설정 아이콘을 선택한 다음 **[!UICONTROL 예외 항목으로 Y축의 크기 조절]** 옵션을 선택합니다.

   때때로 차트를 읽기 어렵게 만들 수 있으므로 이 옵션은 기본적으로 선택하지 않습니다.

1. 업데이트된 라인 차트를 보려면 설정 메뉴 밖을 클릭합니다.

   ![](assets/anomaly_linechart.png)

   예외 항목은 다음과 같이 라인 차트에 표시됩니다.

   데이터 예외 항목이 탐지될 때마다 **흰색 점**&#x200B;이 라인에 나타납니다. ([예외 항목 탐지에 사용되는 통계 기법](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md)에 설명된 대로 고급 통계 기법을 기준으로 관찰 내용을 예외적인 것으로 간주합니다.)

   **밝은 음영 처리 영역**&#x200B;은 값이 발생해야 하는 신뢰 대역 또는 예상 범위입니다. 이 예상 범위를 벗어나는 모든 값은 예외 항목입니다.

   라인 차트에 여러 개의 지표가 있을 경우에는 예외 항목만 표시되고, 사용자는 마우스를 각 예외 항목의 위에 놓아 해당 지표에 대한 신뢰 대역을 확인해야 합니다.

   **점선**&#x200B;은 정확한 예상 값입니다.

1. 예외 항목(흰색 점)을 클릭하면 다음의 정보를 볼 수 있습니다.

   * 예외 항목이 발생한 날짜

   * 예외 항목의 원시 값

   * 녹색 선으로 표시되는 예상 값보다 위 또는 아래 값의 백분율 값

   * 기여도 분석을 시작하는 분석 링크

     (참조: [예외 항목 탐지 개요](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) 을 참조하십시오.)





