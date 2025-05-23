---
description: 알아보기
title: 지표 유형 및 속성
feature: Calculated Metrics
exl-id: 3fb98227-e2ef-4829-ae84-812f845470ee
source-git-commit: 21c4d1b591daf7229bd36845e42e2dec473e792f
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 98%

---

# 지표 유형 및 속성 {#metric-type-attribution}

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


>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_container"
>title="컨테이너"
>abstract="원하는 속성 범위를 설정할 컨테이너를 선택합니다."


>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_lookbackwindow"
>title="전환 확인 기간"
>abstract="이 설정은 각 변환에 적용될 데이터 속성의 기간을 결정합니다."

[계산된 지표 작성](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) 시 지표 유형과 속성 모델을 지정할 수 있습니다.

## 지표 유형

계산된 지표를 작성할 때 지표 유형을 지정하는 방법:

1. 선택하려는 유형의 지표 옆에 있는 톱니바퀴 아이콘을 선택합니다.

   ![](assets/cm_type_alloc.png)

1. 다음 선택 사항 중 하나를 선택합니다.

   | 지표 유형 | 정의 |
   |---|---|
   | 표준 | 이 지표들은 표준 [!DNL Analytics] 보고에서 사용된 것과 동일한 지표입니다. 공식이 하나의 표준 지표로 구성된 경우 계산되지 않은 지표에 해당하는 대응값과 동일한 데이터가 표시됩니다. 표준 지표는 각 개별 라인 항목별로 계산된 지표를 만드는 데 유용합니다. 예를 들어 [주문] / [방문 횟수]는 특정 라인 항목에 대한 주문 수를 그 항목에 대한 방문 횟수로 나눕니다. |
   | 총 합계 | 각 라인 항목에 있는 보고 기간에 대한 총 합계를 사용합니다. 공식이 하나의 총 합계 지표로 구성된 경우 각 라인 항목에서 동일한 합계 숫자가 표시됩니다. 총 합계 지표는 사이트 합계 데이터를 기준으로 비교하는 계산된 지표를 만드는 데 유용합니다. 예를 들어 [주문] / [총 방문 횟수]는 특정 라인 항목에 대한 방문 횟수뿐만 아니라 해당 사이트에 대한 모든 방문 횟수에 대한 주문 수의 비율을 표시합니다. |

## 선형 할당이 작동하는 방식

[기여도 분석](/help/analyze/analysis-workspace/attribution/overview.md)은 계산된 지표에 나타나는 배분 모델을 평가하는 방식입니다.

기본이 아닌 기여도 분석 모델 및 지원되는 전환 확인 기간의 전체 목록에 대해서는 [기여도 분석 모델 및 전환 확인 기간](/help/analyze/analysis-workspace/attribution/models.md)을 참조하십시오.

다음 예제는 선형 할당을 사용하여 계산된 지표가 보고에서 작동되는 방식을 보여 줍니다.

| | 히트 1 | 히트 2 | 히트 3 | 히트 4 | 히트 5 | 히트 6 | 히트 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
| 데이터가 전송됨 | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $10 |
| 마지막 터치 eVar | PROMO A | PROMO A | PROMO A | PROMO B | PROMO B | PROMO C | $10 |
| 첫 번째 터치 eVar | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | $10 |
| 예제 prop | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $10 |

이 예에서 값 A, B, C는 히트 7에서 $10를 구매하기 전에 히트 1, 3, 4, 6에 있는 변수로 전송되었습니다. 두 번째 행에서 그러한 값은 마지막 터치 방문을 기준으로 하여 히트에서 유지됩니다. 세 번째 행은 첫 번째 터치 방문 지속성을 보여 줍니다. 마지막으로, 마지막 행은 지속성이 없는 prop에 대해 데이터가 기록되는 방식을 보여 줍니다.

