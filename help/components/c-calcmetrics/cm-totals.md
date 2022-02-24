---
title: 계산된 지표 합계
description: Analytics 도구에서 계산된 지표 합계가 어떻게 다른지 알아봅니다.
feature: Calculated Metrics
exl-id: 3e4429de-3e0c-49a5-b32c-3a4d24a29816
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '429'
ht-degree: 100%

---

# 계산된 지표 합계

계산된 지표 합계가 표시되는 방식은 [!DNL Reports & Analytics]와 [!DNL Analysis Workspace] 간에 다릅니다. 이 섹션에서는 그 차이를 설명합니다.

## [!DNL Reports & Analytics]의 계산된 지표 합계

[!DNL Reports & Analytics]에서 보고서를 보면, 계산된 지표의 합계 아래에 항상 `n/a`가 표시됩니다. 모든 계산된 지표는 사용자가 정의하므로 이러한 합계가 적절하지 않은 상황은 많습니다. 다음 예를 생각해 보십시오.

조직에서는 사이트에서 구매가 이루어진 방문의 비율을 알기 위해 계산된 지표 `orders` / `visits`을 만들었습니다.  이 지표를 제품 보고서에 사용한 경우 몇 가지 제품이 단일 주문으로 분류됩니다. 그리고, 몇 가지 제품은 단일 방문으로 분류됩니다. 계산된 지표 합계가 이 보고서에 포함된 경우 다음과 같은 의문이 제기됩니다.

| 질문 | 답변 |
|---|---|
| 라인 항목을 합하는 것이 적절한가? | 여러 제품이 단일 주문에 포함될 수 있고, 여러 제품이 단일 방문에 포함될 수 있으므로 적절하지 않습니다. 라인 항목을 집계하면, 총 주문 수 및 총 방문 수가 실제 총 주문 수 및 총 방문 수와 일치하지 않습니다. |
| 총 주문 수 및 총 방문 수를 가져오는 것이 적절한가? | 합계가 개별 라인 항목의 합계와 일치하지 않으므로 적절하지 않습니다. 또한, 총 주문 수 및 총 방문 수는 완전히 따로따로 계산된 지표입니다. |

보고서에서 계산된 지표가 적절한지 여부를 파악하는 논리적이고 구체적인 방법이 없으므로 지표 합계는 모두 생략되었습니다. 합계를 얻으려는 경우, 다음 중 한 가지 방법을 사용할 수 있습니다.

* 포함을 고려하고 있는 지표의 합계 버전을 포함하는 계산된 지표를 만듭니다.
* 예약할 수 있는 데이터 추출 보고서를 만듭니다.
* [!DNL ReportBuilder] 내에서 데이터 요청을 생성합니다.
* [!DNL Analysis Workspace]를 사용합니다 (아래 참조).

## [!DNL Analysis Workspace]의 계산된 지표 합계

Analysis Workspace에서 데이터를 볼 때 대부분의 경우 계산된 지표 합계가 표시됩니다. 보고서의 행이 혼합 형식 (예: 십진수와 통화)인 경우와 같이 일부 경우에는 합계를 제공할 수 없습니다.

합계는 표시될 때 종종 서버 측에서 계산되는데, 이것은 합계가 방문 횟수나 방문자 수와 같은 지표에 대한 중복 제거를 수행함을 의미합니다. 특정 상황에서 계산된 지표는 테이블의 행들을 합하여 클라이언트 측에서 생성되는데, 이것은 이 합계가 방문 횟수 또는 방문자 수와 같은 지표에 대한 중복 제거를 수행하지 않음을 의미합니다.  이 문제는 다음 상황에서 발생합니다.

* 자유 형식 테이블에 [정적 행](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md)을 사용하고 **[!UICONTROL 현재 행의 합계로 표시]** 옵션 (기본값)을 선택한 경우
* [도넛 시각화](/help/analyze/analysis-workspace/visualizations/donut.md)에서 숫자가 최대 100%까지 추가되도록 하는 경우

Analysis Workspace의 합계에 대한 자세한 내용은 [Workspace 합계](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.html?lang=ko#static-row-total)를 참조하십시오.
