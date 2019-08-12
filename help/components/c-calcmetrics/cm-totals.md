---
title: 계산된 지표 합계
seo-title: 계산된 지표 합계
description: Analytics 도구의 계산된 지표 합계가 어떻게 다른지 알아보기
seo-description: 계산된 지표 합계를 계산하는 방법
translation-type: tm+mt
source-git-commit: 540e03f2e541cc5ea0a78e4402cd367241b44200

---


# 계산된 지표 합계

계산된 지표 합계가 표시되는 방식은 [!DNL Reports & Analytics] 과 [!DNL Analysis Workspace]다릅니다. 이 섹션에서는 차이에 대해 설명합니다.

## 계산된 지표 합계 [!DNL Reports & Analytics]

에서 [!DNL Reports & Analytics]보고서를 보면 계산된 지표가 항상 합계 `n/a` 아래에 표시됩니다. 모든 계산된 지표는 사용자가 정의하므로 이 총계가 적합하지 않는 경우가 많습니다. 다음 예를 생각해 보십시오.

조직에서 계산된 지표 `orders` / `visits` 를 만들어 사이트에서 어떤 것을 구매한 방문의 비율을 결정했습니다. 이 지표를 제품 보고서로 가져오면 여러 제품이 단일 주문으로 귀속됩니다. 또한 여러 제품은 한 번의 방문으로 인해 발생합니다. 계산된 지표 합계가 이 보고서에 포함되어 있으면 다음과 같은 질문이 발생합니다.

| 질문 | 답변 |
|---|---|
| 라인 항목의 합계는 적절합니까? | 여러 제품을 단일 주문으로 포함시킬 수 있고 단일 방문에 여러 제품을 포함시킬 수 있으므로 그렇지 않습니다. 라인 항목이 집계된 경우 총 주문 수와 총 방문 수는 실제 총 주문 수 및 총 방문 수와 일치하지 않습니다. |
| 총 주문 수 및 총 방문 수는 적절합니까? | 합계가 개별 라인 항목의 합계와 일치하지 않으므로 그렇지 않습니다. 또한 총 주문 수 및 총 방문 수는 별도로 계산된 지표입니다. |

보고에서 계산된 지표가 적절한지를 확인하는 논리적이고 구체적인 방법이 없으므로 지표 총계는 모두 생략됩니다. 총계를 얻으려면 다음 중 하나를 수행할 수 있습니다.

* 포함하려는 지표의 전체 버전을 포함하는 계산된 지표를 만듭니다.
* 예약할 수 있는 데이터 추출 보고서를 만듭니다.
* Reportbuilder 내에서 데이터 요청을 만듭니다.
* 분석 작업 공간을 사용합니다 (아래 참조).

## 계산된 지표 합계 [!DNL Analysis Workspace]

분석 작업 공간에서 특정 상황에서 계산된 지표를 합산하여 합계를 표시합니다.

* [정적 행이](/help/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.md) 있을 때 현재 각 열 옵션에서 값을 합산하여 합계 **[!UICONTROL 계산]** (기본값) 이 선택되어 있습니다.
* In the [Donut Visualization](/help/analyze/analysis-workspace/visualizations/donut.md).
* 의 요약 [변경 사항 시각화에서](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)
