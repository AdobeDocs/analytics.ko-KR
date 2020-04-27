---
description: 리포트 빌더에서 예외 항목 탐지 요청을 만드는 방법을 설명하는 단계
title: 예외 항목 탐지 요청 구성
topic: Report builder
uuid: 1e504ff9-df88-4fa7-95ea-1ca05a6f9c0d
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 예외 항목 탐지 요청 구성

Report Builder에서 예외 항목 탐지 요청을 만드는 방법을 설명하는 단계

1. > 보고서와 같은 트렌드 보고서를 **[!UICONTROL Site Metrics]** 선택합니다 **[!UICONTROL Traffic]** .
1. 메뉴에서 [!UICONTROL Apply Granularity] 을 선택합니다 **[!UICONTROL Day]**.

   >[!NOTE]
   >
   >The [!UICONTROL Anomaly Detection] menu is available only when you select Day granularity. 선택하는 날짜 범위와 관계없이 통계 데이터 교육 기간으로 이전 30일의 데이터가 사용됩니다.

1. After configuring date ranges, click **[!UICONTROL Next]**.

   단계 결과 1. On the Request Wizard: Step 2 of 2, add a metric, such as **[!UICONTROL Visits]**.

   단계 결과 1. For the added metric, click the **[!UICONTROL None]** link.

   ![단계 결과](assets/anomaly_select.png)

1. 선택 **[!UICONTROL Anomaly Detection]** > **[!UICONTROL `<selection>`]**.

   ![단계 정보](assets/anomaly_visit.png)

   이러한 옵션 중 하나를 선택하면 원래 지표의 예외 항목 탐지 복사본이 만들어집니다. For example, for the Visit metric, a Lower Bound Visit metric is added to the [!UICONTROL Metric] group.
1. Click **[!UICONTROL Finish]** and select the cell for output to Excel.

   [예외 항목 탐지](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md)에서 정의를 참조하십시오.
