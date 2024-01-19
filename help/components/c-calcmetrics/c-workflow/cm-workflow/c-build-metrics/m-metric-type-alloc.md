---
description: 알아보기
title: 지표 유형 및 속성
feature: Calculated Metrics
exl-id: 3fb98227-e2ef-4829-ae84-812f845470ee
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 69%

---

# 지표 유형 및 속성

날짜 [계산된 지표 작성](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md), 지표 유형 및 속성 모델을 지정할 수 있습니다.

## 지표 유형

계산된 지표를 작성할 때 지표 유형을 지정하려면 다음을 수행하십시오.

1. 유형을 선택하려는 지표 옆에 있는 톱니바퀴 아이콘을 선택합니다.

   ![](assets/cm_type_alloc.png)

1. 다음 선택 사항 중 하나를 선택합니다.

   | 지표 유형 | 정의 |
   |---|---|
   | 표준 | 이 지표들은 표준 [!DNL Analytics] 보고에서 사용된 것과 동일한 지표입니다. 공식이 하나의 표준 지표로 구성된 경우 계산되지 않은 지표에 해당하는 대응값과 동일한 데이터가 표시됩니다. 표준 지표는 각 개별 라인 항목별로 계산된 지표를 만드는 데 유용합니다. 예를 들어 [주문] / [방문 횟수]는 특정 라인 항목에 대한 주문 수를 그 항목에 대한 방문 횟수로 나눕니다. |
   | 총계 | 모든 라인 항목에서 보고 기간에 총계를 사용합니다. 공식이 단일 총계 지표로 구성된 경우 모든 라인 항목에 동일한 총 수를 표시합니다. 총계 지표는 사이트 총계 데이터와 비교하는 계산된 지표를 만드는 데 유용합니다. 예를 들어 [주문] / [총 방문 횟수]는 특정 라인 항목에 대한 방문 횟수뿐만 아니라 해당 사이트에 대한 모든 방문 횟수에 대한 주문 수의 비율을 표시합니다. |

## 선형 할당 작동 방식

[속성](/help/analyze/analysis-workspace/attribution/overview.md) 은 계산된 지표의 할당 모델을 평가하는 방법입니다.

기본이 아닌 기여도 분석 모델 및 지원되는 전환 확인 기간의 전체 목록에 대해서는 [기여도 분석 모델 및 전환 확인 기간](/help/analyze/analysis-workspace/attribution/models.md)을 참조하십시오.

다음 예에서는 선형 할당이 있는 계산된 지표가 보고에서 작동하는 방식을 보여 줍니다.

| | 히트 1 | 히트 2 | 히트 3 | 히트 4 | 히트 5 | 히트 6 | 히트 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
| 데이터가 전송됨 | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $10 |
| 마지막 터치 eVar | PROMO A | PROMO A | PROMO A | PROMO B | PROMO B | PROMO C | $10 |
| 첫 번째 터치 eVar | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | $10 |
| 예제 prop | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $10 |

이 예에서, 값 A, B, C는 히트 7에서 $10를 구매하기 전에 히트 1, 3, 4, 6에 있는 변수로 전송되었습니다. 두 번째 행에서 그러한 값은 마지막 터치 방문을 기준으로 하여 히트에서 유지됩니다. 세 번째 행은 첫 번째 터치 방문 지속성을 보여 줍니다. 마지막으로, 마지막 행은 지속성이 없는 prop에 대해 데이터가 기록되는 방식을 보여 줍니다.

