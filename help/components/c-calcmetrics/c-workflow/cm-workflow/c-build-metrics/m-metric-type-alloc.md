---
description: '자세한 내용 '
title: 지표 유형 및 기여도 분석
uuid: 64649698-df2a-42c3-bb31-938f766e1d1f
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# 지표 유형 및 기여도 분석

지표 옆에 있는 톱니바퀴 아이콘을 선택하여 지표 유형 및 속성 모델을 지정할 수 있습니다.

* [지표 유형](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_34A86FB402F94E988724232283BF18B7)
* [열 기여도 분석 모델](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_F9690FD1943B403AB28E2FAC54EFE032)
* [선형 할당 작동 방식(2018년 7월 19일 자)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_EDBB2E14A6C248C5A79C0913C02D7CA1)

## 지표 유형

![](assets/cm_type_alloc.png)

| 지표 유형 | 정의 |
|---|---|
| 표준 | 이 지표들은 표준 [!DNL Analytics] 보고에서 사용된 것과 동일한 지표입니다. 공식이 하나의 표준 지표로 구성된 경우 계산되지 않은 지표에 해당하는 대응값과 동일한 데이터가 표시됩니다. 표준 지표는 각 개별 라인 항목별로 계산된 지표를 만드는 데 유용합니다. 예를 들어, [주문] / [방문 횟수]는 특정 라인 항목에 대한 주문 수를 그 항목에 대한 방문 횟수로 나눕니다. |
| 합계 | 각 라인 항목에 있는 보고 기간에 대한 합계를 사용하십시오. 공식이 하나의 합계 지표로 구성된 경우 각 라인 항목에서 동일한 합계 숫자가 표시됩니다. 합계 지표는 사이트 합계 데이터를 기준으로 비교하는 계산된 지표를 만드는 데 유용합니다. 예를 들어, [주문] / [총 방문 횟수]는 특정 라인 항목에 대한 방문 횟수뿐만 아니라, 해당 사이트에 대한 모든 방문 횟수에 대한 주문 수의 비율을 표시합니다. |

## 열 기여도 분석 모델

>[!IMPORTANT]
>
>2018년 7월에 [!DNL Analytics]에서 계산된 지표의 할당 모델을 평가하는 방법을 수정한 [기여도 분석 IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html)를 도입했습니다. 이 변경의 일부로, 기본이 아닌 할당 모델을 사용하는 계산된 지표는 개선된 새로운 기여도 분석 모델로 마이그레이션되었습니다.
>
>* 기본이 아닌 기여도 분석 모델 및 전환 확인 기간 창의 전체 목록에 대해서는 [기여도 분석 IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html) 설명서를 참조하십시오.
>* &quot;마케팅 채널 마지막 터치&quot; 및 &quot;마케팅 채널 첫 번째 터치&quot; 할당 모델은 새 &quot;마지막 터치&quot; 및 &quot;첫 번째 터치&quot; 기여도 분석 모델로 마이그레이션됩니다. 참고: &quot;마케팅 채널&quot;은 더 이상 사용되지 않으며, 계산된 지표에 나타나는 두 개의 할당 모델만 사용됩니다.
>* 또한 선형 할당이 계산되는 방법을 수정할 예정입니다. 고객이 &quot;선형&quot; 할당 모델에 계산된 지표를 사용하는 경우 수정된 새로운 기여도 분석 모델을 반영하도록 보고서가 약간 변경될 수 있습니다. 계산된 지표에 대한 이러한 변경 내용은 Analysis Workspace, Reports &amp; Analytics, Reporting API, Report Builder 및 Ad Hoc Analysis에 반영됩니다. For more information, see **How Linear Allocation works (as of July 19, 2018**, below.
>



## 선형 할당이 작동하는 방식(2018년 7월 19일 기준)

2018년 7월에 Adobe는 계산된 지표에 대해 선형 할당을 보고하는 방법을 변경했습니다. 이 변경 사항은 Analysis Workspace, Ad Hoc Analysis, Reports &amp; Analytics, Report Builder, Activity Map 및 Reporting API에 영향을 줍니다. 변경 사항은 주로 지속성이 있는 eVar 및 기타 차원에 영향을 줍니다. 이러한 변경 사항은 계산된 지표에만 적용되며 선형 할당을 사용하는 다른 보고서(예: 보고 및 분석의 페이지 보고서)에는 영향을 주지 않습니다. 선형 할당을 사용하는 다른 보고서는 계속해서 기존의 선형 할당 방법을 사용합니다.

다음 예제는 선형 할당을 사용하여 계산된 지표가 보고에서 변경되는 방식을 보여줍니다.

|  | 히트 1 | 히트 2 | 히트 3 | 히트 4 | 히트 5 | 히트 6 | 히트 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
| 데이터가 전송됨 | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $10 |
| 마지막 터치 eVar | PROMO A | PROMO A | PROMO A | PROMO B | PROMO B | PROMO C | $10 |
| 첫 번째 터치 eVar | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | $10 |
| 예제 prop | PROMO A | - | PROMO A | PROMO B | - | PROMO C | $10 |

이 예에서, 값 A, B, C는 히트 7에서 $10를 구매하기 전에 히트 1, 3, 4, 6에 있는 변수로 전송되었습니다. 두 번째 행에서 그러한 값은 마지막 터치 방문을 기준으로 하여 히트에서 유지됩니다. 세 번째 행은 첫 번째 터치 방문 지속성을 보여 줍니다. 마지막으로, 마지막 행은 지속성이 없는 prop에 대해 데이터가 기록되는 방식을 보여줍니다.

## 보고 및 분석과 작업 공간에서 선형 할당이 작동하는 방식에 대한 차이점

이러한 두 도구 간에는 선형 속성이 작동하는 방식에 몇 가지 차이점이 있습니다.

* 보고 및 분석에서 (처리된) 선형 속성은 항상 방문을 기준으로 하는 반면, Workspace에서는 방문 또는 방문자를 기반으로 할 수 있습니다.
* 보고 및 분석에서, 방문의 첫 번째 히트에서 값이 전달되지 않은 경우, (초기) 값은 이전 방문에서 지속됩니다. 이것은 작업 공간(속성 IQ)의 경우가 아닙니다. 방문의 첫 번째 히트에서 값이 전달되지 않으면 &#39;없음&#39;이 초기 값입니다.

## 선형 할당이 2018년 7월 이전에 작동한 방법

2018년 7월 19일 이전에 선형 속성은 첫 번째 터치 또는 마지막 터치 지속이 발생한 후에 계산됩니다. 즉, 위의 마지막 터치 eVar의 경우 $10는 다음과 같이 분산됩니다. A = 10 * (3/6) = $5, B = 10 * (2/6) = $3.33, C = 10 * (1/6) = $1.67.

위의 첫 번째 터치 eVar의 경우 $10 전체가 A에 제공됩니다. prop의 경우 다음과 같습니다. A = 10 * (2/4) = $5, B = 10 * (1/4) = $2.50, and C = 10 * (1/4) = $2.5. 이전에 작업한 대로 선형 할당을 요약하려면 다음을 수행하십시오.

| 값 | 현재 마지막 터치 eVar | 현재 첫 번째 터치 eVar | 현재 Prop |
|---|---|---|---|
| PROMO A | $5.00 | $10.00 | $5.00 |
| PROMO B | $3.33 | $0 | $2.50 |
| PROMO C | $1.67 | $0 | $2.50 |
| 합계 | $10.00 | $10.00 | $10.00 |

**2018년 7월 19일부터 선형 할당이 작동하는 방식 요약**

7월 19일 이후에 계산된 지표에서 이 동작을 수정했습니다. [!DNL Analytics]에서는 이제 마지막 터치 또는 첫 번째 터치를 기반으로 하여 지속된 값을 사용하지 않고, 맨 위 표의 첫 번째 행에 전달된 값만 사용합니다. 따라서 차원 할당 설정은 더 이상 선형 할당이 계산되는 방식에 영향을 주지 않으며(즉, props 및 eVars가 같은 방식으로 처리됨), 결과는 지속되었을 수 있는 첫 번째 또는 마지막 터치 값이 아닌 처음에 전달된 것을 반영합니다. 따라서 세 가지 경우 모두 A = 10 * (2/4) = $5, B = 10 * (1/4) = $2.50, C = 10 * (1/4) = $2.50입니다.

| 값 | 새로운 마지막 터치 eVar | 새로운 첫 번째 터치 eVar | 새 Prop |
|---|---|---|---|
| PROMO A | $5.00 | $5.00 | $5.00 |
| PROMO B | $2.50 | $2.50 | $2.50 |
| PROMO C | $2.50 | $2.50 | $2.50 |
| 합계 | $10.00 | $10.00 | $10.00 |

