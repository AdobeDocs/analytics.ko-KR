---
description: 지난 달, 지난 해 등에 대한 비교 작성과 같은 Analysis Workspace의 비교 데이터를 쉽게 시각화할 수 있습니다.
title: 콤보 차트 시각화
feature: Visualizations
role: User, Admin
source-git-commit: 04a314e93a77ecf5687e771e143bf68ba911b32b
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 7%

---


# 콤보 차트

>[!NOTE]
>
>이 기능은 현재 [제한적인 테스트](/help/release-notes/releases.md)가 실시되고 있습니다.

다음 [!UICONTROL 콤보 차트] 시각화를 사용하면 먼저 테이블을 작성하지 않고도 비교 시각화를 빠르게 작성할 수 있습니다. 데이터의 트렌드를 라인/막대 조합으로 쉽게 볼 수 있습니다.

콤보 차트를 사용하여 다음을 수행합니다

* 몇 번의 클릭만으로 이번 주의 주문을 지난 달(및 작년)의 주문과 비교할 수 있습니다.

* 여러 지표(예: [!UICONTROL 고유 방문자 수] 및 [!UICONTROL 매출])을 동일한 차트에서 서로 비교합니다.

* 함수에 대해 지표 분석(예: [!UICONTROL 누적 평균])을 선택할 수 있습니다.

## 콤보 차트 작성

1. 왼쪽 레일의 시각화 드롭다운 목록에서 [!UICONTROL 콤보 차트] 시각화를 빈 패널로 이동합니다.

   ![](assets/combo-chart-build.png)

1. 드롭다운 목록에서 X축에 대한 차원 및 Y축에 대한 지표를 선택합니다.

1. 유형 선택 [!UICONTROL 선 비교] 를 사용하려고 합니다.

   | 선 비교 유형 | 정의 |
   | --- | --- |
   | 기간 | 가장 일반적인 비교 유형 - 이 기간을 4주 전에 비교하는 예를 들어, 기간 을 선택한 경우 비교할 기간을 기준으로 보조 선택을 수행합니다.<p>![](assets/combo-time-period.png) |
   | 추가 지표 | 예를 들어 다음과 같은 방법으로 비교할 수 있습니다 [!UICONTROL 매출] 다른 지표에 추가 |
   | 함수로 플러그인 호출 | 다음과 같은 기능을 도입할 수 있습니다 [!UICONTROL 평균] 를 비교로 볼 수 있습니다. |

1. **[!UICONTROL 빌드]**&#x200B;를 클릭합니다.

   출력은 다음과 비슷합니다.

   ![](assets/combo-output.png)





