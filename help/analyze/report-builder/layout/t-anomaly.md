---
description: Report Builder에서 예외 항목 탐지 요청을 만드는 방법을 알아봅니다.
title: 예외 항목 탐지 요청을 구성하는 방법
uuid: 1e504ff9-df88-4fa7-95ea-1ca05a6f9c0d
feature: Report Builder
role: User, Admin
exl-id: 0a8b1971-8d32-424a-9d41-d7ab2af54d1e
source-git-commit: 2eff7656741bdba3d5d7d1f33e9261b59f8e6083
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 72%

---

# 예외 항목 탐지 요청 구성

Report Builder에서 예외 항목 탐지 요청을 만들려면:

1. **[!UICONTROL 사이트 지표]** > **[!UICONTROL 트래픽]** 보고서 등과 같이 트렌드 보고서를 선택합니다.
1. [!UICONTROL 세부기간 적용] 메뉴에서 **[!UICONTROL 일]**&#x200B;을 선택합니다.

   >[!NOTE]
   >
   >[!UICONTROL 예외 항목 탐지] 메뉴는 일 세부기간을 선택하는 경우에만 사용할 수 있습니다. 선택하는 날짜 범위와 관계없이 통계 데이터 교육 기간으로 이전 30일의 데이터가 사용됩니다.

1. 날짜 범위 구성 후 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   요청 마법사: 2/2단계에서 **[!UICONTROL 방문 횟수]** 등의 지표를 추가합니다.

   추가된 지표를 확인하려면 **[!UICONTROL 없음]** 링크를 클릭합니다.

   ![예외 항목 탐지 와 삽입 을 차례로 보여 주고 하한값과 상한값과 예상값의 삽입 옵션을 보여 주는 스크린샷입니다.](assets/anomaly_select.png)

1. **[!UICONTROL 예외 항목 탐지]** > **[!UICONTROL `<selection>`]**&#x200B;를 선택합니다.

   ![요청 마법사 2단계 - 트래픽 보고서를 보여 주는 스크린샷입니다.](assets/anomaly_visit.png)

   이러한 옵션 중 하나를 선택하면 원래 지표의 예외 항목 탐지 복사본이 만들어집니다. 예를 들어 방문 지표의 경우 하한 방문 지표가 [!UICONTROL 지표] 그룹에 추가됩니다.
1. **[!UICONTROL 마침]**&#x200B;을 클릭하고 Excel에 출력할 셀을 선택합니다.

   [예외 항목 탐지](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md)에서 정의를 참조하십시오.
