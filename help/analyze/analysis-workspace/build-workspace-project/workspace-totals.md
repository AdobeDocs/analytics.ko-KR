---
description: 작업 공간 합계를 계산하는 방법.
title: 작업 공간 합계
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 작업 공간 합계

자유 형식 테이블에서, 합계 행은 각 분류 수준에 나타나고 두 개의 합계를 표시할 수 있습니다.

* **[!UICONTROL Grand Total]** (회색 &#39;아웃&#39; 숫자) - 이 합계는 수집된 모든 히트를 나타내며 &#39;보고서 세트 합계&#39;라고도 합니다. 세그먼트가 패널 수준에서 또는 자유 형식 테이블 내에서 적용되면 이 합계는 세그먼트 기준과 일치하는 모든 히트를 반영하도록 조정됩니다.
* **[!UICONTROL Table Total]** (검정 숫자) - 이 합계는 일반적으로 하위 집합과 같거나 [!UICONTROL Grand Total]같습니다. It reflects any table filters applied within the freeform table, including the [!UICONTROL Include None] option.

![](assets/total-row.png)

## 합계 표시 설정

아래에서 **[!UICONTROL Column Settings]**&#x200B;선택할 수 **[!UICONTROL Show Totals]** 있는 옵션들이 **[!UICONTROL Show Grand Total]**&#x200B;있습니다. 이러한 설정을 선택 취소하면 표에서 합계가 제거됩니다. 예를 들어 특정 [계산된 지표 시나리오](https://docs.adobe.com/content/help/ko-KR/analytics/components/calculated-metrics/calcmetrics-reference/cm-totals.html)에서 합계가 적절하지 않은 경우 이 선택 사항이 필요할 수 있습니다.

![](assets/column-settings-total.png)

## 정적 행 합계 설정

[정적 행](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.html) 합계는 다르게 동작하며 아래에서 제어됩니다 **[!UICONTROL Row Settings]**.

* **[!UICONTROL Show sum of current rows as the total]** - 이 표는 표에 있는 행의 클라이언트측 합계를 보여 줍니다. 즉, 합계는 방문 또는 방문자와 같은 중복 지표를 **제거하지 않습니다** .
* **[!UICONTROL Show Grand Total]** - 여기에는 서버 측 합계가 표시됩니다. 즉, 합계는 방문 또는 방문자와 같은 중복 지표를 제거합니다.

![](assets/static-rows.png)

## FAQ

| 질문 | 답변 |
|---|---|
| 회색 열 비율은 어느 &#39;합계&#39;를 기반으로 합니까? | 이것은 다음 아래의 **[!UICONTROL Percentages]** 설정 선택에 따라 다릅니다 **[!UICONTROL Row Settings]**.<ul><li>열별 백분율 계산 - 기본 설정입니다. 백분율이 테이블 합계를 기반으로 합니다.</li><li>행별 백분율 계산 - 백분율이 총계를 기반으로 합니다.</li></ul> |
| 설정이 합계에 어떤 영향을 줍니까? **[!UICONTROL Include Unspecified (None)]** | If the **[!UICONTROL Include Unspecified (None)]** setting is unchecked, the None/Unspecified row will be removed from the table, the Table Total, and will carry through to any calculated metrics that use [&#39;Total&#39; metric types](https://docs.adobe.com/content/help/ko-KR/analytics/components/calculated-metrics/calcmetric-workflow/m-metric-type-alloc.html) |
| 사용자 지정 테이블 필터가 자유 형식 테이블에 적용되는 경우 모든 계산된 지표 및 조건부 서식이 필터를 처리합니까? | 현재 처리하지 않습니다. **[!UICONTROL Include Unspecified (None)]** 에 대해 설명되지만 사용자 지정 테이블 필터는 다음 사항에 영향을 주지 않습니다.<ul><li>조건부 서식에서 사용하는 열 최대/최소 범위는 모든 데이터에 적용됩니다.</li><li>지표 유형을 활용하는 **[!UICONTROL Grand Total]** 계산된 지표.</li><li>자유 형식 테이블의 행들 간에 계산되는 열 합계, 열 최댓값, 열 최솟값, 카운트, 평균, 중간값, 백분위수, 사분위, 행 수, 표준 편차, 분산, 누적, 누적 평균, 회귀 변형, T 스코어, T 테스트, Z 스코어, Z 테스트와 같은 함수를 사용하는 계산된 지표.</li></ul> |
| In Calculated Metrics, what does the **[!UICONTROL Grand Total]** metric type reflect? | **[!UICONTROL Grand Total]** 을 계속 참조할 수 **[!UICONTROL Grand Total]****[!UICONTROL Table Total]**&#x200B;있으며 표 또는 |
| 데이터를 자유 형식 테이블에서 복사하여 붙여넣거나 CSV를 통해 다운로드할 때에는 어떤 합계가 표시됩니까? | 전체 행은 **[!UICONTROL Table Total]** 하나만 반영하며 열 **[!UICONTROL Show Totals]** 설정을 따릅니다. |

