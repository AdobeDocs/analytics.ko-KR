---
description: 리포트 빌더에서 예외 항목 탐지 요청을 만드는 방법을 설명하는 단계
solution: Analytics
title: 예외 항목 탐지 요청 구성
topic: Report builder
uuid: 1e504ff9-df88-4fa7-95ea-1ca05a6f9c0d
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 예외 항목 탐지 요청 구성

Report Builder에서 예외 항목 탐지 요청을 만드는 방법을 설명하는 단계

1. **사이트 지표** &gt; **[!UICONTROL 트래픽]** 보고서 등과 같이 트렌드 보고서를 선택합니다.
1. In the [!UICONTROL Apply Granularity] menu, select **[!UICONTROL Day]**.

   >[!NOTE]
   >
   >The [!UICONTROL Anomaly Detection] menu is available only when you select Day granularity. 선택하는 날짜 범위에 관계없이 통계 데이터 교육 기간으로 이전 30일의 데이터가 사용됩니다.

1. After configuring date ranges, click **[!UICONTROL Next]**.

   단계 결과 1. On the Request Wizard: Step 2 of 2, add a metric, such as **[!UICONTROL Visits]**.

   단계 결과 1. For the added metric, click the **[!UICONTROL None]** link.

   ![단계 결과](assets/anomaly_select.png)

1. Select **[!UICONTROL Anomaly Detection]** &gt; **[!UICONTROL `<selection>`]**.

   ![단계 정보](assets/anomaly_visit.png)

   이러한 옵션 중 하나를 선택하면 원래 지표의 예외 항목 탐지 복사본이 만들어집니다. 예를 들어 방문 지표의 경우 하한 방문 지표가 [!UICONTROL 지표] 그룹에 추가됩니다.
1. Click **[!UICONTROL Finish]** and select the cell for output to Excel.

   See [Anomaly Detection](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) for definitions.
