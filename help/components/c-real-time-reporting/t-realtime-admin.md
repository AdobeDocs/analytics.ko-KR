---
description: 실시간 보고서를 설정하는 관리 단계입니다.
solution: Analytics
title: 실시간 보고서 구성
topic: Admin tools
uuid: a2c3c515-55f2-4c64-ac92-a86d75e78a86
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 실시간 보고서 구성

실시간 보고서를 설정하는 관리 단계입니다.

Setting up real-time reports within [!UICONTROL Reports &amp; Analytics] consists of selecting the report suite and configuring up to 3 reports for it.

1. 실시간 보고서를 활성화할 보고서 세트를 선택합니다.

   Navigate to **[!UICONTROL Analytics]** &gt; **[!UICONTROL Reports]** &gt; **[!UICONTROL View All Reports &gt; Site Metrics]** &gt; **[!UICONTROL Real-Time]** and select the report suite from the drop-down at the top:

   ![](assets/report_suite_selector.png)

   실시간 보고에 대해 설정되지 않은 보고서 세트에 대한 실시간 보고서를 보려고 하면 보고서 세트를 설정할 수 있다는 메시지가 표시됩니다.

   ![](assets/rep_suite_not_set_up.png)

1. Click **[!UICONTROL Configure]** (gear icon) to run the [!UICONTROL Report Suite Manager].

   (Also available under **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin &gt; Report Suites]** &gt; **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Real-Time]**.)

1. Turn on the **[!UICONTROL Enable Real-Time]** setting.
1. 최대 3개의 보고서(보고서당 지표 한 개와 측정기준 또는 분류 세 개가 있음)에 대한 실시간 데이터 수집을 설정합니다.

   ![](assets/real_time_admin.png)

   지원되는 실시간 지표 및 차원에 대한 자세한 내용은 지원되는 지표 [및 차원을 참조하십시오](/help/components/c-real-time-reporting/realtime-metrics.md).

   분류를 생성한 경우, 분류가 정의된 측정기준 아래에 분류가 들여 써진 채로 표시됩니다.

   ![](assets/classifications.png)

   >[!NOTE]
   >
   >단일 실시간 보고서의 경우 각 차원에 대해 다른 분류를 선택하더라도 현재 중복 차원 활성화를 지원하지 않습니다.

   분류에 대한 자세한 내용은 분류 [정보를 참조하십시오](/help/components/c-classifications2/c-classifications.md).

   >[!NOTE]
   >
   >"Search Keyword" 또는 "Product"와 같은 일부 차원은 Adobe Analytics의 다른 곳에서 지속되는 것과 같이 실시간으로 지속되지 않습니다. 지속되지 않는 지표를 선택하면 다음 경고가 표시됩니다.

   ![](assets/warning_dimensions.png)

1. Click **[!UICONTROL Save]** or **[!UICONTROL Save and View Report]**.

   이 초기 보고서 설정 후 데이터 스트리밍이 시작되는 데에는 최대 20까지 소요될 수 있습니다. 그때부터는 데이터를 즉시 사용할 수 있습니다. 실시간 보고서 보기에 대한 자세한 내용은 [실시간 보고서 실행](https://marketing.adobe.com/resources/help/en_US/sc/user/reports_realtime.html)을 참조하십시오.

1. 기본적으로 실시간 보고서에 대한 액세스 권한은 모든 사용자에게 있습니다.
