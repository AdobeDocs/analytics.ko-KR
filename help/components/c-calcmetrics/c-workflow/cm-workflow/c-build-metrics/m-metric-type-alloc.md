---
description: 알아보기
title: 지표 유형 및 속성
feature: Calculated Metrics
exl-id: 3fb98227-e2ef-4829-ae84-812f845470ee
source-git-commit: 07590d00341f9016ee0728970483e77cb8d38a9d
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 77%

---

# 지표 유형 및 속성 {#metric-type-attribution}

계산된 지표 정의에서 지표의 지표 유형과 [속성 모델](#attribution-models)을 구성할 수 있습니다.

1. 지표 구성 요소에서 ![설정](/help/assets/icons/Setting.svg)을 선택합니다.
1. 팝업 대화 상자에서:

   ![지표 유형 및 속성](assets/cm-type-alloc.png)

   * **[!UICONTROL 지표 유형]**&#x200B;을 지정합니다.

     | 지표 유형 | 정의 |
     |---|---|
     | **[!UICONTROL 표준]** | 공식이 하나의 표준 지표로 구성된 경우 계산되지 않은 지표에 해당하는 대응값과 동일한 데이터가 표시됩니다. 표준 지표는 각 개별 라인 항목별로 계산된 지표를 만드는 데 유용합니다. <p>예를 들어, ![이벤트](/help/assets/icons/Event.svg) **[!UICONTROL 주문]** ![나누기](/help/assets/icons/Divide.svg) ![이벤트](/help/assets/icons/Event.svg) **[!UICONTROL 방문]**&#x200B;은(는) 특정 라인 항목에 대한 주문 수를 특정 라인 항목에 대한 방문 횟수로 나눕니다. |
     | **[!UICONTROL 총 합계]** | 각 라인 항목에 있는 보고 기간에 대한 **[!UICONTROL 총 합계]**&#x200B;를 사용합니다. 수식에 단일 총 합계 지표가 포함된 경우 계산된 지표는 모든 라인 항목에 동일한 총 합계를 표시합니다. 총 합계 지표는 사이트 합계 데이터를 기준으로 비교하는 계산된 지표를 만들고자 할 때 유용합니다. <p>예를 들어, ![이벤트](/help/assets/icons/Event.svg) **[!UICONTROL 주문]** ![나누기](/help/assets/icons/Divide.svg) ![이벤트](/help/assets/icons/Event.svg) **[!UICONTROL 총 방문]**&#x200B;은(는) 특정 라인 항목에 대한 방문 횟수뿐만 아니라 모든 방문 횟수에 대한 주문 수의 비율을 표시합니다. 이 예에서는 계산된 지표에서 ![이벤트](/help/assets/icons/Event.svg) **[!UICONTROL 방문]** 지표에 대해 **[!UICONTROL 총계]**&#x200B;를 지정합니다. 그러면 자동으로 ![이벤트](/help/assets/icons/Event.svg) **[!UICONTROL 총 방문]**&#x200B;이 됩니다. |

   * **[!UICONTROL 속성]**&#x200B;을 지정합니다.

      1. 다음과 같은 작업을 수행할 수 있습니다.

         * **[!UICONTROL 비기본 속성 모델 사용]**&#x200B;을 비활성화하여 30일의 전환 확인 기간이 있는 마지막 터치의 기본 열 속성 모델을 사용합니다.
         * **[!UICONTROL 비기본 속성 모델 사용]**&#x200B;을 활성화합니다. **[!UICONTROL 열 속성 모델]** 대화 상자에서

            * [속성 모델](#attribution-models)에서 **[!UICONTROL 모델]**&#x200B;을(를) 선택하십시오.
            * [컨테이너](#container) 옵션에서 **[!UICONTROL 컨테이너]**&#x200B;을(를) 선택하십시오.
            * [전환 확인 기간](#lookback-window) 옵션에서 **[!UICONTROL 전환 확인 기간]**&#x200B;을 선택합니다. **[!UICONTROL 사용자 지정 시간]**&#x200B;을(를) 선택하는 경우 최대 **[!UICONTROL 분기]**&#x200B;까지 **[!UICONTROL 분]**&#x200B;으로 기간을 정의할 수 있습니다.

      1. 비기본 속성 모델을 적용하려면 **[!UICONTROL 적용]**&#x200B;을 선택합니다. 취소하려면 취소를 선택합니다.

     비기본 속성 모델을 이미 정의한 경우 **[!UICONTROL 편집]**&#x200B;을 선택해 선택 항목을 수정합니다.

속성 모델, 컨테이너 및 전환 확인 기간을 사용하는 방법에 대한 예는 [예](#example)를 참조하십시오.


## 속성 모델 {#attribution-models}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_nondefaultattributionmodel"
>title="비기본 속성 모델 사용"
>abstract="선택한 지표에 기본이 아닌 속성 모델을 사용합니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attributionmodel"
>title="모델"
>abstract="지표에 대한 속성 모델을 선택합니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_lasttouch"
>title="마지막 터치"
>abstract="100%의 크레딧이 방문자가 본 마지막 차원 값으로 이동합니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_firsttouch"
>title="첫 번째 터치"
>abstract="100%의 크레딧이 방문자가 본 첫 번째 차원 값으로 이동합니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_linear"
>title="선형"
>abstract="크레딧이 모든 차원 값에 고르게 분산됩니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_participation"
>title="기여도"
>abstract="100%의 크레딧이 방문자가 본 모든 차원 값으로 이동합니다<br/>열 합계가 과대 평가됩니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_sametouch"
>title="동일한 터치"
>abstract="전환과 동일한 이벤트에 발생하는 차원 값에만 크레딧이 제공됩니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_instance"
>title="동일한 터치"
>abstract="전환과 동일한 이벤트에 발생하는 차원 값에만 크레딧이 제공됩니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_ushaped"
>title="U자형"
>abstract="첫 번째 차원 값이 40%의 크레딧, 마지막 차원 값이 40%의 크레딧을 차지하고 나머지 20%의 크레딧은 중간 차원 값에서 공유합니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_jcurve"
>title="J 곡선"
>abstract="마지막 차원 값이 60%의 크레딧, 첫 번째 차원 값이 20%의 크레딧을 차지하고 나머지 20%의 크레딧은 중간 차원 값에서 공유합니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_jshaped"
>title="J 곡선"
>abstract="마지막 차원 값이 60%의 크레딧, 첫 번째 차원 값이 20%의 크레딧을 차지하고 나머지 20%의 크레딧은 중간 차원 값에서 공유합니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_inversej"
>title="J의 역"
>abstract="첫 번째 차원 값이 60%의 크레딧, 마지막 차원 값이 20%의 크레딧을 차지하고 나머지 20%의 크레딧은 중간 차원 값에서 공유합니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_reversejshaped"
>title="J의 역"
>abstract="첫 번째 차원 값이 60%의 크레딧, 마지막 차원 값이 20%의 크레딧을 차지하고 나머지 20%의 크레딧은 중간 차원 값에서 공유합니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_timedecay"
>title="시간 감소"
>abstract="시간적으로 변환에 가장 가까운 차원 값에 가장 많은 크레딧이 제공됩니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_custom"
>title="사용자 정의"
>abstract="고유한 위치 기반 속성 가중치를 정의합니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_positionbased"
>title="사용자 정의"
>abstract="고유한 위치 기반 속성 가중치를 정의합니다."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_algorithmic"
>title="알고리즘"
>abstract="크레딧은 통계적 알고리즘에 따라 동적으로 결정합니다."

{{attribution-models-details}}


## 컨테이너 {#container}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_container"
>title="컨테이너"
>abstract="원하는 기여도 범위를 설정하려면 컨테이너를 선택하십시오."

{{attribution-container}}


## 전환 확인 기간 {#lookback-winwow}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_lookbackwindow"
>title="전환 확인 기간"
>abstract="이 설정은 각 변환에 적용될 데이터 속성의 기간을 결정합니다."

{{attribution-lookback-window}}

## 예

{{attribution-example}}


<!--
When [building a calculated metric](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md), you can specify the metric type and the attribution model.

## Metric type

To specify the metric type when building a calculated metric:

1. Select the gear icon next to the metric whose type you want to select.

   ![](assets/cm-type-alloc.png) 

1. Choose from the following options:

   |  Metric Type  | Definition  |
   |---|---|
   |  Standard  | These metrics are the same metrics used in standard [!DNL Analytics] reporting. If a formula consisted of a single standard metric, it displays identical data to its non-calculated-metric counterpart. Standard metrics are useful for creating calculated metrics specific to each individual line item. For example, [Orders] / [Visits] takes orders for that specific line item and divides it by the number of visits for that specific line item.  |
   |  Grand total  | Use Grand total for the reporting period in every line item. If a formula consisted of a single Grand total metric, it displays the same total number on every line item. Grand total metrics are useful for creating calculated metrics that compare against site total data. For example, [Orders] / [Total Visits] shows the proportion of orders against ALL visits to your site, not just the visits to the specific line item.  |

## How linear allocation works

[Attribution](/help/analyze/analysis-workspace/attribution/overview.md) is how allocation models in calculated metrics are evaluated.

For a full list of non-default attribution models and lookback windows supported, see [Attribution models and lookback windows](/help/analyze/analysis-workspace/attribution/models.md).

The following example illustrates how calculated metrics with linear allocations work in reporting: 

| | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Hit 5 | Hit 6 | Hit 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
|Data Sent In|PROMO A|-|PROMO A|PROMO B|-|PROMO C|$10|
|Last Touch eVar|PROMO A|PROMO A|PROMO A|PROMO B|PROMO B|PROMO C|$10|
|First Touch eVar|PROMO A|PROMO A|PROMO A|PROMO A|PROMO A|PROMO A|$10|
|Example prop|PROMO A|-|PROMO A|PROMO B|-|PROMO C|$10|

In this example, the values A, B, and C were sent into a variable on hits 1, 3, 4, and 6 before a $10 purchase was made on hit 7. In the second row, those values persist across hits on a last touch visit basis. The third row illustrates a first-touch visit persistence. Finally, the last row illustrates how data would be recorded for a prop which does not have persistence.

-->