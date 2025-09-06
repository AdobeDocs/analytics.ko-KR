---
description: 기여도 지표를 만드는 방법을 알아봅니다.
title: 참여도 지표
feature: Calculated Metrics
exl-id: bef185d6-72c0-4068-80f8-57261369573f
source-git-commit: 665319bdfc4c1599292c2e7aea45622d77a291a7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 2%

---

# 참여도 지표


기여도 지표는 차원(예: 페이지 보기 수)에 대한 개별 값이 특정 지표(예: 주문 수)를 포함하는 방문에 기여하거나 참여하는 방식을 수량화하는 데 사용됩니다.

아래 단계는 기여도 지표를 만드는 방법을 보여 줍니다.

1. [계산된 지표를 만듭니다](../cm-workflow.md). [계산된 지표 빌더](cm-build-metrics.md)에서 지표 이름을 `Orders (Visit Participation)` 또는 이와 유사하게 지정합니다.
1. 성공 이벤트(예: [!DNL Online Orders])가 포함된 지표를 [!UICONTROL **[!UICONTROL 정의]**] 영역으로 끌어서 놓습니다.
1. 지표에 대해 ![톱니바퀴](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg)를 선택합니다.
1. 표시되는 팝업에서 **[!UICONTROL 기본값이 아닌 속성 모델 사용]**&#x200B;을 선택하여 해당 이벤트의 [속성 모델](m-metric-type-alloc.md#attribution-models)을(를) **[!UICONTROL 참여]**&#x200B;에 정의하고 **[!UICONTROL 컨테이너]**&#x200B;에 대해 [!UICONTROL 방문]을(를) 선택합니다. **[!UICONTROL 적용]**&#x200B;을 선택하여 확인하십시오.


   ![기여도를 모델로 선택하고 방문을 컨테이너로 선택한 것을 표시하는 열 속성 모델 팝업입니다.](assets/participation-setup.png)

   **(파티션|방문|30일)**&#x200B;이(가) 지표 구성 요소 이름에 추가되었습니다.



1. 지표를 저장하려면 [!UICONTROL **저장**]&#x200B;을 선택하십시오.
1. 보고서에서 계산된 지표를 사용합니다. 예를 들어 보고서에 계산된 [!DNL Orders (Session Participation)] 지표를 사용하여 주문이 포함된 세션에 기여한(또는 참여한) 고객 계층을 표시합니다.

   ![고객 계층 및 주문을 표시하는 자유 형식 테이블입니다.](assets/participation-pages-customer-tier.png)


<!--

The following information explains how to create a metric that shows which pages contributed to (or participated in) visits that contained an order.

This type of information could be useful for any content owner.

>[!NOTE]
>
>You can enable participation metrics in the Admin Tools, but only for custom events 1 - 100.

1. Begin creating a calculated metric, as described in [Build metrics](/help/components/calculated-metrics/workflow/c-build-metrics/cm-build-metrics.md).

1. In the Calculated metrics builder, name the metric "Participation".

1. Drag the success event "Orders" into the Definition canvas.

1. Change the [attribution model](/help/components/calculated-metrics/workflow/c-build-metrics/m-metric-type-alloc.md) of that event to **[!UICONTROL Participation]** under the **[!UICONTROL Settings]** gear. Select **[!UICONTROL Visit]** lookback. The definition should look similar to this:

   ![](assets/participation.png)

1. Select [!UICONTROL **Save**] to save the metric.

1. Use the calculated metric in a **[!UICONTROL Pages]** report.

    ![](assets/participation-pages.png)

1. (Optional) Share the metric with other users in your organization, as described in [Share calculated metrics](/help/components/calculated-metrics/workflow/cm-sharing.md).
-->