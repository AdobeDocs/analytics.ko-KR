---
description: Analysis Workspace에서 집단 타겟을 만들고 구성하고 집단 분석 보고서를 실행하는 방법에 대해 알아봅니다.
keywords: Analysis Workspace
title: 집단 테이블 구성
feature: Visualizations
role: User, Admin
exl-id: 523e6f62-b428-454b-9460-6b06e96742c3
source-git-commit: bf8bc40e3ec325e8e70081955fb533eee66a1734
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 97%

---

# 집단 테이블 구성

[!UICONTROL 코호트 테이블]을 만들고 구성하는 방법:

1. ![TextNumbered](/help/assets/icons/TextNumbered.svg) **[!UICONTROL 코호트 테이블]** 시각화를 추가합니다. [패널 내에 시각화 추가](../freeform-analysis-visualizations.md#add-visualizations-to-a-panel)를 참조하십시오.

1. 아래 테이블에 정의된 대로 **[!UICONTROL 포함 기준]**, **[!UICONTROL 반환 기준]**, **[!UICONTROL 코호트 유형]** 및 **[!UICONTROL 설정]**&#x200B;을 정의합니다.

   ![코호트 테이블 구성](assets/cohort-configure.png)

   | 요소 | 설명 |
   |--- |--- |
   | **[!UICONTROL 포함 기준]** | 최대 10개의 포함 필터와 최대 3개의 포함 지표를 적용할 수 있습니다. 이 지표는 사용자가 어떤 코호트에 속하는지를 지정합니다. 예를 들어 포함 지표가 주문이면, 코호트 분석의 시간 범위 동안 주한 사용자는 초기 코호트에 포함됩니다.<br>지표 간의 기본 연산자는 AND이지만 OR로 변경할 수 있습니다. 또한 이러한 지표에 숫자 필터링을 추가할 수 있습니다. 예: `Sessions >= 1`.</br> |
   | **[!UICONTROL 반환 기준]** | 최대 10개의 반환 필터와 최대 3개의 반환 지표를 적용할 수 있습니다. 지표는 사용자의 유지 또는 이탈 여부를 표시합니다. 예를 들어 반환 지표가 [비디오 보기 횟수]일 경우, 그 다음 기간 동안 비디오를 본 사용자만(코호트에 추가된 기간 후) [보존]으로 표현됩니다. 보존을 수량화하는 다른 지표는 세션입니다. |
   | **[!UICONTROL 세부 기간]** | 시간 세부 기간 일, 주, 월, 분기 또는 년입니다. |
   | **[!UICONTROL 유형]** | **[!UICONTROL 보존]**(기본값): **[!UICONTROL 보존]** 코호트는 방문자 코호트가 시간이 지남에 따라 사용자의 자산으로 어떻게 반환되는지 측정합니다. 보존 코호트는 표준 코호트이며 사용자의 재방문 및 반복 행동을 나타냅니다. [!UICONTROL 보존] 코호트는 테이블에서 녹색으로 표시됩니다.<br>**[!UICONTROL 이탈&#x200B;]**:**[!UICONTROL &#x200B;이탈&#x200B;]**(“감소” 또는 “폴아웃”이라고도 함) 코호트는 방문자 코호트 시간이 지남에 따라 사용자의 자산에서 어떻게 이탈하는지 측정합니다. 이탈은 보존의 반대 개념입니다. `Churn = 1 - Retention`. [!UICONTROL 이탈]은 고객이 다시 돌아오지 않는 빈도를 제시하여 기회와 고착성을 측정하는 좋은 방법입니다. 이탈을 사용하여 코호트 필터가 주의를 기울일 수 있는 집중 영역을 분석하고 식별할 수 있습니다. [!UICONTROL 이탈] 코호트는 테이블에서 빨강색으로 표시되며**[!UICONTROL &#x200B;플로우&#x200B;]**시각화의 폴아웃과 유사합니다.</br> |
   | **[!UICONTROL 설정]** | **[!UICONTROL 순환 계산]**: 포함된 열(기본값)이 아닌 이전 열을 기준으로 보존 또는 이탈을 계산합니다. [!UICONTROL 순환 계산]은 “반환” 기간에 대한 계산 방법을 변경합니다. 일반적인 계산은 반환 기준을 충족하고 포함 기간에 있던 사용자를 찾습니다. 이전 기간에 코호트에 있었는지 여부는 중요하지 않습니다. 대신 [!UICONTROL 순환 계산]은 “반환” 기준을 충족하고 이전 기간에 포함되었던 사용자를 찾습니다. 따라서 [!UICONTROL 순환 계산]은 시간의 경과에 따라 &quot;반환&quot; 기준을 지속적으로 충족하는 사용자를 필터링합니다. 선택한 기간까지 이어지는 각 기간에 대해 [!UICONTROL 반환] 기준이 적용됩니다. </br><br>**[!UICONTROL 지연 테이블&#x200B;]**: [!UICONTROL 지연] 테이블은 포함 이벤트가 발생한 이전 및 이후에 경과한 시간을 측정합니다. [!UICONTROL 지연 테이블]은 이전/이후 분석 시 유용한 도구입니다. 예를 들어 곧 출시될 제품이나 캠페인이 있으며 출시 전후의 행동을 추적하고자 할 수 있습니다. [!UICONTROL 지연 테이블]은 직접적인 영향을 확인하기 위해 사전 및 사후 행동을 나란히 표시합니다. [!UICONTROL 지연 테이블]의 사전 포함 셀은 포함 기간의 [!UICONTROL 포함] 기준을 충족한 사용자를 계산한 다음 포함 기간 이전 기간의 [!UICONTROL 반환] 기준을 충족하는 사용자를 계산합니다. [!UICONTROL 지연 테이블]과 [!UICONTROL 사용자 정의 차원 코호트]는 함께 사용할 수 없습니다.</br><br>**[!UICONTROL 사용자 정의 차원 코호트]**: 시간 기반 코호트(기본값)가 아니라 선택한 차원을 기반으로 그룹을 생성합니다. 많은 고객이 시간 이외의 다른 항목으로 코호트를 분석하기를 원하며 새로운 사용자 정의 차원 코호트 기능은 자신이 선택한 차원을 기준으로 코호트를 구축할 수 있는 유연성을 제공합니다. 마케팅 채널, 캠페인, 제품, 페이지, 영역 또는 다른 차원과 같은 차원을 사용하여 이러한 차원의 다양한 값을 기준으로 보존 상태가 어떻게 변하는지 보여 줍니다. [!UICONTROL 사용자 정의 차원] 코호트 필터 정의는 차원 항목을 반환 정의의 일부가 아닌 포함 기간의 일부로만 적용합니다.</br><br>[!UICONTROL 사용자 정의 차원 코호트] 선택 사항을 선택한 후 원하는 영역으로 차원을 드래그할 수 있습니다. 차원을 추가하면 동일한 기간에 유사한 차원 항목을 비교할 수 있습니다. 예를 들어 도시의 성능, 상품, 캠페인 등을 나란히 비교할 수 있습니다. 코호트 테이블이 상위 14개 차원 항목을 반환합니다. 그러나 ![필터](/help/assets/icons/Filter.svg) 필터를 사용하여 원하는 차원 항목만 표시할 수 있습니다. [!UICONTROL 사용자 정의 차원 코호트]는 [!UICONTROL 지연 테이블] 기능과 함께 사용할 수 없습니다.</br> |

1. **[!UICONTROL 빌드]**&#x200B;를 클릭합니다.
1. [!UICONTROL 코호트 테이블]을 재구성하려면 ![편집](/help/assets/icons/Edit.svg)을 선택합니다.

1. (선택 사항) 선택 항목에서 세그먼트를 만듭니다.

   한 개 이상의 셀(연속 또는 불연속)을 선택한 다음 마우스 오른쪽 버튼 클릭 > **[!UICONTROL 선택 항목으로 세그먼트 만들기]**&#x200B;를 클릭합니다.


1. [세그먼트 빌더](/help/components/segmentation/segmentation-workflow/seg-build.md)에서 세그먼트를 더 편집한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   저장된 세그먼트는 [!UICONTROL Analysis Workspace]의 [!UICONTROL 세그먼트] 패널에서 사용할 수 있습니다.

## 설정

[!UICONTROL 코호트 테이블]에 대해 특정 설정을 정의할 수 있습니다.

1. [!UICONTROL 코호트 테이블] 설정을 조정하려면 ![설정](/help/assets/icons/Setting.svg)을 선택합니다.

   | 설정 | 설명 |
   |---|---|
   | **백분율만 표시** | 숫자 값을 제거하고 백분율만 표시합니다. |
   | **백분율 반올림** | 백분율 값을 소수 값으로 표시하지 않고 가장 가까운 정수로 반올림합니다. |
   | **평균 백분율 행 표시** | 테이블의 맨 위에 새 행을 삽입한 다음 각 열 내의 값에 대한 평균을 추가합니다. |


>[!MORELIKETHIS]
>
>[패널 내에 시각화 추가](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>>[시각화 설정](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>>[시각화 컨텍스트 메뉴](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>

